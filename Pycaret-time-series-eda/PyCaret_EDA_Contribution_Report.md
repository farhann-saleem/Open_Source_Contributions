# PyCaret Time-Series EDA — README (Technical Overview)

## 📍 Project Summary

* **Repository:** [PyCaret](https://github.com/pycaret/pycaret)
* **Fork:** [farhann-saleem/pycaret](https://github.com/farhann-saleem/pycaret)
* **Pull Request:** [#4171 – Time Series EDA](https://github.com/pycaret/pycaret/pull/4171)
* **Linked Issue:** [#4174](https://github.com/pycaret/pycaret/issues/4174)
* **Date:** October 2025
* **Status:** In Review

---

## 🧠 Objective

Add an **Exploratory Data Analysis (EDA)** feature to PyCaret’s `time_series` module to:

* Generate descriptive summaries of time-series data
* Perform ADF-based stationarity tests
* Visualize trends, seasonality, and autocorrelation (ACF)
* Support interactive Plotly plots

---

## ⚙️ Implementation Summary

**File Added:** `pycaret/time_series/eda.py`

### Function Implemented

```python
eda_ts_plot(
    data: pd.Series | pd.DataFrame,
    target: str | None = None,
    show: bool = True,
    acf_lags: int = 30,
    period: int | None = None,
    plotly: bool = False,
)
```

### Features

| Feature            | Description                                   |
| ------------------ | --------------------------------------------- |
| Input Handling     | Accepts Series or DataFrame + target input.   |
| Descriptive Stats  | Calculates mean, min, max, missing values.    |
| Stationarity Test  | Runs ADF test and returns p-value, statistic. |
| Visualization      | Line plot, ACF plot, optional decomposition.  |
| Plotly Integration | Interactive mode with `plotly=True`.          |
| CI Compatibility   | Uses `Agg` backend for headless environments. |

---

## 🧪 Testing Summary

**Test File:** `tests/test_time_series_eda.py`

**Framework:** `pytest`

### Tests Implemented

* Validate Series and DataFrame inputs.
* Confirm ADF test keys exist.
* Ensure decomposition runs when `period` provided.
* Check differencing improves stationarity.
* Error handling for missing `target`.

**Execution:**

```bash
pytest -q tests/test_time_series_eda.py
```

**Result:**

```
3 passed, 1 warning (distutils deprecation)
```

---

## 🧱 Environment

| Component   | Version / Tool                                                   |
| ----------- | ---------------------------------------------------------------- |
| Python      | 3.10.10                                                          |
| Libraries   | pandas, numpy, matplotlib, plotly, statsmodels, pytest           |
| Environment | Virtualenv (`venv`), editable install (`pip install -e .[full]`) |
| IDE         | Visual Studio Code                                               |
| Backend     | Matplotlib Agg                                                   |

---

## 📊 Example Output

```python
{'length': 200, 'missing_values': 0, 'mean': -12.37, 'min': -22.53, 'max': 1.79, 'adf_pvalue': 0.2198, 'adf_stationary': False}
```

---

## 🧩 Screenshots

| Plot                                                                                                  | Description            |
| ----------------------------------------------------------------------------------------------------- | ---------------------- |
| ![series\_line](https://github.com/user-attachments/assets/e1cbab39-1ad9-41b0-8814-0775ee57ac74)      | Time Series Line Plot  |
| ![series\_acf](https://github.com/user-attachments/assets/2b5433ae-5657-4333-a850-85a4c4ec4daf)       | Autocorrelation (ACF)  |
| ![series\_decompose](https://github.com/user-attachments/assets/ccf96b4d-ef31-42fc-b18c-bad33d15f02f) | Seasonal Decomposition |

---

## 📦 Folder Structure

```
pycaret-time-series-eda/
│
├── PyCaret_EDA_Contribution_Report.md  ← this file (README)
├── PyCaret_EDA_Contribution_Report.pdf ← detailed documentation
├── links.txt                           ← references and URLs
├── tests/test_time_series_eda.py
├── pycaret/time_series/eda.py
└── pr_screens/ (plot screenshots)
```

---

**© 2025 Farhan Saleem**
*All code, tests, and documentation authored and maintained by the contributor.*
