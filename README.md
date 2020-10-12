# Portfolio-Analysis using Python, Pandas, Motecarlo Simulations and PLAID API

_Note__: The data produced from the api calls will vary depending on the dates used, causing results that vary from those pictured.

### Budget Analysis

We will use the Plaid API to obtain transaction and account data for the budget analysis section of the report.

Follow the steps outlined in the budget starter notebook (`account_summary.ipynb`) to complete the following:

1. Generate a Plaid access token to access the Developer Sandbox.

2. Use the Access token to fetch account transactions from the sandbox. You should fetch the last 90 days of transactions from the sandbox using the following institution:

    ```python
    INSTITUTION_ID = "ins_109508"
    ```

3. Perform basic budget analysis on the sandbox transaction and generate the following plots:

    * Spending Categories Pie Chart.

      ![Expenses per category](Images/spending-pie.png)

    * Spending Per Month Bar Chart.

      ![Expenses per month](Images/spending-month.png)

4. Use the API to fetch income data from the sandbox and print the following:

* Last Year's Income Before Tax.

* Current Monthly Income.

* Projected Year's Income Before Tax.

### Retirement Planner

In this section, we will use the Alpaca API to fetch historical closing prices for a retirement portfolio and then run Monte Carlo simulations to project the portfolio performance at `30` years. You will then use the Monte Carlo data to answer questions about the portfolio.

Follow the steps outlined in the budget starter notebook to complete the following:

#### Monte Carlo Simulation

Create a Monte Carlo simulation for the retirement portfolio:

1. Use the Alpaca API to fetch historical closing prices for a traditional 60/40 portfolio using the `SPY` and `AGG` tickers to represent the `60%` stocks (`SPY`) and `40%` bonds (`AGG`).

2. Run a Monte Carlo Simulation of `500` runs and `30` years for the `60/40` portfolio and plot the results.

    ![monte carlo](Images/monte-carlo.png)

3. Select the ending cumulative returns from the Monte Carlo simulation and calculate the interval values for a `90`% confidence interval.

4. Using the ending cumulative returns, plot a histogram of the results and plot the `90%` confidence interval as vertical lines on the histogram.

    ![histogram](Images/histogram.png)
