# 💪 FitTrack Pro

A complete **gym fitness tracking web app** built with pure HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step.

---

## 🚀 Features

| Feature | Description |
|---|---|
| 🔥 **Calorie Tracker** | Log meals from a 15-item food database, track macros (protein, carbs, fat) with a live donut chart |
| 🏋️ **Workout Planner** | Pre-built Push / Pull / Leg day plans, custom workouts, exercise library with filters, full workout history |
| ⚖️ **BMI & Stats** | Live BMI gauge with category color coding, weight history chart, body fat tracking |
| 🔔 **Workout Reminders** | Browser push notifications, custom reminder scheduler with day-of-week selection, in-app toasts |
| 💧 **Water Intake** | Quick-add water buttons (250/500/750 ml), daily progress bar |
| 📊 **Dashboard** | Weekly calorie bar chart, macro rings, recent activity feed, all stats at a glance |

---

## 📁 Project Structure

```
fittrack-pro/
│
├── index.html          ← Main entry point (single HTML shell)
│
├── css/
│   └── styles.css      ← Full design system (dark athletic theme, responsive)
│
├── js/
│   ├── app.js          ← Core engine: state, localStorage, routing, notifications
│   └── pages.js        ← All page renderers and UI event handlers
│
├── data/
│   └── mockData.js     ← Food database, exercise library, sample workout plans
│
└── README.md
```

---

## ⚡ Quick Start

### Option 1 — Open directly (simplest)
```bash
# Just open index.html in your browser
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option 2 — Local dev server (recommended for notifications)
```bash
# Using Python
python -m http.server 8080

# Using Node.js (npx)
npx serve .

# Then open: http://localhost:8080
```

> ⚠️ **Browser Notifications require HTTPS or localhost.** Use Option 2 to test reminders.

---

## 🚢 Deploy to GitHub Pages (Free Hosting)

```bash
# 1. Create a new repo on github.com, then:
git init
git add .
git commit -m "Initial commit — FitTrack Pro"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/fittrack-pro.git
git push -u origin main

# 2. Go to repo → Settings → Pages → Source: "Deploy from branch" → main / root
# 3. Your app will be live at: https://YOUR_USERNAME.github.io/fittrack-pro
```

---

## 🛠️ How to Customize

### Add more foods
Edit `data/mockData.js` → `FOOD_DATABASE` array:
```js
{ id: 16, name: "Paneer (100g)", calories: 265, protein: 18, carbs: 3, fat: 20 }
```

### Add more exercises
Edit `data/mockData.js` → `EXERCISE_DATABASE` array:
```js
{ id: 13, name: "Cable Fly", muscle: "Chest", type: "Strength" }
```

### Change calorie goal default
Edit `js/app.js` → `DEFAULT_PROFILE.calorieGoal`

### Change color theme
Edit `css/styles.css` → `:root` CSS variables:
```css
--accent:  #ff6b35;   /* Main orange — change to any color */
--bg:      #0d0f14;   /* Background */
```

---

## 💾 Data Storage

All data is saved to **localStorage** in the user's browser — no backend or database needed. Data persists across page refreshes and browser sessions on the same device.

| Key | What's stored |
|---|---|
| `fittrack_state` | Profile, food log, workout log, water log, body stats, notifications |

---

## 📱 Browser Support

| Browser | Support |
|---|---|
| Chrome / Edge | ✅ Full (including notifications) |
| Firefox | ✅ Full (including notifications) |
| Safari | ✅ Partial (notifications limited on iOS) |
| Mobile Chrome | ✅ Full |

---

## 📋 Pages Overview

### 🏠 Dashboard
- Greeting with today's date
- 4 stat cards: Calories, Water, Workouts, BMI
- Macro rings (Protein / Carbs / Fat)
- Quick water add buttons
- 7-day calorie bar chart
- Recent workout feed

### 🍽️ Calories
- Live calorie donut chart vs. daily goal
- Searchable food database
- Quantity selector per food item
- Today's food log with remove option
- Full macro breakdown

### 🏋️ Workout
- Push / Pull / Legs pre-built plans
- Custom workout logger
- Exercise library (filter by type)
- Workout history log

### ⚖️ BMI & Stats
- Animated BMI gauge (Underweight / Normal / Overweight / Obese)
- Update weight, height, body fat
- Weight history line chart
- Stats table (last 10 entries)

### 🔔 Reminders
- Enable browser push notifications
- Add reminders with time + day-of-week
- Toggle reminders on/off
- Delete reminders
- Fitness tips section

---

## 👨‍💻 Tech Stack

- **HTML5** — semantic structure
- **CSS3** — custom properties, grid, flexbox, animations
- **Vanilla JavaScript** — ES6+, modules pattern, localStorage API, Notifications API
- **Google Fonts** — Bebas Neue (headings) + DM Sans (body)
- **Zero dependencies** — no npm, no build tools, no frameworks

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

*Built as a college project. Open an issue or PR if you want to contribute!*
