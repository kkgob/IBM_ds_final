# IBM_ds_final – IBM Data Science Final Project
This is the repo for Applied Data Science Capstone Project.

# SpaceX Falcon 9 Landing Prediction 

This project aims to analyze the Falcon 9 launch history from SpaceX to uncover patterns and build a machine learning model that predicts whether the first stage will successfully land. The success of the first-stage landing significantly affects the cost-efficiency of launches, making it a critical aspect for analysis.

Using a complete data science pipeline—data collection, wrangling, EDA, visualization, interactive mapping, dashboarding, and machine learning—this project showcases the practical application of various tools and techniques in the IBM Data Science certification track.

---

## 📁 Project Structure
IBM_ds_final/
├── parts_before_dash/
│   ├── spacex-data-collection-api.ipynb
│   ├── webscraping.ipynb
│   ├── Data wrangling.ipynb
│   ├── edadataviz.ipynb
│   ├── eda-sql-coursera_sqllite.ipynb
│   ├── lab_jupyter_launch_site_location.ipynb
├── dash/
│   └── App files for Plotly Dash dashboard
├── SpaceX_Machine Learning_Prediction_Part_5.ipynb
├── final_report.pdf

---

## 🔍 Project Goals

- Identify features that influence the success of Falcon 9 first-stage landings
- Explore the relationships between payload mass, launch site, orbit type, and outcome
- Create interactive visuals and maps to aid understanding
- Build a machine learning classifier to predict landing success

---

## 🧪 Methodology

### 🛰️ Data Collection

- **API**: Fetched launch data from [SpaceX API v4](https://api.spacexdata.com/v4)  
  → [`spacex-data-collection-api.ipynb`](parts_before_dash/spacex-data-collection-api.ipynb)

- **Web Scraping**: Scraped Falcon 9 launch table from Wikipedia  
  → [`webscraping.ipynb`](parts_before_dash/webscraping.ipynb)

---

### 🧹 Data Wrangling

- Merged API and scraped datasets
- Created `landing_success` labels (True/False)
- Cleaned and normalized data  
  → [`Data wrangling.ipynb`](parts_before_dash/Data%20wrangling.ipynb)

---

### 📊 Exploratory Data Analysis (EDA)

- **Visual EDA**:
  - Flight number vs Launch Site
  - Payload vs Launch Site
  - Orbit type vs Success rate
  - Launch success trend over time  
  → [`edadataviz.ipynb`](parts_before_dash/edadataviz.ipynb)

- **SQL EDA**:
  - Payload totals by agency/booster
  - Mission outcomes and landing success rates
  - Top boosters and failed missions  
  → [`eda-sql-coursera_sqllite.ipynb`](parts_before_dash/eda-sql-coursera_sqllite.ipynb)

---

### 🗺️ Interactive Map with Folium

- Displayed all US launch site locations
- Overlaid labels, distances to highways, and clusters  
  → [`lab_jupyter_launch_site_location.ipynb`](parts_before_dash/lab_jupyter_launch_site_location.ipynb)

---

### 📈 Interactive Dashboard with Dash

- **Widgets and Filters**:
  - Launch Site selection
  - Payload mass range slider
- **Visuals**:
  - Pie charts of success rates
  - Scatter plots of payload vs outcome  
  → [`dash/`](dash/)

---

### 🤖 Machine Learning

- Models: Logistic Regression, SVM, Decision Tree
- Process: Normalize → Train/Test split → Fit → Evaluate
- **Best Model**: Decision Tree (Accuracy: **89%**)  
  → [`SpaceX_Machine Learning_Prediction_Part_5.ipynb`](SpaceX_Machine%20Learning%20Prediction_Part_5.ipynb)

---

## 📌 Key Insights

- **Orbit**: SSO, GEO, and ES-L1 had 100% success. GTO had the lowest.
- **Launch Site**: KSC LC 39A and CCAFS SLC 40 were the most successful.
- **Payload**: Higher payloads were generally more successful in LEO, ISS, and Polar orbits.
- **Trend**: Landing success rates have improved steadily over the years.

---

## 📎 Assets

- 📄 [Final Report PDF](final_report.pdf)
- 📓 Jupyter notebooks (all steps)
- 📊 SQL queries and visualizations
- 📍 Folium maps and Dash app

---

## 🛠️ Technologies Used

- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- SQL (SQLite)
- Folium (Mapping)
- Plotly Dash (Web App)
- BeautifulSoup (Web Scraping)
- SpaceX REST API v4
- Jupyter Notebooks

---

## 📚 References

- [SpaceX REST API](https://api.spacexdata.com/v4)
- [Wikipedia: Falcon 9 Launches](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)

---

## 🤝 Acknowledgements

This project was developed as part of the **IBM Data Science Capstone Project** on Coursera.

---
