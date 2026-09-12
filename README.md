# Smart Tourism Analytics System 🧭

> **B.Tech III Year, I Semester Mini-Project**  
> **Department of Computer Science & Engineering - Data Science (CSD)**  
> **Narayana Engineering College (Autonomous), Nellore, Andhra Pradesh**

---

## 📋 Academic Project Information

| Field | Detail |
| :--- | :--- |
| **Project Title** | **Smart Tourism Analytics System** |
| **Institution** | **Narayana Engineering College (Autonomous), Nellore** |
| **Department** | **CSE - Data Science (CSD)** |
| **Academic Year / Sem**| **III Year, I Semester** |
| **Student Name** | **GURRAM VENKATA SAI LAKSHMI HAASINI** |
| **Roll Number** | **24711A3219** |
| **Project Guide** | **Mrs. D. Saritha**, Assistant Professor |

---

## 🌟 Executive Summary & Objectives

The **Smart Tourism Analytics System** is a data-driven platform designed to ingest, slice, and visualize multidimensional tourist footfall and expenditure metrics. Developed with a high-performance client-side Data Science pipeline, this application eliminates backend latency while providing deep statistical insights into:
- **Spatial Distributions**: High-density tourist hotspots across South, North, East, West, and Central India.
- **Seasonal Spikes**: Seasonal visitor trends across Summer, Winter, Monsoon, and Festive periods.
- **Demographic & Spending Insights**: Travel group preferences (Solo, Couple, Family, Friends) compared against average budgets in ₹ INR.
- **Visitor Motivation**: Analysis of travel categories (Spiritual, Heritage, Eco/Nature, Adventure, Beach).

---

## 🚀 Core Features

1. **Executive KPI Overview Cards**:
   - **Total Annual Visitors**: Real-time counter adapting dynamically to filtered data slices.
   - **Top Destination**: Computed mode of destination frequency distribution.
   - **Average Tourist Spending**: Arithmetic mean of visitor budgets in Indian Rupees (₹).
   - **Peak Season & Satisfaction**: Mode of seasonal footfall combined with average star ratings.

2. **Interactive Visualizations (Chart.js Engine)**:
   - 📊 **Popular Destinations (Bar Chart)**: Ranks locations by total footfall.
   - 📈 **Visitor Trends Over Time (Line Chart)**: 12-month temporal curve illustrating peaks and troughs.
   - 🍩 **Tourist Preferences (Donut Chart)**: Visual breakdown of travel interest categories.
   - 💳 **Expenditure by Travel Group (Bar Chart)**: Compares average spending between Solo, Couple, Family, and Friends.

3. **Multi-Axis Data Filtering Engine**:
   - **Filter by Season**: All, Summer, Winter, Monsoon, Festive.
   - **Filter by Region**: All, South India, North India, East India, West India, Central India.
   - **Filter by Category**: Heritage & Culture, Eco & Nature, Spiritual, Adventure, Leisure & Beach.
   - **Full-Text Live Search**: Search destinations, tourist names, and origin cities.

4. **Granular Dataset Table & CSV Data Export**:
   - Paginated table showing raw tourist rows.
   - **Export CSV** function to export active filtered data for external analysis in Python / Pandas.

5. **Institutional Metadata Badges & Footer**:
   - Prominently showcases college affiliation, guide name, student roll number, and department credentials.

---

## 🛠️ Technology Stack (100% Free & Open-Source)

- **Frontend Framework**: React 18 with TypeScript
- **Bundler & Build Tool**: Vite 6 (Blazing fast HMR)
- **Styling**: Tailwind CSS (Modern dark glassmorphism palette)
- **Charting Library**: Chart.js 4 & `react-chartjs-2`
- **Iconography**: Lucide React
- **Data Engine**: Pure TypeScript client-side statistical pipeline (`src/utils/dataPipeline.ts`)
- **Dual Distribution**:
  1. Full modular TypeScript + React project (`src/`)
  2. Zero-dependency standalone HTML single-file build (`standalone_dashboard.html`) for instant lab presentations!

---

## 📂 Project Structure

```
e:/tourist/
├── index.html                    # Root HTML template
├── standalone_dashboard.html     # Single-file zero-install offline presentation
├── package.json                  # Node.js dependencies & scripts
├── tsconfig.json                 # TypeScript compiler configuration
├── vite.config.ts                # Vite dev server configuration
├── tailwind.config.js            # Tailwind styling setup
├── src/
│   ├── main.tsx                  # React entry point
│   ├── App.tsx                   # Main dashboard layout
│   ├── index.css                 # Base stylesheet & scrollbar styles
│   ├── types/
│   │   └── tourism.ts            # Type interfaces (TouristRecord, FilterState, KpiMetrics)
│   ├── data/
│   │   └── mockTouristData.ts    # 100+ granular tourist records
│   ├── utils/
│   │   └── dataPipeline.ts       # Data science aggregations & statistical calculations
│   └── components/
│       ├── Navbar.tsx            # Academic header & status indicators
│       ├── FilterBar.tsx         # Multi-axis dropdowns & search
│       ├── KpiCards.tsx          # 4 dynamic executive metric cards
│       ├── TouristDataTable.tsx  # Paginated table with CSV download
│       ├── ProjectFooter.tsx     # Institutional metadata footer
│       └── charts/
│           ├── PopularDestinationsChart.tsx  # Bar Chart (Destinations)
│           ├── VisitorTrendsChart.tsx        # Line Chart (Monthly Trends)
│           ├── PreferencesDonutChart.tsx     # Donut Chart (Interests)
│           └── SpendingAnalysisChart.tsx     # Bar Chart (Group Spending)
```

---

## 💻 How to Run the Project

### Option 1: Modern Development Server (Recommended)
In the project directory (`e:\tourist`), run:

```bash
# Start local development server
npm run dev
```
Open your browser and navigate to:
👉 `http://localhost:3000`

---

### Option 2: Production Build & Preview
To test the optimized production build:

```bash
# Build the application
npm run build

# Preview the production build
npm run preview
```

---

### Option 3: Instant Zero-Setup Lab Presentation (Offline / Lab Computers)
If you need to show the project on a college lab PC or presentation projector without Node.js installed:
1. Navigate to `e:\tourist\`.
2. Double-click **`standalone_dashboard.html`**.
3. It will immediately open in Google Chrome, Microsoft Edge, or Mozilla Firefox with all charts, filters, metrics, and dataset table fully functional!

---

## 🎓 Viva & Presentation Talking Points (For CSD Branch)

1. **Client-Side Data Science Pipeline**:
   - Demonstrates how large data arrays can be manipulated in memory using declarative transformations (`filter`, `map`, `reduce`).
   - Slices multidimensional tensors (Season, Region, Travel Group) in $O(N)$ linear time without unnecessary re-renders using React `useMemo`.

2. **Handling Time-Series & Seasonal Trends**:
   - Monthly visitor footfall is bucketed into temporal histograms (Jan–Dec) to compute seasonality indices.

3. **Data Integrity & Export**:
   - Enables exporting the actively filtered dataframe directly to CSV for downstream feature engineering or exploratory data analysis (EDA) in Jupyter Notebooks.
