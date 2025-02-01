# Map Improvements in Hyundai Vehicles (Map Comparison)

## Overview
Modern automotive infotainment systems rely on **accurate and up-to-date mapping services** to enhance user experience. However, inconsistencies in Points of Interest (POI) data across different platforms pose challenges in providing **reliable navigation and EV charging station recommendations**. This project aimed to **automate the comparison of POI data** from multiple mapping services to improve Hyundai’s OEM infotainment system accuracy.
Modern automotive infotainment systems rely on **accurate and up-to-date mapping services** to enhance user experience. However, inconsistencies in Points of Interest (POI) data across different platforms pose challenges in providing **reliable navigation and EV charging station recommendations**. This project aimed to **automate the comparison of POI data** from multiple mapping services to improve Hyundai’s infotainment system accuracy.

## Problem Statement
- Mapping services such as **Google Maps, HERE Maps, and Mappls** provide different POI datasets, leading to inconsistencies.
- Google Maps is considered as the reference standard, and data from HERE Maps and Mappls is compared against it to identify discrepancies.
- Manual comparison and validation of POI data across platforms was time-consuming and inefficient.
- With the rise of **EV adoption**, ensuring the availability and accuracy of **EV charging station** data is critical.
- A scalable and automated solution was needed to **cross-verify and optimize mapping data integration**.
- Mapping services such as **Google Maps, HERE Maps, and Mappls** provide different POI datasets, leading to inconsistencies.
- Manual comparison and validation of POI data across platforms was time-consuming and inefficient.
- With the rise of **EV adoption**, ensuring the availability and accuracy of **EV charging station** data is critical.
- A scalable and automated solution was needed to **cross-verify and optimize mapping data integration**.

## System Architecture
The system architecture consists of the following key components:
1. **Data Collection Module** – Uses web scraping tools (**Selenium, BeautifulSoup, Requests**) to extract POI data from multiple sources.
2. **Data Processing & Storage** – Stores and processes data in **AWS S3 and Elastic Search**, ensuring fast retrieval and indexing.
3. **Comparison & Analysis Engine** – Implements Python-based algorithms to compare attributes such as **location coordinates, phone numbers, timings, amenities, and service charges**.
4. **Visualization & Reporting** – Uses **Kibana dashboards** for easy analysis and reporting of inconsistencies.

## Technologies Used
- **Programming & Scraping:** Python, Selenium, Requests, XPath, CSS, BeautifulSoup
- **Backend & Data Processing:** Django, JSON, CSV, Excel
- **Cloud & Data Storage:** AWS S3, Elastic Search, Kibana

## Key Features
- **Automated Data Extraction:** Gathers POI data from **Google Maps (reference), HERE Maps, and Mappls**.
- **Scalable Data Comparison System:** Compares **EV charging stations** across multiple platforms using Google Maps as the standard.
- **Infotainment System Enhancement:** Improves map accuracy for **OEM navigation, route planning, and POI recommendations**.
- **Real-Time Data Visualization:** Uses **Kibana dashboards** for **data validation and reporting**.
- **Automated Data Extraction:** Gathers POI data from **Google Maps, HERE Maps, and Mappls**.
- **Scalable Data Comparison System:** Compares **EV charging stations** across multiple platforms.
- **Infotainment System Enhancement:** Improves map accuracy for **OEM navigation, route planning, and POI recommendations**.
- **Real-Time Data Visualization:** Uses **Kibana dashboards** for **data validation and reporting**.
- **Automated Data Extraction:** Gathers POI data from **Google Maps, HERE Maps, and Mappls**.
- **Scalable Data Comparison System:** Compares **EV charging stations** across multiple platforms.
- **Infotainment System Enhancement:** Improves map accuracy for **navigation, route planning, and POI recommendations**.
- **Real-Time Data Visualization:** Uses **Kibana dashboards** for **data validation and reporting**.

## Key Projects & Use Cases
- **EV Charging Station Comparison:** Cross-validates data from **Google Maps, Mappls, and EV Yatra** to improve Hyundai’s EV ecosystem.
- **Infotainment System Optimization:** Automates POI data validation, **reducing manual workload** for infotainment engineers.
- **City-Wide POI Analytics:** Enables comparison of **restaurants, gas stations, and service centers** to enhance Hyundai’s in-car navigation.

## Workflow (Pseudocode)
```python
# Step 1: Scrape POI Data
poi_data_google = scrape_google_maps()
poi_data_here = scrape_here_maps()
poi_data_mappls = scrape_mappls()

# Step 2: Preprocess Data
def preprocess_data(data):
    data = remove_duplicates(data)
    data = normalize_location_coordinates(data)
    return data

processed_google = preprocess_data(poi_data_google)
processed_here = preprocess_data(poi_data_here)
processed_mappls = preprocess_data(poi_data_mappls)

# Step 3: Compare POI Data
def compare_poi_data(google, here, mappls):
    comparison_results = []
    for poi in google:
        match_here = find_closest_match(poi, here)
        match_mappls = find_closest_match(poi, mappls)
        comparison_results.append((poi, match_here, match_mappls))
    return comparison_results

comparison_output = compare_poi_data(processed_google, processed_here, processed_mappls)

# Step 4: Store and Visualize Results
store_to_elastic_search(comparison_output)
visualize_with_kibana(comparison_output)
```

## Impact & Achievements
- **Reduced Manual Effort:** Automated POI validation, cutting down manual comparison time from **weeks to hours**.
- **Improved Data Accuracy:** Ensured **consistent and accurate** infotainment recommendations across Hyundai vehicles.
- **Enhanced EV Charging Infrastructure:** Improved the integration of **EV station data**, benefiting Hyundai’s electric vehicle ecosystem.
- **Scalability & Future Adoption:** The system was recognized as a **scalable solution** for ongoing mapping enhancements.

## Future Enhancements
- **Integration with Real-Time APIs:** Implement real-time **Google Maps & HERE API calls** for instant data updates.
- **Crowdsourced POI Validation:** Enable Hyundai users to **report inaccuracies and suggest corrections**.
- **Expansion to Other Infotainment Features:** Extend the project to include **live traffic data & route optimization**.

## Conclusion
The **Map Improvements in Hyundai Vehicles (Map Comparison)** project successfully automated POI data validation, significantly improving Hyundai’s **infotainment system accuracy**. By leveraging **AI, web scraping, and cloud technologies**, the system enhanced **EV charging infrastructure, navigation precision, and user experience**.
