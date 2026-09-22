# Task 15 — Product Count Analysis

**Track:** Data Analytics (Veda Technology Internship — Level 1, Day 15)
**Tool:** Microsoft Excel (COUNTIF / COUNTIFS)
**Dataset:** Superstore — `Product_Dimension` (1,894 product records)

## Objective
Count products by category and identify the largest category, using COUNTIF/COUNTIFS.

## Approach
1. Copied the `Product_Dimension` table (Product ID, Category, Sub-Category, Product Name) into a `Product_Data` sheet.
2. Built a **Product Count Table** on the `Summary` sheet with one row per category:
   - **Total Product Records** — `COUNTIF(Category range, category)`
   - **Unique Products** — a `SUMPRODUCT` + `COUNTIFS` distinct-count formula, since 32 Product IDs repeat across multiple rows
   - **Duplicate Records** — Total − Unique
3. Identified the **largest category** with `INDEX/MATCH` against `MAX()`, both by total records and by unique products.

## Results

| Category        | Total Product Records | Unique Products | Duplicate Records |
|------------------|-----------------------|------------------|--------------------|
| Furniture        | 383                   | 375              | 8                  |
| Office Supplies  | **1,098**             | **1,083**        | 15                 |
| Technology       | 413                   | 404              | 9                  |
| **Grand Total**  | **1,894**             | **1,862**        | 32                 |

**Largest category: Office Supplies** — both by total product records (1,098) and by unique products (1,083). It also has the most sub-categories (9, vs. 4 each for Furniture and Technology), which explains its size.

## Files
- `Product_Count_Analysis.xlsx` — workbook with `Product_Data` and `Summary` sheets (live formulas)
- `report.pdf` — one-page project report

---
*Veda Technology Data Analytics Internship — Task 15/45*
