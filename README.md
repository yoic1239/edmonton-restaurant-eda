# Edmonton Restaurant Exploratory Data Analysis

## Project Overview
This project performs an end-to-end exploratory data analysis on restaurant data in Edmonton, with the goal of understanding how ratings, pricing, and location relate to restaurant popularity and customer engagement.

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
- Restaurant ratings show a strong positive bias, with more than 60% ratings above 4.0. This suggests that user-generated ratings may reflect selective reviewing behavior rather than a balanced assessment of overall quality.
- User rating counts are highly concentrated among a small subset of restaurants, with the majority receiving relatively few reviews. This indicates that restaurant visibility and popularity are unevenly distributed, and review count may be driven more by exposure than by quality alone.
- Restaurant type shows meaningful differences in both prevalence and performance. Fast or casual dining and Western cuisine dominate in volume, while less common categories such as “other cuisine” tend to achieve higher average ratings, suggesting potential niche advantages.
- Price level is positively associated with both ratings and user engagement, as higher-priced restaurants generally receive more reviews and slightly higher ratings. This may reflect higher customer expectations, branding effects, or greater motivation to leave feedback.
- Operating hours and weekend availability show little to no observable relationship with restaurant ratings, indicating that longer opening hours alone do not translate into higher perceived quality.
- Neighborhood-level analysis reveals disparities in restaurant density, with certain areas hosting a large number of restaurants but not necessarily achieving higher average ratings. This suggests that higher competition does not automatically lead to better customer experiences.

## Practical Implications
- For new or small restaurant owners, early visibility is critical, as customer engagement (measured by review count) is highly skewed toward a small number of popular restaurants. Strategies such as promotional campaigns or platform optimization may be more impactful than incremental quality improvements alone.
- Pricing strategy appears to influence customer engagement more than perceived quality, as higher-priced restaurants tend to attract more reviews but only slightly higher ratings. This suggests that pricing may shape customer expectations and willingness to provide feedback rather than guarantee superior experiences.
- Restaurant operators should not assume that longer operating hours lead to higher ratings, as no clear relationship was observed between opening hours, weekend availability, and customer ratings. Operational decisions should prioritize efficiency and consistency over extended hours.
- Location selection should consider competitive density rather than rating averages alone, as neighborhoods with high restaurant density do not necessarily achieve higher ratings. Entering a saturated area may increase exposure but also intensify competition without improving perceived quality.

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