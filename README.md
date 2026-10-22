# Track Your Money

A single-file web app. No installs, no server, no internet needed.

## Run it
track-your-money-nu.vercel.app

## Use it
1. Click **Try with sample data** to see a demo, or drop your own bank/UPI statement **CSV**.
2. Pick a month, read the insights, fix any wrong category in the table.
3. **Download categorized CSV** to save the result.

Your data never leaves the browser. Category fixes are remembered in the browser's local storage.

## Getting a CSV from your bank
Download the statement from net banking. If it is Excel, open it and use Save As → CSV.
Supported layouts: separate Debit/Credit columns, one Amount column (negative = spent),
or Amount + Dr/Cr column. Dates like 25/12/2025, 2025-12-25, 25-Dec-2025.
If income shows up as spending, tick **Swap debit/credit**.

## Add transactions by hand
Spent cash on chai or an auto? Use **Add a transaction by hand** (above the transactions table).
Pick the date, what it was for, the amount and whether you spent or received it. Category is
auto-detected unless you choose one. Entries are saved in your browser, work with or without a CSV,
show a small "manual" tag, and can be deleted with the ✕ button. To start a new month fresh, click **Clear all my manual entries** (it asks first, so download your PDF report before clearing).

## PDF report
Click **Download PDF report**. In the print window choose **Save as PDF** as the destination.
The report covers the month (or all time) selected in the Period dropdown and includes the totals,
chart, insights, category breakdown, recurring payments and top spends. The transaction list is left out
to keep it short.

## What it does
- Auto-categorizes transactions by keywords (Swiggy, Zomato, Uber, Amazon, Netflix, Jio, rent, salary...)
- Income vs spending chart, category donut, top merchants, biggest one-off expenses
- Detects recurring payments (rent, subscriptions, bills)
- Plain-language insights: savings rate, month-on-month change, food-delivery habit

## Change the categories
Edit `SPEND_RULES` and `INCOME_RULES` near the top of the `<script>` in `index.html`.
