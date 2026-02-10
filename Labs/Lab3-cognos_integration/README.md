# Lab 3 - Maximize Cognos Analytics Investments to Deliver Conversational BI Experience

This lab dives into the **data configuration experience** with **IBM Cognos Analytics Framework Manager (FM) Packages**.

Here, you will take the role of a **data steward**, **data modeler**, or **data analyst** to set up and enrich a **semantic layer** - the foundation for consistent and accurate business insights.

---

- [Lab 3 - Maximize Cognos Analytics Investments to Deliver Conversational BI Experience](#lab-3---maximize-cognos-analytics-investments-to-deliver-conversational-bi-experience)
  - [Section 1: Metadata \& Semantic data model export](#section-1-metadata--semantic-data-model-export)
    - [1.1 Create a project](#11-create-a-project)
    - [1.2 Create Medatadata Import](#12-create-medatadata-import)
    - [1.3 Create Connection to IBM Cognos Analytics](#13-create-connection-to-ibm-cognos-analytics)
  - [Section 2: Export Metrics Definition](#section-2-export-metrics-definition)
  - [Section 3: Conversation](#section-3-conversation)
    - [Sample Questions to Test](#sample-questions-to-test)


---

## Section 1: Metadata & Semantic data model export

This section contains the steps to perform metadata import and importing the semantic model from IBM Cognos Analytics Framework Manager (FM) package into Watsonx BI.

### 1.1 Create a project

A project is a collaborative workspace where users can work with their data and other assets to accomplish a particular goal, such as creating metrics. You will begin by creating a project to store all the materials you will use for your analysis.

1. Hover over the left-side of interface to open watsonx BI’s **side navigation panel**, and then select **Data and Metrics (A)** <br><br>

    ![screenshot](./attachments/1.0.png) <br><br>

2. Create a new project by selecting the **plus sign (+)** in the upper right-side of the interface (A), Enter the name **Cognos_FM** for the new project (B) and Select the blue **Submit** button (C). <br><br>

    ![screenshot](./attachments/1.png) <br><br>


### 1.2 Create Medatadata Import

You can capture and import asset metadata and lineage information for the data in your organization. This data can be on a wide variety of data sources. When you import asset metadata, assets are created.

1. Click on the hamburger menu (A) to **View all projects** (B). <br><br>

    ![screenshot](./attachments/2.png) <br><br>

2. Select Your Project from the list of projects - **Cognos_FM** <br><br>

    ![screenshot](./attachments/3.png) <br><br>

3. Create a New Asset - Within the selected project, go to **Assets** (A) → **Create a new asset** (B). <br><br>

    ![screenshot](./attachments/4.png) <br><br>

4. Import Metadata for Data Assets - Choose **Import metadata for data assets**. <br><br>
   
    ![screenshot](./attachments/5.png) <br><br>

5. Define Metadata Import Details - Enter the name **CA_FM_GoSales** (A) and proceed with **Next** (B).  <br><br>

    ![screenshot](./attachments/6.png) <br><br>

6. Define Goals for the Metadata Import - Select **Import asset metadata** (A) and click **Next** (B).  <br><br>

    ![screenshot](./attachments/7.png)  <br><br>

7. Select Data Source & Scope - Choose **Connection** as the data source. <br><br>

    ![screenshot](./attachments/8.png) <br><br>

### 1.3 Create Connection to IBM Cognos Analytics

8. Click **Create a new connection**. <br><br>

    ![screenshot](./attachments/9.png) <br><br>
  
9. The **Add connection** window appears. From the list of available data sources on the left panel, select **IBM Cognos Analytics** (A). <br><br>

10. Select the **IBM Cognos Analytics** connector tile (B) <br><br>

11. Click the blue **Next** button (C). <br><br>

    ![screenshot](./attachments/10.png) <br><br>

12. The **Create connection: IBM Cognos Analytics** screen appears. Within the Connection overview subsection, enter **cognos_fm_connection** as the **Name** (A) and provide an optional description (B). <br><br>

13. In the **Connection details** subsection, Paste the connection details shared with you under **Gateway URL** (C). <br><br>
  
    ![screenshot](./attachments/11.png) <br><br>

14. (A) In the **Credentials** subsection, select **User credentials** as **Authentication method** and enter the credentials shared with you under -
    - **Namespace ID**
    - **Username**
    - **Password** <br><br>
  
15. Click the **Test connection** link in the upper right of the interface (B). <br><br>
    
16. You should receive a banner with a green checkmark indicated that **The test was successful** (F). If you receive an error, double-check that you have entered the correct information above. <br><br>
    
17. Click the blue **Create** button (C). <br><br>

    ![screenshot](./attachments/12.png) <br><br>

18. Once the connection is created, you'll be back to the metadata import creation page. Next, verify **Connection** (A) and **Select assets** (B) for the data scope. <br><br>

    ![screenshot](./attachments/13.png) <br><br>

19. The **Select scope from the connection** window appears. Under **Databases**, select **Team Content** (A) <br><br>

20. Under the **Team Content** database, check the **GO Data Warehouse (query)** package (B) and click the blue **Select** button (C). <br><br>

    ![screenshot](./attachments/14.png) <br><br>

21. Verify the selected assets (A) and proceed with **Next** (B). <br><br>

    ![screenshot](./attachments/15.png) <br><br>

22. Define Job Details - Enter **CA_FM_GoSales job** as the Job name (A) and proceed to the **Next** step (B). <br><br>

    ![screenshot](./attachments/16.png) <br><br>

23. Skip the advanced options and click **Next**. <br><br>

    ![screenshot](./attachments/17.png) <br><br>

24. Review all configurations and click **Create** to complete metadata import. <br><br>

    ![screenshot](./attachments/18.png) <br><br>

25. Your metadata import job will begin. You may need to wait for the job to complete. You can refresh the status using the **Refresh** button. <br><br>

    ![screenshot](./attachments/19.png) <br><br>

    The banner saying **Metadata Import complete** means it is successfully imported.<br>
    ![screenshot](./attachments/19.1.png) <br><br>

26. Once imported, return to your project. You’ll now see both **Metadata import** and a **Semantic data model**. <br><br>

    ![screenshot](./attachments/20.png) <br><br>

## Section 2: Export Metrics Definition

In this section you'll export the Cognos metrics definition and converse with it.

1. Click on the **Semantic data model** to view the model. <br><br>

    ![screenshot](./attachments/21.png) <br><br>

2. In the **Semantic model** page, select **Employee-Course Data** (A), click on the 3-dot ellipsis (B), and choose **Export metrics definition** (C) (since this is an FM package and metrics are already generated). <br><br>

    ![screenshot](./attachments/22.png) <br><br>

    If you can't find **Employee-Course Data**, search "gross" keyword (A), you might be able to find multiple results (B) choose one of **metrics** (C), click on the 3-dot ellipsis, and choose **Export metrics definition**. <br><br>

    ![screenshot](./attachments/40.png) <br><br>

3. Now, Go back to your project. You’ll see two new assets created (A): **Metric** and **Metadata Enrichment**. Click on the Export Metrics Job (B) to check for its status.<br><br>

    ![screenshot](./attachments/23.png) <br><br>

4. On the **Job Details** page you'll see a job run (A) created, you can refresh (B) to get the lastest status. <br><br>

    ![screenshot](./attachments/23.1.png) <br><br>

5. Once the status changes to **Completed**, click on it to see its details. <br><br>

    ![screenshot](./attachments/23.2.png) <br><br>

6. On the Job run details page, you can see **Compute vectors objective** (A) failed. To check for why, click on **Log** (B). <br><br>

    ![screenshot](./attachments/23.3.png) <br><br>

7. Scrolling down the log shows a non-fatal asset issues (A). This is relate to an asset which does not have string data to vectorise, so they can be ignored. All good! We are all set to have a conversation with our data.<br><br>
   
8. Click on the **IBM Watsonx BI** logo in the upper-left of the interface (B) to go to the conversation page.<br><br>

    ![screenshot](./attachments/23.4.png) <br><br>


## Section 3: Conversation

The Conversations page is where you interact with the data and metrics through natural language questions to gain business insights from the data.

1. Create a **New conversation** (A) and select your project - **Cognos_FM** as the data source. <br><br>

    ![screenshot](./attachments/24.png) <br><br>

2. Ask a question and observe the response. <br><br>

    ![screenshot](./attachments/25.png) <br><br>

### Sample Questions to Test

1. Show me total revenue for each year 
2. Which product line generated the highest revenue in the year 2013? 
3. What is the quantity by city for the state of California in the year 2011? 
4. Show me the gross profit by country for the year 2012
<!-- 5. Which order method type had the highest planned revenue in the year 2010?  -->
5. Which product had the highest gross profit in the year 2011? 
6. Compare the average unit sale price between different states. 
7. Can you provide the cost of goods sold by product line? 
8. What was the average unit price for the 'Camping Equipment' product line in the year 2012?  
9. Show me a pie chart of Revenue by Product Line 
10. Can you show a chart of the top 5 products by revenue in the United States? 
11. Which country had the highest average gross profit?

<!-- ## Section 4: Validate Cognos Data Source Connection - Optional

The section of the lab is to illustrate the key point that whenever there are changes to the Cognos Package the Watsonx BI team needs to be in the loop on the changes.  This is critical to ensure watsonx BI configuratiion is such metadata and  metrics definitions are kept upto date with the Cognos package changes.  This section of the lab is a demonstration of the impact to watsonx BI configuration when there are changes to the Cognos package name.


1. To confirm Cognos integration, open the **Cognos Analytics Service Dashboard** by visiting the **Cognos Analytics Gateway URL** (A) shared with you. <br><br>
   
2. Log in (D) to the dashboard by using the credentials shared with you:
   - **User ID** (B)
   - **Password** (C) <br><br>

    ![screenshot](./attachments/26.1.png) <br><br>

3. Click on the **hamburger menu** (A) and find **Content** folder (B) and click on it. <br><br>

    ![screenshot](./attachments/26.2.png) <br><br>
   
4. In **Content** folder, navigate to the **Team content** and you'll see **GO Data Warehouse (query)** FM package (A), click on the 3-dot ellipsis (B), and select **Properties** (C). <br><br>

    ![screenshot](./attachments/26.png) <br><br>

5. Update the package name from **GO Data Warehouse (query)** to **GO Data Warehouse (query)-1** (A) and **Save** (B). <br><br>
   
    ![screenshot](./attachments/27.png)  <br><br>

6. Return to **IBM Watsonx BI** conversation experience and ask the same question. This time it will not work as expected. <br><br>

    ![screenshot](./attachments/28.png) <br><br>

7. Now, go back to the Cognos Dashboard and Revert the changes made in the Cognos package. <br><br>

    ![screenshot](./attachments/29.png) <br><br>

8. Ask the same question again in **IBM Watsonx BI**. This time it works as expected - this validates the connection. <br><br>

    ![screenshot](./attachments/30.png) <br><br> -->
