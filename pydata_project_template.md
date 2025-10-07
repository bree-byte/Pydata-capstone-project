#  Kenya Events Data Analysis

##  Project Overview
This project focuses on **collecting and analyzing data from Eventbrite’s public API** for events happening in **Kenya (mainly Nairobi)** between **2019 and 2025**.  
The goal is to uncover **trends in event organization, ticketing, and audience behavior** using **Python, SQLite, Pandas, NumPy, and Matplotlib**.

---

##  How It Works

### 1. API Extraction
- Uses Python’s `requests` library to pull event data from the **Eventbrite API**.
- Each record includes details such as:
  - Event name  
  - Category  
  - Start time  
  - Venue  
  - Ticket information  

### 2. Database Storage
- Data is stored in a **SQLite database (`kenya_events.db`)** using a **class-based approach**.
- Two main tables are created:
  - `events` → General event information  
  - `tickets` → Ticket types and sales details  

### 3. Processing & Cleaning
- Uses **Pandas** to clean and structure the data.  
- Adds new columns for `year`, `month`, and `day_of_week` for time-based analysis.

---

## Analysis & Insights

###  With NumPy:
- Calculate **mean, median, and standard deviation** of event capacities.  
- Find **percentiles** to understand the spread of event sizes.  
- Use **NumPy arrays** for fast statistical summaries.

###  With Pandas:
- Group events by **year**, **month**, and **category** to identify active periods.  
- Count **free vs paid events**.  
- Identify **most common venues**.

###  With Matplotlib:
- Visualize trends using charts:
  - **Events per Year** (Bar chart)  
  - **Events by Month** (Line chart)  
  - **Event Categories** (Bar chart)  
  - **Free vs Paid Events** (Pie chart)  
  - **Top Venues** (Horizontal bar chart)

---

##  Key Findings
- Event counts fluctuate yearly, with noticeable **peaks in certain months**.  
- A significant proportion of events are **free**, reflecting accessibility.  
- **Music, Business, and Technology** emerge as top event categories.  
- Certain venues consistently host **large-scale or recurring events**.

---

##  Technical Skills Demonstrated
- **API data extraction & automation** using `requests`  
- **Database design & management** with `sqlite3`  
- **Data cleaning & analysis** using `pandas` and `numpy`  
- **Visualization & storytelling** using `matplotlib`  
- **Interpreting real-world data** into actionable insights  

---

##  Future Improvements
- Integrate **additional event data sources** (e.g., Quicket, Meetup, KenyaBuzz).  
- Automate **daily or weekly updates**.  
- Build a **dashboard** for live visualization and monitoring.

---

##  References & Data Sources
- [Eventbrite Developer Platform & API Guide](https://www.eventbrite.com/platform/api)  
- [Eventbrite Nairobi Listings](https://www.eventbrite.com/d/kenya--nairobi/events/)  
- [Quicket Kenya API & Listings](https://www.quicket.co.ke/)  
- [Meetup Nairobi Events](https://www.meetup.com/find/?location=Nairobi)  
- [KenyaBuzz Events Portal](https://www.kenyabuzz.com/)  

---

###  Summary
This project demonstrates how **public API data** can be transformed into **insights for decision-making and trend analysis** in the event industry.  
It bridges the gap between **data collection, analysis, and visualization** a complete data lifecycle project from API to insight.

---
