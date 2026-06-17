# 📈 Stock Data Extraction and Revenue Dashboard

A data science project that extracts historical stock price data and quarterly revenue figures for **Tesla (TSLA)** and **GameStop (GME)**, then visualizes them side-by-side in a two-panel dashboard. Built as part of the IBM Data Science Professional Certificate on Coursera.

---

## 📌 Project Overview

This project demonstrates two core data collection techniques used in financial data analysis:

1. **API-based extraction** — using `yfinance` to pull historical OHLCV (Open, High, Low, Close, Volume) stock data directly from Yahoo Finance
2. **Web scraping** — using `requests` and `BeautifulSoup` to extract quarterly revenue tables from HTML pages

The extracted data is then cleaned, structured into pandas DataFrames, and visualized using `matplotlib` to build a simple but informative stock dashboard.

---

## 📂 Repository Structure

```
stock-dashboard-project/
│
├── notebooks/
│   └── Revenue_Data_and_Building_a_Dashboard.ipynb   # Main analysis notebook
│
├── images/                  # Output dashboard screenshots (add after running)
├── data/                    # Placeholder for any saved data files
├── requirements.txt         # Python dependencies
├── .gitignore               # Files excluded from version control
└── README.md                # You are here
```

---

## 🔍 Questions Covered

| # | Task | Method |
|---|------|--------|
| Q1 | Extract Tesla (TSLA) historical stock data | `yfinance` |
| Q2 | Extract Tesla quarterly revenue data | Web scraping (`requests` + `BeautifulSoup`) |
| Q3 | Extract GameStop (GME) historical stock data | `yfinance` |
| Q4 | Extract GameStop quarterly revenue data | Web scraping (`requests` + `BeautifulSoup`) |
| Q5 | Plot Tesla stock price + revenue dashboard | `matplotlib` |
| Q6 | Plot GameStop stock price + revenue dashboard | `matplotlib` |

---

## 📊 Sample Output

### Tesla Dashboard
The Tesla dashboard shows a steady climb in both revenue and share price from 2010 through mid-2021, reflecting the company's growth from a niche EV startup to one of the world's most valuable automakers.

### GameStop Dashboard
The GameStop dashboard is a fascinating case study — the revenue chart shows years of flat-to-declining performance, while the stock price chart captures the dramatic short squeeze of early 2021. It's a clear visual example of how market sentiment can diverge from company fundamentals.

> After running the notebook, save the output graphs to the `images/` folder and update this section with the actual screenshots.

---

## 🛠️ Tech Stack

| Library | Purpose |
|--------|---------|
| `yfinance` | Fetching stock price history from Yahoo Finance |
| `pandas` | Data manipulation and cleaning |
| `requests` | Downloading HTML pages for scraping |
| `beautifulsoup4` | Parsing HTML and extracting tables |
| `matplotlib` | Plotting the stock + revenue dashboards |
| `nbformat` | Jupyter notebook compatibility |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/stock-dashboard-project.git
cd stock-dashboard-project
```

### 2. Create and activate a virtual environment (recommended)

```bash
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook notebooks/Revenue_Data_and_Building_a_Dashboard.ipynb
```

### 5. Run all cells

Use **Kernel → Restart & Run All** to execute the notebook from top to bottom. The two dashboard plots will appear inline at Questions 5 and 6.

---

## 📋 Data Sources

| Data | Source |
|------|--------|
| Tesla (TSLA) stock price | [Yahoo Finance via yfinance](https://finance.yahoo.com/quote/TSLA/) |
| Tesla quarterly revenue | [IBM Skills Network hosted HTML](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm) |
| GameStop (GME) stock price | [Yahoo Finance via yfinance](https://finance.yahoo.com/quote/GME/) |
| GameStop quarterly revenue | [IBM Skills Network hosted HTML](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html) |

> **Note:** All graphs display data up to **June 2021** as defined in the `make_graph` function.

---

## 💡 Key Concepts Demonstrated

- **Ticker objects** with `yfinance.Ticker()` and `.history(period="max")`
- **DataFrame index management** with `reset_index(inplace=True)`
- **HTML table extraction** using `pd.read_html()` and `BeautifulSoup`
- **String cleaning** with `.str.replace()` using regex to remove `$` and `,`
- **Handling missing data** with `.dropna()` and boolean filtering
- **Multi-panel plotting** with `matplotlib.pyplot.subplots(2, 1)`

---

## 🙋 About

This project was completed as part of the [IBM Data Science Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-science) on Coursera — specifically the *Python Project for Data Science* course.

**Original lab authors:** Joseph Santarcangelo, Azim Hirjani (IBM)

---

## 📄 License

This project is for educational purposes. Stock data is sourced from Yahoo Finance via the `yfinance` library. Revenue data is hosted by IBM Skills Network for the course.
