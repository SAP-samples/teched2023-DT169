# Exercise 3 - Embedded SAC Stories Runtime analysis

In this exercise we will explore how to use Intent Based navigation, filters, and variant management for SAC stories.

Click on the **DT169 – XXX Purchasing Spend Dashboard** tile created for your Story.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/86cdc235-f2ad-4898-9075-3743aa690aa6)

On launch of the application, the Overview page is displayed which comes from the pre-defined story which had been copied initially to create your custom Story.

Click on the dropdown and switch to the **‘Open Purchase Orders**’ page that was added to your story in the previous exercise.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/d523f76b-b1fc-428f-854a-673edafa180f)

Notice that the story page layout displayed during the runtime is the same as that which was set during the designing phase. This is the WYSIWYG (What you see is what you get) factor in creating analytical reports through Manage KPIs and Reports.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/d80b9690-e8d2-4385-9af3-d676799f4a81)

**Intent Based Navigation**

In this exercise we will see how you can seamlessly navigate from the SAC story to another S/4HANA application with the required context passed between the two. 
Scenario for analysis - We want to find the details of the Supplier with the highest number of open purchase order items.

In the ‘Open Purchase Orders’ page, scroll to the chart which displays the Number of Open PO items per Supplier.

Click on the **Ellipsis** button. 

Select **Rank -> Supplier -> Top 5**. This sorts the data in the chart to display the 5 suppliers with the highest open PO items.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/d099de57-677a-4120-869e-a1e4be83fad6)


Click on the bar showing the maximum number of Open PO Items.
Select the **Jump To** option. This displays the list of applications to which navigation is possible from this story.

Click on the icon beside Supplier to **Open Supplier in new tab**. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/02dca1bc-1cc0-4d55-a792-680930ba6ae7)

It will navigate to the Supplier application with the context of the selected Supplier. You can find all required details for the specified supplier in this page. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a5548408-117c-4f1f-b081-b9f6dabee3d3)

Note the name of this Supplier (i.e.RookEquip in this example) which we will be using for further analysis. 
Navigate back to the SAC story screen.


**Filters**

Now we want to analyze the data specific for this Supplier. We will now explore how to apply filters in Stories.  

Click on the **Filters** icon on top of the screen.

Click on the **Add filter icon** that appears on the top-left of the screen.

Set a filter for the C_PURCHASEORDERVALUEQUERY which is selected by default.

Search for Supplier in the list of fields and click on it. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/4f6ba866-24a0-4d1e-b7c4-8abe09bb6f6c)

In the list of values search for the Supplier name noted from the Supplier details page.

Select the supplier and Click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/97454ff0-d0bb-441e-a01e-2be8b175a0a5)

Although the filter was applied on the C_PURCHASEORDERVALUEQUERY model and the chart in ‘Open Purchase Orders’ page is created on YY1_PURCHASING_DT169_XXX model, the chart data will get updated with the selected Supplier filter. This is because while configuring the story in Exercise 2, we had linked the Supplier dimensions between C_PURCHASEORDERVALUEQUERY and YY1_PURCHASING_DT169_XXX. 

So setting a Supplier filter on either of the models will update the charts built on both models simultaneously. 
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/8ee9a2a7-183f-4bc1-ba1c-56c34a13ab0c)

Switch to the **Overview page** to view the charts configured for the C_PURCHASEORDERVALUEQUERY model.

Scroll to the “**by Supplier**” chart to view the updated data filtered on selected Supplier.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/cc3f4234-5902-4583-81bc-75214705449a)


**Variant Management**

Variants store the application settings, such as the filters, as quick-access views. 
Now we will create a new filter for Purchasing Organization and save it as a default variant. When you access your story from the Fiori Launchpad tile the next time, it will directly launch the application with your stored filters.

Switch to the ‘**Open Purchase Orders**’ page.

In the filters section, **remove** the Supplier filter.

Switch the **Data source** selection to **YY1_PURCHASING_DT169_XXX**. 

Select ‘**Purch. Org. Name**’.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/f7cef207-7ead-4d3d-9afe-ee29ba136510)

Set the filter value for ‘**DE Purchasing Org**’ and click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a4b08166-001a-48f0-aa85-3a55050178bb)

The data will get updated for all the widgets in the Open Purchase Order page. Observe that the colour of the **Number of Open PO items** will change according to the thresholds that were set for the Numerical point widget.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/cb1221a2-3758-44d3-9077-9a5333d0c53e)


To save this filter state as a variant, select the drop-down menu available next to the text Standard.

Click on **Save as** button. 

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/b1126e41-3efc-4d7b-8716-64e9844af159)


Add a name for the view such as ‘Open PO Items for a specific Purch. Org.’ and click on **Save**.
![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/dc58e1af-6cdd-44e8-adcd-20bf89e0342a)

The new variant is now available. You can switch between the Standard and your created variants from the **Select View** dropdown button.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/1cf9b062-231d-43fb-af38-8dd751aa4666)

To set your new view as the Default variant, click on **Manage**.

![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/a7e67b0e-3de3-4a73-becf-612832eec1e8)


On this screen, you can set or remove the view as a favorite, remove variants, or set the variant as the default. 

Change the **Default** selection to the ‘Open PO Items..’ view and click on **Save**.


![image](https://github.com/SAP-samples/teched2023-DT169/assets/145970887/01054228-6805-4745-8418-6d5770af9a94)


Go back to Fiori Launchpad Home page and relaunch your application from the **DT169-XXX Purchasing Spend Dashboard** tile.

The SAC story will now be launched with the settings of the Open PO Items for a specific Purch. Org. variant. That is, the filter for Purchasing Organization will already be applied on the story during launch.  



## Summary

You've now analyzed different features of a custom embedded analytical story. 

Continue to - [Exercise 4 - Create Custom KPI Tile for story ](../ex4/README.md)
