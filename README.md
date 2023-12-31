# Project-1-Revisited

<p align = "center"> 
Impactful Features
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Lin_Reg_3_Largest_Coefficients.png">
</p>
<p>
If the observation belongs to `Outlet_Type`, then the target sales will increase by 896.195 rupees. There are 4 types of stores that were analyzed: Grocery Store, Supermarket Type 1, Supermarket Type 2, Supermarket Type 3. The type of store you have and its size has a direct impact on the sales.

If the observation belongs to `Item Visibility`, then the target sales will decrease by 423.390 rupees. Certain items are easily visible in multiple locations in the store while others are very hard to find. If items are not visible, they will be hard to find and this will hinder sales.

If the observation belongs to `Outlet_Identifier_OUT019`, then the target sales will decrease by 467.652 rupees. This store is of a specific type and has several factors that hinder sales.
</p>


<p align = "center"> 
Feature Importance
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Dec_Tree_5_Most_Important_Features.png">
</p>
<p>
The most important feature for the Decision Tree Model is `Item_MRP`, with a feature importance of about 0.45. This means that the model relied on this feature to make its decisions to split nodes about 45% of the time. This makes sense because the higher the retail price, the more sales it will have if it is a high sales item.  

The other top features were `Outlet_Type`, `Item_Visibility`, `Item_Weight`, and `Outlet_Establishment_Year_1985`. The model made decisions based on these features 25%, 10%, 5% and 1% respectively. These features account for the majority of the decisions made by the model at any given time. `Outlet_Type` and `Item_Visibility` were also important in the Linear Regression model.

If the observation belongs to `Outlet_Type`, there are 4 types of stores that were analyzed: Grocery Store, Supermarket Type 1, Supermarket Type 2, Supermarket Type 3. The type of store you have and its size has a direct impact on the sales.

If the observation belongs to Item `Visibility`, certain items are easily visible in multiple locations in the store while others are very hard to find. If items are not visible, they will be hard to find and this will hinder sales.
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
</p>


<p align = "center"> 
Lime Tabular Explanation(Minimum Sales)
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/LIME_Min_Sales.png">
</p>

As we can see above, this was the maximum sales value from the target.

There were several features that led to this minimum value:
- Item_MRP = 32.89
  - This item has the largest negative value and affects the predicted value the most. It decreased the sales by 632.56 rupees.
- Outlet_Type = 0
  - The outlet type also played a big factor in the sales. This type of store decreased the sales by 944.46
- Outlet_Establishment_Year_1985 = 1
  - Although the year a store cannot be too much of a factor because all the stores can't be created the same year, this year was a good year for the store. Possibly because the store filled a need in the area it was placed in. 
- Item_Type_Seafood = 0
  - Seafood must not be popular in the area of these stores so it has an impact on the outcome of the model.
- Item_Type_Soft Drinks = 0
  - Soft Drinks must not be popular in the area of these stores so it has an impact on the outcome of the model. 
- Outlet_Identifier_OUT027 = 0
  - Store 027 is one of the lower selling stores, so the fact that is is not apart of the lower selling group is helping the overall outcome of the model. 
- Item_Type_Others = 0
  - Other items must not be popular in the area of these stores so it has an impact on the outcome of the model.

The most impactful features that are working against the maximum sales are:

- Item_Type_Breakfast = 0
  - Breakfast must not be popular in the area of these stores so it has an impact on the outcome of the model.
- Outlet_Identifier_OUT019 = 0
  - Store 019 is one of the lower selling stores, so the fact that is is not apart of the lower selling group is helping the overall outcome of the model.
- Item_Type_Snack Food = 0
  - Snack Foods must not be popular in the area of these stores so it has an impact on the outcome of the model.
</p>


<p align = "center"> 
Force Plot(Minimum Sales)
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Force_Plot_Min_Sales.png">
</p>

In the visual above, we can see:

* A number line at the top of the visual (with the base value labeled).
  * Here the base value is 2,210.
* A bold value at the intersection of the red and blue is the final SHAP value for the observation.
  * Here the SHAP value is 75.90
* The red and blue segments with arrows towards the middle are "pushing" against each other.
  * Visually, the contributions of the blue features are greater than the red which means a greater "push" towards lower revenue.
  * The wider the segment is for the feature, the greater its contribution to the prediction is.
* As you can see, Item_MRP is the most important feature for this output. Further, the actual value for each feature is listed. For the sales, this Item_MRP = 32.89 Rupees.
</p>


<p align = "center"> 
Lime Tabular Explanation(Maximum Sales)
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/LIME_Max_Sales.png">
</p>

As we can see above, this was the maximum sales value from the target.


There were several features that led to this maximum value:
- Item_MRP = 235
  - This item has the largest positive value and affects the predicted value the most. It increased the sales by 1542.98 rupees.
- Outlet_Type = 3
  - The outlet type played a big factor in the sales. This type of store increased the sales by 837.67
- Item_Type_Bread = 0
  - Bread must not be popular in the area of these stores so it has an impact on the outcome of the model.
- Outlet_Establishment_Year_1985 = 1
  - Although the year a store cannot be too much of a factor because all the stores can't be created the same year, this year was a good year for the store. Possibly because the store filled a need in the area it was placed in. 
- Item_Type_Meat = 0
  - Meat must not be popular in the area of these stores so it has an impact on the outcome of the model.

The most impactful features that are working against the maximum sales are:
- Item_Type_Seafood = 0
  - Seafood must not be popular in the area of these stores so it has an impact on the outcome of the model.
- Outlet_Identifier_OUT010 = 0
  - Store 010 is one of the lower selling stores, so the fact that is is not apart of the lower selling group is helping the overall outcome of the model.
- Item_Type_Fruits and Vegetables = 0
  - Fruits and Vegetables must not be popular in the area of these stores so it has an impact on the outcome of the model.
- Outlet_Identifier_OUT019 = 0
  - Store 019 is one of the lower selling stores, so the fact that is is not apart of the lower selling group is helping the overall outcome of the model.
- Item_Type_Snack Food = 0
  - Snack Foods must not be popular in the area of these stores so it has an impact on the outcome of the model.
</p>


<p align = "center"> 
Force Plot(Maximum Sales)
</p>

<p align = "center"> 
<img src = "https://github.com/jaytrey777/Project-1-Revisited/blob/main/Images/Force_Plot_Max_Sales.png">
</p>

In the visual above, we can see:

- A number line at the top of the visual (with the base value labeled).
  - Here the base value is 2,210.
- A bold value at the intersection of the red and blue is the final SHAP value for the observation.
  - Here the SHAP value is 2,554.01
- The red and blue segments with arrows towards the middle are "pushing" against each other.
  - Visually, the contributions of the red features are greater than the blue which means a greater "push" towards higher revenue.
  - The wider the segment is for the feature, the greater its contribution to the prediction is.
- As you can see, `Item_MRP` is the most important feature for this output. Further, the actual value for each feature is listed. For the sales, this `Item_MRP` = 235 Rupees.
</p>
