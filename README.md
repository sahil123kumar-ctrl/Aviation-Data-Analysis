# Exploratory Data Analysis on Aviation Dataset

## Project Overview
This project explores and analyzes aviation accident data collected from the **National Transportation Safety Board (NTSB)**.  
The dataset contains detailed records of both accidents and incidents involving various aircraft types, across multiple countries and time periods.  

The goal of this analysis is to identify **key trends, causes, and patterns** behind aviation accidents — enabling data-driven decisions for improved safety, training, and aircraft design.

---

## Objectives
1. Identify trends and patterns in aviation accidents over time.  
2. Assess how **weather conditions**, **flight phases**, and **aircraft configurations** affect accident severity.  
3. Examine which **aircraft models, airports, and engine types** are most frequently involved in accidents.  
4. Provide insights that support **policy-making and safety improvements** in the aviation industry.

---

## Dataset Overview
The dataset includes detailed information about accident type, aircraft specifications, flight conditions, and outcomes.

| Column Name | Description |
| ------------ | ------------ |
| **Event Id** | Unique identifier for each event (accident/incident) |
| **Investigation Type** | Type of investigation (Accident / Incident) |
| **Accident Number** | Case number for the accident |
| **Event Date** | Date when the event occurred |
| **Location** | City or area where the event took place |
| **Country** | Country where the event occurred |
| **Latitude / Longitude** | Coordinates of the event location |
| **Airport Code / Name** | Details of airport involved (if any) |
| **Injury Severity** | Classification of injuries (Fatal, Serious, Minor, None) |
| **Aircraft Damage** | Extent of aircraft damage (Substantial, Destroyed, Minor) |
| **Aircraft Category** | Type of aircraft (Airplane, Helicopter, etc.) |
| **Make / Model** | Manufacturer and model of the aircraft |
| **Number of Engines / Engine Type** | Engine configuration details |
| **Purpose of Flight** | Flight category (Personal, Business, Instructional) |
| **Total Fatal / Serious / Minor Injuries** | Number of passengers affected |
| **Weather Condition** | Conditions during event (Visual, Instrument) |
| **Broad Phase of Flight** | Phase during which event occurred (Takeoff, Landing, etc.) |

---

## Data Preprocessing Steps
1. **Importing necessary libraries**  
2. **Loading and reading dataset**  
3. **Checking column overview and data types**  
4. **Handling missing values**  
   - Replaced missing categorical values with “Unknown”  
   - Filled missing numeric values with median  
5. **Dropped unnecessary columns and duplicates**  
6. **Converted data types** (e.g., event dates to datetime)  
7. **Created derived features** – Year, Month, Day  
8. **Exploratory visualizations** using boxplots and histograms  

---

## Key Insights

### 1. Engine Configuration
- Most aircraft had **1 engine (69,582)**.  
- 3 aircraft had **8 engines**, representing the highest engine count.  
- 1,226 aircraft had **no engines**, possibly gliders or similar crafts.

### 2. Fatal and Serious Injuries
- The **deadliest accident** occurred on **1996-11-12 in New Delhi, India**, with **349 fatalities**.  
- **Highest serious injuries (161)** recorded on **2020-02-05 in Istanbul, Turkey**.  
- **Highest minor injuries** occurred in **Montreal, Canada (2000-07-23)**.

### 3. Weather Conditions
- **Most accidents (77,302)** occurred during **clear weather (VMC)** — not poor weather (IMC).  
- Indicates that **human or mechanical errors** are often more critical than weather.

### 4. Aircraft Damage by Weather
- VMC conditions still showed **higher numbers of substantial aircraft damage**, suggesting human factors or operational errors.

### 5. Top Airports by Accidents/Incidents
- The **“Private” airport category** recorded the highest number of events (~230).  
- Private and small-scale airstrips may lack robust safety infrastructure.

### 6. Aircraft Models and Accident Frequency
- **Model 152** had the highest number of **accidents**.  
- **Model 737** recorded the highest number of **incidents**.

### 7. Engine Type vs. Accidents
- Aircraft with **Reciprocating Engines** were most often involved in accidents, likely due to their usage in smaller, older aircraft.

### 8. Accidents by Flight Phase
- **Landing** and **Takeoff** phases showed the **highest accident frequency**, the most critical phases of flight.

### 9. Injury Severity by Flight Phase
- Most severe injuries occurred during **Cruise**, **Takeoff**, and **Approach** stages.  
- Suggests importance of pilot readiness and equipment reliability during these phases.

### 10. Fatality Analysis
- **Weak correlation (0.071)** between number of engines and fatality rate.  
- **Cessna** aircraft recorded the highest number of **total fatal injuries (7,688)**.  
- **Tupolev** had a **100% fatality rate**, making it among the most unsafe aircraft models.

### 11. Survival Rate by Number of Engines
- Survival rate is highest for **1–2 engine aircraft**, near **100% median**.  
- **8-engine aircraft** show lowest median survival (~20%), indicating higher operational risk.

### 12. Geographical Insights
- **United States** recorded the highest number of total injuries (**72,231**).  
- **New Delhi, India**, had the highest local injury count (**709**).

---

## Conclusions
1. **Clear weather does not guarantee safety** — most accidents occurred in good weather, implying pilot error or operational issues.  
2. **Critical flight phases (Landing, Takeoff, Cruise)** account for the majority of severe accidents.  
3. **Reciprocating engine aircraft** are most prone to incidents, likely due to age or private use.  
4. Certain aircraft models (e.g., **Cessna 152**, **Boeing 737**) appear frequently in accident records.  
5. **Fatality rates increase with engine count**, suggesting that larger, complex aircraft need stricter operational monitoring.  
6. **Private airports and training flights** need stronger safety regulations and oversight.  
7. **Regional hotspots** like the U.S. and India require continuous safety audits and preventive measures.

---

## Recommendations

### 1. Operational Safety
- Enhance pilot focus and standard operating discipline, even under clear weather.  
- Provide advanced **simulator training** for Takeoff, Landing, and Cruise phases.

### 2. Aircraft and Engine Management
- Conduct stricter inspections on **Reciprocating Engine** aircraft.  
- Monitor and review high-risk models like **Tupolev** and **Cessna 152**.

### 3. Airport and Infrastructure Safety
- Strengthen **private airport safety infrastructure** and compliance monitoring.  
- Enforce safety certification for smaller and private operators.

### 4. Technology and Predictive Analytics
- Implement **AI-based predictive models** to forecast accident probability based on flight conditions.  
- Use **machine learning models** to identify high-risk routes and aircraft configurations.

### 5. Policy and Regional Focus
- Conduct **targeted safety initiatives** in the United States and India — the top injury regions.  
- Encourage cross-country data sharing for global aviation safety improvements.

---

## Tools and Technologies
- **Python** – Data preprocessing, statistical analysis, and visualization  
- **Pandas / NumPy** – Data manipulation and transformation  
- **Matplotlib / Seaborn** – Visualization and pattern discovery  
- **Jupyter Notebook** – Exploratory and documentation environment  

---

 
