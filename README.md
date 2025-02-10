# SQL1_Project-IPL-Cricket-2024

# Cricket Data Analysis SQL Project

## Introduction

This project is designed to analyze cricket 2024 IPL cricket match data between teams Chennai Super Kings (CSK) and Royal Challengers Bangalore (RCB) using SQL. The repository contains SQL code files that implement various queries and data transformations, along with a comprehensive data model that captures key aspects of cricket matches. The goal is to derive insights into match outcomes, player performance, and other relevant metrics in the sport.
 
https://www.iplt20.com/match/2024/1354


## Project Overview

The project leverages historical data—including daily match details, ball-by-ball scoring, and player/team information—to support advanced analytics and reporting. The repository includes:

- SQL scripts for data extraction, transformation, and analysis.
- A detailed data model comprising tables for venues, matches, innings, results, ball-by-ball scores, players, and teams.

## Data Model Description

### Venue Table
- **Purpose:** Stores information about cricket venues
- **Relationship:** Each venue can host multiple matches.

### Match Table
- **Purpose:** Contains details about individual matches (e.g., match date, participating teams).
- **Relationships:**
  - Each match is held at a specific venue.
  - Each match involves two teams playing against each other.
  - Each match consists of two innings.
  - Each match is linked to an entry in the **Results Table** to record the outcome.

### Innings Table
- **Purpose:** Captures details of each innings within a match.
- **Relationship:** Every match has two innings (one per team).

### Results Table
- **Purpose:** Records the outcome of each match.
- **Key Attributes:**
  - The winning team.
  - The "Man of the Match" (only one player is selected per match).
- **Relationship:** Each match in the **Match Table** is associated with one record in the **Results Table**.

### Score_by_ball Table
- **Purpose:** Provides detailed ball-by-ball scoring information.
- **Key Attributes:**
  - For each ball, information is captured on the bowler, the striker (batsman), and the non-striker.
- **Cricket Specifics:** Although a T20 match is scheduled for 20 overs with 6 legal balls per over, extra deliveries (wides, no balls, byes, leg byes) may occur, increasing the actual number of balls.

### Player Table
- **Purpose:** Contains information about individual players (e.g., name, role, performance statistics).
- **Relationship:** Players are linked to teams.

### Team Table
- **Purpose:** Stores details about the teams.
- **Key Attributes:** Each team typically consists of 12 players.
- **Relationship:** Teams participate in matches, with each match involving two teams.

## Cricket Match Structure

- **Format:** The data model is designed around the T20 (Twenty20) cricket format.
- **Overs and Balls:**  
  - Each match is scheduled for 20 overs per team.
  - An over typically consists of 6 legal balls.
  - However, due to extra deliveries such as wides, no balls, byes, or leg byes, the actual number of balls per over can be higher than 6.

## Analysis

The SQL analysis in this project covers several aspects of cricket match data to provide comprehensive insights. The following summaries were generated:

1. **Match Summary**  
   - **Attributes:** Match Number, Venue, Match Date, Winning Team Name  

2. **Innings Level Summary**  
   - **Attributes:** Name of the teams that played, Total Runs Scored, Total Wickets Lost, Total Overs Played  

3. **Batting Summary**  
   - **Attributes:** Team Name, Batsman Name, Runs, Balls, 4s, 6s, Strike Rate  

4. **Batting Summary (Extras)**  
   - **Attributes:** Team Name, Extras, No-balls, Wides, Byes, Leg byes, Penalties  

5. **Bowling Summary**  
   - **Attributes:** Batting Team Name, Bowler Name, Overs, Runs, Wickets, Economy, Dots  

These analyses were performed using SQL queries against our well-structured data model, which includes tables for Venue, Match, Innings, Results, Score_by_ball, Player, and Team. The insights obtained from these queries help in understanding overall match outcomes, individual performance metrics, and other critical aspects of the game.


## Conclusion

This SQL project demonstrates how to analyze cricket match data using a comprehensive and well-designed data model. The model includes tables for venues, matches, innings, results, ball-by-ball scores, players, and teams, providing a robust framework for in-depth cricket analytics. The project enables detailed analysis of player performance, match strategies, and overall outcomes, offering valuable insights for coaches, analysts, and cricket enthusiasts.
