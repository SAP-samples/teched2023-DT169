# Exercise 2 - Design and publish custom SAC Stories 

In this exercise, we will design a SAC Story by copying and enhancing a pre-defined story from the Manage KPIs and Reports application. The charts in this story will be configured on the custom analytical query created in Exercise 1. Once the story is activated, we will create an application to launch the story directly from the Fiori Launchpad.

## Exercise 2.1 Access embedded SAC stories from Manage KPIs and Reports

Go back to the Analytics Page in Fiori Launchpad.

Under KPI Design group, launch the **Manage KPIs and Reports** application.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/1.png)

Go to the ‘**Stories**’ tab. You will find the list of embedded analytical stories under the ‘**Embedded Stories**’ section. 

Search for ‘Purchasing Spend Dashboard’. 

The search result will display the predefined story. Click on the row to navigate inside the Purchasing Spend Dashboard story details page.

Switch to **Configuration** section to view the predefined story configuration.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/2.png)

## Exercise 2.2 Copy pre-defined dashboard and enhance the story with the custom analytical query


Click on **Copy** button on the top of the screen.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/3.png)

Enter the title as ‘DT169-XXX Purchasing Spend Dashboard’ and click on **Copy**.
(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/4.png)

You will be navigated to the display page of your newly copied story. 

Click on the **Edit** button on top.

To add a new page, Click on the “+” button beside **Off Contract Details** and select **Responsive**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/5.png)

Rename the page by clicking on the down arrow beside ‘**Page 1**’.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/6.png)

Enter ‘Open Purchase Orders’ as the new name for the page. 

Under Data section, add New Data source.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/7.png)

Search for the custom analytical query created in Exercise 1, i.e, **YY1_PURCHASING_DT169_XXX**.
(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/8.png)

A prompt will be displayed to set the variables for the data source. Since the filter values were already prefilled during the query designing, no change is required here. 

Click on **Set**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/9.png)

## Exercise 2.3 Add widgets and activate the story

First, we will add a chart to see the Number of Open PO Items per Supplier. Note that **Number of Open PO Items** is the field which was added in the custom query as a new calculated measure. 

Under the **Insert** section, click on the **Chart** icon to add a new chart.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/10.png)

In the **Builder** section, scroll down to **Measures** section and click on **Add Measure**.
![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/11.png)

Select ‘**Number of Open PO items from…**’ .

Under Dimensions sections, click on **Add Dimensions** and select ‘**Supplier**’ and ‘**Name of Supplier**’.

The chart will get updated with the appropriate title on the widget. 

Similarly, add another chart widget that will display the Number of open PO Items per Purchasing Organization Name. 

Along with selecting the required measures and dimensions, you can also change the Chart orientation from ‘Horizontal’ to ‘Vertical’.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/12.png)

The chart data will get updated in real time inside the widgets.

Now we will add another calculated measure and add a chart for it. 

Click on the empty space in the page section on the right and add another chart widget.

In the **Builder** section, go to **Measures** section and click on **Calculated measure**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/13.png)

Enter the Name as ‘PO Net Amount in Thousands’.

Inside the **Edit formula** section, type PO and select **PO Net Amount** from the suggestions.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/14.png)

Add ‘ / 1000 ‘ after the PO Net amount to scale the amount in thousands.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/15.png)

Click on **OK**.

In the Dimensions, add ‘**Calendar Month**’ and ‘**Supplier**’ to the same chart widget.

Change the **Chart** structure to **Trend -> Line**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/16.png)

Change the titles of the page sections.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/17.png)

You can explore the other designing options in the Builder and add more charts to your page.


**Adding Numerical points in the story**

Add another chart with **Measure** ‘Number of Open PO Items from..’.

Change the Chart structure to **Indicator** -> **Numeric Point**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/18.png)

Go to **Color** section and click on **Add Threshold**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/19.png)

Inside thresholds, select the Measure as ‘**Number of Open PO items from…**’. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/20.png)

Maintain the **Ranges** as displayed in the image below. These define the thresholds for being marked in the OK, Warning or Critical state.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/21.png)

Click on **Apply**.

The numerical point will update the color of the data according to the defined threshold values.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/22.png)



**Linking models within the story**

You can link dimensions between models to create charts or tables that display data from multiple models. Linked dimensions also let you create filters that simultaneously update all charts that include linked data. 

Click on the ‘**Link Dimensions**’ icon on the top. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/23.png)

Select the model on the left as ‘C_PURCHASEORDERVALUEQUERY’ and the custom query ‘YY1_PURCHASING_DT169_XXX’ on the right dropdown.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/24.png)


Choose the ‘**Supplier**’ dimension on both sides.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/25.png)

Click on **Set**. Click on **Done**.

You can modify the visualization of the numerical point by selecting the required options from **Show/Hide**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/26.png)


You can explore further by adding more widgets with charts, tables, data points with different measures and dimensions. 
You can also rearrange and resize the widgets freely according to your design requirements.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/27.png)

Once your story configuration is completed, click on the **Definition** tab on top. Since this is a copied story, the Description and the Tags is already populated from the parent story. You can modify these as per your requirements.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/Definition.png)

Click on **Activate**.

You will be navigated to the Display Story page after successful activation. 

You can review the modifications from the **Configuration** tab.

## Exercise 2.4 Create Fiori Launchpad application to launch the story

Switch to the **Applications** tab and click on the + icon. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/28.png)


Select **Static** tile and click on OK.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/29.png)

Title will be pre-filled with the name of the Story. You can change the title and subtitle as per your requirement. These texts will be used to distinguish your tile in the Fiori Launchpad.

Under Target mapping section, enter the Semantic Object as ‘**DT169_XXX**’. 
(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/30.png)

Default Values and Navigation Intents can be left empty for this exercise.

Click on **Save and Publish**.

You will be navigated to the **Custom Catalog Extensions** app. This enables you to make an application available on the SAP Fiori Launchpad by assigning it to the required business catalogs and publishing it. 

Click on **Add** and search for the catalog ‘**SAP_MM_BC_PO_MANAGE_PC**’. 

Select the Catalog and click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/31.png)

Click on **Publish**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/32.png)

When the status changes from ‘Publishing’ to ‘Published’, your tile is ready for use.  

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/33.png)


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/34.png)

## Exercise 2.5 Accessing the application from Fiori Launchpad

Launch https://my407161.s4hana.cloud.sap/ui in a new tab in your browser.

From the Home page, navigate to the ‘**Purchase Order Processing**’ section under **Purchasing page**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/35.png)

Go to the User settings icon on the top-right and click on **Edit Current Page**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/36.png)

Click on **Add tile**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/37.png)

Search the title of your newly created application in the search bar. 

The search result will show your tile. Click on the **add** icon.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/38.png)

Exit edit mode and go back to the Purchase Order Processing page.
![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/39.png)

You can now launch your Story from the Fiori Launchpad tile. Proceed to the next exercise where we will explore some of the features inside this SAC story report.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex2/images/40.png)

## Summary

You've now created a custom embedded analytical story and published it as an application

Continue to - [Exercise 3 - Embedded SAC Stories Runtime Analysis ](../ex3/README.md)
