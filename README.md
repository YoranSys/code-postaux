# 📊 French Postal Code Dashboard

An interactive web-based dashboard for analyzing French postal code data with beautiful visualizations, statistics, and an interactive map.

![Dashboard Preview](https://via.placeholder.com/800x400/667eea/ffffff?text=Dashboard+Preview)

## ✨ Features

### 📁 **File Upload System**
- **Drag & Drop** CSV files directly onto the interface
- **Click to browse** file selection
- **Real-time validation** with user-friendly error messages
- **Flexible CSV format support** - automatically detects column headers

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
2. **Upload your CSV file** using one of these methods:
   - Drag and drop the CSV file onto the upload area
   - Click "📂 Choisir un fichier CSV" to browse and select
3. **View the analysis** - the dashboard will automatically process and display your data
4. **Interact with the visualizations**:
   - Hover over map departments for details
   - Search postal codes in real-time
   - Click on top postal codes to highlight on map

## 📋 CSV Format Requirements

### Required Columns
Your CSV file must contain at least two columns:

| Column Type | Accepted Names | Example |
|-------------|----------------|---------|
| **Postal Codes** | `Code Postaux`, `CP`, `postal`, `code` | 75001, 69001, 13001 |
| **Count Data** | `Count de Matricule Ouvrant-droit`, `Count`, `nombre`, `matricule`, `total` | 25, 18, 12 |

### Supported Formats

**Format 1 (Recommended):**
```csv
Code Postaux,Count de Matricule Ouvrant-droit
75001,25
75002,18
69001,12
13001,30
```

**Format 2 (Alternative):**
```csv
CP,Nombre
75001,25
75002,18
69001,12
13001,30
```

**Format 3 (Generic):**
```csv
postal,total
75001,25
75002,18
69001,12
13001,30
```

### Data Requirements
- ✅ CSV file format (`.csv` extension)
- ✅ French postal codes (5 digits)
- ✅ Header row with column names
- ✅ Positive integer values for counts
- ✅ UTF-8 encoding (recommended)

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
- **Employee distribution** analysis by region
- **Regional performance** tracking
- **Geographic insights** for business planning

### Research & Education
- **Demographic studies** using postal code data
- **Geographic data visualization** projects
- **Statistical analysis** teaching tool

### Government & Public Sector
- **Population distribution** analysis
- **Resource allocation** planning
- **Public service** optimization

## 📊 Sample Data Structure

Here's what your data might look like:

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
- **Export functionality** (PDF, PNG, CSV)
- **Multiple file comparison** support
- **Time-series analysis** for historical data
- **Advanced filtering** options
- **Custom map regions** selection
- **API integration** for real-time data

---

**Made with ❤️ for French postal code analysis**
