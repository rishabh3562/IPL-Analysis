# **IPL Cricket Matches & Ball-by-Ball Data (2008-2024)**  

This dataset provides a **detailed** ball-by-ball record of **all IPL matches from 2008 to 2024**, covering **match details, player performances, and game outcomes**. It is ideal for **sports analytics, match predictions, and player performance evaluation**.  

---

## **📌 Dataset Overview**  
- **Matches Data:** Covers match date, venue, teams, toss results, winners, and match outcomes.  
- **Ball-by-Ball Data:** Tracks every legal and extra delivery, including batsmen, bowlers, runs, and wickets.  
- **Dismissals & Wickets:** Includes details on player dismissals, types (bowled, caught, run-out, etc.), and involved fielders.  
- **Innings & Overs:** Records innings progression, legal deliveries, extras, and Super Overs (if applicable).  

---

## **📊 Column Descriptions**  

### **📂 Match & Inning Details**  
| Column Name | Description |
|------------|-------------|
| `match_id` | Unique ID for each match. |
| `season` | Year of the IPL season (2008-2024). |
| `venue` | Stadium where the match was played. |
| `date` | Date of the match. |
| `match_type` | Format of the match (T20). |
| `inning` | Inning number (1st or 2nd, more if Super Over). |

### **🏏 Team & Toss Information**  
| Column Name | Description |
|------------|-------------|
| `batting_team` | Team currently batting. |
| `bowling_team` | Team currently bowling. |
| `team1` | One of the competing teams. |
| `team2` | Opposing team in the match. |
| `toss_winner` | Team that won the toss. |
| `toss_decision` | Decision made by toss-winning team (bat or field). |
| `winner` | Team that won the match. |

### **🔄 Over & Ball Tracking**  
| Column Name | Description |
|------------|-------------|
| `over` | Over number (0-19 in T20). |
| `ball` | Ball number within an over (1-6, can exceed due to extras). |
| `is_legal` | Boolean (1 for legal, 0 for extras like wides & no-balls). |
| `legal_ball` | Count of legal deliveries within an over. |
| `all_balls_over_ball` | Over and ball combined as a decimal (includes all balls). |
| `adjusted_over_ball` | Over and ball combined as a decimal (only legal deliveries). |

### **👤 Player Details**  
| Column Name | Description |
|------------|-------------|
| `batter` | Batsman on strike. |
| `bowler` | Bowler delivering the ball. |
| `non_striker` | Batsman at the non-striker’s end. |

### **🏆 Runs & Extras**  
| Column Name | Description |
|------------|-------------|
| `batsman_runs` | Runs scored by the batsman on that ball. |
| `extra_runs` | Additional runs (wides, no-balls, leg byes, etc.). |
| `total_runs` | Sum of batsman’s runs and extras in that ball. |
| `extras_type` | Type of extra (wide, leg bye, no-ball, etc.). |

### **❌ Wicket Details**  
| Column Name | Description |
|------------|-------------|
| `is_wicket` | Boolean (1 for wicket, 0 otherwise). |
| `player_dismissed` | Name of the dismissed player (if any). |
| `dismissal_kind` | Type of dismissal (bowled, caught, LBW, etc.). |
| `fielder` | Fielder involved in the dismissal (if applicable). |

### **📊 Match-Level Aggregations**  
| Column Name | Description |
|------------|-------------|
| `match_number_of_that_season` | Match number within that season. |
| `matches_in_that_season` | Total matches played in that season. |
| `match_number_in_total` | Overall match number in the dataset. |

### **📌 Other Columns**  
| Column Name | Description |
|------------|-------------|
| `id` | Duplicate of `match_id` (retained from merge). |
| `player_of_match` | Player awarded as "Man of the Match". |
| `result` | Match outcome (win, tie, no result). |
| `result_margin` | Margin of victory (runs or wickets). |
| `target_runs` | Target score set for the chasing team. |
| `target_overs` | Number of overs available to chase the target. |
| `super_over` | Boolean (1 if a Super Over was played). |

---

### **⚠️ Cause of Concerns**  

While this dataset provides comprehensive IPL match and ball-by-ball data, a few limitations should be considered:  

1. **Data Accuracy & Completeness** – The dataset is compiled from various sources; minor discrepancies in player names, venues, or match details may exist.  
2. **Missing Data for Specific Matches** – Some matches, especially rain-affected ones, might have incomplete or missing ball-by-ball details.  
3. **Super Over Handling** – Matches with Super Overs have additional innings, which might require special handling in analysis.  
4. **Merging Duplicates** – Some columns (`id` and `match_id`) exist due to merging; redundant columns should be handled carefully in analysis.  
5. **Evolving IPL Formats** – Rule changes over the years (e.g., impact player rule, changes in points system) may impact trend analysis.  
6. **Toss & Match Outcome Bias** – The dataset doesn’t directly account for external factors like pitch conditions, weather, or DLS calculations.  
7. **Player Name Variations** – Some players might have inconsistent name formats (e.g., "MS Dhoni" vs. "M.S. Dhoni"), requiring preprocessing for accurate analysis.  

### **🔍 How to Mitigate?**  
- **Data Cleaning:** Handle missing values, standardize player names, and drop redundant columns.  
- **Feature Engineering:** Consider match conditions (home/away advantage, team strengths) for better predictive models.  
- **Super Over Handling:** Filter separately for Super Overs before aggregating statistics.  

⚠️ **Keep these factors in mind when conducting analysis to ensure accurate insights!**

---

## **🎯 Potential Use Cases**  
✔️ **Win Prediction:** Predict match outcomes based on historical trends.  
✔️ **Player Performance Analysis:** Track runs, wickets, and match-winning contributions.  
✔️ **Team Strategies & Toss Impact:** Analyze toss-winning decisions and their effect on results.  
✔️ **Exploratory Data Analysis (EDA):** Build visualizations and dashboards for IPL insights.  

📢 **If you find this dataset useful, don’t forget to upvote! 🚀**  
