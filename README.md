# Olympics-Dataset-Analysis
An exploratory data analysis and Power BI dashboard project visualizing historical Olympic Games data, including medal counts, athlete demographics, and sport-specific trends.

![Olympics Dataset Analysis Dashboard](olymbic_data_analysis.png)

---

## 📊 At a Glance

| Metric | Value |
|---|---|
| 🥇 Total Medals Earned | **39,780** |
| 🏋️ Sports Played | **66** |
| 🌍 Countries Participated | **136** |

---

## 🗂️ Data Model

The report is built on two tables:

### `athlete_events`
The primary fact table. Each row represents one athlete's participation in one Olympic event.

| Column | Description |
|---|---|
| `Name` | Athlete's full name |
| `Gender` | M / F |
| `Age` | Age at time of event |
| `Country` | Country represented |
| `Year` | Year of the Olympic Games |
| `Season` | Summer or Winter |
| `Sport` | Sport category |
| `Event` | Specific event within the sport |
| `Medal` | Gold, Silver, Bronze, or NA |

### `country_definitions`
A dimension/lookup table providing additional metadata about participating countries.

---

## 📈 Dashboard Visuals

The report contains **12 visual components** on a single page:

| Visual | Type | Description |
|---|---|---|
| KPI Cards (×3) | Card | Total medals, sports played, countries participated |
| Medal by Gender | Pie Chart | Share of all medals between male and female athletes |
| Medal by Season & Country | Bar Chart | Summer vs Winter medal counts across top countries |
| Athlete Count by Year & Gender | Line Chart | Historical participation trend (1880–2020) |
| Top 10 Players by Medals | Column Chart | Gold / Silver / Bronze breakdown per top athlete |
| Medal Count by Country | Pivot Table | Full country-level medal table with totals |
| Medal by Age & Type | Ribbon Chart | Medal counts across age groups and medal types |
| Medal Count by Sport | Treemap | Relative medal volume across all 66 sports |

---

## 🔍 Key Insights

### 🌍 Country Performance

| Country | Bronze | Gold | Silver | Total |
|---------|--------|------|--------|-------|
| USA | 1,358 | 2,638 | 1,641 | **5,637** |
| Russia | 1,178 | 1,599 | 1,170 | **3,947** |
| Germany | 1,260 | 1,301 | 1,195 | **3,756** |
| France | 666 | 501 | 610 | **1,777** |
| UK | 651 | 678 | 739 | **2,068** |
| Italy | 531 | 575 | 531 | **1,637** |
| Sweden | 535 | 479 | 522 | **1,536** |
| Canada | 451 | 463 | 438 | **1,352** |
| Australia | 522 | 368 | 459 | **1,349** |
| Hungary | 371 | 432 | 332 | **1,135** |

### 🚻 Gender Distribution
- **Male athletes** account for **72.51%** of all medals (196.59K)
- **Female athletes** account for **27.49%** (74.52K), with representation growing significantly post-1960

### 🏟️ Top Sports by Medal Count
1. **Athletics** — highest medal total overall
2. **Gymnastics** — 26.71K medals
3. **Swimming** — 23.20K medals
4. **Cross Country Skiing** — 9.13K medals
5. Boxing, Wrestling, Speed Skating, Alpine Skiing, Football, Ice Hockey, Basketball

### 🏆 Top Athletes by Total Medals
| Athlete | Gold | Silver | Bronze | Total |
|---------|------|--------|--------|-------|
| Michael Fred Phelps | 23 | 3 | 4 | **30** |
| Edoardo Mangiarotti | 6 | 6 | 8 | **20** |
| Larysa Semeniuk | 9 | 5 | 4 | **18** |
| Aleksey Yuryev | 6 | 8 | 4 | **18** |
| Ole Einar Bjørndalen | 8 | 4 | 4 | **16** |
| Birgit Fischer-Schmidt | 8 | 4 | 4 | **16** |

### 📅 Historical Trends (1880–2020)
- Male participation surged after **1900** and peaked around **1980–2000**
- Female participation began rising meaningfully after **1960**
- The gender gap in athlete count has steadily narrowed in recent decades
- Peak total participation was recorded around **1996–2004**

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Power BI Desktop** (v2025.09) | Dashboard design, DAX measures, data modelling |
| **Power Query (M)** | Data transformation and cleaning |
| **Kaggle** | Source dataset |

---

## 📁 Repository Structure

```
olympics-dataset-analysis/
│
├── data/
│   └── athlete_events.csv            # Raw athlete-level dataset
│
├── OLMPICS_DATASET_ANALYSIS.pbix     # Power BI Desktop file
├── olymbic_data_analysis.png         # Dashboard screenshot
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free download)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/olympics-dataset-analysis.git
   cd olympics-dataset-analysis
   ```

2. **Open the report**  
   Double-click `OLMPICS_DATASET_ANALYSIS.pbix` or open it from within Power BI Desktop via `File → Open`.

3. **Refresh the data** *(only needed if the CSV path has changed)*  
   Go to `Home → Transform Data → Data Source Settings` and update the path to point to `athlete_events.csv`.

4. **Explore the dashboard**  
   Use the built-in cross-filtering to interact across all visuals.

---

## 📦 Dataset

**Source:** [120 Years of Olympic History: Athletes and Results](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results) — Kaggle

The dataset covers every athlete who competed in the modern Olympics between **1896 and 2016**, with some records extending back to **1880**. It includes athlete demographics, event details, and medal outcomes.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request for:
- New report pages or visuals
- Additional DAX measures
- Data quality improvements
- Documentation updates

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- Dataset by [rgriffin](https://www.kaggle.com/heesoo37) on Kaggle
- Built with Microsoft Power BI Desktop
- Inspired by the spirit of the Olympic Games 🕊️

