# CodeAlpha Data Analytics Internship — Task 2: Exploratory Data Analysis

## Overview
For this task, I carried out an exploratory data analysis (EDA) on the book dataset I collected in Task 1 (1,000 books scraped from books.toscrape.com, with Title, Price, and Rating). The goal was to understand the structure of the data, summarize it statistically, and look for patterns or relationships worth reporting — particularly whether price and rating are related.

## Questions Asked
- What is the typical price of a book in this dataset, and how spread out are prices?
- How are customer ratings distributed across the catalogue?
- Do higher-rated books tend to cost more than lower-rated ones?

## Data Structure
- **Title** — text field, unique book name
- **Price** — numeric, in GBP (£)
- **Rating** — numeric, 1 to 5 stars
- No missing values or duplicate rows were found in the cleaned dataset (1,000 rows).

## Summary Statistics

| Metric | Value |
|---|---|
| Total books analyzed | 1,000 |
| Average price | £35.07 |
| Median price | £35.98 |
| Lowest price | £10.00 |
| Highest price | £59.99 |
| Average rating | 2.92 (out of 5) |

## Analysis

### Price Distribution
A histogram of prices across ten equal buckets (£10 to £61) shows a fairly even spread, with no strong skew toward either the cheap or expensive end. Counts per bucket mostly sit between 85 and 120 books, meaning the catalogue offers a broad, balanced range of price points rather than clustering around one price tier.

### Rating Distribution
Books are spread almost evenly across the five rating levels, each holding roughly 180–230 books out of 1,000. No single rating dominates the catalogue, and 1-star books are (slightly) the most common at 226, with 4-star books the least common at 179.

### Price vs. Rating
Grouping average price by rating shows very little variation:

| Rating | Count | Average Price |
|---|---|---|
| 1 | 226 | £34.56 |
| 2 | 196 | £34.81 |
| 3 | 203 | £34.69 |
| 4 | 179 | £36.09 |
| 5 | 196 | £35.37 |
| **Total** | **1,000** | **£35.07** |

The average price stays within a narrow band (£34.56 to £36.09) across all five rating levels — a spread of under £1.60. This indicates price and rating are essentially uncorrelated in this dataset: a book's price is not a signal of how well it is rated, and vice versa.

## Key Findings
- The average book price is £35.07, with prices ranging from £10.00 to £59.99 and a median of £35.98.
- The average customer rating across the catalogue is 2.92 out of 5.
- Book prices are broadly and evenly distributed — no single price range dominates the catalogue.
- Ratings are also evenly distributed across all five star levels.
- Price shows no meaningful relationship with rating: expensive books are not rated notably higher or lower than cheap ones.

## Conclusion
The EDA confirms the Task 1 dataset is clean, balanced, and free of major structural issues. The most notable insight is the lack of correlation between price and rating — suggesting that, at least on this site, pricing is not used as a proxy for perceived quality. These findings and visualizations are included in the accompanying Excel workbook.

## Files in This Repository
- `BOOKS_CLEAN.xlsx` — cleaned dataset with pivot tables and charts (price distribution, average price by rating, books per rating)
- `README.md` — this write-up
