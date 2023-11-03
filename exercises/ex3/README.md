# Exercise 3 - Embedded SAC Stories Runtime analysis

In this exercise we will explore how to use Intent Based navigation, filters, and variant management for SAC stories.

Click on the **DT169 – XXX Purchasing Spend Dashboard** tile created for your Story.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/1.png)

On launch of the application, the Overview page is displayed which comes from the pre-defined story which had been copied initially to create your custom Story.

Click on the dropdown and switch to the **‘Open Purchase Orders**’ page that was added to your story in the previous exercise.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/2.png)

Notice that the story page layout displayed during the runtime is the same as that which was set during the designing phase. This is the WYSIWYG (What you see is what you get) factor in creating analytical reports through Manage KPIs and Reports.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/3.png)

**Intent Based Navigation**

In this exercise we will see how you can seamlessly navigate from the SAC story to another S/4HANA application with the required context passed between the two. 
Scenario for analysis - We want to find the details of the Supplier with the highest number of open purchase order items.

In the **‘Open Purchase Orders’** page, scroll to the chart which displays the Number of Open PO items per Supplier and click on it.

Click on the **Ellipsis** button. 

Select **Rank -> Supplier -> Top 5**. This sorts the data in the chart to display the 5 suppliers with the highest open PO items.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/4.png)


Click on the bar showing the maximum number of Open PO Items.

Select the **Jump To** option. This displays the list of applications to which navigation is possible from this story.

Click on the icon beside Supplier to **Open Supplier in new tab**. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/5.png)

It will navigate to the Supplier application with the context of the selected Supplier. You can find all required details for the specified supplier in this page. 


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/6.png)

Note the name of this Supplier (i.e.RookEquip in this example) which we will be using for further analysis.

Navigate back to the SAC story screen.


**Filters**

Now we want to analyze the data specific for this Supplier. We will now explore how to apply filters in Stories.  

Click on the **Filters** icon on top of the screen.

Click on the **Add filter icon** that appears on the top-left of the screen.

Set a filter for the C_PURCHASEORDERVALUEQUERY which is selected by default.

Search for Supplier in the list of fields and click on it. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/7.png)

In the list of values search for the Supplier name noted from the Supplier details page.

Select the supplier and Click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/8.png)

Although the filter was applied on the C_PURCHASEORDERVALUEQUERY model and the chart in ‘Open Purchase Orders’ page is created on YY1_PURCHASING_DT169_XXX model, the chart data will get updated with the selected Supplier filter. This is because while configuring the story in Exercise 2, we had linked the Supplier dimensions between C_PURCHASEORDERVALUEQUERY and YY1_PURCHASING_DT169_XXX. 

Therefore, setting a Supplier filter on either of the models will update the charts built on both models simultaneously. 
![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/9.png)

Switch to the **Overview page** to view the charts configured for the C_PURCHASEORDERVALUEQUERY model.

Scroll to the “**by Supplier**” chart to view the updated data filtered on selected Supplier.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/10.png)


**Variant Management**

Variants store the application settings, such as the filters, as quick-access views. 
Now we will create a new filter for Purchasing Organization and save it as a default variant. When you access your story from the Fiori Launchpad tile the next time, it will directly launch the application with your stored filters.

Switch to the ‘**Open Purchase Orders**’ page.

In the filters section, **remove** the Supplier filter.

Switch the **Data source** selection to **YY1_PURCHASING_DT169_XXX**. 

Select ‘**Purch. Org. Name**’.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/11.png)

Set the filter value for ‘**DE Purchasing Org**’ and click on **OK**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/12.png)

The data will get updated for all the widgets in the Open Purchase Order page. Observe that the colour of the **Number of Open PO items** will change according to the thresholds that were set for the Numerical point widget.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/13.png)


To save this filter state as a variant, select the drop-down menu available next to the text Standard.

Click on **Save as** button. 

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/14.png)


Add a name for the view such as ‘Open PO Items for a specific Purch. Org.’ and click on **Save**.
![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/15.png)

The new variant is now available. You can switch between the Standard and your created variants from the **Select View** dropdown button.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/16.png)

To set your new view as the Default variant, click on **Manage**.

![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/17.png)


On this screen, you can set or remove the view as a favorite, remove variants, or set the variant as the default. 

Change the **Default** selection to the ‘Open PO Items..’ view and click on **Save**.


![image](https://github.com/SAP-samples/teched2023-DT169/blob/main/exercises/ex3/images/18.png)


Go back to Fiori Launchpad Home page and relaunch your application from the **DT169-XXX Purchasing Spend Dashboard** tile.

The SAC story will now be launched with the settings of the Open PO Items for a specific Purch. Org. variant. That is, the filter for Purchasing Organization will already be applied on the story during launch.  



## Summary

You have now analyzed different features of a custom embedded analytical story. 

Continue to - [Exercise 4 - Create Custom KPI Tile for story ](../ex4/README.md)
