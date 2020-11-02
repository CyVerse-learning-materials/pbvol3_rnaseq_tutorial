.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Obtain Accession Numbers and Metadata from the SRA
---------------------------------------------------

**Description:**

In this section, we will describe how to import data from the NCBI Sequence Read Archive (SRA). The example dataset is available at the SRA under the accession PRJNA553702. It is not possible to directly download sequencing files from the SRA. Instead, we must obtain the accessions for the individual sequencing files and use the ‘sra-tools’ software to download those files.

----


*Get SRA Accession Metadata*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. 	#### Comment: Step title should be descriptive (i.e. Cleaning Read data) ###

1. Go to the |SRA|.

2. Enter the BioProject accession **PRJNA553702** in the search bar and press **Search**.

3. This search should return 12 entries which are individual sequence files associated with this experiment. Click on any of the results (e.g., GSM3936272: 100µM MEL rep3; Arabidopsis thaliana; RNA-Seq). This will lead to a page with a detailed description of the experiment.

4. Under the **Study** heading, find the link to **All runs** and click this to access the SRA Run Selector. (Direct link: |SRP214076|)

5.	Under the **Select** heading, there are two downloads (simple text files) available for download. Click on **Metadata** and **Accession** list to download both files. The metadata file will be called **SraRunTable.txt** and the accession list will be called **SRR_Acc_List.txt**.

  .. note::

    All metadata and accession lists from the SRA will have the same file names. Be sure to rename or carefully organize these files if you will be downloading other SRA data.


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - SraRunTable.txt
      - Metadata from the SRA
      - |SraRunTable|
    * - SRR_Acc_List.txt
      - Accession list from the SRA
      - |SRR_Acc_List|

----

**Description of output and results**

The **SraRunTable.txt** will be used to label our files using the Data Store's metadata capabilities. We will use the **SRR_Acc_List.txt** as input for importing files from the SRA.


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

.. Comment: Place Images Below This Line
   use :width: to give a desired width for your image
   use :height: to give a desired height for your image
   replace the image name/location and URL if hyperlinked


 .. |Clickable hyperlinked image| image:: ./img/IMAGENAME.png
    :width: 500
    :height: 100
 .. _CyVerse logo: http://learning.cyverse.org/

 .. |Static image| image:: ./img/IMAGENAME.png
    :width: 25
    :height: 25



.. Comment: Place URLS Below This Line

   # Use this example to ensure that links open in new tabs, avoiding
   # forcing users to leave the document, and making it easy to update links
   # In a single place in this document

   .. |Substitution| raw:: html # Place this anywhere in the text you want a hyperlink

      <a href="REPLACE_THIS_WITH_URL" target="blank">Replace_with_text</a>


.. |Github Repo Link|  raw:: html

   <a href="FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX_FIX" target="blank">Github Repo Link</a>
