Power BI
What is Power Bi?
Power Bi is a business intelligence tool which will help you to analyze your data to clean your data and convert that data into visual format where you can create different reports and different dashboards so this is a business intelligence.
Power Bi Is a Data Visualization and Business Intelligence tool that covert 
Power bi is a collection of components 
•	Power Query
•	Power Pivot
•	Power Bi
•	Power Bi Service

Power query is a etl tool which will extract transform and load the data or in another language if i say it is for cleaning the data when you have blank records null values empty records or different unclean data it will clean data for visualization.
Power Pivot is used for data modeling when you have multiple data sources if you want to connect them create relationship between them you can use power pivot.
Power View visualization that is power view power view can help you to create 250 plus charts that can be bar chart or donor chart or scienti chart this different type of charts will be useful for presentation for reports and dashboards after creating all this after cleaning visualization.
Power Bi service if you want to share this report with different people sitting across the world you can use power bs service so power bs service will help you your users to communicate between each other via that reports so it's a package of four components power query power pivot power view and power bi service now
Power Bi only a visualization tool?  
No power bi is not only a visualization tool but it can do much more beyond visualization and what is that you can also filter data from the visual that is keep only and exclude along with that you can export data from the visual itself so suppose you have created some chart you can filter data and convert into a csv format and that you can export into csv.

DAX  (Data Analysis Expression)
Dax is a library of function and operators that can be combined build formulas and Expression used by Microsoft Power Bi Tools.
Dax is also knows as function language, where the full code is kept inside a function.
Where DAX can be used,
•	Power Bi
•	Power Pivot for Excel
•	SSAS Tabular Model
•	 Azure Analysis Service
What is the purpose Of DAX
By using Data Analysis Expressions(DAX)
You can add three types of calculations to your data model
•	Calculated Columns
•	Measures
•	Calculated Tables


  
Calculated Column	Measure
Expands Table by creating new column	Summarizes data into a single value
Stored along with table. Consumes Memory	Calculated at runtime / Stored temporarily
Less Analytical Capability	Rich Analytical capabilities

Calculated Columns
 
New Measures
 
Calculated Tables

 
Calculated Table :
•	Date tables
•	Role-playing Dimension
•	What-if analysis
Syntax:
•	DAX formulas are very similar to the Excel formulas, but there are some key differences
•	In Microsoft Excel you can reference individual cells or arrays, but in DAX you can reference only complete tables or columns of data
•	DAX formulas do not support exactly the same data type as Microsoft Excel.

Total Sales = Sum(‘F act Sales’[Sales Amount])
 
This formula includes the following syntax elements:
A. The measure name, Total Sales.
B. The equals sign operator (=), which indicates the beginning of the formula. When calculated, it will return a result.
C. The DAX function SUM, which adds up all of the numbers in the Sales[SalesAmount] column. You’ll learn more about functions later.
D. Parenthesis (), which surround an expression that contains one or more arguments. Most functions require at least one argument. An argument passes a value to a function.
E. The referenced table, Sales.
F. The referenced column, [SalesAmount], in the Sales table. With this argument, the SUM function knows on which column to aggregate a SUM.
Operators:
 
Data Types:
 
Power BI DAX Basics: Types of Functions in DAX
Aggregate Functions
MIN
Fetches the minimum value in a given column.
Syntax 
MIN(<column>)
Example 
=MIN( [ SellerMargin] )
MINA
Fetches the minimum value along with Aggregate Functions Logical values and text representation of numbers if any
Syntax
MINA( <column> )
Example
=MINA( InternetSales[Freight] )
MINX
Fetches the minimum value after evaluation of each row expression in a given table.
Syntax
MINX  ( < table >, <expression> )
Example
 =MINX(  FILTER( InternetSales ) ,  [ SalesTerittoryKey ] = 2 ,  [Freight] )
Other functions
•	MAX
•	MAXA
•	MAXX
•	SUM
•	AVERAGE
•	SUMX
•	AVERAGEX
#2. Count Functions
DISTINCTCOUNT
Fetches the count of distinct numbers avoiding any replication.
Syntax
DISTINCTCOUNT( <column> )
 Example
=DISTINCTCOUNT( ProductsList[ProductID] )   
COUNT
Fetches the total count of items even if repetitions are present.
Syntax
 COUNT( <column> )
Example
=COUNT ( [ShipDate]  )   
COUNTA
Fetches the count of items in a non-empty column.
Syntax
COUNTA( <column> )
Example
= COUNTA( ‘ProductSeller’[Phone] )   
COUNTROWS
Fetches the number of rows in a given table.
Syntax
COUNTROWS( < table > )
Example
=COUNTROWS( ‘Enquiries’ )

#3. Date-Time Functions  
DATE
Fetches the desired date in Date-time format.
Syntax
DATE ( <year>, <month>, <day> )
Example  
=DATE ( 2020,02,27 )  
HOUR
Fetches hours in the AM PM format.
Syntax
HOUR ( <datetime> )
Example
=HOUR( ‘Orders’ [TransactionTime] )
TODAY
Fetches the current date.
Syntax
TODAY()
Example
 = YEAR ( TODAY())-2012
Other functions
•	NOW
•	EOMONTH

#4. Math Functions
ABS
Fetches the absolute value.
Syntax
ABS( <number> )
Example
=ABS( [LabelPrice] - [SellingPrice] )   
EXP
Fetches the exponent's value.
Syntax
EXP( <number> )
Example
=EXP( [Power] )  
FACT
Fetches the factorial of a given number.
Syntax
FACT( <number> )
Example
=FACT( [Values] )
Other functions
•	LN
•	LOG
•	PI
•	POWER
•	QUOTIENT
•	SIGN
•	SQRT

#5. Logical Functions   
AND
Performs the logical conjunction on two specified expressions.
Syntax
AND( <logical1> , <logical2 > )
Example
 =IF( AND(1<2 , 2<3) , “All true” , “One or false” ) 
OR
Performs the logical disjunction on two specified expressions.
Syntax
OR( <logical1 > , <logical2 > )
Example
=( IF(OR(1<2 , 2<3) , “All true” , “One or more false” )   
NOT
Performs logical negation on the given expression.
Syntax
NOT( <logical > )
Example
 =NOT( [ProductPrices] )
Other functions
•	IF
•	IFERROR

#6. Information Functions
ISBLANK
Declares if the value is blank or not as true or false.
Syntax
ISBLANK( <value> )
Example
=IF( ISBLANK(‘CalculatedMeasures’[PreviousYearTotalSales]) ,BLANK() , (CalculatedMeasures’[PreviousYearTotalSales]/ ‘CalculatedMeasures’[PreviousyearTotalSales])
ISNUMBER
Declares if the value is a number or not.
Syntax
ISNUMBER(<value>)
Example
=IF( ISNUMBER(2), “Is number”, “Is Not number” )   
ISNONTEXT
Declare if the value is non-text.
Syntax
 ISNONTEXT( <value> )
Example
=IF( ISNONTEXT(“ ”), “Is Non-Text”, “Is Text” )
Other functions
•	ISERROR
•	ISTEXT
#7. Text Functions
CONCATENATE
Performs joining of two strings.
Syntax
CONCATENATE( <text1> , <text2> )
Example
= CONCATENATE( “Hello” , “Learner” )     
FIXED
Performs rounding off of number to a given decimal.
Syntax
FIXED( <number> , <decimals> , <no_commas> )
Example
=FIXED( [LabelPrice], 3,1 )   
REPLACE
Replaces part of a string with specified characters.
Syntax
REPLACE( <old_text> , <start_num>, <num_chars> , <new_text> )
Example
=REPLACE( ‘New Services’[Service ID],2,3,”AB” )
Other functions:
•	SEARCH
•	CONCATENATEX
•	SEARCH
•	UPPER


