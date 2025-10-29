# 🧾 Excel Project: Kitchen Equipment Revenue Dashboard

## 📊 Overview
An **interactive Excel dashboard** analyzing **Home Luxury Kitchen’s 2022 sales performance** by product, state, quantity, revenue, and sales channel.  
Built **entirely with Excel formulas** (no PivotTables) using a **multi-year dataset (2019–2022)**, with the dashboard focused on **2022 insights**.

---

## 🧩 Data Model
- **Columns:** Year, Product, State, Quantity, Revenue, Sales Channel  
- **Scope:** 2019–2022 (Dashboard filtered to 2022 by default)  
- **Entities:** 50 U.S. states, 10+ kitchen products (e.g., Kettle, Toaster, Teapot, Dishwasher, etc.), and two sales channels (In Store, Online).  
- **Structure:** Data formatted as an Excel Table for structured references and stable range management.  

---

## 📈 Metrics & Logic
| Metric | Logic / Formula |
|---------|-----------------|
| **Total Revenue (2022)** | `SUMIFS(Revenue, Year, 2022, …)` with optional Product/State filters |
| **Total Quantity (2022)** | `SUMIFS(Quantity, Year, 2022, …)` |
| **Revenue by Product** | `SUMIFS` grouped by Product (Top products: Teapot, Egg slicer, Kettle) |
| **Revenue by State** | `SUMIFS` grouped by State (Top states: Colorado, Massachusetts, Kentucky, Illinois, California) |
| **Revenue by Channel** | `SUMIFS` split between *In Store* and *Online* (e.g., 63.85% vs 36.15%) |
| **YOY Scaffolding** | Optional “Change” fields for multi-year extension beyond 2022 |

---

## 🌟 Dashboard Features
- Default **Year = 2022** (per project brief)
- **Dropdown selectors** for Product and State
- **KPI cards:** Total Revenue, Quantity, Channel Split  
- **Top 10 States chart** (dynamic `LARGE` + `INDEX/MATCH` logic)
- **Clean single-page layout**, following “Make it simple” guidance
- Formula-driven — no PivotTables, macros, or VBA

---

## 🧠 How to Use
1. Open **Sales-Dashboard.xlsx**
2. Go to the **Dashboard** sheet  
3. Use dropdowns to select *Year (2022)*, *Product*, or *State*  
4. Review:
   - KPI cards for revenue and quantity  
   - Top Products and Top 10 States  
   - Channel split (In Store vs Online)  
5. Explore **Analysis** sheet to view formula logic (`SUMIFS`, `INDEX/MATCH`, `LARGE`, etc.)

---

## 💡 Key Insights (Example)
- **Kettle 2022 Revenue:** \$5,278,636 — among the top products  
- **Channel Mix:** In Store ≈ 64%, Online ≈ 36% — stronger in-store performance  
- **High-Performing States:** Colorado, Massachusetts, Kentucky, Illinois, and California lead 2022 revenue

---

## 🧮 Core Excel Techniques
- `SUMIFS()` for conditional totals (Year, Product, State, Channel)
- Structured Table references for data integrity
- `INDEX/MATCH` or `XLOOKUP` for dynamic captions and KPIs
- `LARGE` + `MATCH` for Top 10 extraction without PivotTables
- Data Validation for dropdown selectors (Year, Product)
- Named Ranges for cleaner formulas

---

## 📊 Recommendations
- **Double down on top states** (e.g., Colorado, Massachusetts) with in-store promotions  
- **Expand inventory and marketing** for high-performing products (Teapot, Egg slicer, Kettle)  
- **Boost Online conversions** through product bundles (e.g., Toaster + Breadbox)  
- Maintain a formula-first design, but consider **Power Query** for scalable data updates in future years

---

## ⚙️ Setup & Replication
1. Keep raw data as an Excel Table with headers: `Year, Product, State, Quantity, Revenue, Sales Channel`
2. Update named ranges and validation lists for new years or products
3. Adjust `LARGE` function ranges for Top 10 logic if data expands

---

## 📋 Constraints
- **No PivotTables** (per project brief)  
- All calculations and visuals are **formula-driven**  
- Lightweight, transparent, and easily auditable design  
