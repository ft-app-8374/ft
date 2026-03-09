# FitTrack iPhone Install Guide

## Quick Start (2 minutes)

### 1. Start the server
```bash
cd /home/sandbox/.openclaw/workspace/fittrack
python3 -m http.server 8080 --bind 0.0.0.0
```

### 2. Find your IP
```bash
hostname -I | awk '{print $1}'
```
Use the first IP, e.g. `http://192.168.1.20:8080`

### 3. Install on iPhone
1. Open **Safari** on iPhone (must be Safari, not Chrome)
2. Go to `http://<your-ip>:8080`
3. Tap the **Share** button (square with arrow)
4. Scroll down, tap **Add to Home Screen**
5. Name it **FitTrack**, tap **Add**

### 4. Verify
- Launch from Home Screen — should open full-screen (no Safari UI)
- Add a test workout entry
- Close and reopen — data should persist
- Check all 6 tabs work

## Features
- **Today**: Daily check-in (energy/sleep/soreness ratings), quick food logging
- **Workout**: Exercise tracking with sets/reps/weight, rest timer, form tips, video links
- **Measures**: Body weight & measurements tracking with trend chart
- **Import**: Apple Health XML import, manual data entry
- **Analysis**: Workout streaks, volume trends, wellness insights, recommendations
- **Charts**: Weight, volume, calories, and wellness charts with time ranges

## Notes
- iPhone and server must be on the **same WiFi network**
- Data is stored in the browser's localStorage (persists across sessions)
- Works offline after first load (service worker caches everything)
- For a permanent setup, consider running the server as a systemd service
