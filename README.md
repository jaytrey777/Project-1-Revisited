# Project-1-Revisited

<p align = "center"> 
Feature Importance
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Dec_Tree_5_Most_Important_Features.png">
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
