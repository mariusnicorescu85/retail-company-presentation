# Opatra Sales Dashboard

## Real-Time Sales Analytics Platform

---

## 📊 Project Overview

**Opatra Sales Dashboard** is a modern, real-time sales analytics platform that connects to Airtable to provide comprehensive insights into employee performance, shop sales, and business metrics.

### Key Highlights

- **Real-time data** from Airtable
- **Interactive visualizations** with advanced charts
- **Multi-dimensional filtering** (Shop, Employee, Year)
- **Advanced BI metrics** (ROI, Profit Margin, Efficiency Ratio)
- **Performance rankings** and trend analysis

---

## 🎯 Problem Statement

### Business Challenges

- Need for real-time visibility into sales performance
- Manual data analysis is time-consuming
- Lack of actionable insights for decision-making
- Difficulty tracking employee performance across multiple shops
- No centralized view of sales metrics and trends

### Solution

A unified dashboard that automatically pulls data from Airtable and presents it in an intuitive, interactive format with actionable insights.

---

## 🏗️ Architecture & Technology Stack

### Frontend

- **Next.js 14** - React framework with App Router
- **React 18** - Modern React with hooks
- **Recharts** - Professional charting library
- **Lucide React** - Modern icon library

### Backend

- **Next.js API Routes** - Serverless API endpoints
- **Airtable API** - Data source integration

### Key Features

- ✅ Server-side rendering (SSR)
- ✅ Client-side interactivity
- ✅ Environment variable configuration
- ✅ Error handling and validation
- ✅ Responsive design

---

## 🔌 Airtable Integration

### API Route Features

- **Secure API key management** (environment variables or query params)
- **Pagination support** - Handles large datasets automatically
- **Error handling** - Comprehensive error messages
- **Table name sanitization** - Robust data fetching

### Configuration Options

1. **Environment Variables** (Recommended)

   - `AIRTABLE_API_KEY`
   - `NEXT_PUBLIC_AIRTABLE_BASE_ID`
   - `NEXT_PUBLIC_AIRTABLE_TABLE_NAME`

2. **Manual Configuration**
   - User-friendly config screen
   - Runtime API key input
   - Base ID and table name selection

---

## 📈 Dashboard Features

### 1. Key Performance Indicators (KPIs)

- **Total Sales** - Aggregate sales across filters
- **Average Sales** - Mean sales per record
- **Total Salary** - Cumulative salary costs
- **Average Sales per Day** - Daily performance metric
- **ROI (Return on Investment)** - Profitability indicator
- **Cost per Sale** - Efficiency metric
- **Profit Margin** - Percentage profitability
- **Efficiency Ratio** - Sales to salary ratio

### 2. Interactive Visualizations

#### Sales Trends

- **Line Charts** - Time-series sales data
- **Month-over-Month Comparison** - Growth tracking
- **Trend Indicators** - Visual up/down arrows

#### Performance Analysis

- **Bar Charts** - Comparative analysis
- **Composed Charts** - Multi-metric visualization
- **Area Charts** - Cumulative trends

#### Employee & Shop Analytics

- **Performance Rankings** - Top and bottom performers
- **Shop Comparison** - Cross-location analysis
- **Employee Breakdown** - Individual performance metrics

### 3. Advanced Filtering

#### Multi-Dimensional Filters

- **Shop Filter** - Filter by specific shop (e.g., "Opatra")
- **Employee Filter** - Individual employee analysis
- **Year Filter** - Time-based filtering
- **Combined Filters** - Multiple filters simultaneously

### 4. Salary Calculation

#### Flexible Rate System

- **Hourly Rate** - Configurable hourly wage (default: $15)
- **Daily Rate** - Alternative daily rate (default: $120)
- **Toggle Between Rates** - Switch calculation method
- **Automatic Calculation** - Based on worked hours/days

---

## 💡 Key Metrics & Insights

### Business Intelligence Metrics

1. **ROI Calculation**

   ```
   ROI = ((Total Sales - Total Salary) / Total Salary) × 100
   ```

   - Measures return on employee investment
   - Higher ROI = Better profitability

2. **Cost per Sale**

   ```
   Cost per Sale = Total Salary / Total Sales
   ```

   - Lower is better
   - Indicates efficiency of sales operations

3. **Profit Margin**

   ```
   Profit Margin = ((Total Sales - Total Salary) / Total Sales) × 100
   ```

   - Percentage of sales that is profit
   - Key indicator of business health

4. **Efficiency Ratio**
   ```
   Efficiency Ratio = Total Sales / Total Salary
   ```
   - Sales generated per dollar of salary
   - Higher ratio = More efficient operations

---

## 🎨 User Interface

### Design Principles

- **Clean & Modern** - Minimalist design
- **Responsive** - Works on all screen sizes
- **Intuitive** - Easy to navigate
- **Color-coded** - Visual indicators for trends
- **Interactive** - Hover states and tooltips

### Visual Elements

- **Status Indicators** - Connection status, loading states
- **Icon System** - Lucide React icons for clarity
- **Chart Tooltips** - Detailed information on hover
- **Filter Controls** - Dropdown selectors
- **Refresh Button** - Manual data reload

---

## 🔄 Data Flow

```
Airtable Database
    ↓
Next.js API Route (/api/airtable)
    ↓
Data Processing & Validation
    ↓
React State Management
    ↓
Filtering & Calculations
    ↓
Chart Rendering (Recharts)
    ↓
User Interface
```

### Data Processing Pipeline

1. **Fetch** - Retrieve data from Airtable API
2. **Validate** - Check API keys and parameters
3. **Transform** - Process and structure data
4. **Filter** - Apply user-selected filters
5. **Calculate** - Compute KPIs and metrics
6. **Visualize** - Render charts and displays

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- Airtable account with API access
- Airtable base with sales data

### Installation

```bash
npm install
```

### Configuration

1. Set environment variables:

   ```env
   AIRTABLE_API_KEY=your_api_key
   NEXT_PUBLIC_AIRTABLE_BASE_ID=your_base_id
   NEXT_PUBLIC_AIRTABLE_TABLE_NAME=Employees
   ```

2. Or use the in-app configuration screen

### Running the Application

```bash
# Development
npm run dev

# Production Build
npm run build
npm start
```

---

## 📊 Sample Data Structure

The dashboard expects Airtable records with the following fields:

- `month` - Date/period identifier
- `shop` - Shop name (e.g., "Opatra")
- `employee` - Employee name
- `workedDays` - Number of days worked
- `workedHours` - Total hours worked
- `totalSales` - Sales amount
- `additionalSales` - Extra sales (optional)
- `adjustedSales` - Total adjusted sales
- `totalShopSales` - Shop-wide sales
- `salary` - Calculated salary

---

## 🎯 Use Cases

### 1. Management Dashboard

- Monitor overall sales performance
- Track shop-level metrics
- Identify trends and patterns

### 2. Employee Performance Review

- Individual employee analysis
- Performance comparisons
- Salary vs. sales efficiency

### 3. Business Planning

- ROI analysis for staffing decisions
- Cost optimization insights
- Growth trend identification

### 4. Real-Time Monitoring

- Live data updates from Airtable
- Quick access to current metrics
- Instant filtering and analysis

---

## 🔒 Security Features

- **API Key Protection** - Environment variable storage
- **Server-side Validation** - Input sanitization
- **Error Handling** - Graceful failure modes
- **Secure API Calls** - Bearer token authentication

---

## 📈 Future Enhancements

### Potential Improvements

- [ ] Export functionality (CSV, PDF)
- [ ] Email reports and alerts
- [ ] Custom date range selection
- [ ] Advanced analytics (predictions, forecasting)
- [ ] Multi-user authentication
- [ ] Dashboard customization
- [ ] Mobile app version
- [ ] Real-time notifications

---

## 🛠️ Technical Highlights

### Code Quality

- **Modern React Patterns** - Hooks, functional components
- **Performance Optimization** - useMemo for calculations
- **Type Safety** - Ready for TypeScript migration
- **Error Boundaries** - Comprehensive error handling

### Best Practices

- ✅ Component-based architecture
- ✅ Separation of concerns
- ✅ Reusable utilities
- ✅ Environment-based configuration
- ✅ Responsive design principles

---

## 📝 Project Structure

```
opatra-sales-dashboard/
├── app/
│   ├── api/
│   │   └── airtable/
│   │       └── route.js      # API endpoint
│   ├── layout.js              # Root layout
│   └── page.js                # Main dashboard
├── next.config.js             # Next.js configuration
└── package.json               # Dependencies
```

---

## 🎓 Key Learnings & Technologies

### Technologies Mastered

- Next.js App Router
- React Hooks (useState, useMemo, useEffect)
- Recharts for data visualization
- Airtable API integration
- Serverless API routes
- Environment variable management

### Skills Demonstrated

- Full-stack development
- Data visualization
- API integration
- State management
- Responsive UI design
- Business intelligence metrics

---

## 📞 Project Summary

**Opatra Sales Dashboard** is a production-ready application that transforms raw Airtable data into actionable business insights. It combines modern web technologies with practical business intelligence to provide a powerful analytics platform.

### Value Proposition

- ⚡ **Real-time** - Live data from Airtable
- 📊 **Comprehensive** - Multiple metrics and visualizations
- 🎯 **Actionable** - Clear insights for decision-making
- 🔧 **Flexible** - Customizable filters and settings
- 🚀 **Scalable** - Built on modern, performant stack

---

## 🙏 Thank You

Questions & Discussion

---

_Built with Next.js, React, and Recharts_
_Connected to Airtable for real-time data_
