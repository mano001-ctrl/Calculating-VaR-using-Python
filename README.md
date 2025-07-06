# Calculating VaR Using Python

**Calculating VaR Using Python** is a hands‑on repository demonstrating multiple approaches to computing Value at Risk (VaR) for financial portfolios. Through interactive Jupyter Notebooks and standalone Python scripts, you will learn how to: Historical Simulation, Parametric (Variance‑Covariance), and Monte Carlo methods. The repo includes sample data, visualization code, and risk‑reporting templates.

---

## Repository Structure

```plaintext
Calculating-VaR-using-Python/
├── data/                              # Sample price and returns CSV files
│   ├── sample_prices.csv              # Time series of asset prices
│   └── sample_returns.csv             # Precomputed daily returns
│
├── notebooks/                         # Jupyter notebooks demonstrating each method
│   ├── 01_Historical_Simulation.ipynb # Historical VaR calculation and backtesting
│   ├── 02_Parametric_VaR.ipynb        # Variance-Covariance VaR with normal assumptions
│   ├── 03_Monte_Carlo_VaR.ipynb       # Simulated VaR using random sampling
│   └── 04_Comparing_VaR_Methods.ipynb # Side-by-side comparison and visualization
│
├── scripts/                           # Modular Python scripts for batch runs
│   ├── historical_var.py              # CLI for historical simulation VaR
│   ├── parametric_var.py              # CLI for parametric VaR
│   └── monte_carlo_var.py             # CLI for Monte Carlo VaR
│
├── reports/                           # Example PDF and HTML risk reports
│   └── VaR_Report_Sample.pdf
│
├── requirements.txt                  # List of Python dependencies
├── LICENSE                            # MIT License
└── README.md                          # This file
```

---

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/mano001-ctrl/Calculating-VaR-using-Python.git
   cd Calculating-VaR-using-Python
   ```

2. **Create and activate a virtual environment** (recommended)

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate    # macOS/Linux
   .\.venv\Scripts\activate   # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### Jupyter Notebooks

1. Launch Jupyter Lab or Notebook:

   ```bash
   jupyter lab
   ```
2. Open any notebook under `notebooks/` and follow the step-by-step cells to compute and visualize VaR.

### CLI Scripts

Each method has a corresponding script in `scripts/`. Example usage:

```bash
# Historical simulation VaR at 95% confidence, 1-day horizon
python scripts/historical_var.py --input data/sample_returns.csv --alpha 0.95 --output reports/hist_var_results.csv

# Parametric VaR
python scripts/parametric_var.py --input data/sample_returns.csv --alpha 0.99

# Monte Carlo VaR with 10,000 simulations
python scripts/monte_carlo_var.py --input data/sample_prices.csv --alpha 0.95 --simulations 10000
```

Outputs are printed to console or saved to CSV/plot images as indicated in each script.

---

## Examples and Visualizations

* **Backtesting Historical VaR:** Compare predicted VaR against actual portfolio losses over time.
* **Parametric VaR Sensitivity:** Explore how changing correlation and volatility assumptions affects VaR.
* **Monte Carlo Distributions:** Plot simulated profit & loss distributions and highlight the VaR threshold.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/my-vaR-method`.
3. Add new notebooks, scripts, or improve existing code.
4. Ensure new dependencies are added to `requirements.txt`.
5. Submit a pull request describing your changes.

Please follow PEP8 coding style and document notebooks clearly.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Contact

For questions or feedback, open an issue on GitHub or reach out to the maintainer.
