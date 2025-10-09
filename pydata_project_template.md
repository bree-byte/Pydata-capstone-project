# Kenyan Olympic Performance and Global Medal Mapping Project

## Project Overview
This project uses the **120 Years of Olympic History** dataset from Kaggle, comprising two CSV files: `athlete_events.csv` (athlete records including name, age, sex, sport, event, and medals from 1896–2024) and `noc_regions.csv` (mapping NOC codes to country names), last updated in May 2025 [](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results). The goal is to analyze Kenya’s Olympic achievements and visualize global medal distributions, uncovering both well-known trends (e.g., Kenya’s athletics dominance) and novel insights (e.g., medal efficiency). The project leverages Python’s PyData stack for data processing, statistical analysis, and visualization, with results compiled in a Jupyter notebook for clarity and reproducibility.

## Research Questions
The project will address the following questions to provide both foundational and unique insights:
1. **How many medals has Kenya won, and in which sports and events?** (Reveals Kenya’s strengths, e.g., in 3,000m steeplechase.)
2. **How have Kenya’s medal counts evolved over time (1956–2024)?** (Tracks historical trends since Kenya’s Olympic debut.)
3. **What are the typical age and gender profiles of Kenyan medalists?** (Explores demographic patterns in successful athletes.)
4. **Which events does Kenya dominate compared to other countries?** (Identifies Kenya’s competitive edge globally.)
5. **Is there a time African countries were doing better than Kenya?** (Compares continental performance across Olympic years.)
6. **What underdog sports has Kenya tried beyond athletics, and how successful were they?** (Uncovers lesser-known participation, e.g., in boxing or swimming.)
7. **Does Kenya’s medal efficiency (medals per athlete) outrank other nations?** (Highlights efficiency despite smaller delegations.)
8. **How are Olympic medals distributed geographically across all countries?** (Maps global medal counts, with Kenya highlighted.)

## Visualizations
The analysis will employ at least six different visualizations to answer the research questions, combining both static and interactive graphics for deeper insight:
1. **Bar Chart** – Kenya’s total medals by sport to show areas of dominance.
2. **Line Plot** – Medal trends over time (1956–2024) to capture historical progression.
3. **Boxplot and Pie Chart** – Athlete age distributions and gender composition among medalists.
4. **Bar Chart (Events)** – Top medal-winning events for Kenya to highlight consistent strengths.
5. **Comparative Line Plot** – Kenya vs other African countries (especially Ethiopia and Uganda) to visualize regional competition and periods when others outperformed Kenya.
6. **Scatter Plot** – Medal efficiency (medals per athlete) comparison across nations.
7. **Interactive Choropleth Map** – Global medal distribution map with Kenya emphasized, enabling geographic context and exploration.

## Tools and Methods
- **Dataset**:
  - `athlete_events.csv` (~3MB, ~270K rows): Core data with athlete details and medals.
  - `noc_regions.csv` (~30KB, ~230 rows): Maps NOC codes (e.g., `KEN` for Kenya) to country names.
- **Python Libraries**:
  - **Pandas**: For loading, merging, cleaning (e.g., handling NaN medals, standardizing country names), and aggregating data (e.g., `df.groupby('Country')['Medal'].count()`).
  - **NumPy**: For numerical operations (e.g., computing efficiency ratios).
  - **Seaborn/Matplotlib**: For static visualizations like bar plots (Kenya’s medals by event), line plots (historical trends), and boxplots (athlete demographics).
  - **Plotly**: For an interactive choropleth map showing global medal counts, with Kenya marked by a red star.
- **Data Cleaning**:
  - Merge CSVs on `NOC` to add country names.
  - Convert `Medal` NaN to “None” (no medal).
  - Impute `Age`, `Height`, `Weight` with medians for numerical analysis.
  - Standardize country names (e.g., “United States” to “USA”) for Plotly mapping.
  - Map historical NOCs (e.g., `URS` to Russia) and remove duplicates.
  - Filter for `NOC == 'KEN'` for Kenyan-focused analysis (1956–2024).
- **Analysis Workflow**:
  - Aggregate medal counts by country, sport, and event using Pandas.
  - Compute efficiency (medals per athlete) and compare globally.
  - Create visualizations in a Jupyter notebook, saving the map as HTML and static plots as PNGs.
- **Outputs**:
  - Jupyter notebook with all code, visualizations, and insights.
  - Interactive world map (HTML) showing medal distributions.
  - Static plots (PNG) for reports, highlighting Kenyan trends and global comparisons.
