# 🏏 T20 World Cup 2022 Data Analysis & Best XI Selection

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

## 📊 Project Overview
This project involves a comprehensive analysis of the **ICC Men's T20 World Cup 2022** data. Using Power BI, I developed a data-driven dashboard to evaluate player performance and select the **"Best 11"** team of the tournament. The analysis focuses on identifying impact players across different roles such as Power Hitters, Anchors, Finishers, and Specialist Bowlers.

## ❓ Problem Statement
In cricket, standard metrics like "Total Runs" or "Total Wickets" often fail to capture the true impact of a player in the T20 format. A player scoring 30 runs off 10 balls (Strike Rate: 300) can be more valuable than someone scoring 50 runs off 50 balls.

**The Challenge:**
To assemble the best possible cricket team from the 2022 World Cup by defining specific performance criteria for each playing role.

**Key Questions Answered:**
* Who were the most effective "Power Hitters" in the powerplay?
* Which "Anchors" provided the best stability with a high batting average?
* Who were the most economical bowlers in the death overs?
* **Final Goal:** Select the ultimate **Best XI** team based on data.

## 📂 Data Sourcing & Preparation
* **Source:** Data was scraped from **ESPNcricinfo** (Match Summaries, Batting Cards, Bowling Cards, Player Info).
* **Format:** CSV files (processed and cleaned).
* **Data Modeling:** Connected multiple datasets (`dim_players`, `dim_match_summary`, `fact_bating_summary`, `fact_bowling_summary`) using a Star Schema in Power BI.

**Data Transformation Steps:**
1.  **Data Cleaning:** Removed special characters from player names and handled null values in bowling economy rates.
2.  **Feature Engineering:** Created calculated columns for:
    * **Boundary %:** `(Fours + Sixes) / Total Balls Faced`
    * **Batting Average:** `Total Runs / Total Outs`
    * **Strike Rate:** `(Total Runs / Total Balls) * 100`

## 🔑 Key Performance Indicators (KPIs)
The dashboard evaluates players based on the following metrics:
1.  **Batting Average & Strike Rate:** To balance consistency with aggression.
2.  **Boundary Percentage:** To measure hitting ability.
3.  **Economy Rate:** Runs conceded per over (crucial for bowlers).
4.  **Dot Ball Percentage:** Percentage of deliveries where no run was scored.
5.  **Player Role Classification:** Filtered players into Openers, Middle Order, All-rounders, and Bowlers.

## 📈 Visualizations & Insights
The report is divided into role-specific analysis pages:

### 1. Power Hitters (Openers)
* **Criteria:** High Strike Rate (>140) in the Powerplay overs.
* **Visuals:** Scatter Chart (Strike Rate vs. Average).
* **Top Picks:** [e.g., Jos Buttler, Alex Hales]

### 2. Anchors / Middle Order
* **Criteria:** High Batting Average (>40) to stabilize innings.
* **Visuals:** Bar Charts comparing innings duration and runs.
* **Top Picks:** [e.g., Virat Kohli, Glenn Phillips]

### 3. Finishers (Death Overs)
* **Criteria:** ability to accelerate scoring in the final 5 overs.
* **Insight:** Highlighted players with the highest Boundary %.

### 4. Specialist Fast Bowlers
* **Criteria:** Low Economy Rate (<7.0) and High Wicket Taking ability.
* **Top Picks:** [e.g., Shaheen Afridi, Sam Curran]

### 5. Final Best XI Team
* A consolidated view selecting the top performing 11 players that fit into a balanced team structure (Batters, All-rounders, Bowlers).

## 🛠️ Tools Used
* **Microsoft Power BI:** For building the interactive dashboard and visualizations.
* **Power Query:** For ETL (Extract, Transform, Load) operations.
* **DAX (Data Analysis Expressions):** For creating complex measures like `Batting Average` and `Strike Rate`.
* **Python / Pandas:** Used for initial data scraping and validation.

## 📸 Dashboard Screenshots

### Main Dashboard View
![Main View](screenshots/main_dashboard_view.png)
*(Replace this link with your actual image path)*

### Player Analysis (Scatter Plot)
![Player Analysis](screenshots/player_analysis.png)
*(Replace this link with your actual image path)*

### Final 11 Selection
![Final 11](screenshots/final_11.png)
*(Replace this link with your actual image path)*

## 🔄 Conclusion
The analysis successfully identified a balanced "Team of the Tournament" that statistically outperforms individual team squads. This project demonstrates how sports analytics can be used to make objective selection decisions, moving beyond intuition to data-backed strategies.
