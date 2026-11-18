# Project Documentation - E-commerce Sales Analysis

## 1. Objective
Analyse 100 orders from Jan-Dec 2025 to measure sales and profit, find best-selling and most profitable products, understand monthly trends and recommend actions.

## 2. Dataset (fictional, 100 rows)
| Column | Meaning | Type |
|---|---|---|
| Order ID, Order Date | ORD1001 - ORD1100, date of order | Input |
| Customer Name, City | Buyer and delivery city (8 cities) | Input |
| Category, Product | 4 categories, 12 products | Input |
| Quantity, Unit Price, Unit Cost | Units sold, selling price, cost to the store (INR) | Input |
| Discount % | 0, 5, 10 or 15% | Input |
| Payment Method | UPI, Credit Card, Debit Card, Cash on Delivery, Net Banking | Input |
| Month No / Month | From the date | **Formula** `=MONTH(B2)`, `=CHOOSE(...)` |
| Sales | Quantity x Price x (1 - Discount) | **Formula** |
| Total Cost | Quantity x Unit Cost | **Formula** |
| Profit | Sales - Total Cost | **Formula** |
| Profit Margin | Profit / Sales | **Formula** |

Assumption: cost price is not discounted - only the selling price is.

## 3. Step-by-step (simple language)
1. **Create the data** - 100 orders across 12 months with a festive-season (Oct-Dec) peak.
2. **Check the data** - no blanks, valid dates, positive quantities, discounts between 0 and 15%.
3. **Add calculated columns** - Month, Sales, Cost, Profit, Margin using formulas.
4. **KPIs** - Total Sales, Profit, Orders, Units, Average Order Value (= Sales / Orders), Margin.
5. **Monthly trend** - SUMIF by month number plus month-on-month growth.
6. **Product performance** - sales, units and profit per product; rank with RANK.
7. **Category, city and payment analysis** - SUMIF and COUNTIF tables.
8. **Top 5 / Bottom 3 lists** - rank + INDEX/MATCH.
9. **Reconciliation check** - monthly, product and category totals all equal the main total (cell shows "Check OK").
10. **Dashboard** - 6 KPI cards and 6 charts.
11. **Practise real PivotTables** with the Pivot_Guide sheet.

## 4. Results
**KPIs:** Sales INR 350,654 | Cost INR 224,280 | Profit INR 126,374 | Margin 36.0% | Orders 100 | Units 178 | Average order value INR 3,507 | Average discount 6.1%

**Monthly trend**
| Month | Orders | Units | Sales | Profit | Margin | MoM growth |
|---|---|---|---|---|---|---|
| Jan | 5 | 8 | 12,517 | 5,557 | 44.4% | nan% |
| Feb | 5 | 10 | 20,601 | 6,301 | 30.6% | 64.6% |
| Mar | 7 | 13 | 18,838 | 7,838 | 41.6% | -8.6% |
| Apr | 7 | 16 | 20,301 | 7,451 | 36.7% | 7.8% |
| May | 7 | 11 | 29,010 | 10,010 | 34.5% | 42.9% |
| Jun | 7 | 11 | 32,725 | 10,625 | 32.5% | 12.8% |
| Jul | 8 | 14 | 34,291 | 12,641 | 36.9% | 4.8% |
| Aug | 8 | 14 | 27,827 | 9,527 | 34.2% | -18.9% |
| Sep | 9 | 17 | 19,659 | 7,599 | 38.7% | -29.4% |
| Oct | 12 | 24 | 43,973 | 15,353 | 34.9% | 123.7% |
| Nov | 13 | 19 | 43,808 | 16,258 | 37.1% | -0.4% |
| Dec | 12 | 21 | 47,105 | 17,215 | 36.5% | 7.5% |

**Products (sorted by sales)**
| Product | Category | Orders | Units | Sales | Profit | Margin |
|---|---|---|---|---|---|---|
| Air Fryer | Home & Kitchen | 7 | 12 | 68,689 | 20,689 | 30.1% |
| Mixer Grinder | Home & Kitchen | 10 | 17 | 55,459 | 18,059 | 32.6% |
| Men's Sneakers | Fashion | 11 | 15 | 42,436 | 16,936 | 39.9% |
| Wireless Earbuds | Electronics | 9 | 13 | 30,488 | 10,988 | 36.0% |
| Smart Watch | Electronics | 6 | 6 | 28,994 | 9,194 | 31.7% |
| Python Programming Book | Books | 17 | 48 | 26,356 | 11,956 | 45.4% |
| Bluetooth Speaker | Electronics | 9 | 13 | 24,488 | 8,888 | 36.3% |
| Women's Handbag | Fashion | 6 | 8 | 18,618 | 8,218 | 44.1% |
| Power Bank | Electronics | 8 | 14 | 17,536 | 7,036 | 40.1% |
| Denim Jacket | Fashion | 5 | 5 | 15,175 | 5,675 | 37.4% |
| Cookware Set | Home & Kitchen | 3 | 6 | 14,555 | 4,655 | 32.0% |
| Self-Help Bestseller | Books | 9 | 21 | 7,860 | 4,080 | 51.9% |

**Categories**
| Category | Orders | Sales | Profit | Margin | % of sales |
|---|---|---|---|---|---|
| Electronics | 32 | 101,506 | 36,106 | 35.6% | 28.9% |
| Fashion | 22 | 76,229 | 30,829 | 40.4% | 21.7% |
| Home & Kitchen | 20 | 138,702 | 43,402 | 31.3% | 39.6% |
| Books | 26 | 34,216 | 16,036 | 46.9% | 9.8% |

**Cities**
| City | Orders | Sales | % of sales |
|---|---|---|---|
| Hyderabad | 16 | 77,138 | 22.0% |
| Bengaluru | 21 | 60,775 | 17.3% |
| Chennai | 11 | 50,392 | 14.4% |
| Delhi | 13 | 44,626 | 12.7% |
| Mumbai | 14 | 40,303 | 11.5% |
| Kolkata | 11 | 34,516 | 9.8% |
| Pune | 8 | 26,158 | 7.5% |
| Noida | 6 | 16,747 | 4.8% |

**Payment methods**
| Method | Orders | % of orders |
|---|---|---|
| UPI | 40 | 40% |
| Credit Card | 21 | 21% |
| Debit Card | 16 | 16% |
| Cash on Delivery | 17 | 17% |
| Net Banking | 6 | 6% |

## 5. Business insights
1. **Sales and profit:** the store earned INR 350,654 in sales and INR 126,374 in profit, a **36.0% margin**; average order value was INR 3,507.
2. **Top products by sales:** Air Fryer (68,689), Mixer Grinder (55,459), Men's Sneakers (42,436), Wireless Earbuds (30,488), Smart Watch (28,994). **Air Fryer** is the top earner.
3. **Best-selling by units:** Python Programming Book (48 units), Self-Help Bestseller (21 units), Mixer Grinder (17 units), Men's Sneakers (15 units), Power Bank (14 units). Cheap items sell in volume but earn little revenue - **Python Programming Book** has the most units but only rank 6 by sales.
4. **Seasonality:** Dec was the best month (INR 47,105); Jan was the weakest (INR 12,517). Just three months (Oct-Dec) delivered 38% of annual sales (37 of 100 orders) - as much as the six months Jan-Jun (38%) - so the average month in Oct-Dec sold about INR 44,962 vs INR 22,332 in Jan-Jun.
5. **Category:** Home & Kitchen generates the most sales (40%) but has the lowest margin (31.3% for Home & Kitchen); Books has the best margin (46.9%).
6. **Product margins:** Self-Help Bestseller has the highest margin (51.9%); Air Fryer has the lowest (30.1%).
7. **Weakest products:** Self-Help Bestseller (7,860) and Cookware Set (14,555) have the lowest sales.
8. **Geography:** Hyderabad is the top city (22% of sales); Noida is the lowest (5%).
9. **Payments:** UPI is the most-used method (40% of orders).
10. **Discounts:** 40 of 100 orders carried a 10-15% discount; discounting is heaviest in Oct-Nov.

## 6. Recommendations
- Stock up and plan campaigns before **October** - the peak quarter.
- Promote high-margin items (books, handbags) and bundle them with expensive products.
- Review discounts on low-margin products such as Air Fryer.
- Increase marketing in low-sales cities (Noida) and keep UPI checkout smooth.
- Bundle the lowest-revenue items (Self-Help Bestseller, Cookware Set) with popular products to lift basket size.

## 7. Limitations
- Fictional dataset with only 100 orders from a single year; monthly differences can be due to chance.
- Returns, shipping cost and taxes are not included.
