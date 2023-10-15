# Exercise 1 - Create Custom Analytical Queries

In this exercise, we will create a Custom Analytical query based on a cube view. We will learn how to design the metadata of a custom query, add new calculated fields as measures and preview the data in Multi-dimensional reports before publishing the query.

## Exercise 1.1	Launch View Browser to get the details of all the views available in the system

Click on the Analytics Page. 
Scroll to the Query Design group and launch the View Browser application.
View Browser application is used to get a list of all CDS views available in the current system along with the details, such as category, view types, fields, annotations, supported capabilities, modeling pattern of the CDS views. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/8c0b5caf-011b-4ec3-9d99-582033ab54ad)

Search for C_PURCHASINGGROUPANALYSIS in the search bar. 
Click on the checkbox to select the C_PURCHASINGGROUPANALYSIS view.
Click on the Ellipses icon on the right to expand the available options for the view.
Choose Create Analytical Query.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/dad688e6-5996-4f37-b101-680d04165ce1)

## Exercise 1.2 Designing the custom analytical query

You will be navigated to the create page of Custom Analytical Queries application.
Enter 'PURCHASING_DT169_XXX' as the query name. (_XXX Should be replaced with your group number for eg for place nmber 25 it is 025_)
'YY1_' prefix will be added to the name of the query automatically. Click on OK.
Provide a Label for the query, for example 'Purchasing Analysis Open Purchase Orders'.

Switch to the Field selection tab to design the metadata of your query.
    Select the following fields for your custom query: 
        - Invoice Amount
        - PO Net Amount
        - Number of Purchase Order Items
        - Supplier
        - Name of Supplier
        - Calendar Month
        - Purch. Organization
        - Purch. Org. Name

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/16636397-279a-4be1-8a04-c3aa3cd623f3)

Switch to Display tab to view the selected fields.

For the dimension fields (Supplier, Name of Supplier, Calendar Month, Purch. Organization, Purch. Org. Name), click on the Axis property on the right and change to 'Row'. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/045667c9-70ae-42b2-bcf5-114e2bce3683)

Search for the measure 'NUMBEROFPURCHASEORDERITEMS', and under the Properties section, enter the 'Override Label' as 'Number of PO Items'.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/98c03490-3945-4041-8b65-482621635c40)

## Exercise 1.3 Add a Calculated measure to the custom query

In the same **Display** section, click on Add button and select **Add Calculated Measure**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/0bc961ae-2d63-4299-b070-cdd9186d4873)

Provide a Label 'Number of Open PO Items' and click on OK.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/84b75412-55c4-4fda-87c3-5e5585292228)

It is possible to configure a dynamic label for the calculated measure which would display the text according to a specified template. For this exercise, we will configure the Dynamic Label to show ’Number of Open PO Items from 01/01/2023 to 03/11/2023’ for this new field.
To implement this- 
Go to the details section on the right where the details of the newly added field are displayed.
Under Properties section, select **Dynamic Label** and click on **Create Dynamic Label**.
Type in the static text 'Number of Open PO Item from ’ in the text area.
Click on **User Input Filter** and select ‘**P_StartDate**’ which will be the dynamic input for this text. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/e4a951f1-a706-4d85-848e-95562c3b3d0d)

Add ‘to’ after this P_StartDate in the text area.
Click on **User Input Filter** again and select '**P_EndDate**'.
The final expression will look like **Number of Open PO Items from "P_StartDate" to "P_EndDate"**

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/72efed8a-b72c-4e7b-99bf-d1428dd1c567)

Defining the formula for the calculated field -     
Scroll down to '**Expression**' and click on Edit for the Formula section.
Click on '**Measures**' button and select 'Number of PO Items'. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/1764911f-745e-4dd4-9630-4021cce9bd0c)

Click on the minus ('-') button.
Click on '**Measures**' button again and select 'Number of Deliveries'. 
The final expression should look like "Number of PO Items"-"Number of Deliveries". Click on OK.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/55eef340-2f93-4a13-989c-0442fdb23ff9)

## Exercise 1.4 Add default values for input filters

Switch to Filters tab.
Select the field 'Display Currency'. 
The details of the field are displayed on the right. 
Under **User Input Values**, enter 'EUR' as the Default value for Display Currency.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f057ece8-f2ac-48df-8e3f-dafc3bdea2f2)

In the list of fields, search for 'Relative Date Function' and select the field.
Under **User Input Values** and maintain **Default Value** as "relative:YEARTODATE".

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a1c1e110-2ac0-4b2b-858f-8e7accae812b)

Next, search for 'Validity Start’ and select the field.
Go to 'Fixed Values' and click on the value help icon.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/bc801437-0ffd-44a2-b9c0-da449455d5c1)

Select the '**User Input Values**' tab and select the 'P_Datefunction'. Click on OK. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/cd66767b-4c6c-48c6-9cf1-182741555bb8)
The dropdown beside the Include field should display 'Start'.

Search for 'Validity End' and select the field.
Go to 'Fixed Values' and click on the value help icon.
Select the 'User Input Values' tab and select the 'P_Datefunction'. Click on OK.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/7989ea6e-040f-4d21-b1b7-b27473f112d0)
Click on the dropdown beside the Include field and change the value to 'End'. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/032973dd-8a0d-4759-92d6-bbb693980bba)

## Exercise 1.5 Publish the Query and Open it for analysis in preview mode

Click on 'Save Draft'. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/2c710ba4-006f-431e-bfe0-2d3972969370)

Once the draft is saved, click on 'Preview'. 
The query will be displayed in the preview mode of Multi-dimensional Web Dynpro Report.     
Multi-dimensional reports allow insight-driven, explorative, and flexible analyses of large amounts of data. They usually focus on a specific topic, for example, sales orders or cost centers. You can switch the display from table (grid) to graphical display, and both displays can be further configured via the settings menu.

Click on **Go** to view the data for the configured filters.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/ac57d6de-2e00-4356-a362-c78c30d1e0e0)

Navigate back to the Custom Analytical Queries and click on Publish.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/82478948-ba1b-415e-a59b-d1ba828b6f31)
The query is now ready for consumption in analytical reports.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f3dfddd1-457b-44c9-ac2e-3031839bc0a1)




## Summary

You've now created Custom analytical Query. Let us now consume this query in Embedded SAC stories

Continue to - [Exercise 2 - Design and launch custom SAC Stories ](../ex2/README.md)

