### metromove-transit-analytics

### Project overview

MetroMove Transit Analytics is an end-to-end data analytics and reporting project built
around a fictional public transportation company operating buses, trains, ferries, and trams
across multiple cities. we seek to identify trends, make data-drive recommendation, and get a deeper understanding of the
company performance.

### Data source

MetroMove: the primary data-set use for this analysis is the "MetroMove_csv" file, containing detail information of trip
made by the company.

### Tool

- Python-Core analysis language[]()
- pandas-Data cleaning and KPI computation[]()
- Jupyter Notebook- Exploratory data analysis

- ## Data cleaning/Preparation
 
in the initial preparation Phase, we perform the following:
1. Data loading and inspection.
2.  handling missing values.
3. Data cleaning and formatting

   ### Exploratory data analysis

   EDA analysis was perform to answer the following question.
   1. How does trip duration vary across modes?
   1. Which stations are the most active?
   3. When is the network busiest?
   4. Which mode is the most expensive to ride?
   5.  Which transport mode carries the most trips?
  
    ### Data analysis

      ```python
      df["Trip_Duration_Minutes"] = pd.to_numeric(df["Trip_Duration_Minutes"], errors="coerce")

def trip_type(x):
    if x <= 50:
        return "<=50 very short trip"
    elif x <= 100:
        return "51-100 short trip"
    else:
        return ">=101 long trip"

df["trip_type"] = df["Trip_Duration_Minutes"].apply(trip_type)

### Resulting/Findings

Analysis result are summarize as follows.
1. with 32.2% per trips, the Bus network is the backbone of MetroMoves service. Generating the highest Revenue
   with Ferries and Trains 28.7% and 24.3% respectively, while Trams represent a smaller but valuable 13.3%
2. Ridership peaks are on sundays with 168 trips and dips on thursday with 118 trips.
3. the Airport station lead all others on both arrival and departure station.

   ### Recommendation

   
