Power BI Project 3 – Logistics & Transportation: Fleet Performance & Delivery Efficiency
📄 Project Overview

This Power BI project analyzes fleet performance for a logistics company — focusing on delivery efficiency, fuel performance, and operational cost optimization. The dashboard provides actionable insights into on-time deliveries, fuel consumption, and cost per kilometer to improve fleet utilization and logistics planning.

🧩 Problem Statement

A logistics company aims to assess its fleet’s performance in terms of on-time deliveries, fuel efficiency, and cost per mile.
The analysis identifies trends, inefficiencies, and optimization opportunities for better operational management.

📊 Dataset Description

Dataset Used: Logistic Dataset
The dataset contains two primary tables:

1. Trip Data

Trip ID

Vehicle ID

Driver ID

Origin

Destination

Distance (km)

Fuel Consumed (liters)

Delivery Status (On-Time/Late)

Delivery Date

2. Vehicle Master

Vehicle ID

Vehicle Type

Capacity

Maintenance Cost

⚙️ Project Steps and Objectives
1. Data Cleaning & Modeling (5 Marks)

Handled missing Fuel Consumed values by replacing them with the average per vehicle type.

Created a relationship between Trips and Vehicle Master tables using Vehicle ID.

Ensured all fields were properly formatted and data types aligned for analysis.

2. DAX Measures (5 Marks)

Fuel Efficiency:

Fuel Efficiency = DIVIDE(SUM(Trips[Distance]), SUM(Trips[Fuel Consumed]))


On-Time Delivery %:

On-Time Delivery % = DIVIDE(CALCULATE(COUNTROWS(Trips), Trips[Delivery Status] = "On-Time"), COUNTROWS(Trips))


Cost per km:

Cost per km = DIVIDE(SUM(Vehicle[Maintenance Cost]) + SUM(Trips[Fuel Cost]), SUM(Trips[Distance]))

3. Visualization (5 Marks)

📊 Bar Chart: On-Time Delivery % by Route (Origin → Destination).

📈 Line Chart: Monthly trend of Fuel Efficiency.

🎯 KPI Cards: Average Delivery Time, Cost per km, and Fuel Efficiency.

🗺️ Map Visual: Geographic representation of delivery routes and their performance.

🚀 Expected Output

An interactive Power BI dashboard showcasing:

Route-wise performance and delivery efficiency

Fuel consumption trends and cost analysis

KPIs to monitor fleet utilization and operational health

This enables data-driven decision-making for optimizing logistics routes, improving on-time delivery, and minimizing transportation costs.

📁 Repository Structure
📂 PowerBI-Logistics-Fleet-Performance
 ┣ 📊 Logistics_Fleet_Performance.pbix
 ┣ 📈 Dataset/
 ┃ ┣ Trips.csv
 ┃ ┗ VehicleMaster.csv
 ┗ 📘 README.md

💡 Insights Gained

Identified routes with higher late delivery percentages

Pinpointed vehicles with poor fuel efficiency

Calculated cost-per-kilometer to prioritize maintenance and scheduling

Improved visibility into route and driver performance

🧠 Tools & Technologies Used

Power BI – Data modeling, DAX, visualization

Excel / CSV – Source data cleaning

DAX – Custom metrics and measures

👩‍💼 Author

Agnes A
📧 agnes11raj@gmail.com
💼 Data Analyst | Power BI Developer | Business Intelligence Enthusiast
