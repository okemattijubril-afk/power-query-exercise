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
4. Promoted the first row to headers and removed the extra row.
5. unpivoted the other columns, then split the attribute column by comma into Ship Mode and Segment.
6. Renamed the columns and set the data types (Order Date to Date, Sales to decimal).
7. Loaded the cleaned table.
Result: 822 rows, 4 column (Ship Mode, segment, Order Date, sales).

### Exercise 3: Jumbled Customer Details Data Extraction
* **File:** `3.Jumbled-up-Customers-Details.xlsx` (Query: `Dim_Customer_Details`)
* **Objective:** Extract unstructured, single-string text records into normalized dimension columns.
* **Key Transformations:**
  * Header demotion (`Use Headers as First Row`) to preserve Row 1 data.
  * Delimiter-based text extraction (`Text Between Delimiters` & `Text After Delimiter`) for `Name`, `Address`, `Age`, and `Gender`.
  * Data type coercion (`Age` to Whole Number) and original column cleanup.
 
    ## Exercise 4: Superstore_StarSchema_Model
     # Power BI Data Modeling & Transformation Portfolio

## Project Overview
This repository showcases end-to-end data preparation, cleaning, and Star Schema modeling using **Power BI Desktop** and **Power Query**. The exercises demonstrate best practices in ETL (Extract, Transform, Load), data normalization, and relationship management for analytics readiness.

### 1. `Superstore_StarSchema_Model.pbix`
* **Description:** Complete Power BI data model built from transactional retail data.
* **Architecture:** Star Schema design featuring a central Fact table surrounded by single-direction 1-to-many ($1:*$) dimension relationships.
* **Tables:**
  * **`Orders` (Fact):** Contains transactional metrics (`Sales`, `Quantity`, `Discount`, `Profit`) and key references.
  * **`Dim_Customer`:** Cleaned dimension containing unique customer profiles (`Customer ID`, `Customer Name`, `Segment`).
  * **`Dim_Product`:** Product details categorized by `Category` and `Sub-Category`.
  * **`Dim_Location`:** Geographic dimension mapped by `Postal Code`, `City`, `State`, and `Region`.

### 2. `Clean_Customer_Details.xlsx`
* **Description:** Processed customer directory parsed from unformatted, single-string raw text (`Dirty 3`).
* **Transformations Applied:**
  * Header demotion and custom string parsing using text delimiters (`Name`, `Address`, `Age`, `Gender`).
  * Data type assignment and removal of original unstructured attributes.
  * Staged into the query model as **`Dim_Customer_Details`**.

### 3. `8. Add Columns.xlsx`
* **Description:** Exercise dataset practicing advanced Power Query column creation techniques.
* **Key Workflows:**
  * **General & Data Types:** Formatting, casing, and primitive conversions.
  * **Conditional Columns:** Rule-based categorization and logic branching.
  * **Custom Columns:** Advanced M-code calculations and custom field generation.

## 🛠️ Tools & Technologies Used
* **Power BI Desktop:** Model view configuration, relationship cardinality setup.
* **Power Query Editor:** M-code transformations, string extraction, table duplication, deduplication, and data type coercion.
