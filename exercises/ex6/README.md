# Exercise 6 - Create and launch Generic Drilldown report for KPI

In this exercise we will create a different type of analytical report available in S/4HANA, the Generic drilldown reports for KPIs.

Generic reports are visualizations using charts and tables in which the data is filtered based on values defined in the KPI.


## Exercise 6.1	Create Generic Drilldown Reports using Manage KPIs and Reports


Go to the **Analytics Page** in Fiori Launchpad.
Under **KPI Design** group, launch the **Manage KPIs and Reports** application.
Click on the **KPIs** tab.
Search for your KPI ‘DT169_XXX Purchase Order KPI’ and click on the row to navigate to the details page.
Click on **Create Report -> Generic Drilldown**. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/36b3ed88-6eb9-4e21-8ec4-7ac68944854f)


The **Definition** section is prefilled with the name of the KPI. You can change it to any suitable name for your Report. 
Switch to the **Configuration** section. 

**Mini Tiles**
You can add miniature tile visualizations to your drill-down report. These mini charts are supported by visualizations, such as number, trends, comparisons, actual vs. target, and comparison of multiple measures. These visualizations can be configured to show the data for the current KPI and also associated KPIs. 

Under **Mini tiles** section click on **Add** button.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/296141c9-0605-437e-9a84-8f3fee7ac4da)


Change Tile Format to **Trend tile**.
Select the Dimension as ‘**Calendar Month**’ and sort order as Dimension Ascending.
Click on OK.  

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/bcabb0d6-9960-4cc5-a330-e24506391e7f)


Click on **Add** to add another mini tile.
Change Tile format to Comparison – Multiple Measure tile. 
Measure selections can be left as is pre-filled. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/92205bc8-36f6-43d8-be0b-c611bc8fd1cb)


**Configuring Views**


Under Charts and Tables section, click on **Add**.  

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/58d6355a-70d1-4e3e-920d-d8fd524e01d0)

Enter the View title as ‘**By Purchasing Org.**’ and click on **Add**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/032580a2-1978-443a-ab9f-d35825a65b8e)


Click on the **Settings** button on the toolbar of the chart area.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/60bf2d16-f912-4436-b654-b00a5ed57fa4)


Select the dimensions and measures as shown in the image. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/d2846841-790e-4177-8699-b54092451741)


Change the Chart type to Pie Chart.


![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/be92454e-9be3-4e92-ba54-b1448d40206a)


Similarly Add another view named ‘Document View’, and select View Type as Table.


![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/eed74bd7-57be-4f7a-8fa6-14e3cb9c8065)


Click on the **settings** icon and select all the Columns. 
You can rearrange the fields to place the Dimensions before the Measures in the Columns settings.


![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/897c60ed-93b6-4fc5-b4f6-77014e761f86)


Under Navigation Intents, add the semantic object & Action of the KPI tile which was created in Exercise 4.2 ( DT_169_XXX_KPI - analyze).
For reference: [Exercise 4.2 - Create and publish KPI tile to launch story ](../ex4/README.md#exercise-42-create-and-publish-kpi-tile-to-launch-story)

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f4414206-f539-4f6e-a475-35102f22cbc8)


Click on **Activate**. You will be navigated to the Display page. You can review the configuration here.


![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/388c4e38-6162-40e6-a2d7-7f55a0ec6e31)


## Exercise 6.2	Create and publish application for Generic drilldown report

Now we will create a Fiori Launchpad tile to launch this Generic drilldown report. 
Click on **Applications** tab.
Create another tile with the following configuration.
**Tile format** : Actual vs. Target Tile
Title : “DT169_XXX Purchasing Group Analysis”
**Subtitle** : “Open PO Items”  
KPI name will already be pre-populated.




## Summary

You've now learn on how to consider default values for analytical reports

Continue to - [Exercise 6 - Design and launch custom SAC Stories ](../ex2/README.md)



