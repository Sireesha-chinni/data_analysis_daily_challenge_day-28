# Insurance Claims Analysis (Day 28 – Data Analytics Challenge)

A beginner-friendly Python challenge where I act as a Data Analyst at an insurance company and analyze raw claim data stored in plain Python **lists**, using only loops and conditionals (no pandas).

## Repository Contents

| File | Description |
|------|-------------|
| `Day-28-Data-analytics-challenge-python.ipynb` | Jupyter Notebook with the solutions and outputs |
| `Day28_Insurance_Claims_Analysis.pdf` | The original problem statement |
| `README.md` | Project overview (this file) |

## Dataset

```python
policy_ids    = [101, 102, 103, 104, 105, 106]
claim_amounts = [5000, 15000, 7000, 20000, 3000, 12000]
claim_status  = ["Approved", "Rejected", "Approved", "Approved", "Rejected", "Approved"]
customer_age  = [25, 45, 35, 50, 23, 40]
```

Each index across the four lists represents one policy/claim.

## Tasks and Results

| # | Task | Result |
|---|------|--------|
| 1 | Total claim amount of all **Approved** claims | `44000` |
| 2 | Count of **Rejected** claims | `2` |
| 3 | Policy IDs with claim amount > ₹10,000 | `[102, 104, 106]` |
| 4 | Average age of customers with **Approved** claims | `37.5` |
| 5 | Risk category for each customer | `['Low Risk', 'Medium Risk', 'Medium Risk', 'High Risk', 'Low Risk', 'Medium Risk']` |

### Risk Category Rules (Task 5)

- Age < 30 → **Low Risk**
- Age 30–45 → **Medium Risk**
- Age > 45 → **High Risk**

## Approach

- **Task 1:** Loop over indices, and add `claim_amounts[i]` to a running total whenever `claim_status[i] == "Approved"`.
- **Task 2:** Loop over `claim_status` and increment a counter for each `"Rejected"`.
- **Task 3:** Loop over indices, and append `policy_ids[i]` to a result list when `claim_amounts[i] > 10000`.
- **Task 4:** Collect ages of approved customers into a list, then compute `sum(ages) / len(ages)`.
- **Task 5:** Loop through `customer_age`, apply `if / elif / else` rules, and append the label to `risk_category`.

## Concepts Practiced

- Python lists and indexing
- `for` loops with `range(len(...))`
- Conditional logic (`if / elif / else`)
- Accumulator and counter patterns
- Building new lists with `append()`

## How to Run

1. Clone the repository:
   ```bash
   git clone <https://github.com/Sireesha-chinni/data_analysis_daily_challenge_day-28>
   cd <data_analysis_daily_challenge_day-28>
   ```
2. Make sure Python 3.9+ and Jupyter are installed:
   ```bash
   pip install notebook
   ```
3. Launch the notebook:
   ```bash
   jupyter notebook Day-28-Data-analytics-challenge-python.ipynb
   ```
4. Run the cells from top to bottom (`Kernel → Restart & Run All`).

## Possible Improvements

- Rewrite the solutions using `zip()` and list comprehensions
- Reimplement the analysis with pandas for comparison
- Add approval-rate and average-claim-amount metrics
- Wrap each task in a reusable function with simple tests

## Author

Ch Sai Sireesha — [GitHub](https://github.com/Sireesha-chinni)
