# Crypto Community Leaderboard

## Setup Instructions

1. **Get the Google Sheet ID:**
   - From the Google Sheet URL: `https://docs.google.com/spreadsheets/d/SHEET_ID/edit`
   - Copy the SHEET_ID part

2. **Configure the Page:**
   - Open `index.html`
   - Replace `YOUR_GOOGLE_SHEET_ID` with the sheet ID
   - The sheet must be publicly viewable ("Anyone with the link can view")

4. **Deploy:**
   - Upload to any web hosting service
   - Or open `index.html` directly in browser for local testing

## Sheet Format
```
| Name          | XP    |
|---------------|-------|
| CryptoUser1   | 1500  |
| CryptoUser2   | 1200  |
| CryptoUser3   | 800   |
```

The leaderboard automatically refreshes every 5 minutes.

**Note:** This works with view-only access - no API key needed!