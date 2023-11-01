# Exercise 6 - Create and launch Generic Drilldown report for KPI

In this exercise we will create a different type of analytical report available in S/4HANA, the Generic drilldown reports for KPIs.

Generic reports are visualizations using charts and tables in which the data is filtered based on values defined in the KPI.


## Exercise 6.1	Create Generic Drilldown Reports using Manage KPIs and Reports


Go to the **Analytics Page** in Fiori Launchpad.

Under **KPI Design** group, launch the **Manage KPIs and Reports** application.

Click on the **KPIs** tab.

Search for your KPI ‘DT169_XXX Purchase Order KPI’ and click on the row to navigate to the details page.

Click on **Create Report -> Generic Drilldown**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-1.png)


The **Definition** section is prefilled with the name of the KPI. You can change it to any suitable name for your Report. 

Switch to the **Configuration** section. 

**Mini Tiles**

You can add miniature tile visualizations to your drill-down report. These mini charts are supported by visualizations, such as number, trends, comparisons, actual vs. target, and comparison of multiple measures. These visualizations can be configured to show the data for the current KPI and also associated KPIs. 

Under **Mini tiles** section click on **Add** button.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-2.png)


Change Tile Format to **Trend tile**.

Select the Dimension as ‘**Calendar Month**’ and sort order as Dimension Ascending.

Click on OK.  

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-3.png)


Click on **Add** to add another mini tile.

Change Tile format to **Comparison – Multiple Measure tile**. 

Measure selections can be left as is pre-filled. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-4.png)



**Configuring Views**


Under Charts and Tables section, click on **Add**.  

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-5.png)

Enter the View title as ‘**By Purchasing Org.**’ and click on **Add**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-6.png)


Click on the **Settings** button on the toolbar of the chart area.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-7.png)


Select the dimensions and measures as shown in the image. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-8.png)


Change the Chart type to Pie Chart.


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-9.png)


Similarly add another view named ‘Document View’, and select View Type as **Table**.


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-10.png)


Click on the **settings** icon and select all the Columns. 

You can rearrange the fields to place the Dimensions before the Measures in the Columns settings.


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-11.png)


Under **Navigation Intents**, add the semantic object & Action of the KPI tile which was created in Exercise 4.2 ( DT169_XXX_KPI - analyze).
(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

For reference: [Exercise 4.2 - Create and publish KPI tile to launch story ](../ex4/README.md#exercise-42-create-and-publish-kpi-tile-to-launch-story)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-12.png)


Click on **Activate**. You will be navigated to the Display page. You can review the configuration here.


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-13.png)


## Exercise 6.2	Create and publish application for Generic drilldown report

Now we will create a Fiori Launchpad tile to launch this Generic drilldown report. 

Click on **Applications** tab.

Create another tile with the following configuration.

**Tile format** : Actual vs. Target Tile

Title : “DT169_XXX Purchasing Group Analysis” (_XXX should be replaced with your group number for eg for place number 25 it is 025_)

**Subtitle** : “Open PO Items”  

KPI name will already be pre-populated.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-14.png)

Add Semantic Object as “DT169_XXX_Report”. (_XXX should be replaced with your group number for eg for place number 25 it is 025_)

Click on Save and Publish. 


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-15.png)


From the Custom Catalog Extensions application, publish your tile to ‘**SAP_MM_BC_PO_MANAGE_PC**’ , similar to the steps done in Exercise 2.4.

Reference: [Exercise 2.4 Create Fiori Launchpad application to launch the story](../ex2/README.md#exercise-24-create-fiori-launchpad-application-to-launch-the-story)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-16.png)



Repeat the steps in Exercise 2.5 to add the tile in the ‘Purchase Order Processing’ section. 

Reference: [Exercise 2.5 -  Accessing the application from Fiori Launchpad ](../ex2/README.md#exercise-25-accessing-the-application-from-fiori-launchpad)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-17.png)


## Exercise 6.3	Launch Generic drilldown report application

Launch the application from the tile.
Click on the ‘**Toggle Data Label visibility**’ to view the numerical values on the pie chart.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-18.png)


Select the section of the pie chart representing the data for ‘US Purchasing Org’.

Click on the **Jump To** button on top and click on the ‘DT169 – XXX Purchasing Spend Dashboard’. This application appears as an available option to Jump to, because the semantic object and action for this app was added in the tile configuration under Navigation Intents.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-19.png)


You will be navigated to your Story application with the context of ‘US Purchasing Org’ applied as a filter.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-20.png)


The Purch. Organization filter passed from the Generic drilldown report to this Story is applied on all models. This is another example of Intent based navigation.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-21.png)

Go back to the Generic drilldown page.

Click on ‘**Show Mini Tiles**’ to view the tile visualizations configured as mini tiles.

Switch the view to ‘**Document view**’ to see the table view in the Generic drilldown. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex6/images/ex6-22.png)




## Summary


You have now created and launched a generic drilldown report based on a KPI




