# Exercise 4 - Create KPI tile for Story

In this exercise, we will create a KPI tile to launch the same Story.  

KPIs are used to identify and measure key metrics of a business. The different visualizations of KPI tiles help users quickly evaluate the performance of their business towards a goal, from the Fiori Launchpad itself.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2b361e60-7bcd-46ae-897d-d4e2c52887fe)

The goal of this exercise will be to create a Numeric tile to display the Number of open purchase order items on the Fiori Launchpad tile and on clicking of the tile, the custom created Story should be launched.

## Exercise 4.1 Create KPI from Manage KPIs and Reports

Go to the **Analytics Page** in Fiori Launchpad.
Under **KPI Design** group, launch the **Manage KPIs and Reports** application. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/c739e266-c8d0-44e8-af7c-bc49ed9fe1a8)

A list of Groups will be displayed. Click on **Create**.
Enter title for the Group ‘DT_169_XXX Group’.
Click on **Save and Activate**. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/04540932-660c-4ec7-a9f4-68fae2166897)


Go to **KPIs** section and click on **Add** button. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/add51599-23f4-4b08-a454-6ca5aaa2a657)

Enter the title as ‘DT_169_XXX Purchase Order KPI’.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/c009cb3f-288c-420b-ac90-c88bb6b7e2a1)

Scroll to the **Data Source** section and click on **Define**. 
Search for your custom analytical query ‘YY1_PURCHASING_DT169_XXX’.
Select the view, the oData service and Entity set will get automatically populated.
Click on OK. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/aebafd4f-032b-436f-b89c-a737e065e980)

Click on the Value help for **Value Measure** and select ‘Number of Open PO Items from..’.
The other fields can remain as they are. 
Maintain the **Threshold** values as shown in the image below. 
Click on **Save and Activate**. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/4a5bcb20-333a-4388-91e7-168ea321974f)

You will be navigated to the Display KPI page. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/bc8adc8f-3f59-4e3c-9451-bd42c5770af2)

## Exercise 4.2 Create and publish KPI tile to launch story 

Go back to the main page of Manage KPIs and Reports. 
Switch to the **Stories** tab and search for your Story ‘DT169-XXX Purchasing Spend Dashboard’. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/68b18a20-be73-401f-b024-ad1877c131f2)

Click on the row to navigate to your story details page and go to the Applications tab.
Click on **Add Tile**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/fa6947c2-f961-4d9e-9b95-dd91f34db290)

Select **Numeric Tile** and click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a24b65b0-2011-4f03-b4dc-acba94dc2ba5)

Change the title and subtitle according to your requirement. 

Click on the value help for KPI name and search for the your KPI ‘DT_169_XXX Purchase Order KPI’.  
Add Semantic Object as ‘DT169_XXX_KPI’. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/5beaaad8-2b59-4fdd-8d05-5b4031cc023f)

Click on **Save and Publish**. 
From the Custom Catalog Extensions application, publish your tile to ‘**SAP_MM_BC_PO_MANAGE_PC**’ , similar to the steps done in Exercise 2.4.
Repeat the steps in Exercise 2.5 to add the tile in the ‘**Purchase Order Processing**’ section. For reference: [Exercise 2.5 -  Accessing the application from Fiori Launchpad ](../ex2/README.md#exercise-25-accessing-the-application-from-fiori-launchpad)

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/b531df1f-24eb-447a-8703-7b6282035e62)

You can now launch your SAC Story from a KPI tile that displays the value of the main measure (that is, the calculated measure Number of Open PO Items from.. created in the custom analytical query) in a Numeric format. 

Go to the ‘Open Purchase Orders’ page of your story, and you will see that the **Number of Open PO items** displayed in your numeric point chart matches the data that was displayed on the Fiori Launchpad tile.


## Summary

You've now created a custom KPI and used this KPI to create an application to launch embedded analytical story and published it as an application

Continue to - [Exercise 5 - Considering Default Values in SAC Stories ](../ex5/README.md)


