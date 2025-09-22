# Uber--Trip-Analytics-Dashboard---Power-BI-Project
This project is an end-to-end Power BI dashboard analyzing Uber ride data. It provides insights into trip distribution, revenue, customer preferences, and time-based patterns.   
 The dashboard enables data-driven decision-making by tracking KPIs such as total trips, fare, duration, distance, and night trip percentage.


## 📌 Project Overview  
This project is an **end-to-end Power BI dashboard** analyzing Uber ride data. It provides insights into trip distribution, revenue, customer preferences, and time-based patterns.  

The dashboard enables **data-driven decision-making** by tracking KPIs such as total trips, fare, duration, distance, and night trip percentage.  

---
## 🎯 Objectives  
- Develop an interactive dashboard to monitor Uber rides.  
- Track key performance indicators (KPIs).  
- Provide geographic and time-based insights.  
- Analyze payment preferences.  

---

## 📊 Key Performance Indicators (KPIs)  
- **Total Trips** – Count of trips  
- **Total Fare** – Revenue generated  
- **Total Duration** – Total time spent on trips  
- **Total Distance** – Kilometers covered  
- **Night Trip %** – Percentage of trips during night  

---

## 🛠️ Data Sources  
- **Trip Details Fact Table** – Trip ID, duration, distance, fare, payment type, pickup time  
- **Location Dimension Table** – Location ID, Location Name  

---

## 🔄 Data Preparation (Power Query)  
- Changed column data types  
- Removed null/unwanted rows  
- Standardized payment types (Cash, Uber Pay, Google Pay, Amazon Pay)  
- Created custom columns (Day/Night classification)  

---

## 📐 Data Model  
- **Fact Table** – Trip Details  
- **Dimension Tables** – Date Table, Location Table, Payment Types  
- Relationships: Trip Fact ↔ Location, Trip Fact ↔ Date  

---

## 🧮 DAX Measures  
```DAX
Total Trips = COUNT('Trip Details'[Trip ID])
Total Fare = SUM('Trip Details'[Fare])
Total Duration = SUM('Trip Details'[Duration])
Total Distance = SUM('Trip Details'[Distance])

Night Trip % =
VAR NightCount = CALCULATE([Total Trips], 'Trip Details'[Shift] = "Night")
RETURN DIVIDE(NightCount, [Total Trips], 0)

---

## 👨‍💻 Author

**Abhishek Bity**  
Data Analyst | Power BI Developer  

- 💼 LinkedIn: [linkedin.com/in/abhishekbity](https://linkedin.com/in/abhishekbity)  
- 📧 Email: bityabhishekwork@gmail.com  
- 📂 GitHub: [github.com/abhishekbity](https://github.com/abhishekbity)  

---



