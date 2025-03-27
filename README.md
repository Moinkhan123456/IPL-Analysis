# Power BI IPL Analysis Dashboard - End-to-End Process Documentation

**1. Data Modeling & Data Processing**
  - **Data Sources: Integrated datasets (ipl_matches_2008_2022, ipl_ball_by_ball_2008_2022, Calendar Table).**
  - **Relationships: Established relationships between match-level and ball-level datasets to enable in-depth analysis.**
  - **Transformations: Standardized data formats, handled missing values, and ensured consistency in naming conventions.**
  - **Calculated Columns & Measures: Created new columns using DAX for computed values like total runs, wickets, strike rates, averages, etc.**

**2. Data Cleaning & Preparation**
  - **Handling Missing Data: Filtered and removed inconsistencies.**
  - **Data Formatting: Converted data types for numerical and categorical variables for efficient analysis.**
  - **Filtering Unnecessary Data: Removed unwanted fields to improve dashboard performance.**

**3. Data Visualization**
  - **Dashboard Overview:**
      - **Title Winner: Displays IPL-winning team (e.g., Gujarat Titans).**
      - **Orange Cap (Most Runs): Identifies the top run-scorer (e.g., Virat Kohli - 6634 runs).**
      - **Purple Cap (Most Wickets): Identifies the top wicket-taker (e.g., DJ Bravo - 183 wickets).**
      - **Tournament 6s & 4s: Displays the total number of sixes (10.66K) and fours (25.49K).**
      - **IPL Batting Stats: Player-specific stats including total runs, 4s, 6s, and strike rate.**
      - **IPL Bowling Stats: Player-specific stats including total wickets, economy, and strike rate.**
      - **Matches Win by Venue: Bar chart representation of match wins at different stadiums.**
      - **Total Wins by Team in a Season: Displays team-wise wins for different seasons.**
      - **Match Wins Based on Toss Decision: Pie chart showing the impact of toss choices.**
      - **Match Wins by Result Type: Pie chart visualizing how matches were won (by wickets, runs, super overs, or no result).**

**4. DAX Functions Used**
  - **Measures Created Using DAX:**
      - **Total Runs = SUM(ipl_ball_by_ball_2008_2022[runs])**
      - **Strike Rate = DIVIDE(SUM(ipl_ball_by_ball_2008_2022[runs]), SUM(ipl_ball_by_ball_2008_2022[balls])) * 100**
      - **Total Wickets = COUNT(ipl_ball_by_ball_2008_2022[wickets])**
      - **Average Runs = AVERAGE(ipl_ball_by_ball_2008_2022[runs])**
      - **Bowling Economy = DIVIDE(SUM(ipl_ball_by_ball_2008_2022[runs]), SUM(ipl_ball_by_ball_2008_2022[overs]))**

Dashboard Interaction <a href="https://github.com/Moinkhan123456/IPL-Analysis/blob/main/Screenshot%20(15).png">View Dashboard of IPL</a>
<br>
Analysis and create a dashboard report.
