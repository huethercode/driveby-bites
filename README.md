# 🍔 DriveBy Bites

**Zero-Look Roadside Culinary Capture & Weighted Priority Roulette**

DriveBy Bites is a single-file, zero-backend Progressive Web App (PWA) designed to capture roadside restaurants while you are driving—using one-tap GPS vector pinning and speech-to-text—and later rank them with an "obscure" weighted priority algorithm so you always know where to eat when hunger strikes.

Try It: [Driveby-Bites](https://huethercode.github.io/driveby-bites/)  https://huethercode.github.io/driveby-bites/

---

## ✨ Key Features

* **Zero-Look Drive-By Capture:** Giant, high-contrast automotive controls engineered for single-tap GPS coordinate capture, compass heading detection, side-of-road vector offsets (`Right`, `Left`, `Just Passed`), and 4-second speech-to-text voice notes.
* **Capture Inbox:** Queues unverified roadside pins so you can safely review GPS coordinates, look up the storefront when parked, assign tags, and promote discoveries to the roulette wheel.
* **Culinary Gravity Index (CGI) Scoring Engine:** Ranks restaurants on a 0–100 scale using four non-obvious sub-metrics:
  1. **Hole-in-the-Wall Anomaly Quotient ($A_q$):** Rewards the 4.1–4.6 star, 50–400 review "hidden gem" sweet spot over massive corporate chains.
  2. **Personal Taste Match ($G_s$):** Compares menu tags against your culinary profile and applies a **48-Hour Palate Fatigue Penalty (`-25 pts`)** if you recently ate pizza, tacos, burgers, or subs.
  3. **Curiosity Urgency ($U_v$):** Boosts spots you have pinned multiple times on repeat drives or newly discovered places.
  4. **Contextual Friction ($C_b$):** Weights proximity and open-status convenience.
* **Weighted Priority Roulette:** Generates an interactive SVG roulette wheel where every restaurant's slice size is proportional to its live CGI score. Landing on a spot opens a **Tactical Culinary Dossier** with tags, score breakdowns, one-tap Google Maps directions, and a **Veto / Demote (`-30%`)** button.
* **100% Offline-First & Cross-Platform:** Runs completely out of a single `index.html` file with automatic `localStorage` persistence and JSON export/import backups to sync between your Android phone and Mac.

---

## 🚀 Deployment: Host on GitHub Pages (3 Minutes)

1. **Create a Repository:** Log in to [GitHub](https://github.com) and create a new repository named `driveby-bites`.
2. **Add `index.html`:** Click **Add file → Create new file**, name it `index.html`, paste the standalone HTML application code, and click **Commit changes**.
3. **Enable GitHub Pages:**
   * Open **Settings → Pages** in your repository.
   * Under **Build and deployment → Branch**, select **`main`** (keep `/ (root)`) and click **Save**.
   * Wait ~45 seconds and refresh; your live app URL will appear at `https://<your-username>.github.io/driveby-bites/`.

---

## 📱 Installation on Android & macOS

### Android (Chrome)
1. Open your `github.io` URL in **Google Chrome** on your Android phone.
2. Tap the **Install App** button in the top-right header of the app (or tap Chrome's **`⋮` menu → Add to Home screen / Install app**).
3. Confirm **Install**. DriveBy Bites will appear on your home screen and app drawer as a full-screen standalone app with offline caching.

### macOS (Safari or Chrome)
1. Open the exact same `github.io` URL on your Mac.
2. In **Safari**, click **File → Add to Dock** (in **Chrome**, click the **Install** icon in the right side of the address bar).
3. Use the Mac desktop window to curate your Capture Inbox, edit tags, and export/import JSON backups.

---

## 📖 Usage Directions

### Phase 1: Pinning a Spot While Driving (`Zero-Look Capture` Tab)
1. Open the **Zero-Look Capture** tab before hitting the road (or launch from your home screen).
2. When you pass an interesting restaurant, select the road direction (**On the Right**, **On the Left**, or **Just Passed It**).
3. Tap the large green **Tap to Pin Roadside Spot** button.
4. Your phone immediately locks your GPS coordinates, compass bearing, and speed, then activates the microphone for a quick voice note (e.g., *"Neon birria taco sign next to the hardware store"*).
5. The pin is saved automatically to your **Capture Inbox** for safe review later.

### Phase 2: Confirming Storefronts (`Capture Inbox` Tab)
1. Once parked or at home on your Mac, open the **Capture Inbox** tab.
2. Review your pinned GPS coordinates, timestamp, and transcribed voice memo.
3. Enter or confirm the official restaurant name, add menu/vibe tags (e.g., `#DriveThru`, `#Birria`, `#StripMallGem`), and click **Promote to Roulette**.

### Phase 3: Deciding Where to Eat (`Priority Roulette` Tab)
1. Open the **Priority Roulette** tab when you are ready to eat.
2. Toggle any **48-Hour Palate Fatigue** pills (e.g., `Had Pizza`, `Had Tacos`) to temporarily shrink those categories' slices on the wheel.
3. Filter by tags if desired (such as `#DriveThru` or `#Independent`), then tap **Spin Priority Roulette** (or tap any slice directly).
4. Inspect the **Tactical Culinary Dossier** pop-up and choose an action:
   * **Let's Roll:** Launches turn-by-turn navigation directly to the restaurant.
   * **Snooze Today:** Removes the spot from today's spin without hurting its priority score.
   * **Veto / Demote (-30%):** Reduces its CGI score by 30% so other discoveries get a turn on future spins.

### Phase 4: Tuning & Backups (`CGI Engine` & `Data` Tabs)
* **Adjust Scoring Weights:** Use the sliders in the **CGI Engine** tab to change how heavily the wheel favors hole-in-the-wall anomalies, personal taste matches, or repeat drive-by urgency.
* **Sync Between Phone & Mac:** Use **Export JSON Backup** and **Import JSON** in the top bar (or Data tab) to transfer your restaurant list and custom scores between devices.
