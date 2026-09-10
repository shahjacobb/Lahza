<p align="center">
  <img src="docs/shots/banner.png" alt="Lahza — a quieter way to hold time" width="100%" />
</p>

# Lahza

Lahza is a focus timer for Chrome. You can run a classic Pomodoro — 25 minutes of work, 5 of rest — or set the lengths yourself. After four focus sessions it offers a longer break.

Pin it on the toolbar. While a session is running, the icon shows the time you have left. When it ends, Chrome sends a notification. There’s a chime too, if you leave sound on.

Activity has today, your week, and your streak. Week is a bar chart. Month is a heat map of the days you focused.

`Alt+Shift+P` starts or pauses from any tab. Sign in if you want the same timer on every Chrome profile.

*Lahza* (لحظة) is said **LAH-zah**.

<p align="center">
  <img src="docs/shots/timer.png" alt="Idle timer" width="240" />
  <img src="docs/shots/running.png" alt="Focus in progress" width="240" />
  <img src="docs/shots/settings.png" alt="Settings" width="240" />
</p>

<p align="center">
  <img src="docs/shots/activity.png" alt="Weekly activity" width="240" />
  <img src="docs/shots/month.png" alt="Month heat map" width="240" />
  <img src="docs/shots/complete.png" alt="Session complete" width="240" />
</p>

![Using Lahza](docs/demo.gif)

---

## Install

[Download `lahza.zip`](release/lahza.zip). Unzip it.

1. `chrome://extensions`
2. Developer mode on
3. **Load unpacked**
4. Pick the folder that contains `manifest.json`
5. Pin **Lahza**

From source:

```bash
git clone https://github.com/shahjacobb/Lazha.git
cd Lazha
npm install
npm run build
```

Load unpacked on **`dist`**. After you change code: `npm run build`, then **Reload**.

---

## Notes

The popup is Timer, Activity, and Settings. Settings has **← Timer** at the top. Session lengths first; sound and auto-start under that; account last.

Cloud sync is optional. Wire it once with `docs/supabase.md`. Without that, the timer still works on this profile.

Store listing paste: `docs/store/listing.md`. Color system: `docs/color-system.pdf`.

```bash
npm run build      # typecheck + dist/
npm run package    # build + lahza.zip
npm run preview    # Vite, /popup.html
```
