.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Organize files, validate import, and extract to FastQ format
-------------------------------------------------------------

**Description:**

At this point, we will put all of the files imported from the SRA into a single location. We will verify the integrity of the files and then extract them from the SRA format into the FastQ format.

----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - SRA files (SRR9666131.sra, SRR9666132.sra …)
      - These are sequence data in the SRA format
      - |SRA files|

*Organize files*
~~~~~~~~~~~~~~~~~~~

1. In your **rna-seq-tutorial** tutorial folder, create a new folder: **imported_sra**.

2. Next, in the data window go to the **File** menu and select **New Data Window at this location**.

3. In one data window, navigate to the SRA files imported in the previous section. Each SRA file is in its own folder. Drag each of the 12 .sra files (e.g., SRR9666131.sra, SRR9666132.sra…) into the newly created **imported_sra** folder; we want to end up with all 12 files in the **imported_sra folder**.



*Use sra-tools vdb-validate app to validate SRA files*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Before extracting these files, we can do a check here to verify the integrity of our import from the SRA.

1. In the App panel, search for and launch the sra-tools vdb-validate app.

  You can use this direct link: |sra-tools vdb-validate app|

2. (Optional) you can name this analysis and provide any comments in the App launch window.

3.	Under **Select output folder**, navigate to the **rna-seq-tutorial** folder created earlier. Your outputs will automatically be placed in this folder.

4. Under **SRA Files (Input)** browse to the **imported_sra** (created above) and add the 12 files. Then click **Launch Analysis**.

5. To see the current status of the job, click on the **Analyses** button. When the job is complete, you can click on the job name (e.g., **sra-tools_vdb-validate_analysis1**) to open a data window and browse the results.

    .. note::

       You may need to Refresh to see the current job status. This job is estimated to take about 5-10 minutes.

6. Back in the Analyses window, go back and select (checkbox) the analysis (e.g., **sra-tools_vdb-validate_analysis1**) and select the **Analyses** menu. Then choose **View Parameters** to present the parameters used in this analysis. Then choose **Save to File**; save this text file in your output folder (e.g., **rna-seq-tutorial/ sra-tools_vdb-validate_analysis1-2020-10-04-11-40-57.1**) as **job_parameters.txt**.

7. The expected output will be a text file (**vdb-validation.txt**). This is a series of tests (including checksums – an algorithmically generated signature that confirms the file’s integrity). A sample output is shown below with ‘ok’ indications for each test. A similar set of 8 lines should appear in the file for each of the verified SRA files.

  .. code:: `bash`

    2020-10-06T22:04:41 vdb-validate.2.10.8 info: Database 'SRR9666131.sra' metadata: md5 ok
    2020-10-06T22:04:41 vdb-validate.2.10.8 info: Table 'SEQUENCE' metadata: md5 ok
    2020-10-06T22:04:41 vdb-validate.2.10.8 info: Column 'ALTREAD': checksums ok
    2020-10-06T22:04:42 vdb-validate.2.10.8 info: Column 'QUALITY': checksums ok
    2020-10-06T22:04:43 vdb-validate.2.10.8 info: Column 'READ': checksums ok
    2020-10-06T22:04:43 vdb-validate.2.10.8 info: Column 'READ_LEN': checksums ok
    2020-10-06T22:04:44 vdb-validate.2.10.8 info: Column 'READ_START': checksums ok
    2020-10-06T22:04:44 vdb-validate.2.10.8 info: Column 'SPOT_GROUP': checksums ok



*Use sra-tools fasterq-dump app to extract into FastQ format*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. In the **App panel**, search for and launch the **sra-tools fasterq-dump**
app.

  You can use this direct link: |sra-tools fasterq-dump app|

2. (Optional) you can name this analysis and provide any comments in the App
launch window.

3. Under **Select output folder**, navigate to the **rna-seq-tutorial** folder
created earlier. Your outputs will automatically be placed in this folder.

4. Under **SRA Files (Input)** browse to the **imported_sra** and add the 12
SRA files. Then click **Launch Analysis**.

5. To see the current status of the job, click on the **Analyses button**. When
the job is complete, you can click on the job name (e.g., **sra-tools_fasterq-
dump_analysis1**) to open a data window and browse the results.

  .. note::

     You may need to Refresh to see the current job status. This job is
     estimated to take about 30-40 minutes.

6. Back in the **Analyses** window, go back and select (checkbox) the analysis
(e.g. **sra-tools_fasterq-dump_analysis1**) and select the **Analyses** menu.
Then choose **View Parameters**. This will present the parameters used in this
analysis. Then choose **Save to File**; save this text file in your output
folder (e.g., **rna-seq-tutorial/ sra-tools_fasterq-dump_analysis1-2020-10-04-
11-40-57.1)** as **job_parameters.txt**.

7. The expected output will be 12 FastQ formatted files (e.g. SRR9666131.sra.fastq,SRR9666132.sra.fastq…).

8. Create a **fastq_files** folder (**File** menu; **New Folder**) in your **rna-seq-tutorial** and move the 12 FastQ files there.

9. Since the SRA files are already maintained on NCBI, you can safely delete the
original SRA files. While this deletion is not mandatory, it is a responsible
use of public infrastructure to remove large unneeded files. Browse to the
**rna-seq-tutorial** folder and select the **imported_sra folder**. Under the
**File** menu,choose **Move to Trash**. Next to the search bar, you can then
use the **Trash menu** to empty the trash.


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - FastQ files (e.g. SRR9666131.sra.fastq,SRR9666132.sra.fastq…)
      - Sequencing data in FastQ format
      - |SRA FastQ Files|


----

**Description of output and results**

In this section we have validated the imported SRA files and transformed them
into the FastQ format, the input for a variety of sequencing-based analyses.

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
