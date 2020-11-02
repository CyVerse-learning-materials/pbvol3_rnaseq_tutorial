.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Evaluate differential expression with Sleuth
----------------------------------------------

**Description:**

In this final section of the tutorial, we will use the R package Sleuth to visualize our data and perform differential expression analysis. We will summarize the R analysis steps, but the tutorial itself is provided in the form of an RMarkdown notebook.


----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - Kallisto quantification results (abundances.h5, abundances.tsv,
        run_info.json for each FastQ file analyzed )
      - See detailed description below
      - |Kallisto outputs|

*Use Sleuth in RStudio app to calculate and visualize results*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. In the **App** window, search for and launch the **RStudio Sleuth** app.

    You can use this direct link: |Sleuth app|

2. (Optional) you can name this analysis and provide any comments in the
**App launch window**.

3. Under **Select output folder**, navigate to the **rna-seq-tutorial** folder
created earlier. Your outputs will automatically be placed in this folder.

4. Under **Notebooks** a default folder containing notebook specific to this
tutorial will be loaded (**/iplant/home/shared/cyverse_training/tutorials/pbv3/
R**). You may change this if you have an alternative notebook.

5. Under **Datasets** and **Data for analysis** navigate to the **rna-seq-
tutorial** folder created earlier, go into the folder containing your Kallisto output, and select the **Kallisto_quant_output** folder.

6. Under **Datasets** and **Study design file** navigate to the **rna-seq-
tutorial** folder created earlier, go into the **metadata** folder and select
the experimental design file (i.e., **experimental_design.tsv**); click
**Launch Analysis**.

7. Back in the **Analyses** window look for the analysis you just launched
(e.g. **RStudio_Sleuth _analysis1**). There will be a link icon immediately to
the left of the analysis name. Click this to open the RStudio session in a new
browser tab.

8. We need to modify our RStudio home directory to make it easier to save
files. Open the **Terminal** tab. Paste in the following command and hit enter.

  .. code::

    sudo chown -R rstudio /home/rstudio

9. In the RStudio **Files** tab, go to the R folder and click
**sleuth_pb_tutorial.Rmd** to open the notebook.

10. Follow the notebook by clicking the green “play” button in each section
(chunk) of R code. You can follow along with the notebooks explanations and
then press play to run each code chunk. The final code chunk will launch the
interactive visualizations in the R Shiny application.

**Rstudio Outline**

Without replicating the actual code presented in the notebook, here are the major steps presented:

  (a) **Step 1**: The Sleuth library and additional libraries for plotting and
      retrieving data from Ensembl are loaded.
  (b) **Step 2**: The experimental design file is loaded, and a table is created
      that maps this metadata with the Kallisto outputs.
  (c) **Step 3**: We use the biomaRt package to load gene names from Ensembl so
      that we can more descriptively annotate our transcripts.
  (d) **Step 4**: We indicate the variables we want to compare and use the
      Sleuth
      functions to create the data model.
  (e) **Step 5**: We do an exploratory visualization of the dataset using PCA
      plotting.
  (f) **Step 6**: A liner model is created, and the results of the analysis are
      displayed in an interactive R Shiny application. The R Shiny application will generate tables of results and figures that can be downloaded and further analyzed. Note: The test table available from the R Shiny application contains a complete list of gene names, quantifications, and other statistics. You can download this directly from the R Shiny app.

         .. note::

           Your web browser must have pop-up blocking disabled to view the Shiny application.

11. When you have finished with your RStudio session, return to the **Analysis**
window and select (checkbox) the RStudio analysis. Go to the Analysis menu and
select **Complete and Save Outputs**. Any files created during your RStudio
analysis will be saved.

    .. note::

       VICE applications (Like this RStudio application) typically have a 48
       hour run time on CyVerse. The application will automatically terminate
       and save outputs at this time.


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - Varies
      - In the Sleuth Shiny application you can export tables with your
        differential testing results and a variety of graphs.
      - NA


----

**Description of output and results**

Sleuth Shiny application allows you to interactively examine and tailor tables
of differential testing results as well as graphs of gene expression and other
metrics. The Application also allows you to export and save these outputs.

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
