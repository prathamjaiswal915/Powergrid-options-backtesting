# POWERGRID Options Backtesting — Short Straddle vs Buy & Hold

## Project Overview
A quantitative backtesting project comparing two investment strategies on 
**POWERGRID Corporation of India (NSE)** over a 2-year period (Oct 2023 – Sep 2025).

---

## Strategies Compared
| Strategy | Description |
|---|---|
| **Buy & Hold** | Buy POWERGRID stock on 03-Oct-2023 and hold till 30-Sep-2025 |
| **Short Straddle** | Sell ATM CE + PE every month, manage with SL and profit target |

---

## Short Straddle Rules
- **Capital**: Fixed ₹1,30,000 per month
- **Entry**: First trading day of each expiry series (sell ATM CE + PE at Close price)
- **Lot Size**: As per NSE/SEBI circular (changes from 3600 → 1800 → 1900)
- **Profit Target**: Square off when MTM profit ≥ 50% of total premium collected
- **Stop Loss**: Square off when MTM loss ≥ ₹20,000
- **Expiry Exit**: If neither triggered, exit at LTP on expiry date
- **Next Trade**: Starts the day after previous month's expiry

---

## Data Files
| File | Description |
|---|---|
| `POWERGRID_Historical_Data.csv` | Daily OHLC price data of POWERGRID stock |
| `Call_option_Data.csv` | Monthly ATM CE option chain data |
| `Put_Option_Data.csv` | Monthly ATM PE option chain data |
| `Lot_Size_List.csv` | NSE lot size changes across 24 months |

---

## Key Results

| Metric | Buy & Hold | Short Straddle |
|---|---|---|
| Absolute Return | 40.44% | 76.88% |
| CAGR | 18.58% | 33.13% |
| Sharpe Ratio | 0.45 | 0.46 |
| Max Drawdown | -31.36% | -56.45% |
| Win Rate | 54.2% | 54.2% |

---

## Project Structure
```
├── Short_Straddle.ipynb   # Main Jupyter Notebook
├── *.csv                  # Data files
└── README.md              # Project documentation
```

## How to Run
1. Clone this repository
```bash
git clone https://github.com/YOUR_USERNAME/powergrid-options-backtesting.git
```
2. Install dependencies
```bash
pip install pandas numpy matplotlib
```
3. Open Jupyter Notebook
```bash
jupyter notebook Short_Straddle.ipynb
```
4. Update the file paths in **Cell 2 and Cell 5** to your local path
5. Run all cells in order

---

## Tools & Libraries
- **Python 3.x**
- **Pandas** — data manipulation
- **NumPy** — numerical calculations
- **Matplotlib** — visualisations
- **Jupyter Notebook** — interactive development

---

## Author
**Pratham Jaiswal**  
Quantitative Trading Enthusiast | Python | Options Strategies | NSE Markets  
[GitHub Profile](https://github.com/prathamjaiswal915)
