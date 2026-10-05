# 🏆 FIFA World Cup 2014 Player Statistics – Power BI Dashboard

## 📊 Project Overview

This project is an interactive **Power BI dashboard** created using FIFA World Cup 2014 player statistics.

The dashboard provides insights into player performance, goals, assists, player positions, teams/squads, appearances, minutes played, disciplinary records, and goal contributions.

The project is designed to demonstrate **data visualization, DAX calculations, interactive filtering, and dashboard design using Microsoft Power BI**.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze FIFA World Cup 2014 player statistics.
* Compare player goals and assists.
* Understand player distribution across different positions.
* Analyze goal contributions by position.
* Explore player-level performance.
* Provide interactive filtering based on national team/squad.
* Create meaningful KPIs using DAX.
* Present football statistics through an interactive dashboard.

---

## 📁 Dataset

The dashboard uses the **FIFA World Cup 2014 player statistics** dataset.

### Main Dataset Table

`wcplayerstatistics2014`

### Important Columns

| Column      | Description                       |
| ----------- | --------------------------------- |
| `Player`    | Player name                       |
| `Pos`       | Player position                   |
| `Squad`     | National team/squad               |
| `Age`       | Player age                        |
| `Born`      | Birth information                 |
| `MP`        | Matches played                    |
| `Starts`    | Matches started                   |
| `Min`       | Minutes played                    |
| `90s`       | 90-minute equivalents             |
| `Gls`       | Goals scored                      |
| `Ast`       | Assists                           |
| `G+A`       | Goals + assists                   |
| `G-PK`      | Non-penalty goals                 |
| `PK`        | Penalty goals                     |
| `PKatt`     | Penalty attempts                  |
| `CrdY`      | Yellow cards                      |
| `CrdR`      | Red cards                         |
| `PlayerID`  | Player identifier                 |
| `AstPer90`  | Assists per 90 minutes            |
| `GlsPer90`  | Goals per 90 minutes              |
| `G+APer90`  | Goal contributions per 90 minutes |
| `SecondPos` | Secondary position                |

---

## 📈 Dashboard Visualizations

The Power BI report contains several interactive visualizations.

### 1. 📊 Area Chart – Goals and Assists by Position

Displays the relationship between:

* Goals
* Assists
* Player position

This helps identify which positions contributed most to attacking performance.

**Fields:**

* Axis: `Pos`
* Values: `Gls`, `Ast`

---

### 2. 🍩 Donut Chart – Players by Position

Shows the distribution of players across different playing positions.

**Fields:**

* Category: `Pos`
* Values: Count of `Player`

This provides a quick overview of the composition of the World Cup player pool.

---

### 3. ⚽ Funnel Chart – Goals by Position

The funnel chart compares total goals scored by players across different positions.

**Fields:**

* Category: `Pos`
* Values: `Gls`

It helps identify which positions produced the highest number of goals.

---

### 4. 🔵 Scatter Chart – Goals vs Assists

The scatter chart compares individual player goals and assists.

**Fields:**

* X-axis: `Gls`
* Y-axis: `Ast`
* Details/Category: `Player`
* Series: `Pos`

This visualization makes it easier to identify highly productive attacking players.

---

### 5. 📊 Bar Chart – Player Goals

A clustered bar chart displays goals scored by individual players.

**Fields:**

* Axis: `Player`
* Values: `Gls`

This can be used to identify the top goal scorers.

---

### 6. 🎛️ Squad Button/Slicer

The dashboard contains an interactive squad filter based on:

`Squad`

Users can select a national team to dynamically filter the dashboard and analyze its players.

---

## 🧮 DAX Measures

The Power BI model includes the following DAX measures:

```DAX
Total Players =
DISTINCT('wcplayerstatistics2014'[Player])
```

```DAX
Total Teams =
DISTINCT('wcplayerstatistics2014'[Squad])
```

```DAX
Total Goals =
SUM(wcplayerstatistics2014[Gls])
```

```DAX
Total Assists =
SUM(wcplayerstatistics2014[Ast])
```

```DAX
Total Goal Contributions =
SUM(wcplayerstatistics2014[G+A])
```

```DAX
Total Minutes =
SUM(wcplayerstatistics2014[Min])
```

```DAX
Total Starts =
SUM(wcplayerstatistics2014[Starts])
```

```DAX
Yellow Cards =
SUM(wcplayerstatistics2014[CrdY])
```

```DAX
Red Cards =
SUM(wcplayerstatistics2014[CrdR])
```

```DAX
Penalty Goals =
SUM(wcplayerstatistics2014[PK])
```

```DAX
Penalty Attempts =
SUM(wcplayerstatistics2014[PKatt])
```

---

## 🎨 Dashboard Design

The dashboard uses a football-inspired visual design with:

* Green background
* Custom theme
* Large **WORLD CUP** heading
* Dashboard title
* Interactive visualizations
* Player/team filtering
* Cross-filtering between visuals

The report page is configured for a **1920 × 1080** dashboard layout.

---

## 🔄 Interactivity

The dashboard supports interactive analysis through:

* Squad filtering
* Cross-filtering
* Visual interactions
* Position-based analysis
* Player-level analysis
* Drill/filter interactions

Selecting a squad allows users to analyze the performance of players belonging to that national team.

---

## 🛠️ Technologies Used

* **Microsoft Power BI**
* **DAX**
* **Power BI Data Model**
* **Data Visualization**
* **Interactive Dashboard Design**
* **FIFA World Cup 2014 Player Statistics**

---

## 📂 Project Structure

```text
Power-BI-World-Cup-2014/
│
├── Power BI (Project-2).pbit
├── README.md
└── Dataset/
    └── wcplayerstatistics2014.csv
```

> The `.pbit` file is a Power BI Template file. Open it using Microsoft Power BI Desktop and provide/refresh the required data source when prompted.

---

## 🚀 How to Run the Project

### Step 1 – Download the Repository

Clone the repository:

```bash
git clone https://github.com/your-username/Power-BI-World-Cup-2014.git
```

### Step 2 – Open Power BI

Install and open **Microsoft Power BI Desktop**.

### Step 3 – Open the Template

Open:

```text
Power BI (Project-2).pbit
```

### Step 4 – Load/Refresh the Dataset

If Power BI asks for the dataset location, provide the location of:

```text
wcplayerstatistics2014.csv
```

### Step 5 – Explore the Dashboard

Use the **Squad** slicer and interact with the charts to explore player statistics.

---

## 📌 Key Insights That Can Be Explored

The dashboard can be used to answer questions such as:

* Which positions scored the most goals?
* Which players recorded the highest number of goals?
* Which players provided the most assists?
* Which players had high goal and assist contributions?
* How are players distributed across positions?
* How does a particular national team perform?
* Which players have high attacking output?
* Which positions contribute most to overall goals?
* Which players received yellow or red cards?

---

## 📊 Skills Demonstrated

This project demonstrates practical skills in:

* Data loading
* Data modeling
* DAX
* KPI creation
* Interactive filtering
* Power BI visualizations
* Dashboard layout and design
* Football/sports data analysis
* Exploratory data analysis
* Business intelligence reporting

---

## 🔮 Future Improvements

Possible enhancements include:

* Add KPI cards for total players, goals, assists, and teams.
* Add a top-10 goal scorers chart.
* Add a top-10 assist providers chart.
* Add player profile drill-through pages.
* Add team-level performance pages.
* Add age-group analysis.
* Add goals/assists per 90-minute analysis.
* Add disciplinary analysis.
* Add additional World Cup editions for historical comparison.
* Add bookmarks and navigation buttons.
* Add a dedicated player comparison page.

---

## 👨‍💻 Author

**Kaushik**

### Project

**FIFA World Cup 2014 Player Statistics – Interactive Power BI Dashboard**

---

## ⭐ Acknowledgement

This project was created for learning and demonstrating **Power BI, DAX, data visualization, and business intelligence dashboard development** using FIFA World Cup player statistics.

If you find this project useful, consider giving the repository a ⭐.

---

## 📜 License

This project is intended for **educational and learning purposes**.
<img width="1917" height="738" alt="Screenshot 2026-10-05 162534" src="https://github.com/user-attachments/assets/7e943f61-c11f-4276-ac65-5217a9b6d05c" />
