# My Virtual iPhone — shared settings version

## 1. Replace the website file
1. Open your GitHub repository: https://github.com/leerionz10/virtual-iphon
2. Choose `Add file` → `Upload files`.
3. Upload this ZIP's `index.html` (not the ZIP itself).
4. Commit the change and wait a few minutes.

## 2. Publish your chosen settings for every visitor
1. Open your website and go to Settings.
2. Change wallpaper, home caption, auto-reply, and add the contacts you want.
3. Tap **설정 백업**. It downloads `my-iphone-settings.json`.
4. Rename that downloaded file to **site-config.json**.
5. Upload `site-config.json` to the root of the same GitHub repository (same level as `index.html`) and commit it.
6. Reload the website. Visitors will load the shared configuration file when they open the site.

The shared config file contains the wallpaper data and contact/message setup included in the export. Do not put private or sensitive conversations in a public repository: anyone may be able to read the published JSON file.

## Important limits
- This is a browser simulator. It does not send real SMS/iMessage or make real phone calls.
- Shared config is public to site visitors. Do not include passwords or private information.
- Photo gallery uploads and music file selections are not included in the shared-settings export; they remain local to the browser. Audio sharing can be added separately by using public audio files with appropriate rights.
- If a visitor already had the older version open, refresh the page after deployment.
