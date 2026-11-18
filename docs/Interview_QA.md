# Interview Questions & Answers - E-commerce Sales Analysis

**Q1. Explain this project in 30 seconds.**
I analysed 100 online orders for 2025 in Excel. I calculated sales, cost and profit with formulas, built summary tables and a dashboard, and found total sales of INR 350,654 with a 36.0% margin, strong Oct-Dec seasonality and a big gap between best-selling and highest-revenue products.

**Q2. What is the business problem?**
The store wanted to know what sells, what earns profit, when demand peaks and where to focus marketing.

**Q3. Where did the data come from?**
It is a fictional dataset created for practice. In a real company it would be exported from the order management system or Shopify/Amazon seller reports.

**Q4. How is Sales calculated?**
`=Quantity*UnitPrice*(1-Discount)`. Profit = Sales - (Quantity x UnitCost).

**Q5. What is Average Order Value (AOV) and what is yours?**
AOV = Total Sales / Total Orders = INR 350,654 / 100 = INR 3,507.

**Q6. What is profit margin?**
Profit divided by Sales. Overall margin is 36.0%. Margin tells how much profit each rupee of sales produces, which is different from total profit.

**Q7. Which product is best-selling?**
By units: Python Programming Book (48 units). By sales value: Air Fryer. "Best" depends on the metric, so I report both.

**Q8. How did you find monthly trends?**
I extracted the month number with MONTH(), then used SUMIF to total sales and profit per month and added month-on-month growth. Dec was highest and sales rose strongly from October.

**Q9. What is the difference between SUM, SUMIF and a PivotTable?**
SUM adds everything; SUMIF adds only rows meeting a condition (e.g. one month); a PivotTable does many SUMIFs at once by dragging fields. I built formula summaries and documented how to make the matching PivotTables.

**Q10. How did you check that your analysis is correct?**
Monthly, product and category totals all reconcile to the grand total (INR 350,654), and the sheet shows "Check OK". I also recalculated key numbers independently.

**Q11. What recommendations would you give the business?**
Prepare stock and marketing for Oct-Dec, push high-margin items, review discounts on low-margin products, and grow low-sales cities.

**Q12. Why is the top-selling product by units not the top by revenue?**
Low-priced items such as books sell many units but each unit brings little revenue; premium items like the Air Fryer bring more revenue per unit.

**Q13. What is seasonality?**
Regular sales patterns linked to the calendar - here, festive months (Oct-Dec) have 38% of annual sales.

**Q14. What are the limitations?**
Small fictional dataset, one year, no returns/shipping/tax. Insights should be validated with real data.

**Q15. What would you add next?**
Customer-level analysis (repeat buyers), returns, forecasting, and a Power BI version of the dashboard.
