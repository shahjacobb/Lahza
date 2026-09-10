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

## Install

[Download `lahza.zip`](release/lahza.zip). Unzip it. In Chrome, open `chrome://extensions`, turn on Developer mode, and click **Load unpacked**. Choose the unzipped folder — the one that contains `manifest.json`. Pin Lahza.

To build from source you need [Node.js](https://nodejs.org/) 18 or newer:

```bash
git clone https://github.com/shahjacobb/Lazha.git
cd Lazha
npm install
npm run build
```

Then load unpacked on the `dist` folder. After you edit the code, run `npm run build` again and click **Reload** on the extension card.

Cloud sync is optional. If you want it, follow `docs/supabase.md`. The timer works without an account.
