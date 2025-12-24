---
marp: true
theme: default
paginate: true
style: |
  section {
    font-family: 'Segoe UI', Arial, sans-serif;
  }
  h1 {
    color: #2563eb;
    font-size: 2.5em;
  }
  h2 {
    color: #1e40af;
    font-size: 2em;
  }
---

# Opatra Sales Dashboard

## Real-Time Sales Analytics Platform

**Transforming Airtable Data into Actionable Business Insights**

---

## 📊 Project Overview

**Opatra Sales Dashboard** is a modern, real-time sales analytics platform

### Key Features

- ✅ Real-time data from Airtable
- ✅ Interactive visualizations
- ✅ Multi-dimensional filtering
- ✅ Advanced BI metrics
- ✅ Performance rankings

**Built with Next.js 14 & React 18**

---

## 🎯 Problem Statement

### Business Challenges

- Need for real-time visibility into sales performance
- Manual data analysis is time-consuming
- Lack of actionable insights
- Difficulty tracking employee performance
- No centralized view of metrics

### Our Solution

**A unified dashboard that automatically pulls data from Airtable and presents it in an intuitive, interactive format**

---

## 🏗️ Technology Stack

### Frontend

- **Next.js 14** - React framework with App Router
- **React 18** - Modern React with hooks
- **Recharts** - Professional charting library
- **Lucide React** - Modern icon library

### Backend

- **Next.js API Routes** - Serverless endpoints
- **Airtable API** - Data source integration

---

## 🔌 Airtable Integration

### API Route Features

- Secure API key management
- Automatic pagination for large datasets
- Comprehensive error handling
- Table name sanitization

### Configuration Options

1. **Environment Variables** (Recommended)
2. **Manual Configuration** via UI

---

## 📈 Dashboard Features - KPIs

### Key Performance Indicators

| Metric               | Description                     |
| -------------------- | ------------------------------- |
| **Total Sales**      | Aggregate sales across filters  |
| **ROI**              | Return on Investment percentage |
| **Profit Margin**    | Percentage profitability        |
| **Efficiency Ratio** | Sales per dollar of salary      |
| **Cost per Sale**    | Salary cost efficiency          |

---

## 📊 Visualizations

### Chart Types

- **Line Charts** - Time-series sales trends
- **Bar Charts** - Comparative analysis
- **Composed Charts** - Multi-metric views
- **Area Charts** - Cumulative trends

### Interactive Features

- Hover tooltips with detailed data
- Click-to-filter capabilities
- Responsive design for all devices

---

## 🔍 Advanced Filtering

### Multi-Dimensional Filters

- **Shop Filter** - Filter by specific location
- **Employee Filter** - Individual analysis
- **Year Filter** - Time-based filtering
- **Combined Filters** - Multiple filters simultaneously

**Real-time updates** as filters change

---

## 💰 Salary Calculation

### Flexible Rate System

- **Hourly Rate** - Configurable (default: $15/hr)
- **Daily Rate** - Alternative (default: $120/day)
- **Toggle Between Rates** - Switch calculation method
- **Automatic Calculation** - Based on worked hours/days

---

## 📐 Business Intelligence Metrics

### ROI Calculation

```
ROI = ((Total Sales - Total Salary) / Total Salary) × 100
```

Measures return on employee investment

### Profit Margin

```
Profit Margin = ((Total Sales - Total Salary) / Total Sales) × 100
```

Percentage of sales that is profit

### Efficiency Ratio

```
Efficiency Ratio = Total Sales / Total Salary
```

Sales generated per dollar of salary

---

## 🔄 Data Flow Architecture

```
Airtable Database
    ↓
Next.js API Route
    ↓
Data Processing
    ↓
React State Management
    ↓
Filtering & Calculations
    ↓
Chart Rendering
    ↓
User Interface
```

---

## 🎨 User Interface

### Design Principles

- **Clean & Modern** - Minimalist design
- **Responsive** - All screen sizes
- **Intuitive** - Easy navigation
- **Color-coded** - Visual trend indicators
- **Interactive** - Hover states and tooltips

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- Airtable account with API access

### Quick Start

```bash
npm install
npm run dev
```

### Configuration

Set environment variables or use in-app config screen

---

## 📊 Sample Data Structure

### Expected Airtable Fields

- `month` - Date/period
- `shop` - Shop name
- `employee` - Employee name
- `workedDays` / `workedHours`
- `totalSales` / `adjustedSales`
- `totalShopSales`
- `salary` - Calculated

---

## 🎯 Use Cases

### 1. Management Dashboard

Monitor overall sales performance and shop-level metrics

### 2. Employee Performance Review

Individual analysis and performance comparisons

### 3. Business Planning

ROI analysis for staffing decisions and cost optimization

### 4. Real-Time Monitoring

Live data updates with instant filtering

---

## 🔒 Security Features

- ✅ API Key Protection via environment variables
- ✅ Server-side Validation
- ✅ Input Sanitization
- ✅ Secure API Calls with Bearer tokens
- ✅ Comprehensive Error Handling

---

## 📈 Future Enhancements

- Export functionality (CSV, PDF)
- Email reports and alerts
- Custom date range selection
- Advanced analytics (predictions)
- Multi-user authentication
- Dashboard customization
- Mobile app version

---

## 🛠️ Technical Highlights

### Code Quality

- Modern React Patterns (Hooks)
- Performance Optimization (useMemo)
- Component-based Architecture
- Separation of Concerns
- Responsive Design Principles

---

## 📝 Project Structure

```
opatra-sales-dashboard/
├── app/
│   ├── api/airtable/route.js
│   ├── layout.js
│   └── page.js
├── next.config.js
└── package.json
```

**Clean, organized, and maintainable**

---

## 🎓 Key Technologies & Skills

### Technologies

- Next.js App Router
- React Hooks
- Recharts
- Airtable API
- Serverless Architecture

### Skills Demonstrated

- Full-stack Development
- Data Visualization
- API Integration
- State Management
- Business Intelligence

---

## 💡 Value Proposition

### Why Opatra Sales Dashboard?

- ⚡ **Real-time** - Live data from Airtable
- 📊 **Comprehensive** - Multiple metrics
- 🎯 **Actionable** - Clear insights
- 🔧 **Flexible** - Customizable filters
- 🚀 **Scalable** - Modern, performant stack

---

## 📞 Summary

**Opatra Sales Dashboard** transforms raw Airtable data into actionable business insights

### Production-Ready Features

- Real-time data synchronization
- Advanced analytics and KPIs
- Interactive visualizations
- Flexible filtering system
- Secure API integration

---

## 🙏 Thank You

### Questions & Discussion

**Built with Next.js, React, and Recharts**  
**Connected to Airtable for real-time data**

---
