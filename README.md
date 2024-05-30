# Sales-Dashboard-in-Power-BI
Sales Dashboard in Power BI - Analyze and present comprehensive insights into sales, profits, orders, profit margins &amp; various comparisons. Power Query, Analysis, Creating New Measures
DAX Calculations
Measures Total Sales
Sales = SUM(Sales_Data[Sales])

Measures Previous Year Toal Sales
Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))

Diffrence Between Current Year Sales & Previous Year Sales
Sales vs PY = [Sales] - [Sales PY]

Percentage Increase or Decrease in sales year on year (YOY%)
Sales vs py % = DIVIDE([Sales vs PY],[Sales],0)

 Products Sold = SUM(Sales_Data[Order Quantity])
Profit = SUM(Sales_Data[Profit]) 
Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))
Profit Vs LY = [Profit]- [Profit LY]
Profit vs LY % = [Profit Vs LY]/[Profit]
Profit Margin = DIVIDE([Profit],[Sales],0)
Total Cost = SUM(Sales_Data[Total Cost]) 
