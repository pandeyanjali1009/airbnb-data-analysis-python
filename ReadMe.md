# 🏠 Airbnb NYC Data Analysis (Python EDA)

Exploratory Data Analysis on ~49,000 New York City Airbnb listings to understand where listings are concentrated, how prices differ by area and room type, who the biggest hosts are, and how availability and minimum-stay rules shape the market.

## 📌 Problem Statement
Which areas have the most listings, where are prices highest, which room types dominate, and how do hosts, availability and minimum-night rules affect the market?

## 📂 Dataset
- **Source:** [Kaggle – New York City Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data)
- **File:** `AB_NYC_2019.csv` (48,895 rows, 16 columns)

## 🛠️ Tools
Python · Pandas · NumPy · Matplotlib · Seaborn · Google Colab

## 🧹 Data Cleaning
- Filled missing `reviews_per_month` with 0 (listings with no reviews yet)
- Filled missing `name` / `host_name` with "Unknown"; converted `last_review` to datetime
- Removed duplicates and listings with `price = 0`
- Capped extreme outliers at the 99th percentile of price ($799)
- **Final clean dataset: 48,410 listings**

## 📊 Key Insights
1. **Supply is concentrated in two boroughs.** Manhattan (21,312) and Brooklyn (19,992) hold about 85% of all listings. Queens has 5,650, Bronx 1,087 and Staten Island only 369.
2. **Manhattan is the most expensive borough.** Bronx and Queens are the cheapest, so price follows location more than volume.
3. **Entire homes earn the most.** Average nightly price: Entire home/apt **$189.10**, Private room **$83.39**, Shared room **$64.20**. A whole apartment costs more than 2x a private room.
4. **Premium Manhattan pockets.** Most expensive neighbourhoods (min. 30 listings): Tribeca ($295.65), NoHo ($276.25), Flatiron District ($258.16), Midtown ($255.75), SoHo ($229.83).
5. **Busiest neighbourhoods are in Brooklyn.** Williamsburg (3,904) and Bedford-Stuyvesant (3,694) lead, followed by Harlem (2,645) and Bushwick (2,458).
6. **Professional operators exist.** Sonder (NYC) has 327 listings, Blueground 232 and Corporate Housing 91. Sonder appears under two host IDs (327 + 96), so the real total is higher. These are companies, not individual hosts.
7. **More availability, higher price (up to a point).** Average price rises from $125 (0 days available) to $159 (181-270 days), then dips slightly to $153 for 271-365 days.
8. **Most stays are short.** Median minimum stay is 3 nights, but 718 listings require 30+ nights and 14 require more than a year, which behave like long-term rentals.
9. **Price has weak correlation with numeric features.** Highest are listings count per host (0.15) and availability (0.11). Price depends mainly on location and room type.

## 💡 Recommendations
- Expand supply in under-served boroughs (Queens, Bronx) where prices are lower but demand may exist.
- Promote entire-home listings in premium Manhattan areas for higher revenue.
- Tag 30+ night listings as monthly rentals so tourists are not confused.
- Monitor large operators (Sonder, Blueground) as they hold a big share of inventory.

## 🖼️ Screenshots
<img width="1130" height="550" alt="chart1_listings_by_borough" src="https://github.com/user-attachments/assets/927efc35-cba1-4a80-bddd-8650f38d3e9a" />
<img width="1100" height="580" alt="chart2_price_by_room_type" src="https://github.com/user-attachments/assets/0f9e654f-0895-43de-9bca-20e2f1956102" />
<img width="1100" height="680" alt="chart3_price_spread_boxplot" src="https://github.com/user-attachments/assets/1dd58986-250f-4764-9b13-ac8c4eab0344" />
<img width="1090" height="900" alt="chart4_price_map_nyc" src="https://github.com/user-attachments/assets/12530174-46e4-4747-acf2-f7ae422e4046" />

## ▶️ How to Run
1. Download `AB_NYC_2019.csv` from Kaggle
2. Open `Airbnb_NYC_EDA.ipynb` in Google Colab (File → Upload notebook)
3. Upload the CSV and run all cells from top to bottom

## 👩‍💻 Author
**Anjali Pandey** — B.Sc IT student | Python & Machine Learning
