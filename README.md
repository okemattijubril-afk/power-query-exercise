# power-query-exercise
Power Query data cleaning exercise for the BoyCode Africa data analysis class

## Exercise 1: Get Data into power query

Tool: Power BI Desktop (Power query)

Source: 1__Get_Data_Into_Power_Query.xlsx

1. Imported the corporate, Home office and Consumer sheets.
2. Appended them into one table called All Sales (18 rows).
3. Replaced blank ship Mode values with unknown.
4. Replaced the #REF! error in Quantity with 0.
5. Set data types and loaded only All Sales.

 Result: 18 rows, 7 columns.

## Exercise 2: Badly Structured Sales Data

Tool: Power BI Desktop (Power query)

Source: 1_Badly-Structured-Sales-Data.xlsx

1. Loaded the Dirty 1 sheet and transposed it.
2. Filled down the Ship Mode row, merged it with Segment, then transposed back.
3. Promoted the first row to headers and removed the extra row.
4. unpivoted the other columns, then split the attribute column by comma into Ship Mode and Segment.
5. Renamed the columns and set the data types (Order Date to Date, Sales to decimal).
6. Loaded the cleaned table.
