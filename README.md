# joining_python_flights

This project is an in-depth analysis of the `nycflights13` dataset, primarily using the **pandas** library. While it began as a practical exercise to replicate complex SQL join operations in Python, it has expanded into a comprehensive analytical workflow.

The analysis explores various aspects of the flight data, including on-time performance, aircraft details, weather impacts, and airline statistics. Each notebook tackles a different set of analytical questions, progressing from basic data merging to more complex, multi-step aggregations.


---
### Companion Project: SQL Version

This project is one of two companion repositories demonstrating data analysis on the `nycflights13` dataset. This repository contains the analysis performed using **Python (Pandas)**.

For the same analysis performed using **SQL (PostgreSQL)**, please see the companion repository:
**[➡️ SQL Flights Analysis](https://github.com/AliaksandrTrasko/joining_sql_flights.git)**

---


## Project Structure

The analysis is structured across several Jupyter Notebooks, each focusing on a specific set of data manipulation techniques that mirror common SQL patterns:

* **`01_basic_joins.ipynb`**: Covers fundamental join operations, such as `inner` and `left` merges, to combine basic datasets like `flights`, `airlines`, and `planes`.
* **`02_advanced_joins.ipynb`**: Explores more complex scenarios, including **self-joins** (to find related flights) and handling `NaN` values resulting from `left` joins (comparing pandas `groupby` behavior to SQL).
* **`03_set_operations.ipynb`**: Demonstrates set-based logic in pandas, replicating SQL's `INTERSECT` and `EXCEPT` operations to identify unique and common records between datasets.
* **`04_subqueries.ipynb`**: Implements analyses that would typically require subqueries in SQL. This includes multi-step aggregations and filtering based on calculated group statistics (e.g., finding carriers with the highest average delays).
* **`other.ipynb`**: Contains additional exploratory queries and visualizations created during the analysis.


##  Tools & Techniques

This analysis was conducted entirely in Python using the following key libraries and techniques:

* **Pandas**: The primary tool for all data loading, cleaning, manipulation, and analysis.
* **Matplotlib / Seaborn**: Used for generating visualizations to support analytical findings.
* **Jupyter Notebook**: The interactive environment used for developing, documenting, and presenting the analysis.

Key skills demonstrated include data merging/joining, grouping & aggregation, handling missing data, logical filtering, and exploratory data analysis (EDA).


## Dataset

This project uses the **`nycflights13`** dataset, which contains detailed information on all 336,776 flights that departed from New York City (EWR, JFK, LGA) in 2013. The data is comprised of five related tables:
* `flights`
* `weather`
* `planes`
* `airports`
* `airlines`


## Key Insights
- Of the 3,322 aircraft in the registry, 998 of them have never flown, which is 30%. 
- The highest average age of aircraft in the company - 35 years (as for 2013) in Envoy Air with 769 flights.
- Several aircraft were used by several airlines.


## How to Run This Project

1.  Clone the repository:
    ```bash
    git clone [https://github.com/AliaksandrTrasko/joining_python_flights.git](https://github.com/AliaksandrTrasko/joining_python_flights.git)
    ```

2.  Navigate to the project directory:
    ```bash
    cd joining_python_flights
    ```

3.  (Recommended) Create and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv\Scripts\activate  # On MacOS: venv/bin/activate
    ```

4.  Install the required libraries:
    ```bash
    pip install pandas matplotlib seaborn jupyterlab
    ```

5.  Launch Jupyter Lab:
    ```bash
    jupyter lab
    ```
6.  Open the `.ipynb` notebooks to view and run the analysis.