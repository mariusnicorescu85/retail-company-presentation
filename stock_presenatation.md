# Stock Dashboard Presentation

## A Comprehensive Inventory Management System

---

## Slide 1: Project Overview

### Stock Runway & Reorder Dashboard

A real-time inventory management system built to optimize stock levels, prevent stockouts, and streamline reordering processes.

**Key Objectives:**

- Real-time stock monitoring
- Automated runway calculations
- Proactive reorder alerts
- Multi-shop allocation management
- Category-based demand analysis

---

## Slide 2: The Problem We Solved

### Challenges in Inventory Management

**Before:**

- Manual stock tracking across multiple products
- Reactive reordering (too late or too early)
- No visibility into stock runway
- Difficulty allocating stock across multiple shops
- Limited insights into category-level demand

**After:**

- Automated calculations and alerts
- Proactive reorder recommendations
- Real-time visibility into stock levels
- Intelligent shop allocation tools
- Data-driven category insights

---

## Slide 3: Solution Architecture

### Technology Stack

**Frontend:**

- Next.js 16 (App Router)
- React 19
- TypeScript
- Tailwind CSS 4

**Data & Integration:**

- Airtable API (real-time data)
- Server-side rendering (SSR)
- Client-side state management

**Visualization:**

- Recharts for sales history
- Custom UI components

**Key Features:**

- Server Components for performance
- Dynamic routing
- Responsive design

---

## Slide 4: Core Features - Main Dashboard

### Stock Runway & Reorder Dashboard

**Key Capabilities:**

1. **60-Day Stock Outlook**

   - Color-coded time buckets (0-7, 8-14, 15-30, 31-60 days)
   - Critical alerts for urgent items
   - Visual runway indicators

2. **Smart Filtering & Sorting**

   - View modes: Reorder, All, Combos
   - Sort by: Order date, Days left, Quantity, Stock levels
   - Real-time search

3. **Comprehensive Product Table**
   - Current stock + incoming stock
   - Monthly demand tracking
   - Days until runout
   - Recommended order quantities
   - Sales totals (Individual, Combo, Total)

---

## Slide 5: Core Features - Category Analysis

### Category Demand Overview

**Purpose:** Understand demand patterns at the category level

**Features:**

- Year-over-year comparison (2024, 2025)
- Category breakdown:
  - 19mm, 25mm styling tools
  - Titanium, Infrared, Ceramic tools
  - Sets and other categories

**What-If Scenarios:**

- Adjust stock levels
- Modify daily demand
- Change lead times
- See real-time runway calculations

**Benefits:**

- Strategic planning
- Category-level insights
- Historical demand analysis

---

## Slide 6: Core Features - Master Stock Allocation

### Multi-Shop Stock Management

**Problem Solved:** Allocating master stock across multiple retail locations

**Key Features:**

1. **Shop-Based Allocation**

   - Allocate stock to Opatra and PYT shops
   - Track daily demand per shop
   - Calculate shop-specific runway

2. **Bulk Operations**

   - Select multiple products
   - Bulk allocate to shops
   - Export to CSV

3. **Real-Time Calculations**

   - Master stock runway
   - Shop-level runway
   - Remaining stock tracking
   - Visual alerts for low stock

4. **Persistent Storage**
   - LocalStorage for allocations
   - Maintains state across sessions

---

## Slide 7: Core Features - Product Detail Pages

### Individual Product Insights

**Comprehensive Product View:**

1. **Sales History**

   - Monthly sales chart
   - Historical data visualization
   - Year-over-year comparisons

2. **Stock Information**

   - Current stock levels
   - Incoming stock
   - Effective stock calculations

3. **Demand Analysis**

   - Daily demand
   - Monthly totals
   - Same month last year comparison

4. **What-If Panel**

   - Interactive scenario modeling
   - Adjust stock, demand, lead times
   - Real-time runway calculations

5. **Supplier Information**
   - Lead times
   - Order-by dates
   - Recommended quantities

---

## Slide 8: Core Features - Comparison Tools

### Product Comparison Capabilities

**Compare Products:**

- Side-by-side product comparison
- Stock levels, demand, runway
- Quick decision making

**Compare One Product:**

- Detailed single product analysis
- Multiple scenario comparisons

**Use Cases:**

- Reorder prioritization
- Stock level optimization
- Demand pattern analysis

---

## Slide 9: Technical Highlights - Stock Math Engine

### Intelligent Calculations

**Core Algorithm (`StockMath.ts`):**

```typescript
computeStockDerived({
  currentStock,
  incomingStock,
  dailyDemand,
  leadTimeDays,
});
```

**Calculations:**

- Effective stock = Current + Incoming
- Days until runout = Effective stock / Daily demand
- Order-by date = Runout date - Lead time

**Features:**

- UTC date handling
- Null-safe calculations
- Real-time updates

---

## Slide 10: Technical Highlights - Data Integration

### Airtable Integration

**Seamless Data Flow:**

1. **Product Data**

   - Current stock levels
   - Incoming stock
   - Supplier information
   - Lead times

2. **Sales Data**

   - Monthly sales records
   - Historical trends
   - Category breakdowns

3. **Real-Time Updates**
   - 60-second cache for products
   - 300-second cache for suppliers
   - Force-dynamic pages for live data

**Benefits:**

- Single source of truth
- No data duplication
- Always up-to-date

---

## Slide 11: User Experience Design

### Modern, Intuitive Interface

**Design Principles:**

- Dark theme for reduced eye strain
- Color-coded alerts (Red/Amber/Green)
- Responsive design (mobile-friendly)
- Clear visual hierarchy

**UX Features:**

- Sticky table headers
- Hover states and transitions
- Loading states
- Error handling
- Breadcrumb navigation

**Accessibility:**

- Semantic HTML
- Keyboard navigation
- Screen reader friendly
- High contrast ratios

---

## Slide 12: Business Value

### Impact & Benefits

**Operational Efficiency:**

- ⏱️ Time saved: Automated calculations vs manual tracking
- 📊 Visibility: Real-time stock status across all products
- 🎯 Accuracy: Data-driven reorder recommendations

**Risk Mitigation:**

- 🚨 Early warning system for stockouts
- 📈 Proactive reordering
- ⚠️ Lead time vs runway alerts

**Strategic Insights:**

- 📉 Category-level demand patterns
- 📅 Historical sales analysis
- 🔮 What-if scenario planning

**Cost Savings:**

- Reduced stockouts = No lost sales
- Optimized inventory = Lower carrying costs
- Better planning = Improved cash flow

---

## Slide 13: Key Metrics & KPIs

### Dashboard Highlights

**Stock Health Indicators:**

- Items running out in 0-7 days (Critical)
- Items running out in 8-14 days (Urgent)
- Items running out in 15-30 days (Watch)
- Items running out in 31-60 days (Planning)

**Allocation Metrics:**

- Total units to order
- Master stock levels
- Shop allocation efficiency
- Remaining stock tracking

**Demand Metrics:**

- Monthly demand totals
- Daily demand rates
- Category demand breakdowns
- Year-over-year comparisons

---

## Slide 14: Technical Architecture

### System Design

```
┌─────────────────┐
│   Next.js App   │
│  (Server/Client) │
└────────┬────────┘
         │
         ├─── Server Components (Data Fetching)
         ├─── Client Components (Interactivity)
         │
┌────────▼────────┐
│  Airtable API   │
│  (Data Source)  │
└─────────────────┘
         │
         ├─── Products Table
         ├─── Monthly Sales
         ├─── Suppliers
         └─── PYT Products
```

**Key Patterns:**

- Server Components for data fetching
- Client Components for interactivity
- Hybrid rendering approach
- Optimized caching strategy

---

## Slide 15: Future Enhancements

### Potential Improvements

**Short-term:**

- Real shop data integration
- Automated reorder notifications
- Email/SMS alerts for critical items
- Multi-user support

**Medium-term:**

- Advanced analytics dashboard
- Predictive demand forecasting
- Integration with ordering systems
- Mobile app version

**Long-term:**

- AI-powered demand prediction
- Automated reordering
- Multi-warehouse support
- Advanced reporting suite

---

## Slide 16: Project Statistics

### By The Numbers

**Codebase:**

- ~3,500+ lines of TypeScript/React
- 15+ page components
- 10+ reusable components
- 2 core utility libraries

**Features:**

- 6 main views/pages
- 3 comparison tools
- Real-time calculations
- Multiple data sources

**Data:**

- Products tracked: 100+
- Categories: 7
- Shops: 5 (placeholder)
- Historical data: 2+ years

---

## Slide 17: Lessons Learned

### Key Takeaways

**Technical:**

- Server Components provide excellent performance
- TypeScript catches errors early
- Airtable API is powerful but requires careful caching
- Client-side state management is crucial for interactivity

**Design:**

- Color coding is essential for quick scanning
- Responsive design is non-negotiable
- Loading states improve perceived performance
- Dark theme reduces eye strain for long sessions

**Business:**

- Real-time data is critical for inventory management
- Automation saves significant time
- Visual alerts are more effective than numbers alone
- What-if scenarios enable better planning

---

## Slide 18: Demo Highlights

### What to Show

1. **Main Dashboard**

   - 60-day breakdown view
   - Filtering and sorting
   - Product table with alerts

2. **Category Analysis**

   - Year selection
   - Category breakdown
   - What-if panel

3. **Master Stock**

   - Shop allocation
   - Bulk operations
   - Runway calculations

4. **Product Detail**
   - Sales history chart
   - Stock information
   - What-if scenarios

---

## Slide 19: Conclusion

### Summary

**What We Built:**
A comprehensive, real-time inventory management dashboard that transforms how stock is monitored, allocated, and reordered.

**Key Achievements:**
✅ Real-time stock monitoring
✅ Automated runway calculations
✅ Multi-shop allocation system
✅ Category-level insights
✅ Historical sales analysis
✅ What-if scenario planning

**Impact:**

- Improved operational efficiency
- Reduced stockout risk
- Better inventory planning
- Data-driven decision making

---

## Slide 20: Questions & Discussion

### Thank You!

**Project Repository:**

- Next.js 16 + React 19
- TypeScript
- Tailwind CSS
- Airtable Integration

**Ready for:**

- Production deployment
- Further enhancements
- User feedback integration

---

## Appendix: Technical Details

### Key Files & Structure

```
app/
├── page.tsx              # Main dashboard
├── categories/           # Category analysis
├── master-stock/         # Shop allocation
├── product/[id]/         # Product details
├── compare/              # Comparison tools
└── components/           # Shared components

lib/
├── airtable.ts           # Airtable integration
└── StockMath.ts         # Calculation engine
```

### Environment Variables

- `AIRTABLE_API_KEY`
- `AIRTABLE_BASE_ID`
- Table name configurations

### Deployment Ready

- Vercel-optimized
- Environment variable support
- Production build tested
