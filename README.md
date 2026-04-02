# Exploratory Data Analysis on Edmonton Restaurant Market

## Executive Summary
Restaurant ratings and online visibility play a critical role in attracting customers, yet many restaurants lack clear insights into what drives higher ratings in a competitive market like Edmonton.

Using **Python (Pandas, NumPy, BeautifulSoup)** and **Google Places API**, I built a dataset of local restaurants and developed an analytical workflow to uncover the key factors influencing customer ratings and discoverability.

After identifying that review counts, price range, and cuisine type are the strongest drivers of restaurant ratings, I recommend that restaurant owners and marketers focus on the following strategies to improve performance:

- Increase customer review volume through post-visit prompts and engagement strategies.
- Optimize pricing to align with perceived value rather than competing solely on low price.
- Focus on high-demand cuisine categories or differentiate within saturated segments.

## Business Problem
Customer ratings and review visibility are critical to restaurant success, as they directly influence customer acquisition and revenue.
However, many Edmonton restaurants lack data-driven insights into what factors most impact ratings and discoverability.

This creates a challenge for restaurant owners trying to make informed decisions about pricing, positioning, and customer engagement.

How can restaurants identify the key drivers of higher ratings and optimize their positioning to attract more customers?

## Methodology
1. Built data pipeline using **BeautifulSoup** and **Google Places API** to scrape and aggregate restaurant data (`01_get_postal_codes.ipynb` and `02_get_restaurant_data.ipynb`)
2. Leveraged **Pandas** and **NumPy** to clean inconsistent API responses, handle missing values, and transform data for further analysis (`03_data_cleaning.ipynb`)
3. Conducted Exploratory Data Analysis (EDA) using Matplotlib and Seaborn to identify spatial distributions, price-performance correlations, and customer engagement trends (`04_exploratory_data_analysis.ipynb`)


## Skills
- **Data Collection**: BeautifulSoup, Google Places API
- **Data Cleaning & Transformation**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Tools**: Jupyter Notebook

## Results & Business Recommendation
This analysis uncovers the key drivers behind restaurant ratings and provides actionable insights to improve customer acquisition and competitive positioning in the Edmonton market.

Key findings show that:
- Restaurants with higher review volumes consistently achieve stronger ratings, indicating that **social proof is a major factor influencing customer decisions**
- Mid-priced restaurants tend to receive higher ratings than low-priced options, suggesting that customers **value quality and experience over simply low cost**
- Certain cuisine categories outperform others in average ratings, highlighting **clear differences in customer demand across segments**

To improve ratings, visibility, and ultimately revenue, restaurants should focus on:
- **Increasing review volume**: <br/>
Implement post-visit prompts, QR codes, or follow-up messages to encourage satisfied customers to leave reviews.
- **Optimizing pricing strategy**: <br/>
Position offerings to reflect strong value perception rather than competing purely on low price.
- **Leveraging high-demand segments**: <br/>
Align menu offerings with popular cuisine trends or differentiate within competitive categories.
- **Enhancing customer experience**: <br/>
Focus on service quality and consistency to naturally drive higher ratings and repeat visits.

By increasing review volume and improving perceived value, restaurants can achieve higher ratings and better placement on platforms like Google Maps. This can lead to increased visibility, higher customer traffic, and sustained revenue growth.

## API Configuration
This project retrieves restaurant data using [Google Places API](https://developers.google.com/maps/documentation/places/web-service). To run [02_get_restaurant_data.ipynb](02_get_restaurant_data.ipynb), you must obtain your own API key:
1. Optain an API key from the [Google Cloud Console](https://console.cloud.google.com).
2. Create an `.env` file in the root directory.
3. Add your credentials in the following format:
   ```
   API_KEY=your_api_key_here
   ```