# Road to Compostella

1. Unzip the package. Open `config.js` in a text editor and paste your existing Apps Script web app URL ending in `/exec` between the quotes. Use the same URL you used in the Android app. Save the file.
2. Upload the extracted files to the root of a GitHub repository on its `main` branch. You can use **Add file → Upload files**.
3. In **Settings → Pages**, choose **Deploy from a branch**, then **main** and **/(root)**. Save and open the Pages link once published.

Share the GitHub Pages link with players. They sign in with the accounts you made in Sheets. Keep passwords and account data out of the repository.

## First test

Sign in, then edit a friend's current node in Sheets and click **Sync**. Pick a node near yours so both players are visible. Try a move with an available point and test **Enter steps** from an account with `AllowEntryofSteps` set to Yes.

Sync pulls the latest game state from Sheets. For this release, Android Health Connect uploads still happen in the existing APK. Sync on the web map then picks up those uploaded steps.

The site sends JSON in a plain-text POST to the existing Apps Script endpoint. The deployment must accept requests without a Google sign-in. If login fails, first check the `/exec` URL and try the existing backend test page. The live connection from GitHub Pages still needs a test with your deployment.
