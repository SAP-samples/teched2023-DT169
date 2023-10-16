# Exercise 5 - Considering User Default values in SAC Stories

In this exercise, In this exercise, we will explore how to use Default values for our SAC applications.

SAC story applications can be launched with user-specific default values which can be saved in the Fiori Launchpad settings and reused between multiple applications. This helps in reducing the time spent in applying commonly used filter values. For example, default company codes, plants, cost centers, sales areas, etc. 


## Exercise 5.1	Change Designtime tile to consider default values


Go to the **Analytics Page** in Fiori Launchpad.
Under KPI Design group, launch the Manage KPIs and Reports application.
 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2b8d4405-d264-4fed-9091-64c945526016)

Switch to the **Stories** tab and search for your Story ‘DT169-XXX Purchasing Spend Dashboard’. 
Click on the **Applications** count on the right.
Select the KPI based **Numeric tile**.  

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/37ef749f-9956-4a2c-9af1-855ef5ab4afa)

Click on **Edit** button. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/ac330bf2-3f45-4ba9-b0f5-f4a920977e79)

Scroll down to the **Default Values** section and click on **Add**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/1d3b9212-7fe1-4307-a582-d400e66977c9)

Search for ‘Display Currency’ and click on the checkbox to select it.
Search for  ‘Purchasing Org.’  and select it similarly. 
Click on **Select**. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f88fa2e9-575a-4dfc-beb4-fa511855b59a)

Click on **Save and Publish**. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2c289155-8ff9-435e-8d5b-0f257420e9d8)


The status will be displayed as ‘**Publishing**’ in Custom Catalog Extensions application. Wait for the status to change to ‘**Published**’.

## Exercise 5.2	Change User Default values on FLP

Go back to Fiori Launchpad and switch to **Purchase Order Processing** page where your tiles are already present. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/e64a588c-cc8c-4737-8f38-947df25f43f1)

Click on the User settings menu on the top-right and click on **Settings**. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/438a4099-895b-45a8-acfc-4d0a7889e45b)

Select **Default Values**. 
Add ‘USD’ in the **Display Currency** field. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/df89f2d6-2565-4d31-af3c-fffd5eb98656)

Search for **Purchasing Org.** in the list and search for ‘_US Purchasing Org_’. Select the value. 
Click on **Save**.  
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/51c3493c-f878-427d-861b-ae3443ff8cf5)

This sets the default values as Display Currency = EUR and Purchasing Org. = 1710.

Click on the **Refresh** button at the bottom of the KPI tile.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/ea9290b7-d832-478e-be78-257a5f2688dd)


The data will get updated according to the Default values maintained in the Fiori Launchpad settings.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/81cc7e83-6826-40e8-a73b-13fa8dc13187)

Click on the tile to navigate inside the story. 
The Default values will automatically be applied as filter values for all the charts in the story. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/d7239685-10f3-4884-b849-7b543dd313e3)


## Summary

You've now learn on how to consider default values for analytical reports

Continue to - [Exercise 6 - Create and launch Generic Drilldown report for KPI ](../ex6/README.md)


