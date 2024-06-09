# Vrinda_Store_Analysis_usingPowerBI
Analysis of Vrinda Store Data to improve more Sales in 2023


# Vrinda Store Analysis


## Objective:

Vrinda Store wants to create an Annual Sales Report for 2022. So, that Vrinda can understand their customers and grow sales in 2023

## Sample Questions:

1. Compare the sales and order using single chart
2. Which month got the highest sales and orders?
3. Who purchased more – Men or Women?
4. What are the different orders status in 2022?
5. List the top 10 states contributing to the sales
6. Relation between age and gender based on number of orders
7. Which channel is contributing to maximum sales?
8. Highest Selling category?



### Steps followed 

- Step 1 : Data cleaning in excel:
  
		In the gender column, all the 'M' was given as Male and 'F' was Female
		The Qty column, all the One was replaced with 1 and all the Two was replaced by 2

- Step 2 : Data Processing/DAX using Transform Data in PowerBI:
  
		-Extraction of Month from each cell using Transform Data->Add column->Date->Month->Name of the Month
		-Created Age Group column such that the relation between age and gender can be found out
			= Table.AddColumn(#"Inserted Month Name", "Custom", each if [Age] > 50 then "Senior" else if [Age] > 20 then "Adult" else if [Age] > 0 then "Teens" else null)

  
Now we will analyze the data-


- Step 3 : KPI on the following-
            Count(Distinct) of OrderID
            Average of Age
            Total Count of CustID
            Count(Distinct) of Channel

- Step 4 : 
	Visualization - 1: Amount by Month Name: Which month gives maximum sales?

- Step 5 : 
	Visualization - 2: Amount by Gender: To know who does more shopping?

- Step 6 : 
	Visualization - 3: Amount by Category: Whether it is Indian Or Western Attire

- Step 7 : 
	Visualization - 4: Amount by Channel:To know which channel contribute on max sales?

- Step 8 : 
	Visualization - 5: Amount by Ship-State: Which state has contributed mpore on Sales?

- Step 9 : 
	Visualization - 6: Amount by Amount by Age Group and Gender: Which women age group does more shopping?

- Step 10 : 
	Visualization - 7: Amount by Status: To compare whether the delivered status



## Insights/Conclusion:

1. Women are more likely to buy products than men (~64%)
2. Maximum Adult women within the age group (20-60 years) buyers contribute to the sales
3. Max sales happens in March, followed by August
4. Bengaluru, Hyderabad, and Delhi are the top three cities with max buyers
5. Amazon, Myntra, and Flipkart are the channels with the maximum number of buyers
6. Major Purchases are happening on Sets



