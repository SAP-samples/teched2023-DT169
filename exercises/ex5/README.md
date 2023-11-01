# Exercise 5 - Considering User Default values in SAC Stories

In this exercise, In this exercise, we will explore how to use Default values for our SAC applications.

SAC story applications can be launched with user-specific default values which can be saved in the Fiori Launchpad settings and reused between multiple applications. This helps in reducing the time spent in applying commonly used filter values. For example, default company codes, plants, cost centers, sales areas, etc. 


## Exercise 5.1	Change Designtime tile to consider default values


Go to the **Analytics Page** in Fiori Launchpad.

Under KPI Design group, launch the Manage KPIs and Reports application.
 
![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-1.png)

Switch to the **Stories** tab and search for your Story ‘DT169-XXX Purchasing Spend Dashboard’. 

Click on the **Applications** count on the right.

Select the KPI based **Numeric tile**.  

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-2.png)

Click on **Edit** button. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-3.png)

Scroll down to the **Default Values** section and click on **Add**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-4.png)

Search for ‘Display Currency’ and click on the checkbox to select it.

Search for  ‘Purchasing Org.’  and select it similarly.

Click on **Select**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-5.png)

Click on **Save and Publish**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-6.png)


The status will be displayed as ‘**Publishing**’ in Custom Catalog Extensions application. Wait for the status to change to ‘**Published**’.

## Exercise 5.2	Change User Default values on FLP

Go back to Fiori Launchpad and switch to **Purchase Order Processing** page where your tiles are already present. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-7.png)

Click on the User settings menu on the top-right and click on **Settings**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-8.png)

Select **Default Values**. 

Add ‘USD’ in the **Display Currency** field. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-9.png)

Search for **Purchasing Org.** in the list and search for ‘_US Purchasing Org_’. Select the value. 

Click on **Save**.  

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-10.png)

**This sets the default values as Display Currency = USD and Purchasing Org. = 1710.**


Click on the **Refresh** button at the bottom of the KPI tile.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-11.png)


The data will get updated according to the Default values maintained in the Fiori Launchpad settings.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-12.png)

Click on the tile to navigate inside the story. 

The Default values will automatically be applied as filter values for all the charts in the story. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex5/images/ex5-13.png)


## Summary

You have now configured your application to consider default values in analytical reports

Continue to - [Exercise 6 - Create and launch Generic Drilldown report for KPI ](../ex6/README.md)


