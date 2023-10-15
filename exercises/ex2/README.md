# Exercise 2 - Design and publish custom SAC Stories 

In this exercise, we will design a SAC Story by copying and enhancing a pre-defined story from the Manage KPIs and Reports application. The charts in this story will be configured on the custom analytical query created in Exercise 1. Once the story is activated, we will create an application to launch the story directly from the Fiori Launchpad.

## Exercise 2.1 Access embedded SAC stories from Manage KPIs and Reports

Go back to the Analytics Page in Fiori Launchpad.
Under KPI Design group, launch the Manage KPIs and Reports application.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/0f615881-743f-4418-8319-b3dd7055047d)

Go to the ‘**Stories**’ tab. You will find the list of embedded analytical stories under the ‘**Embedded Stories**’ section. 

Search for ‘Purchasing Spend Dashboard’. 
The search result will display the predefined story. Click on the row to navigate inside the Purchasing Spend Dashboard story details page.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/e5d01ac6-6588-4e37-a8be-b31720884bee)

## Exercise 2.2 Copy pre-defined dashboard and enhance the story with the custom analytical query

Switch to **Configuration** section to view the predefined story configuration.
Click on **Copy** button on the top of the screen.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/82ece805-4243-438a-af01-041330aa200f)

Enter the title as ‘DT169-XXX Purchasing Spend Dashboard’ and click on **Copy**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/5a343bb9-ee82-4739-911f-bf57bfdb178f)

You will be navigated to the display page of your newly copied story. 
Click on the **Edit** button on top.
To add a new page, Click on the “+” button beside **Off Contract Details** and select **Responsive**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/9298e670-6351-4808-a92c-0eb9a8480019)

Rename the page by clicking on the down arrow beside ‘**Page 1**’.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f31af115-0556-4399-a5a1-22da002cc99a)

Enter ‘Open Purchase Orders’ as the new name for the page. 

Under Data section, add New Data source.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/e9330ebf-26e6-4984-9d8b-9c863f1d357b)

Search for the custom analytical query created in Exercise 1, i.e, **YY1_PURCHASING_DT169_XXX**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/8f149219-9881-44a5-9ae1-fe5004f1d6dc)

A prompt will be displayed to set the variables for the data source. Since the filter values were already prefilled during the query designing, no change is required here. 
Click on **Set**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/4b2f1b31-f567-441e-a636-eda1479a62c2)

## Exercise 2.3 Add widgets and activate the story

First, we will add a chart to see the Number of Open PO Items per Supplier. The **Number of Open PO Items** is the calculated measure that was introduced in the custom query. 
Under the **Insert** section, click on the **Chart** icon to add a new chart.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/bfa9a843-70b4-4b3f-9687-84d3df2089a4)

In the **Builder** section, scroll down to **Measures** section and click on **Add Measure**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/648d8b11-a8ca-4a09-ab54-b13905f312d7)

Select ‘**Number of Open PO items from…**’ .

Under Dimensions sections, click on Add Dimensions and select ‘**Supplier**’ and ‘**Name of Supplier**’.
The chart will get updated with the appropriate title on the widget. 
Similarly, add another chart widget that will display the Number of open PO Items per Purchasing Organization Name. 
Along with selecting the required measures and dimensions, you can also change the Chart orientation from ‘Horizontal’ to ‘Vertical’.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/c3e54273-1fe0-4aff-b47e-b5ba19a7d897)

The chart data will get updated in real time inside the widgets.

Now we will add a chart configured on a new calculated measure. 
Go to the empty page section on the right and add another chart widget.
In the **Builder** section, go to **Measures** section and click on **Calculated measure**. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/14b826f7-0d12-4296-9282-00d7f8bacac6)

Enter the Name as ‘PO Net Amount in Thousands’.
Inside the **Edit formula** section, type PO and select **PO Net Amount** from the suggestions.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a8f982c2-4a0b-41a4-8b1c-1798fa1747a0)

Add ‘ / 1000 ‘ after the PO Net amount to scale the amount in thousands.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/0eb8ee24-e362-4680-b5d8-f50222640370)

Click on **OK**.

In the Dimensions, add ‘**Calendar Month**’ and ‘**Supplier**’ to the same chart widget.
Change the **Chart** structure to **Trend -> Line**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/542bfb9e-29f0-439b-8e26-f4d303835c0d)

Change the titles of the page sections.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/daf6ee50-8873-4559-b1e6-18392c163ea3)

You can explore the other designing options in the Builder and add more charts to your page.

**Adding Numerical points in the story**

Add another chart with **Measure** ‘Number of Open PO Items from..’.
Change the Chart structure to **Indicator** -> **Numeric Point**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/8f758c26-8f63-456a-85de-67712d4d916a)

Go to **Color** section and click on **Add Threshold**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/aef6ad8c-3499-4680-b181-fbd11dd0dee0)

Inside thresholds, select the Measure as ‘**Number of Open PO items from…**’. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f8d07e42-eca2-4d53-86e6-28c8876b024f)

Maintain the **Ranges** as displayed in the image below. These define the thresholds for being marked in the OK, Warning or Critical state.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/e809593e-5f13-42d4-804a-f543ca9bcf31)

Click on **Apply**.

The numerical point will update the color of the data according to the defined threshold values.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2113b2fd-a9dd-4f24-84ab-dfa47fdf0010)


**Linking models within the story**

You can link dimensions between models to create charts or tables that display data from multiple models. Linked dimensions also let you create filters that simultaneously update all charts that include linked data. 

Click on the ‘**Link Dimensions**’ icon on the top. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/c1c52752-b7d9-4f37-9963-8917b4050999)

Select the model on the left as ‘C_PURCHASEORDERVALUEQUERY’ and the custom query ‘YY1_PURCHASING_DT169_XXX’ on the right dropdown.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f5e4c068-7fa7-4de5-9b49-d8c7e4a24884)


Choose the ‘**Supplier**’ dimension on both sides.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/b2025086-5802-46c3-9ace-1930fb2240f2)

Click on **Set**. Click on **Done**.

You can modify the visualization of the numerical point by selecting the required options from **Show/Hide**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/c3a72d6b-014b-491e-b54a-ab36ffcae88c)


You can explore further by adding more widgets with charts, tables, data points with different measures and dimensions. You can also rearrange and resize the widgets freely according to your design requirements.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/49525d55-8e24-4054-bea4-16856b4f7182)

Click on **Activate**.
You will be navigated to the Display Story page after successful activation. You can review the modifications from the Configuration tab.

## Exercise 2.4 Create Fiori Launchpad application to launch the story

Switch to the **Applications** tab and click on the + icon. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/aa80f1c9-67ee-4944-9430-d6a66c175204)

Select **Static** tile and click on OK.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2c835fe8-5dce-4e17-8c89-18ae7cd054b0)

Title will be pre-filled with the name of the Story. You can change the title and subtitle as per your requirement. These texts will be used to distinguish your tile in the Fiori Launchpad.

Under Target mapping section, enter the Semantic Object as ‘**DT169_XXX**’. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/85db9ac0-a889-44c3-b658-674a04cacdba)

Default Values and Navigation Intents can be left empty for this exercise.
Click on **Save and Publish**.

You will be navigated to the **Custom Catalog Extensions** app. This enables you to make an application available on the SAP Fiori Launchpad by assigning it to the required business catalogs and publishing it. 
Click on **Add** and search for the catalog ‘**SAP_MM_BC_PO_MANAGE_PC**’. 
Select the Catalog and click on **OK**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/cfa6c97a-97f7-4f20-b49a-9c19cd47e124)

Click on **Publish**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/6843a0f0-f468-4fb2-b673-bf09b99df749)

When the status changes from ‘Publishing’ to ‘Published’, your tile is ready for use.  
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/fb7f4be9-721a-4e05-b3a5-6d28cf9c2723)
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/bed4369a-a2c0-4079-825b-60ea12d0b3e4)

## Exercise 2.5 Accessing the application from Fiori Launchpad

Launch https://my407161.s4hana.cloud.sap/ui in a new tab in your browser.
From the Home page, navigate to the ‘**Purchase Order Processing**’ section under **Purchasing page**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/06d0a97b-09ed-4ccc-a693-e3d3f1a77ad8)

Go to the User settings icon on the top-right and click on **Edit Current Page**. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/68492c65-2ce3-451b-811e-28ef1b880e90)

Click on **Add tile**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/c7c1f653-dee1-4420-a583-991bb0bd03dd)

Search the title of your newly created application in the search bar. 
The search result will show your tile. Click on the **add** icon.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a1b89b07-01db-4d1a-b802-b86111cc856a)

Exit edit mode and go back to the Purchase Order Processing page.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2af8481a-6b26-4f34-aab7-e6174e52ee20)

You can now launch your Story from the Fiori Launchpad tile. Proceed to the next exercise where we will explore some of the features inside this SAC story report.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/93d6faea-1f0a-483f-8f42-6ed47f047860)

## Summary

You've now created a custom embedded analytical story and published it as an application

Continue to - [Exercise 3 - Embedded SAC Stories Runtime Analysis ](../ex3/README.md)
