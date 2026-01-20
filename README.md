## DAX Depo – Power BI Project

### Project Overview

This project highlights the practical use of **DAX (Data Analysis Expressions)** in **Power BI** to perform key analytical calculations using **Sales** and **Returns** data. The work mainly focuses on **data modeling** and **backend measure development**, with insights displayed strictly through a **Matrix visual** (as per project rules).

---

### Objective

* Build **calculated columns** and **measures** using DAX
* Analyze **sales, cost, profit, quantity, and returns**
* Apply **time intelligence** calculations such as **YTD, YoY, and MoM**
* Organize all measures using a dedicated **Measure Table**
* Follow the guideline of using **only a Matrix visual** for reporting

---

### Dataset Used

#### Fact Tables

* **Sales_Fact**
* **Returns_Fact**

#### Dimension Tables

* **Customer_Dim**
* **Product_Dim**
* **Date_Dim**
* **Region_Dim**

---

### Data Model

* A **Star Schema** structure is implemented
* **Sales_Fact** serves as the central fact table connected to all dimension tables
* **Returns_Fact** is linked to **Sales_Fact** using **SalesID**
* **Date_Dim** is marked as the official **Date Table** for time intelligence operations

---

### Calculated Columns

#### 1) Profit *(Sales_Fact)*

**Profit = SalesAmount − Cost**

#### 2) ReturnFlag *(Sales_Fact)*

Identifies whether a transaction is **Returned** or **Not Returned**

#### 3) Customer Full Name *(Customer_Dim)*

Combines **First Name + Last Name** and formats the output in **UPPERCASE**

---

### Measure Table

A separate table named **“Measures”** is created to store all DAX measures in one centralized location, ensuring better organization and clean reporting.

---

### Key Measures Created

* **Total Sales**
* **Total Cost**
* **Total Profit**
* **Total Quantity**
* **Average Sale per Transaction**
* **Total Return**
* **Return Rate (%)**

---

### Advanced Measures

#### Time Intelligence

* **Sales Last Year (LY)**
* **Year-over-Year (YoY) Growth**
* **Month-over-Month (MoM) Growth**
* **Running Total Sales**
* **Year-to-Date (YTD) Sales**

#### Filter Context Handling

* **Sales across all regions (ignores filters)**
* **Sales with applied filters (respects slicers/context)**

#### Additional Logic

* **Sales Category:** Low / Medium / High
* Profit calculation using **SUMX** for row-level evaluation

---

### DAX Functions Used

* **Aggregation:** `SUM`, `AVERAGE`, `COUNTROWS`
* **Context & Filters:** `CALCULATE`, `FILTER`, `ALL`
* **Row Context:** `SUMX`
* **Conditions:** `IF`, `SWITCH`
* **Time Intelligence:** `TOTALYTD`, `SAMEPERIODLASTYEAR`, `PREVIOUSMONTH`

---

### Visual Used

✅ **Only Matrix visual** is used throughout the report
❌ No charts, graphs, or additional visuals included

Data is organized and analyzed using combinations of:

* **Region**
* **Date**
* **Product**
* **Customer**

---

### Tools Used

* **Power BI Desktop**
* **DAX (Data Analysis Expressions)**

---

### Author

**Khushi Nagar**

---

### Declaration

This project is developed strictly for **academic purposes** and follows all provided instructions, including model structure, DAX implementation, and matrix-only reporting.
