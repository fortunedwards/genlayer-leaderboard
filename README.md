# 🏆 GenLayer Community Content Leaderboard

<div align="center">
  <img src="https://img.cryptorank.io/coins/gen_layer1758040081896.png" alt="GenLayer Logo" width="100" height="100">
  
  **A modern, real-time leaderboard for the GenLayer community showcasing member XP rankings**
  
  [![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge)](https://genlayer-leaderboard.vercel.app)
  [![GitHub](https://img.shields.io/badge/GitHub-Repository-blue?style=for-the-badge&logo=github)](https://github.com/fortunedwards/genlayer-leaderboard)
  [![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?style=for-the-badge&logo=vercel)](https://vercel.com)
</div>

---

## ✨ Features

### 🎯 **Core Functionality**
- **Real-time Data Sync** - Automatically fetches data from Google Sheets every 5 minutes
- **Smart Update Detection** - Only updates timestamp when actual data changes occur
- **Responsive Design** - Optimized for desktop, tablet, and mobile devices
- **Search & Filter** - Instantly search through community members
- **Pagination** - Displays 50 members per page for optimal performance

### 🏅 **Ranking System**
- **Trophy Icons** - Special visual indicators for top 3 positions
  - 🥇 **1st Place**: Gold trophy with yellow highlight
  - 🥈 **2nd Place**: Silver trophy with gray highlight  
  - 🥉 **3rd Place**: Bronze trophy with orange highlight
- **Persistent Rankings** - Search results maintain original ranking positions
- **XP Display** - Formatted numbers with thousand separators

### 🎨 **Modern UI/UX**
- **Clean White Theme** - Professional appearance with excellent readability
- **Tailwind CSS** - Modern, responsive styling framework
- **Material Icons** - Consistent iconography throughout
- **Smooth Animations** - Hover effects and transitions
- **Avatar Generation** - Dynamic user initials in gradient circles

---

## 🚀 Live Demo

**Visit the live leaderboard:** [https://genlayer-leaderboard.vercel.app](https://genlayer-leaderboard.vercel.app)

---

## 📊 Data Source

The leaderboard connects to a Google Sheets document with the following structure:

### Sheet Format
| Column | Content | Starting Position |
|--------|---------|------------------|
| **A** | Member Names | A3 |
| **B** | Display Names | B4 |
| **C** | XP Values | C4 |

### Example Data
```
|   A   |      B      |   C   |
|-------|-------------|-------|
| Row 1 | Headers     |       |
| Row 2 | ...         |       |
| Row 3 | ...         |       |
| Row 4 | CryptoKing  | 15250 |
| Row 5 | NiftyQueen  | 14800 |
| Row 6 | BitVoyager  | 13550 |
```

---

## 🛠️ Technology Stack

<div align="center">

| Technology | Purpose | Version |
|------------|---------|----------|
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white) | Structure | HTML5 |
| ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white) | Styling | CSS3 |
| ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) | Functionality | ES6+ |
| ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white) | UI Framework | 3.x |
| ![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=flat&logo=google-sheets&logoColor=white) | Data Source | API v4 |
| ![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white) | Deployment | Latest |

</div>

---

## 🏗️ Architecture

```mermaid
graph TD
    A[Google Sheets] -->|CSV Export| B[Fetch API]
    B --> C[Data Processing]
    C --> D[Ranking Algorithm]
    D --> E[UI Rendering]
    E --> F[User Interface]
    
    G[Search Input] --> H[Filter Logic]
    H --> E
    
    I[Pagination] --> E
    J[Auto Refresh] -->|Every 5min| B
```

---

## 📱 Screenshots

<div align="center">
  <img src="https://via.placeholder.com/800x600/f8f9fa/343a40?text=Desktop+View" alt="Desktop View" width="45%">
  <img src="https://via.placeholder.com/400x600/f8f9fa/343a40?text=Mobile+View" alt="Mobile View" width="25%">
</div>

---

## 🚀 Quick Start

### Prerequisites
- A publicly accessible Google Sheets document
- Basic understanding of HTML/CSS (for customization)

### Deployment Options

#### Option 1: Vercel (Recommended)
1. **Fork this repository**
2. **Connect to Vercel**
   - Visit [vercel.com](https://vercel.com)
   - Import your forked repository
   - Deploy automatically

#### Option 2: Local Development
```bash
# Clone the repository
git clone https://github.com/fortunedwards/genlayer-leaderboard.git

# Navigate to project directory
cd genlayer-leaderboard

# Run local server (Python)
python server.py

# Or use any static file server
npx serve .
```

---

## ⚙️ Configuration

### Google Sheets Setup
1. **Create or access your Google Sheet**
2. **Make it publicly viewable**
   - Click "Share" → "Anyone with the link can view"
3. **Copy the Sheet ID** from the URL
   ```
   https://docs.google.com/spreadsheets/d/[SHEET_ID]/edit
   ```
4. **Update the configuration** in `index.html`:
   ```javascript
   const SHEET_ID = 'YOUR_SHEET_ID_HERE';
   ```

### Customization Options
- **Refresh Interval**: Modify the `setInterval` value (default: 5 minutes)
- **Items Per Page**: Change `membersPerPage` constant (default: 50)
- **Styling**: Customize Tailwind classes or add custom CSS
- **Branding**: Replace logo and update footer credits

---

## 🔧 Development

### File Structure
```
genlayer-leaderboard/
├── 📄 index.html          # Main application file
├── 🖼️ logo.png            # GenLayer logo
├── 🐍 server.py           # Local development server
├── 🦇 run.bat             # Windows batch file
├── 📚 README.md           # This file
└── 📋 upload-instructions.txt
```

### Key Functions
- `fetchLeaderboard()` - Retrieves data from Google Sheets
- `displayLeaderboard()` - Renders the leaderboard UI
- `filterMembers()` - Handles search functionality
- `updatePagination()` - Manages page navigation
- `generateDataHash()` - Detects data changes

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **🍴 Fork the repository**
2. **🌿 Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **💾 Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **📤 Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **🔄 Open a Pull Request**

### Development Guidelines
- Follow existing code style and conventions
- Test on multiple devices and browsers
- Update documentation for new features
- Ensure responsive design principles

---

## 📈 Performance

- **Load Time**: < 2 seconds on average connection
- **Data Refresh**: Every 5 minutes automatically
- **Mobile Optimized**: Responsive design for all screen sizes
- **Lightweight**: Minimal dependencies, fast rendering

---

## 🔒 Privacy & Security

- **No API Keys Required**: Uses public Google Sheets CSV export
- **Client-Side Only**: No server-side data processing
- **No User Data Collection**: Privacy-focused design
- **HTTPS Enabled**: Secure connection via Vercel

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👨💻 Author

**Fortune Edwards**
- Created for the GenLayer Community
- GitHub: [@fortunedwards](https://github.com/fortunedwards)

---

## 🙏 Acknowledgments

- **GenLayer Community** - For the inspiration and data
- **Tailwind CSS** - For the beautiful styling framework
- **Google Sheets** - For providing the data backend
- **Vercel** - For seamless deployment and hosting

---

<div align="center">
  <strong>Made with ❤️ for the GenLayer Community</strong>
  
  [![Star this repo](https://img.shields.io/github/stars/fortunedwards/genlayer-leaderboard?style=social)](https://github.com/fortunedwards/genlayer-leaderboard)
</div>