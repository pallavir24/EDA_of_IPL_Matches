# EDA of IPL Matches (2008 - 2023)

## Project Overview
The Indian Premier League (IPL) is a fast-paced, dynamic T20 cricket league where match dynamics, player performances, and venue behaviors shift rapidly. Understanding these trends through raw numbers can be complex. 

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on a detailed ball-by-ball and match dataset covering every IPL match from **2008 to 2023**. Utilizing Python libraries like `Pandas` and `NumPy`, this analysis uncovers key patterns in batting execution, bowling efficiency, historical match outcomes, and stadium/venue impacts.

---

## Problem Statement
Analyzing data across 15+ years of high-intensity cricket requires breaking down granular, delivery-level metrics into actionable insights. This project evaluates granular ball-by-ball records to answer core questions:
* Which batting and bowling strategies yield the highest success rates?
* How do venue characteristics and toss choices affect the ultimate match result?
* What structural patterns emerge during high-pressure run chases?

---

## Dataset Schema & Information
The dataset tracks every delivery bowled, complete with cumulative match context and player performance tracking up to that specific ball.

### 📋 Match Context & Metadata
* **Match ID:** Unique identifier for each individual match.
* **Date:** The calendar date on which the match was played.
* **Venue:** The stadium hosting the match.
* **Winner:** The name of the team that won the match.

### 🏏 Delivery-Level Tracking
* **Innings:** Inning number (`1` or `2`).
* **Over:** The over number within the current inning.
* **Ball:** The ball number within the current over.
* **Valid Ball:** Binary indicator (`1` or `0`) showing if the delivery was legal (excludes wides/no-balls).
* **Ball Rebowled:** Indicator showing if the delivery had to be re-bowled.

### 👥 Player Specifics
* **Bat First / Bat Second:** Teams designated by batting order.
* **Batter / Non Striker:** The active batsmen at the crease.
* **Bowler:** The player delivering the ball.

### 📊 Scoring & Metrics
* **Batter Runs:** Runs scored strictly off the bat on the delivery.
* **Extra Runs:** Extra runs conceded (wides, no-balls, leg byes, byes).
* **Extra Type:** Categorical type of the extra run awarded.
* **Runs From Ball:** Total combined runs from the delivery (`Batter Runs` + `Extra Runs`).
* **Bowler Runs Conceded:** Total runs charged directly against the bowler's statistics on that ball.

### 📉 In-Game Progress & Cumulative Stats
* **Innings Runs / Innings Wickets:** Scoreboard tally at the moment of the delivery.
* **Total Batter Runs / Total Non Striker Runs:** Cumulative runs accumulated by the respective batsmen during the current innings.
* **Batter Balls Faced / Non Striker Balls Faced:** Number of valid legal deliveries faced by the batsmen up to this point.

### 🛑 Dismissal Breakdown
* **Wicket:** Binary indicator (`1` for a dismissal, `0` otherwise).
* **Method:** Mode of dismissal (e.g., bowled, caught, run out, stumped).
* **Player Out:** The name of the dismissed batsman.
* **Player Out Runs / Player Out Balls Faced:** The final runs scored and valid balls faced by the dismissed player prior to their exit.

### 🏁 Run Chase Dynamics (2nd Innings Target Tracking)
* **Target Score:** The exact runs required to win the match.
* **Runs to Get:** Remaining runs required to successfully complete the chase.
* **Balls Remaining:** Legal deliveries left in the innings.
* **Chased Successfully:** Binary indicator (`1` if the target was chased down, `0` if the defending team won).

---

## Technical Stack
* **Language:** Python
* **Environment:** Jupyter Notebook (`.ipynb`)
* **Core Libraries:** Pandas, NumPy, Matplotlib, Seaborn

---

