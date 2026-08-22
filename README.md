# Sakhi App Shell

This is a lightweight Capacitor project whose only job is to load
the live Sakhi website (https://sakhi-chatbot-546613952089.asia-southeast1.run.app)
inside a native Android app, using its own private WebView (not Chrome).

## How to use

1. Create a new GitHub repo (e.g. `sakhi-app-shell`).
2. Upload all files from this zip to that repo, keeping the folder structure
   (including the `.github/workflows/build.yml` file — GitHub may hide
   folders starting with a dot, so make sure it uploads correctly).
3. Once committed, go to the repo's **Actions** tab on GitHub.
4. You should see a workflow run start automatically ("Build Android APK").
   Wait for it to finish (a few minutes).
5. Click into the finished run, scroll to **Artifacts**, and download
   `sakhi-app-debug` — this contains your APK.
6. Unzip it, install `app-debug.apk` on your phone.

## Notes

- This is a debug build (unsigned), fine for personal use and testing.
- The app always loads the live website, so any updates you make to
  your site on AI Studio/Cloud Run will show up in the app automatically
  without needing to rebuild the APK.
- If you change the app name, icon, or the website URL, edit
  `capacitor.config.json` and commit again — the Action will rebuild.
