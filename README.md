LIVE AT --- 
https://asdakhtar.github.io/musafirs-tracks/

# 🧭 Musafir's Tracks v2.0

**A production-grade Islamic habit tracker with daily streaks, progress charts, PDF reports, and Quranic integration.**

![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)
![Version](https://img.shields.io/badge/Version-2.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## ✨ Features

### Core Functionality
- ✅ **Customizable Daily Tasks** - Physical and mental/spiritual categories
- ✅ **Streak Tracking** - Automatic streak counter with visual badges
- ✅ **Progress Charts** - Weekly, 15-day, and monthly performance graphs
- ✅ **PDF Export** - Download personal reports with task summaries
- ✅ **Dark Mode** - Toggle between light and dark themes
- ✅ **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- ✅ **Offline Support** - Works without internet connection (Service Worker)
- ✅ **PWA Installable** - Install as app on mobile devices

### Islamic Features
- 📅 **Dual Calendar Display** - Gregorian + Islamic (Hijri) dates in real-time
- 📖 **Daily Quran Verse** - Random verse from Quran.com API every day
- 🕌 **Islamic Context** - Dark green theme inspired by Islamic design

### Data & Analytics
- 📊 **Statistics Dashboard** - Total tasks, completion rate, average streaks
- 📈 **Performance Graphs** - Track habit completion over time
- 💾 **Persistent Storage** - All data saved in browser (localStorage)
- 🔄 **Auto-Reset** - Completion status resets at midnight, streaks persist

---

## 🚀 Quick Start (2 Minutes)

### Option 1: Deploy on GitHub Pages (Free, Recommended)

1. **Create a new GitHub repository**
   - Go to https://github.com/new
   - Repository name: `musafirs-tracks`
   - Select **Public**
   - Click **Create repository**

2. **Upload the 3 files**
   - Click **uploading an existing file**
   - Drag and drop or select these files:
     - `index.html`
     - `manifest.json`
     - `service-worker.js`
   - Commit message: `Initial commit - Musafir's Tracks v2.0`
   - Click **Commit changes**

3. **Enable GitHub Pages**
   - Click **Settings** (top navigation)
   - Click **Pages** (left sidebar)
   - Under "Source", select **main** branch
   - Click **Save**
   - Wait 2-3 minutes

4. **Your site is live!**
   - URL: `https://[your-username].github.io/musafirs-tracks/`
   - Share this link with anyone

---

### Option 2: Run Locally

1. Save all 3 files in a folder
2. Open `index.html` in your browser
3. Works immediately (no server needed)

---

### Option 3: Deploy on Vercel (Also Free)

1. Push your files to GitHub first (Option 1)
2. Go to https://vercel.com/import
3. Connect your GitHub repository
4. Click **Import**
5. Site deployed automatically with custom domain option

---

## 📋 File Structure

```
musafirs-tracks/
├── index.html           # Main application (all HTML, CSS, JS)
├── manifest.json        # PWA configuration (makes it installable)
└── service-worker.js    # Offline support and caching
```

**That's it. Only 3 files needed.**

---

## 💻 How to Use

### Adding Tasks

1. **Physical Tasks** (e.g., "20 Pull-ups", "8 Runs")
   - Type in the physical tasks input
   - Click "Add" or press Enter
   - Auto-assigned with physical emoji (💪, 🏃, etc.)

2. **Mental & Spiritual Tasks** (e.g., "Daily Quran", "Kalaam")
   - Type in the mental tasks input
   - Click "Add" or press Enter
   - Auto-assigned with mental emoji (📚, 🧠, etc.)

### Tracking Progress

- **Check a Task**: Click the checkbox when you complete it
- **View Streak**: Fire emoji (🔥) shows your current streak
- **Delete Task**: Click "Delete" to remove a task

### Default Tasks

On first load, these tasks are pre-populated:
- **Physical**: 20 Pull-ups, 50 Push-ups, 25 Squats, 8 Runs
- **Mental**: Daily Kalaam, Quran Reading, Coursera Daily

Delete any you don't need and customize!

### Viewing Statistics

1. Click **"📊 Stats"** button in header
2. Choose timeframe:
   - **Weekly** (last 7 days)
   - **15 Days** (last 15 days)
   - **Monthly** (last 30 days)
3. View line graph showing completion for each task
4. See habit performance percentages below chart

### Export as PDF

1. Click **"📥 Export"** button
2. PDF automatically downloads with:
   - Today's date and summary
   - All tasks with completion status
   - Current streaks
   - Professional formatting

### Dark Mode

- Click **"🌙"** button to toggle dark mode
- Your preference is saved automatically

### Install as Mobile App

**On iPhone:**
1. Open in Safari
2. Tap Share button
3. Select "Add to Home Screen"
4. Name: "Musafir's Tracks"
5. Tap "Add"

**On Android:**
1. Open in Chrome
2. Tap menu (⋮)
3. Select "Install app"
4. Tap "Install"

After installation:
- App icon appears on home screen
- Opens like native app (fullscreen, no URL bar)
- Works offline automatically

---

## 🔐 Data & Privacy

- ✅ **100% Private** - All data stored locally in your browser
- ✅ **No Servers** - Nothing sent to external servers (except Quran.com API for daily verse)
- ✅ **No Tracking** - No analytics, no ads, no data collection
- ✅ **You Own It** - Only you can see your habits and streaks
- 💾 **Browser Storage** - Data persists across sessions (localStorage)

**Note:** If you clear browser data/cache, habits are deleted. To back up:
1. Use "📥 Export" to save PDF reports regularly
2. Consider exporting data before clearing browser

---

## 🎨 Customization

### Add Your Own Tasks

Simply type any task name:
- "Read 30 pages" 
- "Meditation (15 min)"
- "Write journal"
- "Help someone"
- "Complete LeetCode problem"

### Change Colors

Edit the CSS variables at top of `index.html`:

```css
:root {
    --primary: #2c5f2d;      /* Main green color */
    --secondary: #97c680;    /* Light green */
    --accent: #ffd700;       /* Gold for streaks */
}
```

### Customize Default Tasks

Find this section in the `<script>` (line ~400):

```javascript
function initializeDefaultTasks() {
    tasks.physical = [
        { id: 1, name: '20 Pull-ups', ... },
        // Add your own
    ];
}
```

---

## 🌐 API Integration

### Quran Verse (Daily)
- **API**: Quran.com API (`api.alquran.cloud`)
- **What it does**: Fetches random Quranic verse in English
- **Update frequency**: Every page load (new verse)
- **Requires**: Internet connection

### Islamic Calendar
- **API**: Aladhan API (`api.aladhan.com`)
- **What it does**: Converts Gregorian date to Hijri date
- **Requires**: Internet connection

**Both APIs are free and don't require authentication.**

---

## 📊 Features Explained

### Streaks
- Increases by 1 each day you complete the task
- Resets to 0 if you don't complete it
- Fire emoji (🔥) indicates active streak
- **Example**: If you do pull-ups 5 days in a row, streak = 5

### Completion Rate
- Shows percentage of tasks completed today
- Example: 3/5 tasks = 60% completion rate
- Resets at midnight

### Charts
- **Line graph** shows completion over time (1 = done, 0 = not done)
- Different color for each habit
- Helps identify patterns and consistency
- Can view last 7, 15, or 30 days

### Average Streak
- Average streak length across all tasks
- Example: If you have habits with streaks of 3, 5, and 7: average = 5

---

## 🛠️ Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (no frameworks)
- **Storage**: Browser localStorage (built-in, no database needed)
- **Charts**: Chart.js library (CDN)
- **PDF Export**: html2pdf.js library (CDN)
- **Offline**: Service Worker + PWA
- **APIs**: 
  - Quran.com (verses)
  - Aladhan (Islamic calendar)

**Size**: ~50KB (incredibly lightweight)

---

## 📱 Browser Support

| Browser | Desktop | Mobile |
|---------|---------|--------|
| Chrome | ✅ | ✅ |
| Firefox | ✅ | ✅ |
| Safari | ✅ | ✅ |
| Edge | ✅ | ✅ |

**Requires**: ES6 JavaScript support (all modern browsers)

---

## 🐛 Troubleshooting

### Data Not Saving?
- Check if localStorage is enabled in browser settings
- Try clearing browser cache and reload
- Check browser console (F12) for errors

### Quran Verse Not Loading?
- Check internet connection
- Reload page
- Try different browser

### Not Installable as App?
- Must be served over HTTPS (GitHub Pages does this automatically)
- Use Chrome/Edge on Android or Safari on iPhone
- Wait a few seconds after page loads before trying to install

### Dark Mode Not Persisting?
- Browser may have cookies disabled
- Clear browser data might reset it
- Re-toggle dark mode to save preference

---

## 🚀 Future Enhancements (Phase 3)

Potential additions (requires backend):
- [ ] User accounts with email login
- [ ] Cloud backup/sync across devices
- [ ] Email weekly reports
- [ ] Google Fit integration (heart rate, steps)
- [ ] Social sharing (leaderboards)
- [ ] Notifications/reminders
- [ ] Community challenges

---

## 📄 License

MIT License - Free to use, modify, and distribute

---

## 👨‍💻 Built By

**Asad Akhtar Fakir**
- GitHub: https://github.com/asdakhtar
- LinkedIn: https://www.linkedin.com/in/asad-fakir-7a256b219
- Email: asadfakirr7@gmail.com

---

## 🙏 Acknowledgments

- Quran.com API for daily verses
- Aladhan API for Islamic calendar
- Chart.js for beautiful graphs
- html2pdf for PDF export

---

## 💡 Tips for Best Experience

1. **Set Realistic Goals** - Start with 3-4 habits, add more gradually
2. **Daily Check-in** - Review progress every evening
3. **Export Monthly** - Save PDF reports at end of each month
4. **Install App** - Use as mobile app for quick access
5. **Share Progress** - Show screenshots to friends for accountability

---

## 📞 Support

For bugs or suggestions:
1. Check this README first
2. Open an issue on GitHub
3. Email directly

---

**Last Updated**: April 2026  
**Version**: 2.0  
**Status**: Production Ready ✅

---

## 🎯 Quick Links

- 🌍 Live Demo: https://asdakhtar.github.io/musafirs-tracks/
- 📁 GitHub: https://github.com/asdakhtar/musafirs-tracks
- 💻 Code: See files above
- 📖 Documentation: This README

---

**Start tracking your journey today. One habit at a time. 🧭**
