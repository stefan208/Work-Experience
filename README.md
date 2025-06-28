# 📦 Operational & Financial KPI Benchmarking – Evro Line

This project automates the calculation and peer-benchmarking of both **operational** and **financial** KPIs for **Evro Line**, an international freight-forwarding company.  
The script transforms raw Excel data into actionable insights on pricing power, cost efficiency, and profitability.

---

## 🎯 Key Objectives
- **Compute unit-economics KPIs** per shipment (revenue, cost, profit, overhead, capex).  
- **Calculate financial ratios** (margins, asset turnover, leverage).  
- **Track trends** (period-over-period growth).  
- **Benchmark Evro Line vs. peer averages** for every period.  
- **Generate strategic commentary**: pricing gap, cost gap, margin gap, profitability gap, and recommended actions.

---

## 📁 Expected Data Structure (context only)
*Input file is **not** included.*  
The script expects a single Excel file (`kpi_data.xlsx`) with one row per **company–period** containing at minimum:

| Column            | Description                                  |
|-------------------|----------------------------------------------|
| `date`            | Period end date (monthly or quarterly)       |
| `company`         | Legal entity / brand name                    |
| `revenue`, `cogs`, `opex`, `ebit`, `net_income` | Financial totals |
| `capex`, `total_assets`, `liabilities`, `equity` | Balance-sheet items |
| `num_invoices`    | Number of shipments/invoices in the period   |

The code labels Evro Line as **`OUR_FIRM = "Evro Line"`**; all other companies are treated as peers.

---

## ▶️ Code Structure
1. **`add_all_kpis()`** – derives unit KPIs, ratios, and growth metrics.  
2. **`build_peer_variance()`** – compares Evro KPIs to peer averages and computes variance columns.  
3. **`dual_line_plot()`** – plots Evro vs. peers over time for any KPI.  
4. **Interpretation block** – evaluates four core gaps (pricing, cost, margin, profitability) and prints a manager-ready recommendation.

---

## 📈 Outputs
| File / Item                         | Purpose                                                  |
|------------------------------------|----------------------------------------------------------|
| `peer_variance_output.xlsx`        | Period-by-period table of Evro KPIs, peer averages, and variance |
| `ebit_margin_evro_vs_peers.png`    | Sample time-series plot (Evro vs. peers)                 |
| Console printout                   | Strategic summary + next-step recommendation             |

---

## 🛠 Tech Stack
- **Python**: `pandas`, `numpy`, `matplotlib`
- Excel (sample data not included due to confidentiality)

---

## 💬 Author
**Stefan Radovic**  
MSc Financial Economics – Erasmus University Rotterdam  
