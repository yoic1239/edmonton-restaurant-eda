# Edmonton Restaurant Exploratory Data Analysis

## Project Overview
This project analyzes restaurant data in Edmonton using Google Maps data (acquired from Places API) to explore patterns in ratings, popularity, pricing, operating hours, and neighborhood distribution.

## Data Pipeline
1. Postal code collection (`01_get_postal_codes.ipynb`)
2. Restaurant data collection (`02_get_restaurant_data.ipynb`)
3. Data cleaning and feature engineering (`03_data_cleaning.ipynb`)
4. Exploratory data analysis (`04_exploratory_data_analysis.ipynb`)

## Key Questions
- Distribution of restaurant ratings across Edmonton.
- Concentration of user reviews among restaurants.
- Differences in popularity and performance across restaurant types.
- Relationship between operating hours, weekend availability, and ratings.
- Location-level differences in restaurant density and ratings.
- Relationship between price level, ratings, and user engagement.

## Key Insights
- Restaurant ratings show a strong positive bias, with more than 60% ratings above 4.0.
- Review counts are highly skewed, indicating popularity concentration.
- Higher-priced restaurants tend to receive higher ratings and more engagement.
- Operating hours show little correlation with ratings.

## Limitations
- Ratings may exhibit positive bias, as users are more likely to leave reviews after positive experiences.
- User rating count reflects engagement rather than true customer volume.
- Observed relationships are descriptive and do not imply causation.

## Tools Used
- Python (Pandas, NumPy)
- Google Places API
- Beautiful Soup
- Matplotlib / Seaborn
- Jupyter Notebook

## API Configuration
This project retrieves restaurant data using [Google Places API](https://developers.google.com/maps/documentation/places/web-service). To run [02_get_restaurant_data.ipynb](02_get_restaurant_data.ipynb), you must obtain your own API key:
1. Optain an API key from the [Google Cloud Console](https://console.cloud.google.com).
2. Create an `.env` file in the root directory.
3. Add your credentials in the following format:
   ```
   API_KEY=your_api_key_here
   ```