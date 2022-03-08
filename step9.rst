.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Prepare Experimental Design Metadata for Sleuth
------------------------------------------------

**Description:**

Before we use Sleuth to analyze our data, we need to create a tab-delimited
file that matches our samples to their conditions. It is convenient to do this
on your local computer, using a spreadsheet program. We can easily modify the
**SraRunTable.txt** file we downloaded from the SRA.

----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - Metadata from the SRA
      - Metadata that describes our dataset; will be modified to appropriately
        indicate experimental variables and controls.
      - |SraRunTable|

*Create Experimental Design Table*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. In your spreadsheet program, open **SraRunTable.txt** (downloaded previously
from SRA).

2. According to the Sleuth instructions, the first column must be named
‘**sample**’; rename the **Run** column to **sample**.

3. Next, you will want to create new columns which specify attributes about
each sample such as what treatment/condition correspond to each sample. In the
table below, we suggest columns that indicate the condition (e.g., control, NAA
treated, high-melatonin, low-melatonin), replicate numbers, etc. See the
|Example experimental design| file for the example of the file to create.

4. Save the experimental design file in TSV format (e.g.
**experimental_design.tsv**).

5. In the |Discovery Environment|, navigate to the **metadata** folder you
created for this experiment (**rna-seq-tutorial/metadata**). Click the **Upload** button and select **Browse Local**.

6. Browse your local computer to select the experimental design file (i.e.,
**experimental_design.tsv**) and upload the file. You will get a notification when upload is completed. You may need to refresh your browser to see the uploaded file.


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - experimental_design.tsv
      - A TSV file describing how each sample relates to an experimental
        condition and/or metadata variable.
      - |Example experimental design|


----

**Description of output and results**

The TSV file created links the name of the sample (in our case synonymous with SRA accession numbers) to the experimental design (e.g. conditions, controls, and other metadata).

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
