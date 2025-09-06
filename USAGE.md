# 📊 French Postal Code Dashboard - Usage Guide

## Quick Start

1. **Open the Dashboard**
   - Open `dashboard.html` in your web browser
   - No installation required - it's a single-file application

2. **Upload Your Data**
   - Drag and drop a CSV file onto the upload area, OR
   - Click "📂 Choisir un fichier CSV" to browse for a file

3. **Explore Your Data**
   - View statistics in the left panel
   - Use the search box to filter postal codes
   - Click on top postal codes to highlight them on the map
   - Hover over map departments for details

## CSV Format Requirements

Your CSV file must contain at least two columns:

### Supported Column Names

**For Postal Codes:**
- `Code Postaux` (recommended)
- `CP`
- `postal` 
- `code`

**For Count Data:**
- `Count de Matricule Ouvrant-droit` (recommended)
- `Count`
- `nombre`
- `matricule`
- `total`

### Example CSV Format

```csv
Code Postaux,Count de Matricule Ouvrant-droit
75001,45
75002,32
69001,89
13001,123
```

## Features

### 📊 Statistics Panel
- **Total Postal Codes**: Number of unique postal codes
- **Total Employees**: Sum of all count values  
- **Average per Code**: Mean employees per postal code
- **Maximum**: Highest single postal code count

### 🔍 Search & Filter
- Type in the search box to filter postal codes in real-time
- Results update automatically as you type
- Clear the search box to show all data

### 🗺️ Interactive Map
- Color-coded departments based on data intensity
- Hover over departments to see tooltips with details
- Click on top postal codes to highlight their department on the map

### 📈 Top Rankings
- **Top 10 Postal Codes**: Ranked by employee count
- **Top 15 Departments**: Bar chart showing department totals
- Click on postal codes to highlight them on the map

## Testing

Run `test.html` to:
- Test the dashboard functionality
- Run automated tests for CSV parsing, search, and statistics
- Follow the manual testing guide

## Sample Data

Use `sample_data.csv` for testing:
- Contains 39 French postal codes
- Covers major departments (Paris, Lyon, Marseille, etc.)
- Ready to upload and explore

## Browser Support

- ✅ Chrome 80+
- ✅ Firefox 75+ 
- ✅ Safari 13+
- ✅ Edge 80+

## Troubleshooting

**Dashboard not loading?**
- Ensure you're using a modern browser
- Check that JavaScript is enabled

**CSV upload fails?**
- Verify your CSV has the correct column headers
- Check that postal codes are 5-digit French codes
- Ensure positive integer values for counts

**Map not displaying?**
- Clear browser cache and reload
- Try a different browser

## Technical Details

- **Single HTML file** with embedded CSS and JavaScript
- **No external dependencies** (all code is self-contained)
- **Responsive design** works on desktop, tablet, and mobile
- **Glassmorphism UI** with modern animations and effects