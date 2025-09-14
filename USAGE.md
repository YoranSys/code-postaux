# 📊 French Postal Code Dashboard - Usage Guide

## Quick Start

1. **Open the Dashboard**
   - Open `dashboard.html` in your web browser
   - No installation required - it's a single-file application

2. **Upload Your Data**
   - Drag and drop one or multiple CSV files onto the upload area, OR
   - Click "📂 Choisir un/des fichier(s) CSV" to browse and select multiple files

3. **Manage Multiple Files** (New Feature!)
   - Use the file management panel to control each file individually
   - Toggle file visibility with 👁️/🚫 buttons 
   - Remove files with 🗑️ buttons
   - Add more files anytime with "➕ Ajouter un autre fichier"

4. **Explore Your Data**
   - View combined statistics from all visible files in the left panel
   - Each file appears in a different color on the map
   - Use the map legend to identify which file each marker represents
   - Use the search box to filter postal codes across all visible files
   - Click on top postal codes to highlight them on the map
   - Hover over map departments for details

## 🎨 Multi-File Features

### Automatic Color Assignment
Each uploaded file gets a unique color for easy identification:
- **File 1**: Blue (#667eea)
- **File 2**: Red (#e74c3c) 
- **File 3**: Green (#27ae60)
- **File 4**: Orange (#f39c12)
- **And more colors for additional files...**

### File Management Panel
- **Individual Controls**: Show/hide each file independently
- **File Statistics**: See postal codes count and employee total per file  
- **Color Indicators**: Visual circles show each file's map color
- **Bulk Actions**: Add more files or clear all at once

### Interactive Map Legend
- **Auto-appears**: Shows when multiple files are visible
- **Color Reference**: Links file names to their map colors
- **Live Updates**: Changes as you show/hide files

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

**For Commune (optional, but recommended for precision):**
- `Commune` (recommended)
- `commune`
- `ville`
- `city`
- `municipality`

### Example CSV Formats

**Format 1: With commune information (recommended)**
```csv
Code Postaux,Commune,Count de Matricule Ouvrant-droit
75001,Paris 1er Arrondissement,45
75002,Paris 2e Arrondissement,32
69001,Lyon 1er Arrondissement,89
13001,Marseille 1er Arrondissement,123
54490,Piennes,25
54490,Cons-la-Grandville,18
```

**Format 2: Standard (postal code only)**
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