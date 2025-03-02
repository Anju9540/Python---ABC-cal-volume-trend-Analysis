# ABC Call Volume Trend Analysis - Python Project 📞📈

## Overview 📝
This project focuses on **inbound call center analytics** for a company named **ABC** (an insurance sector company). The dataset spans **23 days** and includes details such as **Agent Name & ID**, **Queue Time** (time customers wait before an agent answers), **Call Time**, **Call Duration**, and **Call Status** (abandoned, answered, or transferred). The goal is to **analyze call volumes, propose manpower allocations**, and ensure a maximum abandon rate of **10%**.

> **Note:** This analysis was also performed in **Excel**, but the **Python** approach showcased here demonstrates additional benefits such as automation, reproducibility, and advanced analytics capabilities.

---

## Project Description 📋
In today’s customer-centric world, **Customer Experience (CX)** teams play a vital role by analyzing customer feedback and data, identifying areas for improvement, and driving organizational changes. One key aspect of CX involves **call center operations**—managing inbound calls efficiently to minimize abandon rates and maximize customer satisfaction.

### Key Business Questions
1. **Average Call Duration**  
   - *What is the average call duration in each time bucket (e.g., 9-10 AM, 10-11 AM, etc.)?*
2. **Call Volume Analysis**  
   - *How many calls are received in each time bucket?*
3. **Manpower Planning**  
   - *How many agents are needed in each time bucket to reduce the abandon rate from 30% to 10%?*
4. **Night Shift Manpower Planning**  
   - *Assuming 30% of daytime calls also occur at night, how should agents be allocated between 9 PM and 9 AM to maintain a 10% abandon rate?*

### Assumptions
- **Agent Work Schedule:** 6 days a week  
- **Unplanned Leaves:** ~4 per month per agent  
- **Working Hours:** 9 hours total, with 1.5 hours for breaks (lunch/snacks), resulting in 7.5 hours net  
- **Call Handling Time:** Each agent spends ~60% of net working hours on calls  
- **Monthly Basis:** 30 days considered for monthly calculations

---

## Why Use Python? 🔧🐍
- **Automation & Reproducibility:** Python scripts (in Jupyter Notebooks) streamline data cleaning, calculations, and visualizations, ensuring results can be easily reproduced or modified.  
- **Scalability:** Python handles larger datasets more efficiently than Excel, making it well-suited for complex or growing call center data.  
- **Advanced Analytics & Visualization:** Libraries like `pandas`, `numpy`, `matplotlib`, and `seaborn` enable robust statistical analysis, customizable charts, and future integration with machine learning models.  
- **Complement to Excel:** While Excel is user-friendly for quick pivot tables and charts, Python provides more flexibility, automation, and advanced analytics—especially for large datasets and iterative processes.

---

## Data Analysis Tasks & Methodology 🔍

1. **Data Cleaning & Preparation**  
   - Identify and handle null or missing values (e.g., `Agent Name`/`Agent ID` might be `NaN` for abandoned calls).  
   - Convert time-related fields into proper formats for time series analysis.  
   - Verify call statuses (answered, abandoned, transferred) to ensure accurate counting.

2. **Average Call Duration per Time Bucket**  
   - Group calls by hourly buckets (e.g., 9-10 AM, 10-11 AM, etc.).  
   - Calculate the **mean call duration** in each bucket.  
   - Visualize the results to highlight peak durations.

3. **Call Volume Analysis**  
   - Aggregate the total number of calls in each time bucket.  
   - Create bar/line charts to visualize peaks and troughs in call volume.  
   - Identify high-call periods (e.g., 11 AM - 12 PM) and plan accordingly.

4. **Manpower Planning**  
   - **Goal:** Reduce the abandon rate from ~30% to **10%**.  
   - Calculate how many calls were answered vs. abandoned in each time bucket.  
   - Derive the required number of agents per bucket by applying the assumption that an agent spends 60% of their 7.5 working hours on calls.  
   - Compare the current staffing with the needed staffing, highlight gaps, and propose a revised schedule.

5. **Night Shift Planning**  
   - Based on the assumption that for every 100 day calls, there are ~30 night calls (9 PM - 9 AM).  
   - Distribute those 30 calls across night-time buckets.  
   - Determine how many agents are needed to maintain a **10%** abandon rate at night.  
   - Provide a 24-hour coverage plan integrating day and night shifts.

---

## Insights & Recommendations 💡
- **Peak Duration Periods:** Late afternoon to early evening calls have the highest average call duration, suggesting possible reasons such as complex queries or agent fatigue.  
- **Call Volume Peaks:** Highest call volume often occurs mid-morning or mid-day, requiring more agents to minimize wait times.  
- **Reducing Abandon Rate:** To bring abandon rates to 10%, additional agents are needed in certain high-volume time buckets, especially early morning or late evening.  
- **Night Shift Necessity:** With a 30% extension of calls at night, scheduling a minimal number of agents overnight can drastically improve customer satisfaction and reduce abandoned calls.  
- **Optimized Scheduling:** By shifting breaks or administrative tasks to off-peak hours (e.g., mid-afternoon), agent availability can increase during peak periods.

---

## Conclusion ✅
Through this **ABC Call Volume Trend Analysis**, we have:
1. **Identified** key time buckets with high call volume and long average durations.  
2. **Calculated** the manpower needed to reduce abandon rates to 10%.  
3. **Developed** a plan for **night shift coverage**, ensuring minimal customer dissatisfaction outside standard operating hours.  

By **leveraging Python** for data processing, we gained advantages in automation, scalability, and advanced analytics—enhancing the insights we could draw from the data. While **Excel** provides quick and user-friendly pivot-table capabilities, **Python** enables deeper exploration and efficient handling of large datasets. The result is a more proactive and data-driven approach to **customer experience management** in a call center setting.


