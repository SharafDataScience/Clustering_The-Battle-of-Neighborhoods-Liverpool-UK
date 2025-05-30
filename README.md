
# The Battle of Neighborhoods – Liverpool, UK

## Project Overview

This repository presents the final capstone project for the **IBM Data Science Certification** offered on **Coursera**. The project aims to analyze neighborhoods in **Liverpool, United Kingdom**, using **Foursquare API** and **Machine Learning** to uncover business insights, especially for students, and tourists.

## Author

**Abdullah Sharaf**  
Date: October 25, 2020

---

## Business Problem

Liverpool, as the financial capital of the UK and a major hub for business, tourism, and education, presents vast opportunities for new ventures. This project seeks to:
- Identify the most popular venue types across neighborhoods.
- Cluster neighborhoods based on venue similarity.
- Provide actionable insights for:
  - Entrepreneurs evaluating business locations.
  - Tourists seeking attractions and eateries.
  - Students exploring city life and opportunities.

---

## Data Collection & Preparation

Data sources and tools used:
- **Google** and **Foursquare API** to collect venue data.
- **Python libraries**: 
  - `pandas`, `BeautifulSoup` for data wrangling.
  - `geopy` to obtain geographic coordinates.
  - **Foursquare API** to retrieve JSON data on venues within 1000m radius of neighborhoods.

Processed Data Includes:
- Neighborhood names
- Latitude and longitude
- Top venue categories in each neighborhood

---

## Methodology

1. **Data Wrangling**: Extraction and cleaning using pandas and BeautifulSoup.
2. **Exploratory Data Analysis**: 
   - Identified top 5 venues per neighborhood.
   - Most common venue types include **Pub**, **Café**, **Bar**, **Hotel**, and **Coffee Shop**.
3. **Data Normalization**: One-hot encoding used to prepare data for clustering.

---

## Machine Learning – Clustering

- **Algorithm Used**: KMeans Clustering (Unsupervised ML)
- **Objective**: Segment Liverpool neighborhoods into clusters based on venue categories.
- **Number of Clusters**: 5
- **Visualization**: Clusters plotted using `Folium` on an interactive map.

### Cluster Highlights:
- **Cluster 1**: Supermarkets, restaurants, pharmacies, and grocery stores.
- **Cluster 2**: Pubs, cafes, coffee shops – ideal for leisure and social venues.
- **Cluster 3**: Unique venues like watch shops.

---

## Results & Insights

- The project provides a comprehensive overview of neighborhood characteristics.
- Entrepreneurs can use this as a guide to identify high-potential business zones.
- Tourists and students can benefit from the localized venue data for better city exploration.

---

## Conclusion

This analysis highlights Liverpool’s dynamic neighborhood ecosystem, with data-driven insights into where to open businesses or explore urban life. There's significant scope for extending this analysis with additional data layers like demographic info, foot traffic, and commercial real estate trends.

---

## Data Sources Used
1. Neighborhood Names
  Source: Google Search Results

  URL Queried:
  https://www.google.com/search?q=liverpool+neighborhoods

  ### Method Used:

  - Web scraping using requests and BeautifulSoup.

2. Neighborhood Coordinates (Latitude & Longitude)
  Source: OpenStreetMap Nominatim API

  Library Used: geopy.geocoders.Nominatim

  ### Method Used:

  -  For each neighborhood name, geocode it using Nominatim to get latitude and longitude.
3. Venue Data
  Source: Foursquare Places API

  API Endpoint:
  https://api.foursquare.com/v2/venues/explore

  Client Credentials Used:

  CLIENT_ID = 'QEB14EKSXTPMRE32ROLUDFW4TBGMS53BIPRMI1L4MX1CY3S4'

  CLIENT_SECRET = 'HYV4RFEOYQ5LHQIGNJNEFKMDSRPEIZZAPWEWIP2UKUQDQMRW'

