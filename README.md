# Canadian Rent vs. Junior Data Analyst Salary — 2025/2026

> *"Location strategy is now just as important as technical skill."*

A data analysis project comparing 1-bedroom asking rents across Canada's major tech hubs against entry-level Data Analyst wages — built with real government data and Python.

📂 Full methodology in [`rent_vs_salary.ipynb`](rent_vs_salary.ipynb)

---

## 📌 Project Overview

As someone tracking the Canadian tech job market, I wanted to stop relying on headlines and query the raw numbers instead.

This project pulls 2025/2026 data from **Statistics Canada** and the **Government of Canada Job Bank** to answer one question: *how affordable is rent for a junior Data Analyst (NOC 21223) in Canada's major cities?*

The analysis covers **5 cities**: Vancouver, Toronto, Ottawa, Calgary, and Montréal.

---

## 📊 Key Findings

| City | 1BR Rent (Q1 2025) | Low Wage Floor | Rent % of Take-Home |
|------------|-------------------|----------------|---------------------|
| Vancouver | $2,896 | $32.08/hr | ~79% |
| Toronto | $2,587 | $21.90/hr | ~93% ⚠️ |
| Ottawa | $2,100 | $24.73/hr | ~70% |
| Calgary | $1,690 | $28.57/hr | ~49% |
| Montréal | $1,500 | $27.21/hr | ~44% ✅ |

- **The Toronto Paradox** — Vancouver has the highest absolute rent, but Toronto is the hardest city to start a career. At a junior wage floor of $21.90/hr, rent consumes ~93% of take-home pay.
- **The Western Advantage** — Vancouver ($32.08/hr) and Calgary ($28.57/hr) offer higher wage floors, creating a healthier survival gap for new grads.
- **The Sweet Spot** — Montréal is the most viable entry-level city, with the most balanced rent-to-income ratio at ~44%.
- **The 33% Rule** — No city in this analysis meets the standard affordability benchmark for junior analysts.

---

## 🛠️ Tools & Methodology

**Tools:** Python · Pandas · Matplotlib · Jupyter Notebook

**Wage methodology:**
- Filtered Job Bank dataset for NOC 21223 (Data Analyst – Informatics and Systems)
- Used the **low wage floor** (entry-level) per city region: `Low_Wage × 40 hrs × 52 weeks`
- Applied 73% take-home estimate (approx. combined federal + provincial tax)

**Rent methodology:**
- Loaded Statistics Canada Table 46-10-0092-01 (quarterly asking rents)
- Filtered for `Apartment - 1 bedroom`, Q1 2025
- Used Ottawa–Gatineau **Ontario part** CMA only
- Used Lower Mainland–Southwest region for Vancouver (Metro Vancouver)

---

## 📂 Data Sources

| Dataset | Source |
|---|---|
| Asking Rent Prices (Table 46-10-0092-01) | [Statistics Canada](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=4610009201) |
| Hourly Wages by Region — NOC 21223 | [Government of Canada Job Bank](https://www.jobbank.gc.ca/wagereport/occupation/17882) |

---

## 💡 What I Learned

- How to load and clean a Statistics Canada CSV with metadata headers using `skiprows` and `ffill()`
- How to filter and reshape Job Bank wage data by NOC code and region
- How to calculate monthly take-home pay and affordability ratios from raw hourly wages
- How to merge two government datasets on a common city key and visualize the results with Matplotlib
- Why matching the **correct geographic region** matters — Job Bank regions don't always align intuitively with city names (e.g. "Lower Mainland–Southwest" for Vancouver)

---

## 🔗 Let's Connect

I'm documenting my journey into data analytics — one real-world dataset at a time.

[LinkedIn](https://linkedin.com/in/dieudonnentakirutimana/) · [Website](https://dieudonne.ca/)

*#DataAnalytics #Python #CanadaTech #MarketAnalysis #DataVisualization*
