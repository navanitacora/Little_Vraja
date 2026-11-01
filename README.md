# Little Vraja

A cosy pixel game about a little Vrindavan village: serve Radha-Syamasundara, care for the cows, celebrate the festivals and chant Hare Krishna. Free, no accounts, no ads. Progress is kept only in the player's own browser.

## What is in this folder

| File | What it does |
|---|---|
| `index.html` | The whole game |
| `manifest.webmanifest` | Lets phones install the game like an app (name, icon, colours) |
| `sw.js` | The offline helper: after the first visit the game works without internet |
| `icons/` | App icons |
| `.nojekyll` | Tells GitHub Pages to publish the files exactly as they are |

## 1. Put it on GitHub Pages (free)

1. Sign in at github.com and click **New repository**. Name it `little-vraja`, set it to **Public**, and click **Create repository**.
2. On the new repository page click **uploading an existing file**, drag in **everything in this folder** (including the `icons` folder and `.nojekyll`), then click **Commit changes**.
   (If `.nojekyll` is hidden on your computer, that's fine to skip.)
3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, and click **Save**.
4. After a minute or two the page shows your address, something like `https://YOUR-NAME.github.io/little-vraja/`. Open it: that is the game.

**Updating later:** upload the new files over the old ones. Each new version I give you already has a new number inside `sw.js` (this one is `little-vraja-v3`), so phones fetch the new game.

## 2. On a phone straight away (no store)

- **Android (Chrome):** open your game address, tap the ⋮ menu → **Install app** (or **Add to Home screen**).
- **iPhone/iPad (Safari):** open the address, tap **Share** → **Add to Home Screen**.

It gets the Little Vraja icon and opens full-screen. Open it once with internet; after that it works offline.

## 3. A real Android app (Google Play or sharing the file)

1. Go to **pwabuilder.com**, paste your GitHub Pages address, click **Start**.
2. Click **Package for stores → Android → Generate package**. Keep the suggested settings (you can set the app name and package ID, e.g. `io.github.yourname.littlevraja`).
3. Download the zip. Inside are:
   - an **.apk**: you can send this to family/friends to install directly (Android will ask to allow installing from that source);
   - an **.aab**: this is what you upload to Google Play;
   - a **signing key** file and its passwords: **keep these safe**, you need them for every future update.
4. For Google Play: create a developer account at play.google.com/console (one-time fee), create an app, upload the .aab, fill in the store listing and the content rating questionnaire, then submit for review.
5. PWABuilder also gives you an `assetlinks.json` file. Put it in a folder called `.well-known` on your site so the app opens without a browser address bar. (GitHub Pages user sites: this works best on a `YOUR-NAME.github.io` repository or a custom domain; PWABuilder's instructions explain it.)

## 4. A real iPhone app (App Store)

- You need a **Mac** with **Xcode** (free) and an **Apple Developer** membership (yearly fee).
- On pwabuilder.com choose **iOS → Generate package**, download it, open the project in Xcode, set your team, and upload to App Store Connect, then submit for review.
- Apple sometimes asks small web-based apps to show "app-like" value; the offline play, home-screen icon and full-screen game help here.
- If you don't want the App Store, **Add to Home Screen** in Safari (step 2) already gives iPhone users an app icon, for free.

Check each store's current fees and rules when you sign up, as they change from time to time.
