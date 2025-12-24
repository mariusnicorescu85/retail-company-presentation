# Screenshot Guide for Systems Overview Presentation

This guide explains what screenshots to capture for each live system and how to add them to the presentation.

## 📸 Screenshot Recommendations

### System 4: Stock Forecasting & Ordering System
**Recommended Screenshot:**
- **Main Dashboard View** showing:
  - 60-day stock outlook with color-coded time buckets (0-7, 8-14, 15-30, 31-60 days)
  - Product table with stock levels, days until runout, and recommended order quantities
  - Filter options (Reorder, All, Combos)

**File to save as:** `screenshots/stock-dashboard.png`

**How to capture:**
1. Open the Stock Dashboard
2. Navigate to the main dashboard view
3. Ensure the table shows products with color-coded alerts
4. Take a full-page screenshot (browser DevTools → Device Toolbar → Toggle device → Capture screenshot)

---

### System 6: HR & Onboarding System
**Recommended Screenshot:**
- **Onboarding Form Interface** showing:
  - One of the multi-step form pages (Personal Details, Document Upload, or Bank Details)
  - Form fields and validation
  - Progress indicator (if visible)

**File to save as:** `screenshots/hr-onboarding.png`

**How to capture:**
1. Open the onboarding form
2. Navigate to a step that shows form fields clearly
3. Capture the form interface
4. Make sure the form looks complete and professional

---

### System 8: Customer Service & Warranty System

**Two screenshots recommended:**

#### 8a: AI Customer Support Dashboard
**Recommended Screenshot:**
- **Email Review Dashboard** showing:
  - Email queue/list with AI quality scores
  - Risk level indicators
  - Filter options
  - Action buttons (Approve, Reject, Escalate)

**File to save as:** `screenshots/customer-support-dashboard.png`

#### 8b: Warranty Registration Form
**Recommended Screenshot:**
- **Warranty Registration Form** showing:
  - Customer information fields
  - Product details section
  - Receipt upload interface
  - Form validation

**File to save as:** `screenshots/warranty-form.png`

---

### System 11: Staff Sales Evaluation & Profitability System
**Recommended Screenshot:**
- **Main Sales Dashboard** showing:
  - KPI cards at the top (Total Sales, ROI, Profit Margin, Efficiency Ratio)
  - Charts/visualizations (line charts, bar charts)
  - Employee performance table with metrics
  - Filter options (Shop, Employee, Year)

**File to save as:** `screenshots/sales-dashboard.png`

**How to capture:**
1. Open the Sales Dashboard
2. Ensure KPIs are visible at the top
3. Show charts/visualizations in the middle section
4. Include the employee table/performance metrics
5. Take a full-page or main section screenshot

---

## 📁 File Organization

Create a `screenshots` folder in the same directory as `systems_overview_presentation.html`:

```
presentation/
├── systems_overview_presentation.html
├── screenshots/
│   ├── stock-dashboard.png
│   ├── hr-onboarding.png
│   ├── customer-support-dashboard.png
│   ├── warranty-form.png
│   └── sales-dashboard.png
```

---

## 🖼️ How to Add Screenshots to the Presentation

1. **Take the screenshots** using the recommendations above
2. **Save them** in the `screenshots` folder with the exact filenames specified
3. **In the HTML file**, find the screenshot placeholders (they look like commented-out `<img>` tags)
4. **Uncomment the image tags** by removing the `<!-- -->` comments
5. **Comment out or remove** the placeholder divs

### Example:

**Before (placeholder):**
```html
<div class="screenshot-placeholder">
  <strong>📸 Screenshot: Stock Dashboard Main View</strong>
  <p>Recommended: Main dashboard...</p>
</div>
<!-- <img src="screenshots/stock-dashboard.png" alt="Stock Dashboard" class="screenshot" /> -->
```

**After (with screenshot):**
```html
<!-- <div class="screenshot-placeholder">...</div> -->
<img src="screenshots/stock-dashboard.png" alt="Stock Dashboard" class="screenshot" />
```

---

## 💡 Screenshot Tips

### Best Practices:
- **Full-width screenshots** work best (capture the full page width)
- **Clear and readable** - ensure text and numbers are visible
- **Show key features** - capture the most important elements
- **Consistent sizing** - try to keep similar zoom levels
- **Remove sensitive data** - blur or mask any personal/sensitive information before saving

### Browser Tools:
- **Chrome/Edge DevTools**: Press `F12` → Toggle device toolbar (`Ctrl+Shift+M`) → Capture screenshot
- **Firefox**: Press `F12` → Device Toolbar (`Ctrl+Shift+M`) → Screenshot tool
- **Full-page screenshots**: Browser extensions like "Full Page Screen Capture" can capture entire pages

### Image Format:
- Use **PNG format** for best quality (recommended)
- Alternative: **JPG/JPEG** if file size is a concern
- Keep file sizes reasonable (< 2MB per image)

---

## ✅ Checklist

- [ ] Screenshot folder created
- [ ] System 4: Stock dashboard screenshot captured
- [ ] System 6: HR onboarding form screenshot captured
- [ ] System 8a: Customer support dashboard screenshot captured
- [ ] System 8b: Warranty form screenshot captured
- [ ] System 11: Sales dashboard screenshot captured
- [ ] All placeholders replaced with actual `<img>` tags in HTML
- [ ] Screenshots display correctly when opening HTML file
- [ ] All screenshots are clear and readable

---

## 🚀 Quick Start

1. Create the screenshots folder: `mkdir screenshots`
2. Take screenshots according to recommendations above
3. Save them with the exact filenames specified
4. In `systems_overview_presentation.html`, find each placeholder and replace with the image tag
5. Open the HTML file in a browser to verify screenshots display correctly

Once screenshots are added, the presentation will be much more visual and compelling!

