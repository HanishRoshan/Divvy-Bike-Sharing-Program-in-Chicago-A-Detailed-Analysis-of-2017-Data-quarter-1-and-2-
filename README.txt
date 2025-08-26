Divvy Bike Sharing Analysis: Chicago 2017 Q1-Q2

A comprehensive analysis of Chicago's Divvy bike-sharing program using 2017 first and second quarter data, examining user behavior patterns, operational efficiency, and spatial usage trends across the city.

## Project Overview

This project analyzes Chicago's Divvy bike-sharing system through detailed examination of trip records and station data from the first half of 2017. The analysis focuses on understanding user behavior, operational efficiency, and identifying opportunities for system optimization.

**Key Focus**: Understanding spatiotemporal patterns, user demographics, station utilization, and revenue optimization in urban bike-sharing systems.

## Dataset

**Data Sources**: 
- `Divvy_Trips_2017_Q1.csv` & `Divvy_Trips_2017_Q2.csv` - Trip records
- `Divvy_Stations_2017_Q1Q2.csv` - Station information

**Dataset Features**:
- Trip duration, start/end times and locations
- Station details (capacity, coordinates, online dates)
- User demographics (subscribers vs customers, gender, birth year)
- Bike utilization patterns and maintenance indicators

## Key Findings

### Operational Efficiency
- **81,909 stations** experiencing insufficient docking capacity daily
- **Station 35** identified as highest usage station requiring priority resource allocation
- **Columbus Dr & Randolph St** shows highest turnover with more check-outs than check-ins

### Temporal Patterns
- **Peak Day**: Tuesday shows maximum usage
- **Peak Hour**: 5 PM demonstrates highest demand
- **Maintenance Window**: Sunday identified as optimal for service operations
- **Seasonal Trends**: Spring > Summer > Winter usage patterns

### Spatial Analysis
- **High Demand Areas**: Chicago Union Station and surrounding downtown areas
- **Maximum Trip Distance**: 3.54km between Station 66 and Station 171
- **Geographic Distribution**: Clear concentration in central Chicago with sparse suburban usage

### User Behavior
- **Weekend vs Weekday**: Higher frequency on weekdays but longer duration on weekends
- **User Types**: Distinct patterns between subscribers and casual users
- **Revenue Generation**: Detailed breakdown by user category and pricing structure

### Predictive Insights
- **Demand Forecasting**: Actual bike demand consistently exceeds forecast predictions
- **Resource Allocation**: Time series analysis for Station 50 shows optimization opportunities

## Technical Implementation

### Data Processing Pipeline
```python
# Key libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from geopy.distance import geodesic
```

### Analysis Components

#### 1. Data Preprocessing
- **Data Integration**: Merged Q1 and Q2 datasets for comprehensive analysis
- **Data Quality**: Handled missing values in gender and birth year fields
- **Feature Engineering**: Created day-of-week categorizations and calculated fields
- **Data Type Optimization**: Converted datetime fields for temporal analysis

#### 2. Geospatial Analysis
```python
# Haversine formula for distance calculation
def haversine_distance(lat1, lon1, lat2, lon2):
    # Implementation for calculating trip distances
    return distance_km
```

#### 3. Station Utilization Analysis
- **Capacity Assessment**: Daily check-in/check-out vs docking capacity
- **Traffic Imbalance**: Identification of stations with significant deficits
- **Usage Optimization**: Heat mapping for strategic planning

#### 4. Revenue Analysis
```python
# Revenue calculation by user type
subscriber_revenue = subscriber_count * annual_rate
single_ride_revenue = single_ride_trips * single_rate  
day_pass_revenue = day_pass_trips * day_rate
```

## Visualizations

### Geographic Analysis
- **Station Distribution Map**: Showing usage intensity across Chicago
- **Heat Maps**: Identifying high/low demand areas for expansion planning
- **Route Analysis**: Most popular bike routes and traffic patterns

### Temporal Trends
- **Hourly Usage Patterns**: Peak demand identification
- **Weekly Distribution**: Day-of-week usage analysis
- **Seasonal Variations**: Quarterly usage comparisons

### Operational Metrics
- **Bike Utilization**: Top 50 most-used bikes for maintenance scheduling
- **Station Traffic**: In/out flow analysis for capacity optimization
- **Deficit Analysis**: Stations requiring immediate attention

## Business Recommendations

### Infrastructure Optimization
1. **Capacity Expansion**: Address 81,909 insufficient capacity stations
2. **Strategic Placement**: Focus resources on high-traffic areas near Union Station
3. **Rebalancing Systems**: Implement dynamic bike redistribution for deficit stations

### Operational Efficiency
1. **Maintenance Scheduling**: Utilize Sunday low-usage periods for service
2. **Peak Hour Staffing**: Increase support during 5 PM rush hour
3. **Seasonal Adjustments**: Adapt fleet size based on quarterly patterns

### User Experience Enhancement
1. **Route Optimization**: Improve bike lane infrastructure on popular routes
2. **Station Accessibility**: Ensure adequate docking at high-turnover locations
3. **Predictive Availability**: Implement demand forecasting for better service

## Project Structure

```
├── data/
│   ├── Divvy_Trips_2017_Q1.csv
│   ├── Divvy_Trips_2017_Q2.csv
│   └── Divvy_Stations_2017_Q1Q2.csv
├── analysis/
│   ├── data_preprocessing.py
│   ├── geospatial_analysis.py
│   ├── temporal_analysis.py
│   ├── user_behavior_analysis.py
│   └── revenue_analysis.py
├── visualizations/
│   ├── maps/
│   ├── temporal_trends/
│   ├── station_analysis/
│   └── user_patterns/
├── notebooks/
│   └── divvy_comprehensive_analysis.ipynb
├── docs/
│   └── divvy_bikes_report.pdf
└── README.md
```

## Methodology

### Statistical Analysis
- **Descriptive Statistics**: Central tendency and distribution analysis
- **Time Series Analysis**: Temporal pattern identification and forecasting
- **Correlation Analysis**: Relationships between usage patterns and demographics
- **Geospatial Statistics**: Distance calculations and spatial clustering

### Data Quality Assurance
- **Missing Value Treatment**: Strategic handling of incomplete demographic data
- **Outlier Detection**: Identification and treatment of anomalous trip records
- **Data Validation**: Cross-verification of station and trip data consistency

## Key Metrics

### Usage Statistics
- **Total Trips**: Combined Q1-Q2 analysis
- **Average Trip Duration**: Segmented by user type and day of week
- **Station Utilization Rate**: Capacity efficiency measurements
- **Geographic Coverage**: Service area analysis

### Financial Performance
- **Revenue Breakdown**: By user type (Subscribers, Single Ride, Day Pass)
- **Operational Costs**: Station maintenance and bike fleet management
- **ROI Analysis**: Station-level profitability assessment

## Limitations & Future Work

### Current Limitations
- **Weather Data**: Missing meteorological factors affecting usage
- **External Events**: No integration of city events or construction impacts
- **Long-term Trends**: Limited to six-month analysis period
- **Demand Factors**: Simplified forecasting without external variables

### Future Enhancement Opportunities
1. **Machine Learning Models**: Advanced demand prediction algorithms
2. **Real-time Analytics**: Dynamic rebalancing optimization
3. **Multi-year Analysis**: Longer-term trend identification
4. **Integration**: Weather, events, and demographic data incorporation

## Installation & Usage

### Requirements
```bash
pip install pandas numpy matplotlib seaborn
pip install geopandas folium geopy
pip install scikit-learn statsmodels
```

### Running the Analysis
```bash
# Clone repository
git clone [repository-url]

# Install dependencies
pip install -r requirements.txt

# Run complete analysis
python analysis/main_analysis.py

# Generate visualizations
python visualizations/create_maps.py
```

## Business Impact

### Operational Improvements
- Identified 81,909 stations needing capacity upgrades
- Optimized maintenance scheduling using low-usage periods
- Enhanced resource allocation through demand pattern analysis

### Strategic Planning
- Data-driven expansion recommendations for underserved areas
- Route optimization insights for infrastructure development
- Revenue optimization through user behavior understanding

## Academic Context

This analysis demonstrates practical application of:
- **Data Science**: Large-scale urban dataset processing
- **Geospatial Analysis**: Location-based pattern identification
- **Business Intelligence**: Operational optimization through analytics
- **Urban Planning**: Transportation system efficiency assessment

## Author

**Hanish Roshan Rajan**  
University of Bristol Business School  
MSc Business Analytics  
Email: workhanish@gmail.com  
LinkedIn: [linkedin.com/in/hanish-roshan](https://www.linkedin.com/in/hanish-roshan-r-b2b7a3119)

## References

1. Verma, R. (2023). Exploratory data analysis of Chicago Divvy Bicycle Sharing. Medium.
2. Faghih-Imani, A. and Eluru, N. (2015). Analysing bicycle-sharing system user destination choice preferences. Journal of Transport Geography.
3. Zhou, X. (2015). Understanding spatiotemporal patterns of biking behavior by analyzing massive bike sharing data. PLOS ONE.

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

**Data Source**: Chicago Divvy Bike Share System - publicly available data used for educational analysis.
