# 🪔 Diwali Sales Dashboard 2026

A state-wise festive sales dashboard with a Diwali theme, built for the **DataCliq "Skills Wali Diwali" Data Analysis Challenge 2026**.

## Business Question

Which states, categories and weeks drove Diwali sales, and where should the business act next?

## Dataset

File: `diwali_sales_data_2026.csv`

- 1,500 orders from 1 Sep 2026 to 9 Nov 2026
- 10 states: Maharashtra, Uttar Pradesh, Tamil Nadu, Delhi, Karnataka, Gujarat, West Bengal, Telangana, Rajasthan, Madhya Pradesh
- Sample dataset created for practice and dashboard design

| Column | Description |
|---|---|
| Order_ID | Unique order number |
| Order_Date | Date of the order |
| State | State of the customer |
| City_Tier | Tier 1, Tier 2 or Tier 3 |
| Category | Electronics, Jewellery, Fashion, Gifts & Hampers, Home Decor, Sweets & Dry Fruits |
| Payment_Mode | UPI, Credit Card, Debit Card, Cash on Delivery, Wallet |
| Gender | Male or Female |
| Quantity | Items in the order |
| Unit_Price | Price per item (Rs) |
| Discount_Pct | Discount given (%) |
| Sales | Final order value (Rs) |
| Rating | Customer rating (3.2 to 5.0) |

## Dashboard Features

- Filters: State, Category, Payment Mode, City Tier, with a Reset button
- KPI cards: Total Sales, Orders, Average Order Value, Average Rating
- Weekly sales trend with the pre-Diwali peak marked
- State-wise sales (click a state to filter the whole dashboard)
- Category sales, payment mode split, city tier view
- State summary table
- Insights that update with the filters

## Key Insights

1. Total sales were **Rs 108.4 lakh** from **1,500 orders**, with an average order value of **Rs 7,229**.
2. **Maharashtra** leads with **17.2%** of sales, followed by Uttar Pradesh (14.0%) and Tamil Nadu and Delhi (12.2% each).
3. **Madhya Pradesh** has the lowest sales (4.7%), which makes it a growth opportunity.
4. The week starting **3 Nov** (the run-up to Dhanteras and Diwali) brought **26.9%** of all sales.
5. **Electronics** (51.6%) and **Jewellery** (27.2%) together make up about 79% of sales.
6. **UPI** is the top payment mode with 50.5% of sales.
7. Average order value is highest in **Tamil Nadu (Rs 8,777)** and lowest in **Rajasthan (Rs 5,711)**.

## Recommendations

1. Stock up early in the top states before Dhanteras, especially Electronics and Jewellery.
2. Build gift bundles (sweets, gifts, decor) to raise average order value, since these categories are small today.
3. Run targeted offers in low-sales states such as Madhya Pradesh and Rajasthan.
4. Push UPI cashback offers, since half of the sales come through UPI.

## DAX Measures (Power BI)

```
Total Sales = SUM(Diwali[Sales])
Orders = DISTINCTCOUNT(Diwali[Order_ID])
AOV = DIVIDE([Total Sales], [Orders])
Avg Rating = AVERAGE(Diwali[Rating])
Sales Share % = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL(Diwali)))
State Rank = RANKX(ALL(Diwali[State]), [Total Sales])
```

## Repository Files

```
diwali-sales-dashboard-2026/
├── README.md
├── diwali_sales_data_2026.csv
├── diwali_sales_dashboard_2026.html   # interactive dashboard (open in a browser)
└── screenshots/                       # add your dashboard images here
```

## How to View

Download `diwali_sales_dashboard_2026.html` and open it in any browser. No installation is needed.

## Tools

HTML, CSS and JavaScript (interactive dashboard) | Power BI (DAX) | Python (sample data)

## Author

**[Your Name]**
LinkedIn: [your profile link]

Made for the #DataCliq Diwali Challenge 2026 🪔 Shubh Deepavali!
