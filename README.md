# 🍔 **Snack-Analysis & Nutritional Data Pipeline**

A comprehensive data engineering and comparative health analysis project built with **Apache Spark (PySpark)** and **Pandas**, evaluating the nutritional profiles of Starbucks and McDonald's menu items.

---

## 📌 Project Overview:

The objective of this project is to extract, transform, clean, and analyze multi-source nutritional datasets. Because Spark does not natively read Excel files (`.xlsx`), the workflow bridges Pandas for file ingestion/conversion and PySpark for scalable data cleaning, manipulation, and metric aggregation.

### 🔑 **Key Tasks Covered:**
* **Task 1:** Data extraction and ingestion from source files into the pipeline.
* **Task 2:** PySpark-based data cleaning (handling string placeholders like `-`, casting data types) and computing aggregate nutritional statistics (Calories, Fat, Carbs, Fiber, Protein, Sodium).
* **Task 3:** Comprehensive comparative health analysis and technical documentation of engineering challenges faced.

---

## 🛠️ **Tech Stack & Libraries:**

* 🐍 **Language:** Python
* ⚡ **Big Data Framework:** Apache Spark (PySpark SQL, Catalyst Optimizer)
* 🐼 **Data Processing:** Pandas (for native Excel file parsing)
* 📓 **Environment:** Jupyter Notebook (`.ipynb`)

---

## 📂 **Repository Directory Structure:**

```text
├── Data/
│   ├── menu.xlsx                              # McDonald's nutritional menu dataset
│   ├── starbucks-menu-nutrition-drinks.xlsx   # Starbucks drinks nutrition dataset
│   ├── starbucks-menu-nutrition-food.xlsx     # Starbucks food nutrition dataset
│   └── starbucks_drinkMenu_expanded.xlsx      # Expanded Starbucks drink catalog
├── Snack_Analysis.ipynb                       # Main PySpark data cleaning & aggregation notebook
├── Snack_Analysis_Report                      # Comparative analysis & technical challenges report
└── README.md                                  # Project documentation.
```
---
##📊 **Summary of Findings (Task 3):**
☕ Starbucks: Features lower overall caloric averages and drastically lower sodium (~57.93 mg), though carbohydrate levels (~24.74 g) rise in sweetened or dairy-heavy drinks.
🍟 McDonald's: Provides higher protein and macronutrient density at the cost of higher sodium, fats, and overall calories.

---
##⚙️ ****Engineering Challenges & Solutions:**
📄 Excel Parsing: Used Pandas to ingest .xlsx files since Spark lacks a native Excel reader.
🔍 Missing Placeholders (-): Replaced string hyphens with None using conditional expressions (when / otherwise) before casting columns to double.
🔣 Special Characters in Columns: Enclosed column names containing dots and parentheses (e.g., `Carb. (g)`) in backticks to prevent Spark Catalyst Optimizer [UNRESOLVED_COLUMN] errors.

---
##🎯 **Conclusion****
Overall, the analysis helped compare the nutritional characteristics of Starbucks beverages and McDonald’s fast-food items. The preprocessing stage also provided practical experience in handling missing values and special characters while working with PySpark. Resolving these issues made the data suitable for further analysis and helped ensure that the final results were more reliable.

