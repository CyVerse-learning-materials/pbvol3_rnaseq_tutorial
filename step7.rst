.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


QC Reads with FastQC
-------------

**Description:**

We will do a quality check to verify the sequencing data is of suitable quality
for downstream analysis.


----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - FastQ files (e.g. SRR9666131.sra.fastq,SRR9666132.sra.fastq…)
      - Sequencing data in FastQ format
      - |SRA FastQ Files|


*Use FastQC app to report on sequence quality*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. In the **App panel**, search for and launch the **FastQC 0.11.5 (multi-
file)** app.

  You can use this direct link: |FastQC app|

2. (Optional) you can name this analysis and provide any comments in the **App
launch window**.

3. Under **Select output folder**, navigate to the **rna-seq-tutorial** folder
created earlier. Your outputs will automatically be placed in this folder.

4. Under **Input** browse to the **fastq_files** folder and add the 12 files
(e.g., SRR9666131.sra.fastq, SRR9666132.sra.fastq…); then click **Launch
Analysis**.

5. To see the current status of the job, click on the **Analyses** button. When
the job is complete, you can click on the job name (e.g.,
**FastQC_0.11.5__multi-file__analysis1**) to open a data window and browse the
results.

     .. note::

       You may need to **Refresh** to see the current job status. This job is estimated to take about 30-40 minutes.

6. Back in the **Analyses** window, go back and select (checkbox) the analysis
(e.g. **FastQC_0.11.5__multi-file__analysis1**) and select the **Analyses**
menu. Then choose **View Parameters**. This will present the parameters used in
this analysis. Then choose **Save to File**; save this text file in your output
folder (e.g. **rna-seq-tutorial/ FastQC_0.11.5__multi-file__analysis1-2020-10-
04-11-40-57.1**) as **job_parameters.txt**.

7. The expected output will be 12 HTML formatted reports, and 12 zip files
containing additional files including text-based metrics. You can click on and
examine all the HTML files; they will open as new tabs in your web browser.
Review of the example dataset indicates the samples are all of high quality and
additional filtering or trimming would not improve our quantification results.


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - HTML and ZIP files of FastQC reports
      - For each FastQ file an HTML file with an interactive report on sequence
        quality and a ZIP file with components of that report are created.
      - |FastQC Reports|


----

**Description of output and results**

In the case of the tutorial data, the sequence quality is of very high quality.
If necessary, other applications (e.g. Trimmomatic) could be used at this stage
to do further filtering or trimming.

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
