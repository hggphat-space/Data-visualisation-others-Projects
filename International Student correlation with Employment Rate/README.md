# International Student Costs/Opportunity Analysis Dashboard

## Overview

This interactive dashboard provides a comprehensive analysis of international student education costs and employment opportunities across Australian states and territories. The visualization helps prospective international students identify which Australian states offer the best employment prospects after graduation, while also understanding the associated education costs.

**Author:** Hoang Gia Phat (Student ID: 35325453)  
**Course:** FIT3179 - Data Visualisation  
**Assignment:** Assignment 2

## Research Question

**Which Australian state offers the best employment opportunities for international students after graduation, and how do education costs vary across different states and programs?**

This analysis aims to:
- Identify states with the highest employment-to-population rates
- Compare education costs (tuition, living expenses) across different states and cities
- Analyze cost trends over time
- Provide insights to help international students make informed decisions about where to study and potentially settle after graduation

## Dataset Description

### 1. `International_Education_Costs.csv`
Contains comprehensive cost data for international students across various Australian universities, cities, and programs.

**Key Fields:**
- `Country`, `City`, `State`: Geographic location
- `University`: Institution name
- `Program`: Field of study (e.g., Computer Science, Engineering, Business)
- `Level`: Degree level (Bachelor, Master, PhD)
- `Duration_Years`: Program length
- `Tuition_USD`: Annual tuition fees in USD
- `Living_Cost_Index`: Cost of living indicator
- `Rent_USD`: Monthly rent in USD
- `Total_Est_AUD`: Total estimated cost in Australian Dollars (includes tuition, housing, visa, insurance, and other costs)

**Data Source:** Kaggle - International Education Costs Dataset

### 2. `clean_state_labour_force.csv`
Contains monthly employment statistics for all Australian states and territories from 2010 to 2025.

**Key Fields:**
- `Date`, `Month`, `Year`: Temporal information
- `State`: Full state/territory name
- `State Short`: Abbreviated state code (ACT, NSW, VIC, etc.)
- `Employment_to_pop_pct`: Employment-to-population ratio (percentage)
- `Unemployment_rate_pct`: Unemployment rate (percentage)

**Data Source:** Australian Bureau of Statistics (ABS) - Labour Force Statistics

### 3. `clean_state_labour_force_page2.csv`
Aggregated employment statistics with latest values and 12-month averages per state.

**Key Fields:**
- `State`: State/territory name
- `Latest_Date`: Most recent data point
- `Latest_Employment_to_pop_pct`: Most recent employment-to-population percentage
- `Avg12m_Employment_to_pop_pct`: 12-month average employment rate

### 4. `STE_2021_AUST.topojson`
Geographic boundary data for Australian states and territories, used for choropleth mapping.

**Data Source:** Australian Bureau of Statistics - Statistical Area Level 1 (SA1) boundaries

## Visualizations

This dashboard contains **5 interactive visualizations** that work together to answer the research question. Each visualization provides a different perspective on the data, allowing users to explore education costs and employment opportunities from multiple angles.

### Visualization 1: Top 3 Most Expensive Majors in Australia
**Type:** Horizontal Bar Chart  
**File:** `Third_viz.json`  
**Purpose:** Identifies the most costly programs for international students, helping them understand which fields require the highest financial investment.

**Visual Description:**
- Three horizontal bars representing the top 3 most expensive programs
- Bars colored with gradient from light (#BC8F8F) to dark (#001f3f) representing cost magnitude
- Value labels displayed on the right side of each bar
- Y-axis shows program names, X-axis shows cost in thousands of AUD
- Clean, modern design with rounded corners

**Key Insights:**
- Programs like Biotechnology, Climate Science, and Computer Engineering typically rank as the most expensive
- Costs include tuition fees, living expenses, and other associated costs
- Understanding these costs helps students plan their education investment

**What This Shows:** Direct comparison of the top 3 most expensive programs, making it easy to identify which majors require the highest financial commitment.

### Visualization 2: Top 3 States with Highest Employment Rates
**Type:** Horizontal Bar Chart  
**File:** `Thirdviz2.json`  
**Purpose:** Highlights Australian states with the best employment-to-population ratios, indicating where international students are most likely to find work opportunities.

**Visual Description:**
- Three horizontal bars showing states ranked by employment-to-population percentage
- Color gradient similar to Visualization 1, indicating performance level
- Employment percentages displayed on bars
- States sorted by employment rate (highest to lowest)
- Compact design optimized for quick reference

**Key Insights:**
- States like **Australian Capital Territory (ACT)**, **Northern Territory**, and **Western Australia** often lead in employment rates
- Higher employment rates suggest better job market conditions for graduates
- This helps students identify states with strong economies and favorable employment conditions

**What This Shows:** Clear ranking of the top 3 states with best employment opportunities, directly answering which states are most promising for post-graduation employment.

### Visualization 3: Cost Comparison Across States (Interactive Map)
**Type:** Interactive Choropleth Map  
**File:** `First_viz_finished.json`  
**Purpose:** Provides a geographic view of either education costs or employment rates across Australian states, allowing users to toggle between the two perspectives.

**Visual Description:**
- **Map View:** Australia's states and territories displayed as colored regions
- **Toggle Dropdown:** Switch between "Education Costs" and "Employment Rate" views at the top
- **Color Scheme:** 
  - Education Costs: Color intensity shows median cost per state (lighter = cheaper, darker = more expensive)
  - Employment Rate: Blue color scheme showing employment-to-population percentage
- **Interactive Tooltips:** Hover over any state to see:
  - State name
  - Employment-to-population percentage
  - Unemployment rate percentage
- **Geographic Context:** Helps visualize spatial patterns across Australia

**Features:**
- Toggle between "Education Costs" and "Employment Rate" views using dropdown selector
- Color intensity represents the metric value
- Detailed tooltips show state-specific information including unemployment rates
- Geographic representation helps identify regional patterns

**Key Insights:**
- Major cities like Sydney (NSW) and Melbourne (VIC) typically have higher costs
- Regional areas may offer more affordable options with quality education
- Employment rates vary significantly across states
- ACT and NT often show both high costs and high employment rates

**What This Shows:** Geographic distribution of costs and opportunities, allowing users to see where affordability and employment prospects align or diverge.

### Visualization 4: Housing Cost and Living Index by City
**Type:** Dual-Axis Chart (Bar + Line)  
**File:** `Second_viz.json`  
**Purpose:** Compares housing costs and living cost indices across different Australian cities.

**Visual Description:**
- **Bar Chart:** Horizontal bars showing average housing costs (in AUD, thousands)
  - Bars colored in #BC8F8F (Rose Brown)
  - Cities sorted by Living Cost Index (lowest to highest)
- **Line Chart:** Overlay line showing Living Cost Index (LCI)
  - Line colored differently (#001f3f - Navy)
  - Has markers at each city point
  - Right Y-axis shows LCI scale
- **Dual Y-Axes:**
  - Left axis: Housing cost in thousands AUD
  - Right axis: Living Cost Index
- **City Labels:** X-axis shows all major Australian cities with angled labels

**Features:**
- Bars represent average housing costs (in AUD, thousands)
- Line represents average Living Cost Index (LCI)
- Cities sorted by Living Cost Index for easy comparison
- Tooltips show both metrics when hovering

**Key Insights:**
- Housing costs are a major component of total education expenses
- Living Cost Index reflects overall price levels for goods and services
- Some cities have high housing costs but moderate LCI (or vice versa)
- Helps students understand the cost of living in different cities

**What This Shows:** Dual-metric comparison revealing which cities have high housing costs, high overall living costs, or both - crucial for budgeting decisions.

### Visualization 5: Employment Rate Distribution Over Time
**Type:** Kernel Density Estimation (KDE) Plot with Time Slider  
**File:** `Fourth_viz.json`  
**Purpose:** Shows how employment-to-population rates are distributed across states over a 15-year period, revealing labor market trends and conditions.

**Visual Description:**
- **Density Plot:** Smooth curved area showing distribution of employment rates
  - Filled area with blue gradient (light at top, darker at bottom)
  - Line overlay in darker blue (#0d47a1)
  - Points shown where density is significant
- **Interactive Slider:** Year selector at the bottom (2010-2025)
  - Drag to explore different years
  - See how the distribution changes over time
- **X-Axis:** Employment-to-population rate percentage (typically 55-70%)
- **Y-Axis:** Density (frequency/probability)
- **Peaks:** Highest points show the most common employment rate values

**Features:**
- Interactive year slider (2010-2025) at the bottom
- Density curves show the distribution of employment rates across all states
- Peaks indicate the most common rate levels for that year
- Shifts in distribution position reflect changes in labor market conditions
- Smooth interpolation creates aesthetically pleasing curves

**Key Insights:**
- Reveals long-term trends in employment rates across Australia
- Shows how labor market conditions have evolved over 15 years
- Helps identify periods of stronger or weaker employment conditions
- Distribution width shows variability between states
- Peak shifts indicate overall improvements or declines in employment

**What This Shows:** Temporal trends in employment conditions - whether employment rates are improving, declining, or stabilizing over time, and how consistent rates are across states.

### How the Visualizations Work Together

The five visualizations are designed to be viewed in sequence, building a comprehensive picture:

1. **Start with Visualization 1** → Understand which programs are most expensive
2. **Check Visualization 2** → See which states offer the best employment opportunities  
3. **Explore Visualization 3** → Compare costs vs. employment rates geographically
4. **Review Visualization 4** → Understand city-level cost breakdowns (housing & living)
5. **Analyze Visualization 5** → Examine long-term employment trends and stability

**Answer to Research Question:**
- **Best States for Employment:** ACT, Northern Territory, Western Australia (from Viz 2)
- **Cost Considerations:** Major cities (Sydney, Melbourne) have higher costs but offer diverse opportunities (from Viz 3 & 4)
- **Best Strategy:** Balance cost and opportunity - consider regional areas or states with high employment rates and moderate costs
- **Long-term Outlook:** Employment rates have been relatively stable but vary significantly by state (from Viz 5)

## Key Findings

### Employment Opportunities
1. **Australian Capital Territory (ACT)** consistently shows high employment-to-population rates, making it an attractive destination for international students seeking post-graduation employment.
2. **Northern Territory** and **Western Australia** also demonstrate strong employment rates, likely due to labor shortages in key industries.
3. **Major metropolitan areas** (Sydney, Melbourne) may have higher costs but also offer diverse employment opportunities.

### Cost Analysis
1. **Program costs vary significantly** - specialized programs like Biotechnology and Climate Science require higher investment.
2. **State-level cost differences** - Major cities have higher living costs, while regional areas offer more affordable alternatives.
3. **Cost trends** - Education costs have generally increased over time, with some programs showing steeper increases.

### Recommendations for International Students
1. **For employment-focused students:** Consider states with higher employment-to-population rates like ACT, Northern Territory, or Western Australia.
2. **For cost-conscious students:** Explore regional universities and cities with lower living costs while maintaining quality education.
3. **For specialized programs:** Be prepared for higher costs in fields requiring specialized facilities and extended study durations.

## Technical Implementation

### Technologies Used
- **Vega-Lite 5**: Declarative visualization grammar for creating interactive charts
- **Vega-Embed 6**: JavaScript library for embedding Vega-Lite visualizations
- **Pure.css**: Lightweight CSS framework for responsive layout
- **Google Fonts**: Inter and Montserrat font families for typography

### File Structure
```
├── index.html                          # Main dashboard HTML file
├── First_viz_finished.json            # Interactive choropleth map
├── Second_viz.json                    # Housing cost and living index chart
├── Third_viz.json                     # Top 3 expensive majors chart
├── Thirdviz2.json                     # Top 3 states by employment rate
├── Fourth_viz.json                    # Employment rate distribution over time
├── International_Education_Costs.csv  # Education cost dataset
├── clean_state_labour_force.csv       # Employment statistics (monthly)
├── clean_state_labour_force_page2.csv # Employment statistics (aggregated)
├── STE_2021_AUST.topojson            # Australian state boundaries
└── README.md                          # This file
```

### How to Use
1. Open `index.html` in a modern web browser
2. Scroll through the visualizations to explore different aspects of the data
3. Use interactive controls (dropdowns, sliders) to filter and explore the data
4. Hover over visualizations to see detailed tooltips
5. Toggle between views in Visualization 3 to compare costs and employment rates

### View Visualizations Online

You can view each visualization individually using the Vega-Lite editor or by accessing the JSON files:

- **Visualization 1 (Top 3 Expensive Majors):** [View JSON](https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Third_viz.json) | [Open in Vega Editor](https://vega.github.io/editor/#/url/vega-lite/https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Third_viz.json)
- **Visualization 2 (Top 3 States by Employment):** [View JSON](https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Thirdviz2.json) | [Open in Vega Editor](https://vega.github.io/editor/#/url/vega-lite/https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Thirdviz2.json)
- **Visualization 3 (Interactive Map):** [View JSON](https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/First_viz_finished.json) | [Open in Vega Editor](https://vega.github.io/editor/#/url/vega-lite/https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/First_viz_finished.json)
- **Visualization 4 (Housing & Living Costs):** [View JSON](https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Second_viz.json) | [Open in Vega Editor](https://vega.github.io/editor/#/url/vega-lite/https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Second_viz.json)
- **Visualization 5 (Employment Distribution):** [View JSON](https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Fourth_viz.json) | [Open in Vega Editor](https://vega.github.io/editor/#/url/vega-lite/https://raw.githubusercontent.com/hoanggiaphat-monash/FIT3179-Assignment-2/refs/heads/main/Fourth_viz.json)

**Live Dashboard:** View the complete interactive dashboard by opening `index.html` in your browser or hosting it on GitHub Pages.

### Visual Summary of Visualizations

Below is a summary of what each visualization displays:

```
┌─────────────────────────────────────────────────────────────────┐
│                    DASHBOARD OVERVIEW                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  📊 Viz 1: Top 3 Expensive Majors                              │
│     └─ Horizontal bars showing cost by program                 │
│                                                                 │
│  💼 Viz 2: Top 3 States by Employment Rate                     │
│     └─ Horizontal bars ranking states by employment %           │
│                                                                 │
│  🗺️  Viz 3: Interactive Australia Map                        │
│     └─ Choropleth with toggle: Costs ↔ Employment             │
│                                                                 │
│  🏠 Viz 4: Housing & Living Costs by City                      │
│     └─ Dual-axis: Bars (housing) + Line (living index)         │
│                                                                 │
│  📈 Viz 5: Employment Distribution Over Time                   │
│     └─ Density plot with year slider (2010-2025)               │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**Note:** To capture screenshots of the visualizations:
1. Open `index.html` in your browser
2. Use browser developer tools (F12) or screenshot extensions
3. For individual visualizations, use the Vega Editor links above
4. Recommended: Capture the full dashboard showing all 5 visualizations together

## Data Processing

### Data Cleaning Steps
1. **Employment Data:**
   - Converted date formats to standard format
   - Calculated employment-to-population percentages
   - Aggregated monthly data to state-level summaries
   - Created separate files for time-series and aggregated analysis

2. **Education Cost Data:**
   - Converted USD costs to AUD using exchange rates
   - Calculated total estimated costs including all components
   - Aggregated costs by program, state, and city
   - Identified top programs and states for visualization

3. **Geographic Data:**
   - Used TopoJSON format for efficient map rendering
   - Matched state names between datasets for proper joining
   - Ensured consistent state naming conventions

## Limitations and Future Work

### Limitations
1. **Data Currency:** Some employment data may be projected/estimated for future dates
2. **Cost Estimates:** Education costs are estimates and may vary by institution and individual circumstances
3. **Employment Context:** Employment rates don't account for job quality, salary levels, or industry-specific opportunities
4. **Student Preferences:** Analysis focuses on quantitative factors; qualitative aspects (lifestyle, culture) are not considered

### Future Enhancements
1. Add industry-specific employment data
2. Include salary information by state and field
3. Incorporate student satisfaction and quality of life metrics
4. Add filtering by program type or degree level
5. Include migration and visa information
6. Add comparison tools for side-by-side state analysis

## References

- **Australian Bureau of Statistics (ABS):** Labour Force Statistics
- **Kaggle:** International Education Costs Dataset
- **Vega-Lite Documentation:** https://vega.github.io/vega-lite/
- **Australian Government:** Education and Employment Statistics

## License

This project is created for educational purposes as part of FIT3179 Data Visualisation course at Monash University.

## Contact

**Student:** Hoang Gia Phat  
**Student ID:** 35325453  
**GitHub Repository:** https://github.com/hoanggiaphat-monash/FIT3179-Assignment-2

---

*Last Updated: 2025*
