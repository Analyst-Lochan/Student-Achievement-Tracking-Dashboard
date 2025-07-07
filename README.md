# 🎓 OULAD SQL Project – Student Performance Tracking System

This project is based on the **Open University Learning Analytics Dataset (OULAD)**, which is openly available for educational use.

---

## 📝 Project Workflow

### ✅ Step-by-Step Process

#### 1. Dataset Download
- I downloaded the OULAD dataset from the [official website](https://analyse.kmi.open.ac.uk/open_dataset).
- The dataset contains approximately **28,000 student records** across seven tables.

#### 2. Table Selection
- Out of the seven tables, I selected and worked with the following four:
  - `studentinfo`
  - `assessment`
  - `courses`
  - `studentRegistration`

#### 3. Data Cleaning in Excel
- During review, I found **~4,000 duplicate records** in the dataset.
- Actions taken:
  - **Rearranged columns** in Excel to match the SQL table schema.
  - Removed duplicate records using **Excel’s Remove Duplicates** feature.
  - Verified data types (e.g., date format, integer columns).
  - Saved cleaned files in **CSV UTF-8 (Comma delimited)** format to ensure compatibility during SQL import.

#### 4. Database Setup
- Created a new database on my **local SQL Server** named `OULAD`.
- Manually created SQL tables using `CREATE TABLE` statements with the same names as in the dataset.

#### 5. Data Import (Bulk Insert)
- Imported the cleaned `.csv` files into the respective tables using **BULK INSERT** commands.
- Also used proper `CODEPAGE = '65001'` to handle UTF-8 encoded files.

#### 6. ER Diagram Creation
- Generated the ER Diagram using **[dbdiagram.io](https://dbdiagram.io)**.
- I wrote the schema in **DBML language** with support and guidance from ChatGPT.
- Established primary and foreign key relationships based on the structure of the OULAD dataset.

#### 7. SQL Querying & Analysis
- Executed multiple professional-level SQL queries on the database to analyze:
  - Course and assessment participation
  - Student final results
  - Dropout patterns
- Exported key queries and their **outputs into a PDF**, which is attached to the GitHub project repository.

---

## ⚠️ Challenges & Hurdles Faced

1. **CSV Import Errors:**
   - Encountered character encoding issues while importing files.
   - Resolved by converting files to **CSV UTF-8 (CSV-8)** format and setting `CODEPAGE = '65001'` in import commands.

2. **Date Format Issues:**
   - Excel saved dates inconsistently, causing type mismatch in SQL.
   - Fixed by formatting all date columns before saving.

3. **Duplicate Data:**
   - Detected ~4,000 duplicate rows across tables.
   - Cleaned via Excel using filters and conditional formatting before import.

4. **Composite Keys in ER Diagram:**
   - dbdiagram.io required learning **DBML syntax** for defining composite primary keys and references.
   - Learned syntax like:
     ```dbml
     primary key (id_student, code_module, code_presentation)
     ```

---

## ✅ Final Output

- Clean database with four normalized tables.
- ER diagram created and exported using dbdiagram.io.
- SQL query results exported to PDF.
- All assets uploaded to GitHub as part of this portfolio project.

---

> Thank you for visiting this project repository!
