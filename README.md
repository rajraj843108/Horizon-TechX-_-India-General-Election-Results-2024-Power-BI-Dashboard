# Horizon-TechX-_-India-General-Election-Results-2024-Power-BI-Dashboard

**Tool:** Microsoft Power BI Desktop
**Developed by:** Rishi Raj
**Internship:** AI & Data Science Intern @ Horizon TechX (MSME Certified, Govt. of India)
**Program Director:** A. Shrivastava

---

## Election Details

- **Voting Dates:** Fri, 19 April 2024 – Sat, 01 June 2024
- **Result Date:** Tue, 04 June 2024
- **Total Lok Sabha Seats:** 543

---

## Key Results

| Alliance | Seats Won | % of Total |
|----------|-----------|------------|
| NDA Alliance | 292 | 54% |
| I.N.D.I.A. Alliance | 234 | 43% |
| Others / Independent | 17 | 3% |

**NDA — 14 Parties:** BJP (240), TDP (16), JD(U) (12), SHS (7), LJPRV (5), RLD (2), JnP (2), JD(S) (2), and others

**I.N.D.I.A. — 20 Parties:** INC (99), SP (37), AITC (29), DMK (22), SHSUBT (9), NCPSP (8), RJD (4), CPI(M) (4), JMM (3), and others

---

## Project Overview

This Power BI report transforms raw 2024 Indian General Election data into actionable political
insights across 6 interactive dashboards. It helps political analysts, researchers, and citizens
understand voter dynamics, constituency-wise performance, and state-level metrics.

---

## Dashboards

### 1. Landing Page
Central navigation hub with clickable cards to navigate all dashboards.
Includes Home Button on every page to return to the Landing Page.

### 2. Overview Analysis
- Total seats won by NDA, I.N.D.I.A., and Others with percentage share
- Party-wise seat count with party logos for all alliance members
- Bookmark-enabled drill-down grid for each alliance

### 3. State Demographic Analysis
Three interactive map visuals:
- **Map 1:** State-wise total seats, majority alliance, NDA & I.N.D.I.A. seats via tooltip
- **Map 2:** Constituency-wise bubble map — color-coded by NDA, I.N.D.I.A., and Others
- **Map 3:** Alliance dominance choropleth — which alliance won majority seats per state

### 4. Political Landscape by State
- Dynamic state selector dropdown
- KPI cards for I.N.D.I.A., NDA, and Others seat count
- State map with constituency boundaries
- Party-wise results grid with alliance affiliation
- Donut chart for party-wise seat share percentage

### 5. Constituency Analysis
- KPIs: Total Votes, EVM Votes, Postal Votes, Total Candidates
- Winner, Runner-Up, and 2nd Runner-Up with party name, total votes, and vote share %
- Example — AGRA: Winner Prof S P Singh Baghel (BJP) with 5,99,397 votes (53.34%)

### 6. Details Grid
- Full tabular view of all constituency-level data
- Fields: Constituency, Winning Candidate, Runner-Up, Party, Alliance, EVM Votes,
  Postal Votes, Total Votes, Margin
- Drill-through from other dashboards
- Export to Excel functionality

---

## Data Model (ERD)

Five tables connected via primary and foreign keys:

**partywise_results**
- Party, Won, Party ID (PK)

**constituencywise_results**
- Parliament Constituency, Constituency Name, Winning Candidate,
  Total Votes, Margin, Constituency ID (PK), Party ID (FK)

**constituencywise_details**
- Candidate, Party, EVM Votes, Postal Votes, Total Votes,
  % of Votes, Constituency Number (FK)

**statewise_results**
- Constituency, Const. No., Parliament Constituency Name Number,
  Leading Candidate, Trailing Candidate, Margin, Status, State ID, State

**States**
- State ID (PK), State

**Relationships:**
- partywise_results → constituencywise_results via Party ID
- constituencywise_details → constituencywise_results via Constituency Number
- statewise_results → constituencywise_results via Parliament Constituency Name Number
- statewise_results → States via State ID

---

## Skills Used

- Power BI Desktop — Dashboard design, cross-page navigation, bookmarks, tooltips
- DAX — Calculated columns, measures, KPIs, CALCULATE, DIVIDE, filter context
- Data Modeling — Star schema, ERD, primary & foreign keys, table relationships
- Visuals — Map charts (Bing), bubble maps, donut charts, matrix grid
- UX — Drill-through, dynamic filtering, home button navigation, Excel export

---

## How to Use

1. Install Microsoft Power BI Desktop (free) from powerbi.microsoft.com
2. Download and open `India_Election_2024.pbix`
3. Start at the Landing Page and click any dashboard card to navigate
4. Use the State Selector on Political Landscape to filter by state
5. Use the Constituency Selector on Constituency Analysis to drill into any seat
6. Go to Details Grid to explore or export full data as Excel

---

## Repository Structure
