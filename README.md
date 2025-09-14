# 📊 French Postal Code Dashboard

An interactive web-based dashboard for analyzing French postal code data with beautiful visualizations, statistics, and an interactive map. **Now supports multiple CSV files with different colored markers for data comparison and overlay!**

![Multi-file Dashboard](https://github.com/user-attachments/assets/75577a97-6080-405a-9d54-21a7605412ec)

## ✨ Features

### 📁 **Multi-File Upload System**
- **Drag & Drop** multiple CSV files directly onto the interface
- **Click to browse** for multiple file selection
- **Real-time validation** with user-friendly error messages
- **Flexible CSV format support** - automatically detects column headers
- **Individual file management** - show/hide/delete files independently

### 🎨 **Multi-File Visualization**
- **Color-coded markers** - each file gets a unique color on the map
- **Interactive legend** showing active files and their colors
- **File overlay capability** - visualize multiple datasets simultaneously
- **Individual file controls** - toggle visibility without losing data
- **Combined statistics** from all visible files

### 🗺️ **Interactive Map of France**
- **Color-coded departments** based on employee/data intensity
- **Hover tooltips** showing detailed department information
- **Click highlighting** when selecting postal codes
- **Visual legend** with intensity scale
- **Responsive SVG map** that scales with screen size

### 📈 **Comprehensive Statistics**
- **Key metrics dashboard**: Total postal codes, employees, averages, maximums
- **Top 10 postal codes** ranking with click-to-highlight
- **Real-time search** and filtering functionality
- **Department distribution bar chart** showing top 15 departments

### 🎨 **Modern UI/UX**
- **Glassmorphism design** with backdrop blur effects
- **Smooth animations** and hover effects
- **Responsive layout** (mobile, tablet, desktop)
- **Professional gradient themes**
- **Interactive tooltips** and visual feedback

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- CSV file with French postal code data

### Installation

1. **Download the HTML file**
   ```bash
   # Clone this repository or download the HTML file
   wget [your-dashboard-file].html
   ```

2. **Open in browser**
   ```bash
   # Simply open the HTML file in your browser
   open dashboard.html
   # OR double-click the file
   ```

### Usage

1. **Launch the dashboard** by opening the HTML file in your web browser
2. **Upload your CSV file(s)** using one of these methods:
   - Drag and drop one or multiple CSV files onto the upload area
   - Click "📂 Choisir un/des fichier(s) CSV" to browse and select multiple files
3. **Manage your files** in the file management panel:
   - Toggle file visibility with the 👁️/🚫 buttons
   - Remove individual files with the 🗑️ button
   - Add more files with "➕ Ajouter un autre fichier"
4. **View the analysis** - the dashboard will automatically process and display your combined data
5. **Interact with the visualizations**:
   - Hover over map departments for details
   - Search postal codes across all visible files in real-time
   - Click on top postal codes to highlight on map
   - Use the map legend to identify which file each marker represents

## 📋 CSV Format Requirements

### Required Columns
Your CSV file must contain at least two columns:

| Column Type | Accepted Names | Example |
|-------------|----------------|---------|
| **Postal Codes** | `Code Postaux`, `CP`, `postal`, `code` | 75001, 69001, 13001 |
| **Count Data** | `Count de Matricule Ouvrant-droit`, `Count`, `nombre`, `matricule`, `total` | 25, 18, 12 |

### Optional Columns
For enhanced precision, you can include commune information:

| Column Type | Accepted Names | Example |
|-------------|----------------|---------|
| **Commune** | `Commune`, `commune`, `ville`, `city`, `municipality` | Paris 1er Arrondissement, Lyon |

### Supported Formats

**Format 1 (Recommended - with commune):**
```csv
Code Postaux,Commune,Count de Matricule Ouvrant-droit
75001,Paris 1er Arrondissement,25
75002,Paris 2e Arrondissement,18
69001,Lyon 1er Arrondissement,12
13001,Marseille 1er Arrondissement,30
```

**Format 2 (Original - postal code only):**
```csv
Code Postaux,Count de Matricule Ouvrant-droit
75001,25
75002,18
69001,12
13001,30
```

**Format 3 (Alternative column names):**
```csv
CP,Commune,Nombre
75001,Paris 1er Arrondissement,25
75002,Paris 2e Arrondissement,18
69001,Lyon 1er Arrondissement,12
13001,Marseille 1er Arrondissement,30
```

**Format 4 (Generic):**
```csv
postal,city,total
75001,Paris 1er Arrondissement,25
75002,Paris 2e Arrondissement,18
69001,Lyon 1er Arrondissement,12
13001,Marseille 1er Arrondissement,30
```

### Data Requirements
- ✅ CSV file format (`.csv` extension)
- ✅ French postal codes (5 digits)
- ✅ Header row with column names
- ✅ Positive integer values for counts
- ✅ UTF-8 encoding (recommended)

### Why Include Commune Information?

Including commune names in your CSV provides several benefits:

- **🎯 Enhanced Precision**: One postal code can be shared by multiple communes (e.g., 54490 is shared by 7 communes)
- **📍 Accurate Mapping**: Multiple communes can have the same postal code, so specifying the commune ensures precise geolocation
- **📊 Better Analytics**: More accurate geographical distribution analysis
- **🔄 Fallback Support**: If commune geocoding fails, the system automatically falls back to postal code-only matching

**Example of postal code sharing:**
- 54490: Piennes, Cons-la-Grandville, Ville-Houdlémont, Saulnes, Errouville, Crusnes, Gorcy
- Each gets mapped to its specific location when commune is provided

## 🛠️ Technical Details

### Built With
- **HTML5** - Structure and semantics
- **CSS3** - Modern styling with gradients, animations, and glassmorphism
- **Vanilla JavaScript** - Interactive functionality
- **PapaParse** - CSV parsing library
- **SVG** - Scalable vector graphics for map and charts

### Browser Compatibility
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### Performance
- **Lightweight** - No heavy frameworks, fast loading
- **Responsive** - Optimized for all screen sizes
- **Memory efficient** - Handles large CSV files smoothly

## 📊 Dashboard Components

### 1. Statistics Panel
- **Total Postal Codes**: Number of unique postal codes
- **Total Employees**: Sum of all count values
- **Average per Code**: Mean employees per postal code
- **Maximum**: Highest single postal code count

### 2. Interactive Map
- **Department visualization** with color intensity
- **Hover tooltips** showing department details
- **Click-to-highlight** functionality
- **Legend** explaining color coding

### 3. Search & Filter
- **Real-time search** postal codes
- **Dynamic filtering** of results
- **Top rankings** display

### 4. Bar Chart
- **Top 15 departments** by total count
- **Interactive bars** with hover effects
- **Labeled axes** and values

## 🎨 Customization

### Color Scheme
The dashboard uses a modern gradient color palette:
- **Primary**: `#667eea` to `#764ba2`
- **Background**: Dynamic gradient
- **Accents**: Various blue tones
- **Map Colors**: Intensity-based blue scale

### Modifying Colors
To customize colors, edit the CSS variables in the `<style>` section:
```css
/* Example color modifications */
.upload-btn.primary {
    background: linear-gradient(135deg, #your-color-1, #your-color-2);
}
```

## 🐛 Troubleshooting

### Common Issues

**Dashboard not loading:**
- Ensure you're opening the HTML file in a modern browser
- Check browser console for JavaScript errors

**CSV upload fails:**
- Verify your CSV has the correct column headers
- Check that postal codes are 5-digit French codes
- Ensure file size is reasonable (<10MB recommended)

**Map not displaying correctly:**
- Clear browser cache and reload
- Try a different browser
- Check for JavaScript errors in console

**Search not working:**
- Ensure data loaded successfully
- Check for special characters in postal codes
- Verify CSV encoding (UTF-8 recommended)

## 📈 Performance Tips

- **File Size**: Keep CSV files under 10MB for optimal performance
- **Data Cleaning**: Remove empty rows and invalid postal codes before upload
- **Browser Memory**: Close other tabs when analyzing large datasets
- **Mobile Usage**: Use desktop/tablet for better experience with large datasets

## 🤝 Contributing

This is a single-file dashboard project. To contribute:

1. **Fork** the project
2. **Modify** the HTML file with your improvements
3. **Test** across different browsers and devices
4. **Submit** a pull request with your changes

### Development Guidelines
- Maintain vanilla JavaScript (no frameworks)
- Keep all code in single HTML file
- Follow existing code style and structure
- Test with various CSV formats
- Ensure mobile responsiveness

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

If you encounter issues or need help:

1. **Check the troubleshooting section** above
2. **Verify your CSV format** matches requirements
3. **Test with sample data** to isolate issues
4. **Check browser console** for error messages

## 🎯 Use Cases

### Business Analytics
- **Employee distribution** analysis by region across multiple divisions/departments
- **Regional performance** tracking and comparison between different datasets
- **Geographic insights** for business planning with data overlay capabilities
- **Multi-year comparison** by loading different time periods as separate files

### Research & Education
- **Demographic studies** using multiple postal code datasets
- **Geographic data visualization** projects with comparative analysis
- **Statistical analysis** teaching tool with multi-dataset support

### Government & Public Sector
- **Population distribution** analysis across different demographics
- **Resource allocation** planning with multiple data sources
- **Public service** optimization using overlaid datasets

## 📊 Sample Data Structure

Here's what your data might look like:

**With commune information (recommended):**
```csv
Code Postaux,Commune,Count de Matricule Ouvrant-droit
75001,Paris 1er Arrondissement,45
75002,Paris 2e Arrondissement,32
75003,Paris 3e Arrondissement,28
69001,Lyon 1er Arrondissement,67
69002,Lyon 2e Arrondissement,53
13001,Marseille 1er Arrondissement,89
13002,Marseille 2e Arrondissement,76
33000,Bordeaux,34
44000,Nantes,29
85000,La Roche-sur-Yon,156
54490,Piennes,25
54490,Cons-la-Grandville,18
54490,Saulnes,30
```

**Standard format (postal code only):**
```csv
Code Postaux,Count de Matricule Ouvrant-droit
75001,45
75002,32
75003,28
69001,67
69002,53
13001,89
13002,76
33000,34
44000,29
85000,156
```

## 🔮 Future Enhancements

Potential features for future versions:
- **Export functionality** (PDF, PNG, CSV) for multi-file datasets
- **File comparison tools** with side-by-side statistics
- **Time-series analysis** for historical data comparison
- **Advanced filtering** options per file
- **Custom color schemes** for file differentiation
- **File merging capabilities** for data consolidation
- **API integration** for real-time data from multiple sources

---

**Made with ❤️ for French postal code analysis - Now with multi-file support!**
