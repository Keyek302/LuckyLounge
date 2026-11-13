# Lucky Lounge

A play-money casino: Slots, Blackjack, Roulette, Craps, Plinko and Texas Hold'em, with a daily bonus, daily spin and a customizable full-body character. Everything is in `index.html` (plus the files that make it installable as an app).

## Put it on GitHub Pages
1. On github.com click **New repository**. Name it `lucky-lounge`, set it to **Public**, and create it.
2. Click **Add file > Upload files** and drag in everything from this folder (index.html, manifest.json, sw.js, both icon PNGs, .nojekyll). Click **Commit changes**.
3. Go to **Settings > Pages**. Under "Build and deployment" choose **Deploy from a branch**, pick **main** and **/ (root)**, then **Save**.
4. After a minute your game is live at `https://YOUR-USERNAME.github.io/lucky-lounge/`.

## Install it on a phone (no app store)
- **iPhone:** open the link in Safari, tap Share, then **Add to Home Screen**.
- **Android:** open the link in Chrome, tap the menu, then **Install app**.
It opens full-screen like a real app and works offline after the first load.

## Put it in the app stores later
- **Android (Google Play):** go to pwabuilder.com, paste your GitHub Pages link, and download the Android package.
- **iPhone and Android (both):** wrap it with Capacitor: `npm i @capacitor/core @capacitor/cli`, `npx cap init`, put these files in a `www` folder, then `npx cap add ios android`.
- Stores rate this as simulated gambling (17+/Mature). Chip purchases in the store apps must use Apple's and Google's own billing, not Stripe.

## Notes
- Chips, streaks, name and outfits are saved in each player's browser (localStorage), so they don't sync between devices.
- The Chip Shop and the "watch an ad" button are demo placeholders. Set `DEMO=false` in index.html once real payments are connected.
