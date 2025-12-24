# Quantamental Equity Screener: Automating the Buffett Methodology

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-success)

## Project Overview
> **"Price is what you pay. Value is what you get."** — Warren Buffett.

As an engineer turned finance student, I believe the *search* for value should be systematic, while the *decision* remains discretionary. This project is a Python-based engine designed to automate the **Quality at a Reasonable Price (QARP)** filtering process.

It avoids generic P/E screening and instead focuses on **Capital Efficiency (ROIC)**, **Balance Sheet Health**, and **Owner Earnings** to generate a shortlist of high-quality compounders for further manual research.

## The "Moat" Logic (Methodology)
The screener pulls real-time financial data (Balance Sheet, Income Statement, Cash Flow) and filters the universe based on four "Buffett Pillars":

### 1. Capital Efficiency (The Moat)
* **Metric:** Return on Invested Capital (ROIC)
* **Threshold:** `> 15%`
* **Why:** Ensures the business generates returns above its Cost of Capital (WACC), indicating a competitive advantage.

### 2. Financial Fortress (The Safety)
* **Metric:** Net Debt / EBITDA
* **Threshold:** `< 3.0x`
* **Why:** Filters out companies with fragile balance sheets or excessive leverage risk.

### 3. "Owner Earnings" (The Reality)
* **Metric:** Free Cash Flow Conversion (FCF / Net Income)
* **Threshold:** `> 80%`
* **Why:** Verifies that reported accounting earnings are backed by actual cash generation.

### 4. Valuation (The Margin of Safety)
* **Metric:** FCF Yield
* **Threshold:** `> Risk-Free Rate + 3%` (approx >7%)
* **Why:** Buying the cash flow stream at a discount.

## Tech Stack
* **Core:** Python (Pandas, NumPy)
* **Data Fetching:** yFinance API (Yahoo Finance)
* **Visualization:** Matplotlib / Seaborn (for Quality vs. Price regression)
* **Environment:** Jupyter Notebook

## Sample Output
*The script outputs a ranked list of "Quality Compounders" and visualizes the universe.*

| Ticker | Price ($) | ROIC (%) | Net Debt/EBITDA | FCF Yield (%) | P/E |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **UNP** | 245.20 | 16.4 | 2.1 | 5.8 | 21.3 |
| **DE** | 380.10 | 22.1 | 1.8 | 7.2 | 14.5 |
| **ITW** | 260.50 | 28.5 | 1.2 | 4.9 | 24.0 |

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/quantamental-screener.git](https://github.com/yourusername/quantamental-screener.git)
