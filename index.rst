.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

**Plant Bioinformatics Vol 3 RNA-Seq Tutorial**
================================================

..
    #### Comment: Use short, imperative titles e.g. Upload and share data, uploading and
    sharing data ####

Goal
----

This tutorial is an online version of an RNA-Seq tutorial developed for Vol. 3
of Plant Bioinformatics. It is an end-to-end RNA-seq analysis using the Kallisto and Sleuth. The tutorial emphasizes reproducibility features of the
CyVerse platforms.

----

Tutorial Maintainer(s)
------------------------

Who to contact if this guide needs fixing. You can also email
`learning@CyVerse.org <learning@CyVerse.org>`_

.. list-table::
    :header-rows: 1

    * - Maintainer
      - Institution
      - Contact
    * - Jason Williams
      - CyVerse / Cold Spring Harbor Laboratory
      - williams@cshl.edu
----

.. toctree::
	:maxdepth: 2

  Tutorial home <self>
  Discovery Environment Login and Setup <step1.rst>
  Obtain Accession Numbers and Metadata from the SRA <step2.rst>
  Upload Files to the Data Store <step3.rst>
  Import Files from SRA with sra-tools <step4.rst>
  Organize Files, Validate Import, and Extract to FastQ Format <step5.rst>
  Apply Metadata to FastQ Files <step6.rst>
  QC Reads with FastQC <step7.rst>
  Quantify Reads with Kallisto <step8.rst>
  Prepare Experimental Design Metadata for Sleuth <step9.rst>
  Evaluate Differential Expression with Sleuth  <step10.rst>
  Conclusion <step11.rst>

..
	#### Comment:This tutorial can have multiple pages. The table of contents assumes
	you have an additional page called 'Step One' with content located in 'step1.rst'
	Edit these titles and filenames as needed ####


Prerequisites
-------------

Downloads, access, and services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need access to the following services/software*

..
	#### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Prerequisite
      - Preparation/Notes
      - Link/Download
    * - CyVerse account
      - You will need a CyVerse account to complete this exercise
      - |CyVerse User Portal|
    * - Spreadsheet software
      - Software for editing spreadsheet data
      - User provided (e.g. Excel, Google Sheets, or Open Office)
    * - Cyberduck (optional)
      - Standalone software for upload/download to Data Store
      - |Download Cyberduck|

Platform(s)
~~~~~~~~~~~

*We will use the following CyVerse platform(s):*

 ..
   #### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Tour
    * - Data Store
      - GUI/Command line
      - |Data Store|
      - |Data Store Guide|
    * - Discovery Environment
      - Web/Point-and-click
      - |Discovery Environment|
      - |Discovery Environment Guide|


Application(s) used
~~~~~~~~~~~~~~~~~~~
..
	#### Comment: these tables are examples, delete whatever is unnecessary ####

**Discovery Environment App(s):**

.. list-table::
    :header-rows: 1

    * - App name
      - Version
      - Description
      - App link
      - Notes/other links
    * - sra-tools prefetch
      - SRA tools version 2.8.10, CyVerse App version 0.1
      - Utility for downloading data from NCBI Sequence Read Archive
      - |sra-tools prefetch app|
      - |SRA Tools Documentation|
    * - sra-tools vdb-validate
      - SRA tools version 2.8.10, CyVerse App version 0.1
      - Utility for validating downloaded data from NCBI Sequence Read Archive
      - |sra-tools vdb-validate app|
      - |SRA Tools Documentation|
    * - sra-tools fasterq-dump
      - SRA tools version 2.8.10, CyVerse App version 0.1
      - Convert SRA files to FastQ format
      - |sra-tools fasterq-dump app|
      - |SRA Tools Documentation|
    * - FastQC
      - 0.11.5
      - Quality control reports for FastQ files
      - |FastQC app|
      - |FastQC Documentation|
    * - Kallisto
      - 0.43.1
      - RNA-Seq quantification by pseudoalignment
      - |Kallisto app|
      - |Kallisto Documentation|
    * - Sleuth
      - 0.30.0
      - VICE application of RStudio with Sleuth and related R packages
      - |Sleuth app|
      - |Sleuth Documentation|


Input and example data
~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need to have the following inputs prepared*

..
	#### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Input File(s)
      - Format
      - Preparation/Notes
      - Example Data
    * - SRA files (from NCBI Sequence Read Archive) or FastQ files
      - ".sra", ".fastq"
      - This tutorial starts with importing data from the SRA. You could also start at |Organize files, validate import, and extract to FastQ format|
      - |CyVerse Data Commons|
    * - SRA Metadata, custom metadata
      - ".csv"
      - This tutorial uses metadata provided from the SRA. If using your own
        FastQ files, you may create and use any metadata you wish.
      - |CyVerse Data Commons 2|


.. admonition:: sample-data

   The data for this tutorial comes from Zia et al. 2019 which used
   RNA-Seq to explore overlap in signaling pathways in Arabidopsis treated with
   the hormones melatonin and auxin. Although these hormones have similar
   chemical structures (indoles), the study identified distinct signaling
   pathways and changes in gene expression. The dataset is available on the SRA
   under BioProject PRJNA553702. We will attempt to replicate the RNA-Seq
   portion of this analysis.

   Zia, S. F., Berkowitz, O., Bedon, F., Whelan, J., Franks, A. E., & Plummer, K. M. (2019). Direct comparison of Arabidopsis gene expression reveals different responses to melatonin versus auxin. BMC Plant Biology. |https://doi.org/10.1186/s12870-019-2158-3|


----

**Fix or improve this documentation**

- Search for an answer:
  |CyVerse Learning Center|
- Ask us for help:
  click |Intercom| on the lower right-hand side of the page
- Report an issue or submit a change:
  |Github Repo Link|
- Send feedback: `learning@CyVerse.org <learning@CyVerse.org>`_

.. comment:

   Uncomment the below and fix with this repo's information if citing

   **Citation**

   You may cite this work as:
   [Repository Title]
   [Author(s)]
   [Repository Release Version]
   [DOI: Zenodo DOI link (generated from Github Release/Zenodo)]
----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`__


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
