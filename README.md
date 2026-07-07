# Customer Shopping Behavior Analysis 

Hey! This is a little end-to-end data analysis project I put together to dig into how customers actually shop — what they buy, how much they spend, whether discounts and subscriptions change their behavior, and who the "loyal" customers really are.

I started with a raw CSV of customer transactions and took it all the way through SQL analysis, a Jupyter notebook for deeper exploration, and finally a Power BI dashboard so the findings are easy to look at without touching any code. There's also a PDF write-up if you just want the summary.

## What's in here

| File | What it is |
|---|---|
| `customer_shopping_behavior.csv` | The raw dataset — one row per customer transaction |
| `customer_behavior.sql` | All the SQL queries I used to answer the business questions |
| `db_dump.sql` | A database dump of the same data, in case you'd rather load it straight into Postgres/MySQL instead of the CSV |
| `Customer_Shopping_Behavior_Analysis.ipynb` | Jupyter notebook with the exploratory analysis |
| `Customer_Behavior_Dashboard.pbix` | Power BI dashboard — open this in Power BI Desktop for the visual, interactive version |
| `Customer Shopping Behavior Analysis.pdf` | A written report summarizing the findings |

## What I was actually trying to figure out

Rather than just poking around aimlessly, I framed the analysis around a set of real business questions:

1. **Who spends more — men or women?** Total revenue by gender.
2. **Do discounts actually work?** Which customers used a discount but still spent above the average purchase amount?
3. **What are people rating highly?** Top 5 products by average review rating.
4. **Does shipping speed matter?** Comparing average spend between Standard vs. Express shipping.
5. **Are subscribers better customers?** Comparing spend and total revenue between subscribers and non-subscribers.
6. **Where are discounts working hardest?** The 5 products with the highest share of discounted purchases.
7. **Who are the loyal customers?** Segmenting everyone into New, Returning, and Loyal buckets based on purchase history, then counting each group.
8. **What sells best in each category?** Top 3 most-purchased items within every product category.
9. **Do repeat buyers subscribe more?** Looking at whether customers with 5+ past purchases are more likely to be subscribed.
10. **Which age group brings in the most money?** Revenue broken down by age group.

If you open `customer_behavior.sql`, you'll find each of these written out as its own commented query, so it's easy to follow along or reuse them on your own dataset.

## How to actually use this

**Just want the takeaways?** Open the PDF report — it's the quickest way to see what the data says without digging through code.

**Want the interactive version?** Open `Customer_Behavior_Dashboard.pbix` in Power BI Desktop (free download from Microsoft) and click around the visuals yourself.

**Want to run the analysis yourself?**
1. Load `customer_shopping_behavior.csv` into a SQL database (or just restore `db_dump.sql` directly), making sure the table is named `customer`.
2. Run the queries in `customer_behavior.sql` — they're plain, standard SQL and should work in Postgres, MySQL, or anywhere similar with maybe a tiny tweak here or there.
3. Open the Jupyter notebook if you want to see the exploratory side — charts, summary stats, and the messier "let me poke at this" kind of analysis that doesn't always make it into a polished report.

## A note on the data

Each row represents a single customer purchase, with fields like gender, item purchased, category, purchase amount, review rating, subscription status, discount applied, shipping type, previous purchases, and age group. It's a nice, clean dataset to practice SQL analytics, customer segmentation, and dashboarding on — feel free to reuse the queries or dashboard structure for your own retail/e-commerce data.

## Why I built this

Mostly to practice going from raw data → SQL insights → a notebook → an actual dashboard, the same way you'd do it in a real analytics role. It touches a bit of everything: querying, segmentation logic, reporting, and visualization, all on one dataset.

---

Feel free to fork this, tweak the queries, or point the dashboard at your own data. If you spot something worth improving, PRs are always welcome!
