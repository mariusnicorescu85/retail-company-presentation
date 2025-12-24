# PYT Systems Overview Presentation

A comprehensive presentation covering all 12 company-provided systems for PYT / PYT PLUS franchise operations.

## Overview

This presentation provides a complete overview of all systems, their purposes, implementation methods, and critical rules. Systems are marked with their current status (Live or In Development).

## Systems Included

1. **Brand & Concept System** - In Development
2. **Product & Pricing Control System** - In Development
3. **Low-Capital Kiosk Sourcing & Deployment System** - In Development
4. **Stock Forecasting & Ordering System** - ✅ Live
5. **Recruitment & Trial Booking System** - In Development
6. **HR & Onboarding System** - ✅ Live
7. **Training System: Academy (Online + Physical)** - In Development
8. **Customer Service & Warranty System** - ✅ Live
9. **Daily Operations & Control Logic** - In Development
10. **Performance Threshold System** - In Development
11. **Staff Sales Evaluation & Profitability System** - ✅ Live
12. **Pay-Structure Profit Benchmark System** - In Development

## Features

- **Interactive Navigation**: Use arrow keys or navigation buttons
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Status Indicators**: Clear visual distinction between live and in-development systems
- **Keyboard & Touch Support**: Full keyboard navigation and swipe gestures

## Hosting on Vercel

### Option 1: Direct HTML Upload

Simply upload `systems_overview_presentation.html` to Vercel:

1. Create a new project on Vercel
2. Upload the HTML file
3. Vercel will automatically serve it

### Option 2: Using Git

1. Create a repository with the HTML file
2. Connect to Vercel
3. Vercel will automatically deploy

### Option 3: Static Site Configuration

For a more structured approach, you can create a simple structure:

```
/
  index.html (rename systems_overview_presentation.html to index.html)
  vercel.json (optional)
```

Example `vercel.json`:
```json
{
  "rewrites": [
    { "source": "/(.*)", "destination": "/systems_overview_presentation.html" }
  ]
}
```

## Usage

- **Next Slide**: Right Arrow, Down Arrow, or "Next" button
- **Previous Slide**: Left Arrow, Up Arrow, or "Previous" button
- **Mobile**: Swipe left/right to navigate

## Notes

- The presentation is self-contained (no external dependencies)
- All styles and scripts are embedded
- Works offline once downloaded
- Compatible with all modern browsers

