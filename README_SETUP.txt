POULTRY RX PWA WRAPPER v10

IMPORTANT: If users already installed the old Poultry Rx app icon, they should uninstall/remove the old app first, then install again after this update to refresh the icon.

POULTRY RX — INSTALLABLE PWA WRAPPER (v9)

PURPOSE
This folder turns the Google Apps Script dosage calculator into an installable phone app shell.
The actual dosage calculator and Google Sheets database continue to run inside the existing
Apps Script Web App. The wrapper only supplies the phone icon, standalone launch experience,
install prompt, and offline-cached launcher shell.

ONE REQUIRED EDIT
1. Deploy the Google Apps Script calculator as a Web App.
2. Copy the deployment URL ending in /exec.
3. Open config.js.
4. Replace:
   PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE
   with the actual Web App URL.
5. Save config.js.

HOSTING
The PWA wrapper itself must be hosted on HTTPS. Upload the entire folder unchanged to an
HTTPS static host such as your organization's approved web hosting, Firebase Hosting,
GitHub Pages, Netlify, Cloudflare Pages, or equivalent.

PHONE INSTALL
Android / Chrome:
- Open the hosted PWA URL.
- Tap Install if prompted, or browser menu > Install app / Add to Home screen.

iPhone / Safari:
- Open the hosted PWA URL in Safari.
- Share > Add to Home Screen > Add.

IMPORTANT
- Phone operating systems require the user to confirm installation. A website cannot silently
  install itself as an app.
- The PWA launcher shell can reopen offline, but the embedded Google Apps Script calculator
  and Google Sheets synchronization still require network access when the inner web app is loaded.
- Code.gs intentionally uses XFrameOptionsMode.ALLOWALL so the Apps Script calculator can run
  inside this PWA wrapper. Keep the wrapper on a controlled/approved host.
