# NYC Taxi Trip Data Analysis & Operational Optimization

An end-to-end data analytics project that uncovers demand patterns, operational bottlenecks, pricing insights, and customer experience drivers for New York City taxi operations.  

***

## 📋 Table of Contents

1. [Project Overview](#project-overview)  
2. [Data & Tools](#data--tools)  
3. [Methodology](#methodology)  
4. [Key Findings](#key-findings)  
5. [Visual Highlights](#visual-highlights)  
6. [Recommendations](#recommendations)  
7. [Installation & Usage](#installation--usage)  
8. [Contribute & Contact](#contribute--contact)  

***

## 📝 Project Overview

This analysis leverages ~290K NYC taxi trip records to:

- Discover hourly, daily, and seasonal demand peaks  
- Identify congestion bottlenecks and slowest routes  
- Evaluate fare, surcharge, and tipping behaviors  
- Compare vendor pricing strategies  
- Propose dynamic pricing, routing, and fleet-deployment optimizations  

***

## 📊 Data & Tools

- **Data Source:** NYC Taxi and Limousine Commission (TLC) trip records merged with zone lookup  
- **Key Fields:** pickup/dropoff datetime, location IDs, trip distance, fare components, passenger count, vendor  
- **Languages & Libraries:**  
  - Python: Pandas, NumPy, GeoPandas  
  - Visualization: Matplotlib, Seaborn  
  - Jupyter Notebook for interactive exploration  

***

## 🛠 Methodology

1. **Data Preparation**  
   - Loaded raw CSVs, filtered invalid records, converted datetimes, extracted features (hour, day, month).  
   - Applied a 5% random sampling and scaled results to estimate full-population metrics.  

2. **Spatial Integration**  
   - Merged `PULocationID`/`DOLocationID` with zone names and boroughs from GeoJSON.  
   - Aggregated pickup/dropoff volumes and surcharge incidence by zone.  

3. **Feature Engineering**  
   - Computed trip duration, average speed (mph), fare per mile, tip percentage.  
   - Created categorical buckets: time-of-day, distance tiers, passenger-count groups.  

4. **Temporal & Spatial Analysis**  
   - Uncovered peak demand hours (5–7 PM), day-of-week patterns (Tue–Fri business peak), and monthly seasonality.  
   - Mapped route speeds to find congestion hotspots (25%) trips to identify service quality risks.  

***

## 🔑 Key Findings

- **Peak Demand:** Evening rush (5–7 PM) captures 13% of daily trips (~407K real trips projected).  
- **Revenue Split:** Daytime (6 AM–10 PM) accounts for 88% of revenue; nights generate 12%.  
- **Congestion Bottlenecks:** Certain cross-town Manhattan routes average 0.1 mph during rush hours.  
- **Vendor Pricing:** Vendor 2 commands a 38% premium over Vendor 1, especially on short trips (≤2 miles).  
- **Tipping Patterns:** Solo riders tip ~24%, while long, high-fare trips tip ~16%.  
- **Surcharges:** 99.9% of trips incur improvement fees; 92.3% incur congestion fees—Manhattan core vs airport/staten zones.  
- **Passenger Counts:** Outer borough zones average 1.7–2.0 passengers; Manhattan core zones average 1.2–1.3.  

***

## 🎨 Visual Highlights

- **Hourly Heatmap:** Trip volume vs. average speed revealing congestion peaks  
- **Zone Bar Charts:** Top pickup/dropoff zones by volume and passenger count  
- **Scatter Plot:** Inverse relationship between zone trip volume and average group size  
- **Line Plots:** Weekday vs weekend demand curves and tipping percentage trends  

***

## 🚀 Recommendations

- **Routing & Dispatch:** Integrate live traffic data, geofence zones to reduce dead-heading, and forecast surge windows.  
- **Fleet Positioning:** Stage 60–70% of vehicles in high-demand zones during 5–8 PM; pivot to entertainment districts late-night.  
- **Dynamic Pricing:**  
  - Time multipliers: +18% evening, +12% afternoon, +5% night.  
  - Distance tiers: \$17–27/mile (≤2 mi), \$9.18–9.49 (2–5 mi), \$5.99–6.16 (>5 mi).  
  - Ride-sharing: \$3–5 per passenger for 3–6 riders (66–87% cost savings).  
- **Customer Experience:** Enhance service on high-fare trips to boost tips, clearly display surcharges, and reward loyal high-tip riders.  
- **Analytics Ops Center:** Build real-time dashboards, A/B test pricing and positioning, and integrate transit disruption alerts.  

***

## 💻 Installation & Usage

```bash
git clone https://github.com/yourusername/nyc-taxi-data-analysis.git
cd nyc-taxi-data-analysis
conda create -n taxi-analysis python=3.9 pandas geopandas seaborn matplotlib jupyter
conda activate taxi-analysis
jupyter notebook
```

Open **`NYC_Taxi_Analysis.ipynb`** to explore data preprocessing, analysis steps, and visualizations.

***

## 🤝 Contribute & Contact

Feedback, issues, or collaboration ideas welcome!  
- GitHub: https://github.com/yourusername/nyc-taxi-data-analysis  
- Email: your.email@example.com  

***

  
📈 Driven by data -  🚖 Powered by insights -  🌆 Optimized for NYC  
