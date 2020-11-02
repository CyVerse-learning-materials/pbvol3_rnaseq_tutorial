.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Apply metadata to FastQ files
---------------------------------

**Description:**

Here we make use of the Data Store's ability to tag files with metadata. Many of these metadata descriptions will be required for submission of data to a repository prior to publication. We will modify the previously downloaded SraRunTable.txt on our local computer in a spreadsheet program and then upload to the Discovery Environment and link these descriptions to the files. This process of metadata application can be applied to any dataset in the Data Store and is a recommended practice.

  .. tip::

    If you were using this tutorial with your own data, uploading your FastQ
    files and continuing from this section would be a recommended starting
    point. See the |Data Store Guide| for more information about uploading
    files to the Discovery Environment.



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



*Apply metadata*
~~~~~~~~~~~~~~~~~~~

1. In a spreadsheet program (e.g., Excel), open the **SraRunTable.txt** file on
your local computer.

    .. tip::

     Renaming the file with a ‘.csv’ extension before opening the file may make
     it easier for your spreadsheet program to properly interpret.

2. To the spreadsheet, add a new first column (left-most). Name this “**file**.”

3. At this point, sort the spreadsheet by run. This will make it easier in the
subsequent steps when file names will likely be alphanumerically sorted.

4. In the **file** column we will list the path in the Data Store for each FastQ
file as corresponds to its accession in the **Run** column. (e.g.,
**/iplant/home/USERNAME/rna-seq-tutorial/fastq_files/ SRR9666132.sra.fastq**).

  .. note::

     In the data window, clicking the three dots next to any file/folder icon
     reveals a function menu which includes an option Copy path to file/folder.

Your first two columns should be similar to the below (with your username replacing username below:

  .. code::

    File	                                                                 Run
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666131.sra.fastq	SRR9666131
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666132.sra.fastq	SRR9666132
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666133.sra.fastq	SRR9666133
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666134.sra.fastq	SRR9666134
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666135.sra.fastq	SRR9666135
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666136.sra.fastq	SRR9666136
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666137.sra.fastq	SRR9666137
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666138.sra.fastq	SRR9666138
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666139.sra.fastq	SRR9666139
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666140.sra.fastq	SRR9666140
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666141.sra.fastq	SRR9666141
    /iplant/home/username/rna-seq-tutorial/fastq_files/SRR9666142.sra.fastq	SRR9666142

5. (Optional) At this point, you can add any desired additional columns with
any metadata you want to add. For our tutorial this is not necessary.

6. Save this file as **fastq_file_metadata.csv** on your local computer.

7. In the Discovery Environment, navigate to the **metadata** folder in your
**rna-seq-tutorial** folder.

8. In the **Data** window, choose Upload and then **Simple Upload from
Desktop**. Browse for the **fastq_file_metadata.csv** file; click **Upload**.

9. In the **Data** window, navigate to your **rna-seq-tutorial** folder and
select (checkbox) the **fastq_files** folder.

10. In the Data window, go to the **Metadata** menu and select **Apply Bulk
Metadata**, then **Select Metadata File**. Then browse and select the
**fastq_file_metadata.csv** file in the **metadata folder**. You will get a
notification when the metadata has been applied successfully.

11. To view the metadata, in the Data window, navigate to the **fastq_files**
folder and select (checkbox) any individual FastQ file. In the **Metadata**
menu, choose **Edit / View Metadata**. You will then see the applied metadata.
You can build custom search queries on any of these attributes (column names in
your original spreadsheet) and the values (the entries for these columns). See
|Data Store Guide| for more information about advanced search queries and smart folders.

**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - fastq_file_metadata.csv
      - A CSV file containing metadata labels for the FastQ files
      - |FastQ metadata|


----

**Description of output and results**

With metadata applied, this files are now more easy to search and organize.
These metadata properties will also be of use in data submission to
repositories like SRA.


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
