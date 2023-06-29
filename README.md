# Project-1-Revisited

<p align = "center"> 
Impactful Features
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Lin_Reg_3_Largest_Coefficients.png">
</p>
<p>
If the observation belongs to Outlet_Type, then the target sales will increase by 896.195 rupees. The type of store you have can increase your sales.

If the observation belongs to Item Visibility, then the target sales will decrease by 423.390 rupees. If items are not visible, it will hinder sales.

If the observation belongs to Outlet_Identifier_OUT019, then the target sales will decrease by 467.652 rupees. This store can hinder sales.
</p>


<p align = "center"> 
Feature Importance
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Dec_Tree_5_Most_Important_Features.png">
</p>
<p>
The most important feature for the Decision Tree Model is Item_MRP, with a feature importance of about 0.45. This means that the model relied on this feature to make its decisions to split nodes about 45% of the time.

The other top features were Outlet_Type, Item_Visibility, Item_Weight, and Outlet_Establishment_Year_1985. The model made decisions based on these features 25%, 10%, 5% and 1% respectively. These features account for the majority of the decisions made by the model at any given time. Outlet_Type and Item_Visibility were also important in the Linear Regression model.
</p>


<p align = "center"> 
SHAP Bar Plot
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Dec_Tree_SHAP_Bar_Plot.png">
</p>

The Feature Importance and the SHAP output have the same top 5 features in the same order of importance. That means that regardless of how those items are analyzed, they are the most impactful features the the model.


<p align = "center"> 
SHAP Dot Plot
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Dec_Tree_SHAP_Dot_Plot.png">
</p>

The top 3 items on the dot plot are Item_MRP, Outlet_Type and Item_Visibility.
<p>
Item_MRP - The higher the MRP the more money is made. These items will have a linear relationship.
</p>
<p>
Outlet_Type - The type of store determines has an direct impact on the profit. This also has a linear relationship with the target.
</p>
<p>
Item_Visibility - Based on the plot, the visibility of an item has little impact on the profit of the item. There are items that have high profits, but low visibility and vice versa.
