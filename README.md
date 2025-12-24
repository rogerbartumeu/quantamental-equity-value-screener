{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "U7r71swvNQ4i"
      },
      "outputs": [],
      "source": [
        "# Quantamental Equity Screener: Automating the Buffett Methodology\n",
        "\n",
        "![Python](https://img.shields.io/badge/Python-3.9%2B-blue)\n",
        "![License](https://img.shields.io/badge/License-MIT-green)\n",
        "![Status](https://img.shields.io/badge/Status-Active-success)\n",
        "\n",
        "## 📌 Project Overview\n",
        "**\"Price is what you pay. Value is what you get.\"** — Warren Buffett.\n",
        "\n",
        "As an engineer turned finance student, I believe the *search* for value should be systematic, while the *decision* remains discretionary. This project is a Python-based engine designed to automate the **Quality at a Reasonable Price (QARP)** filtering process.\n",
        "\n",
        "It avoids generic P/E screening and instead focuses on **Capital Efficiency (ROIC)**, **Balance Sheet Health**, and **Owner Earnings** to generate a shortlist of high-quality compounders for further manual research.\n",
        "\n",
        "## 📊 The \"Moat\" Logic (Methodology)\n",
        "The screener pulls real-time financial data (Balance Sheet, Income Statement, Cash Flow) and filters the universe based on four \"Buffett Pillars\":\n",
        "\n",
        "### 1. Capital Efficiency (The Moat)\n",
        "* **Metric:** Return on Invested Capital (ROIC)\n",
        "* **Threshold:** `> 15%`\n",
        "* **Why:** Ensures the business generates returns above its Cost of Capital (WACC), indicating a competitive advantage.\n",
        "\n",
        "### 2. Financial Fortress (The Safety)\n",
        "* **Metric:** Net Debt / EBITDA\n",
        "* **Threshold:** `< 3.0x`\n",
        "* **Why:** Filters out companies with fragile balance sheets or excessive leverage risk.\n",
        "\n",
        "### 3. \"Owner Earnings\" (The Reality)\n",
        "* **Metric:** Free Cash Flow Conversion (FCF / Net Income)\n",
        "* **Threshold:** `> 80%`\n",
        "* **Why:** Verifies that reported accounting earnings are backed by actual cash generation.\n",
        "\n",
        "### 4. Valuation (The Margin of Safety)\n",
        "* **Metric:** FCF Yield\n",
        "* **Threshold:** `> Risk-Free Rate + 3%` (approx >7%)\n",
        "* **Why:** Buying the cash flow stream at a discount.\n",
        "\n",
        "## 🛠️ Tech Stack\n",
        "* **Core:** Python (Pandas, NumPy)\n",
        "* **Data Fetching:** yFinance API (Yahoo Finance)\n",
        "* **Environment:** Jupyter Notebook\n",
        "\n",
        "## 📈 Sample Output\n",
        "*The script outputs a ranked list of \"Quality Compounders\" and visualizes the universe.*\n",
        "\n",
        "| Ticker | Price ($) | ROIC (%) | Net Debt/EBITDA | FCF Yield (%) | P/E |\n",
        "| :--- | :--- | :--- | :--- | :--- | :--- |\n",
        "| **UNP** | 245.20 | 16.4 | 2.1 | 5.8 | 21.3 |\n",
        "| **DE** | 380.10 | 22.1 | 1.8 | 7.2 | 14.5 |\n",
        "| **ITW** | 260.50 | 28.5 | 1.2 | 4.9 | 24.0 |\n",
        "\n",
        "## 🚀 How to Run\n",
        "1.  Clone the repository:\n",
        "    ```bash\n",
        "    git clone [https://github.com/yourusername/quantamental-screener.git](https://github.com/yourusername/quantamental-screener.git)\n",
        "    ```\n",
        "2.  Install dependencies:\n",
        "    ```bash\n",
        "    pip install -r requirements.txt\n",
        "    ```\n",
        "3.  Run the notebook:\n",
        "    ```bash\n",
        "    jupyter notebook screener.ipynb\n",
        "    ```"
      ]
    }
  ]
}