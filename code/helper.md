# Notes

<!-- 23 April -->

Show connection between SQL server and Power BI
Show SQL code in Power BI

```sql
SELECT [ProductName]
      ,[Price]
      ,[PurchaseDate]
FROM [TEST].[dbo].[ShoppingBasket]
```

Show CTE in Power BI

Download the .txt file an import into PBI

## Chat GPT

I have a table called Shopping with the following columns: Price, ProductName, PurchaseDate.
Please write a DAX script to create a table that represents a group by ProductName and sum over Price

```dax
ProductSummary = SUMMARIZE(Shopping, Shopping[ProductName], "Total Price", SUM(Shopping[Price]))
```

```dax
EVALUATE
  --  TOPN(100, 'financials_new')
  SUMMARIZE(Shopping, Shopping[ProductName], "Total Price", SUM(Shopping[Price]))
```
Modelling > New Table > ProdTbl = SUMMARIZE(Shopping, Shopping[ProductName], "Total Price", SUM(Shopping[Price]))


I have a table called financials_new and would like to create a table containing the distinct Country values from financials_new table. Please write a DAX script to create this table.

```dax
DistinctCountries = DISTINCT(financials_new[Country])
```
Modelling > New Table > DistinctCountries = DISTINCT(financials_new[Country])



Modelling > New Table > ProdTbl = SUMMARIZE(Shopping, Shopping[ProductName], "Total Price", SUM(Shopping[Price]))

Home  > Enter Data

Copy and paste teh below into `Enter Data` and then click `Load`

```csv   ShoppingCountry

Product	Country
Product A	Mexico
Product B	France
Product C	Germany
Product D	Canada
Product E	Canada
Product F	United States of America
Product G	United States of America
Product H	United States of America
```

Notice the Data Model info and primary keys
If you delete the relationship and then create a table and try and show product with country it wont work
If you recreate teh key and then create the table with product and country - then it works

Check rendering in PBI service portal  

<!-- 24 April -->

1. Matrix - hierarchy
2. Scaling  (https://github.com/gpsuser/samples/blob/master/random%20notes.md)
3. Python
4. SQL   GPS-DELL-XPS\MYTEST, TEST, dbo, ShoppingBasket,   SELECT * FROM ShoppingBasket
   Home > Transform Data > Data Source Settings



<!-- Summary -->

Chart Types
Tables and Matrix
Filtering
Power BI ServicePortal
DataModlleing
Formatting
DAX
Python
SQL
