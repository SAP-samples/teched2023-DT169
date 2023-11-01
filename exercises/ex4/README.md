# Exercise 4 - Create KPI tile for Story

In this exercise, we will create a KPI tile to launch the same Story.  

KPIs are used to identify and measure key metrics of a business. The different visualizations of KPI tiles help users quickly evaluate the performance of their business towards a goal, from the Fiori Launchpad itself.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/1.png)

The goal of this exercise will be to create a Numeric tile to display the Number of open purchase order items on the Fiori Launchpad tile and on clicking of the tile, the custom created Story should be launched.

## Exercise 4.1 Create KPI from Manage KPIs and Reports

Go to the **Analytics Page** in Fiori Launchpad.
Under **KPI Design** group, launch the **Manage KPIs and Reports** application. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/2.png)

A list of Groups will be displayed.

Click on **Create**.

Enter title for the Group ‘DT_169_XXX Group’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

Click on **Save and Activate**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/3.png)


Go to **KPIs** section and click on **Add** button. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/4.png)

Enter the title as ‘DT_169_XXX Purchase Order KPI’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/5.png)

Scroll to the **Data Source** section and click on **Define**. 

Search for your custom analytical query ‘YY1_PURCHASING_DT169_XXX’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

Select the view, the oData service and Entity set will get automatically populated.

Click on OK. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/6.png)

Click on the Value help for **Value Measure** and select ‘Number of Open PO Items from..’.

The other fields can remain as they are. 

Maintain the **Threshold** values as shown in the image below. 

Click on **Save and Activate**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/7.png)

You will be navigated to the Display KPI page. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/8.png)

## Exercise 4.2 Create and publish KPI tile to launch story 

Go back to the main page of Manage KPIs and Reports. 

Switch to the **Stories** tab and search for your Story ‘DT169-XXX Purchasing Spend Dashboard’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/9.png)

Click on the row to navigate to your story details page and go to the Applications tab.

Click on **Add Tile**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/10.png)

Select **Numeric Tile** and click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/11.png)

Change the title and subtitle according to your requirement. 

Click on the value help for KPI name and search for the your KPI ‘DT_169_XXX Purchase Order KPI’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

Add Semantic Object as ‘DT169_XXX_KPI’.(_XXX should be replaced with your group number for eg for place number 25 it is 025_)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/12.png)

Click on **Save and Publish**. 

From the Custom Catalog Extensions application, publish your tile to ‘**SAP_MM_BC_PO_MANAGE_PC**’ , similar to the steps done in Exercise 2.4.

Repeat the steps in Exercise 2.5 to add the tile in the ‘**Purchase Order Processing**’ section. For reference: [Exercise 2.5 -  Accessing the application from Fiori Launchpad ](../ex2/README.md#exercise-25-accessing-the-application-from-fiori-launchpad)

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/13.png)

You can now launch your SAC Story from a KPI tile that displays the value of the main measure (that is, the calculated measure Number of Open PO Items from.. created in the custom analytical query) in a Numeric format. 

Go to the ‘Open Purchase Orders’ page of your story, and you will see that the **Number of Open PO items** displayed in your numeric point chart matches the data that was displayed on the Fiori Launchpad tile.


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex4/images/14.png)



## Summary

You've now created a custom KPI and used this KPI to create an application to launch embedded analytical story and published it as an application

Continue to - [Exercise 5 - Considering Default Values in SAC Stories ](../ex5/README.md)


