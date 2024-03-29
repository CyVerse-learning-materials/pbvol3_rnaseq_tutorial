.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Quantify Reads with Kallisto
------------------------------

**Description:**

Kallisto will individually generate pseudoalignments and quantification for
each replicate of each condition. In the Discovery Environment application, the
‘Kallisto index’ command will first build an index of the transcriptome. Next,
that indexed transcriptome will be used to quantify the read data (equivalent
to the ‘Kallisto quant’ command at the command line).

----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - Transcriptiome
      - A transcriptome for pseudoalignment is required
      - |Arabidopsis transcriptome|
    * - FastQ files (e.g. SRR9666131.sra.fastq,SRR9666132.sra.fastq…)
      - Sequencing data in FastQ format
      - |SRA FastQ Files|



*Import Transcriptome from Ensembl*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Go to the Ensembl homepage for Arabidopsis at https://plants.ensembl.org/Arabidopsis_thaliana/Info/Index.

2. Under **Gene annotation** click the **FASTA** link under **‘Download genes, cDNAs, ncRNA, proteins’** ; ftp://ftp.ensemblgenomes.org/pub/plants/release-48/fasta/arabidopsis_thaliana.

3. In the **cnda** folder, locate the file
**Arabidopsis_thaliana.TAIR10.cdna.all.fa.gz**.

4. In your web browser, copy the URL for this file (left click, **Copy Link Location** for most browsers). The URL for release 48 of Ensembl is ftp://ftp.ensemblgenomes.org/pub/plants/release-48/fasta/arabidopsis_thaliana/cdna/Arabidopsis_thaliana.TAIR10.cdna.all.fa.gz.

  .. tip::

      Ensure you use the ‘cdna.all.fa.gz’; your annotation release must match what is used later in the Sleuth analysis


5. In the Data view in the |Discovery Environment|, navigate to your **rna-seq-tutorial** folder.

6. Create a new folder called **transcriptome** and navigate into the newly created folder.

7. In the **Data** view, click the **Upload** button and choose **Import from URL**; paste in the URL for the *Arabidopsis* transcriptome. Be sure to avoid any extra spaces or characters at the end of your URL. Click **Import** to complete this action. You will get a notification when import is complete. You may need to refresh your browser to see the imported file.

8. Back on the Ensembl page, also copy the URL for the CHECKSUMS file and repeat the import procedure to the same folder.

    .. tip::

      You can also apply metadata to the imported transcriptome. See also the |Data Store Guide| for additional options for apply metadata.


*Use Kallisto App to Psuedoalign Reads*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

9. Click on the **Data** icon and navigate to your **rna-seq-tutorial** tutorial folder and create a folder to store outputs, name the folder **kallisto_analyses**.

10. In the **Apps** view, search for and launch the **Kallisto-v.0.43.1** app.

11. In **Analysis Info** you can name this analysis and provide any comments (optional). Under **Output folder**, navigate to the **kallisto_analyses** folder created earlier. Your outputs will automatically be placed in this folder; click **Next**.

11. In **Parameters** under **Input**:

    (a)	For **The transcript fasta file supplied (fasta or gzipped)** browse to the **transcriptome** folder and add the **Arabidopsis_thaliana.TAIR10.cdna.all.fa.gz** file.

    (b)	For **Paired or single end** choose single.

    (c)	Under **FASTQ Files (Read1)**: Click **Browse** and browse to the **fastq_files** folder and select 12 files (e.g., SRR9666131.sra.fastq, SRR9666132.sra.fastq…).

    *Under Options*

    (a)	For **Number of bootstrap samples** enter 25.

    (b)	For **Estimated average fragment length (required for single end reads)** enter 200.

    (c)	For **Estimated standard deviation of fragment length (required for single end reads)** enter 20.;

                .. note::

                  Although SRA data usually does not
                  contain fragment length and standard deviation, these are common
                  values. For other options for this application, consult the
                  |Kallisto Documentation|. Bootstrapping is the most
                  computationally intensive option, so higher numbers of
                  bootstrapping operations will cause the analysis to take longer
                  to complete.

Click **Next**.

12. Click **Next** again to skip **Advanced Settings (optional)**; under **Review and Launch** click **Launch Analysis**.

13. Click on **Analyses** view to see the current status of the job; you can also click on the **Analyses** icon to navigate to this section. When the job is complete, you can click on the **folder** icon next to the analyses name to browse the results. You may need to **Refresh** to see the current job status. This job is estimated to take about 60-70 minutes.

14. When the job has status **Completed** to navigate to the expected output. The expected output will be a folder **Kallisto_quant_output** containing 12 folders (labeled with the accession name).


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - Kallisto quantification results (abundances.h5, abundances.tsv,
        run_info.json for each FastQ file analyzed )
      - See detailed description below
      - |Kallisto outputs|

----

**Description of output and results**

Kallisto will generate a set of results for each FastQ file (or pairs of FastQ
files if our data were paired-end sequenced). Inside each folder will be:

- **abundances.h5**: HDF5 binary file containing run info, abundance estimates,
  bootstrap estimates, and transcript length information length. This file can
  be read in by Sleuth.
- **abundances.tsv**: plaintext file of the abundance estimates. It does not
  contain bootstrap estimates. When plaintext mode is selected; output
  plaintext abundance estimates. Alternatively, Kallisto h5dump will output an
  HDF5 file to plaintext. The first line contains a header for each column,
  including estimated counts, TPM, effective length.
- **run_info.json**: a json file containing information about the run.

    .. note::

      We did not select the BAM file creation option when launching the app. Although a BAM file will be created, it is empty and can be ignored.

----

**Fix or improve this documentation**

- Search for an answer:
  |CyVerse Learning Center|
- Ask us for help:
  click |Intercom| on the lower right-hand side of the page
- Report an issue or submit a change:
  |Github Repo Link|
- Send feedback: `learning@CyVerse.org <learning@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


.. |Github Repo Link|  raw:: html

   <a href="FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX" target="blank">Github Repo Link</a>
