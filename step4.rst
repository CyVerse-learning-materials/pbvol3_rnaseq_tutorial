.. include:: cyverse_rst_defined_substitutions.txt
.. include:: custom_urls.txt

|CyVerse_logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Import files from SRA with sra-tools
--------------------------------------

**Description:**

Now that we have a list of accessions, we can use our first application. The
sra-tools prefetch app will allow us to import data from the SRA. All of the
applications we will be using in the Discovery Environment have been collected
together. You may access them by going to the Communities section under the
Preferences and Groups icon (See Figure 2). Select the All Communities view and
scroll to find the Plant Bioinformatics Vol. 3 Tutorial community.  You may
also search for any application by name in the Apps catalogue.

----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - SRR_Acc_List.txt
      - Accession list from the SRA
      - |SRR_Acc_List|

*Use sra-tools prefetch app to import SRA data*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. In the |Discovery Environment|, go to **Apps** and search for **sra-tools prefetch**.
   You can use this direct link: |sra-tools prefetch app|

  .. note::

    All applications used in this tutorial are collected in the **Plant Bioinformatics Vol. 3 Tutorial** community (The apps navigation window has a **My Communities** directory where you may also find this community and the apps if you have joined that community as mentioned above).

2. Click on the App name to open the application window.

3. (Optional) you can name this analysis and provide any comments in the **App launch window**.

4. Under **Select output folder**, navigate to the **rna-seq-tutorial** folder created earlier. Your outputs will automatically be placed in this folder. **Note**: In your **Preferences and groups** menu, the **Preferences** setting will allow you to change the default setting (i.e., your **analyses** folder) for your outputs. This can be useful when you will be doing several analyses and you want them to go to a folder other than your analyses folder.

5. In the **App launch window**, go to the **accession list** section. Under **Accession list** browse to your **rna-seq-tutorial** folder and browse the **metadata** folder; select **SRR_Acc_List.txt** as input.

6. (optional) Each application in the Discovery Environment has a ‘Resource Requirements’ option. These are some minimal computational resources that you can choose for the application. When the Discovery Environment launches an analysis job, it may be run on computing hardware of various capabilities (according to what “nodes” are available to accept the job). App developers may have set minimums here, or you may choose to make adjustments. If you don’t know which minimums to choose, you can ignore these options. If you do run into errors, you can contact CyVerse support. Also contact support if the resources you need for an app do not appear in the list of options; CyVerse can increase these minimums.

7. Click **Launch Analysis** to begin the analysis job. You will get notification(s) in the Discovery Environment about the status of the job, including an email (by default preferences settings) when the job is complete.

8. To see the current status of the job, click on the **Analyses button**. When the job is complete, you can click on the job name (e.g., **sra-tools_prefetch_analysis1**) to open a data window and browse the results. Note: You may need to Refresh to see the current job status.

  .. note::

    This job will vary on connection speed between the CyVerse servers and NCBI. This job is estimated to take about 15-30 minutes.

9. Back in the **Analyses** window, go back and select (checkbox) the analysis (e.g. **sra-tools_prefetch_analysis1**) and select the **Analyses menu**. And choose **View Parameters**. This will present the parameters used in this analysis. Then choose **Save to File**; save this text file in your output folder (e.g., **rna-seq-tutorial/sra-tools_prefetch_analysis1-2020-10-04-11-40-57.1**) as **job_parameters.txt**. Although this job has few parameters, routinely saving your parameters to a file for analyses you have completed is a recommended reproducibility practice.

10. The resulting output will be 12 folders (one for each accession), each containing a single SRA file (e.g., SRR9666131.sra, SRR9666132.sra …).


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - SRA files (SRR9666131.sra, SRR9666132.sra …)
      - These are sequence data in the SRA format
      - |SRA files|


----

**Description of output and results**

The imported SRA files should be validated for their integrity - these are large files and we want to make sure the data has not be corrupted. We will
do this integrity check in the next step.

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
