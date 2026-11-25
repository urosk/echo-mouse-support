# Echo Mouse Support Site

Static support page for Echo Mouse for macOS.

## Deployment

- Support page: <https://urosk.github.io/echo-mouse-support/>
- GitHub repository: <https://github.com/urosk/echo-mouse-support>

GitHub Pages publishes the root of the repository's `main` branch. HTTPS is
enabled. Every commit to `main` triggers a new deployment, which normally
appears within a few minutes.

The deployed repository is separate from the Echo Mouse app repository.
Editing files in this `support-site` folder does not publish them automatically.

## Files

- `index.html` — support, setup, playback, and troubleshooting
- `privacy.html` — privacy policy
- `styles.css` — shared responsive styling
- `app-icon.png` — site icon and header artwork
- `mac-app-store-badge.svg` — Apple’s Mac App Store badge
- `.nojekyll` — tells GitHub Pages to serve the files without Jekyll processing

## Deploying updates

### GitHub website

1. Edit and verify the files in this folder.
2. Open <https://github.com/urosk/echo-mouse-support/upload/main>.
3. Upload every changed file, replacing the existing copy.
4. Enter a short commit summary and commit directly to `main`.
5. Wait for GitHub Pages to finish, then verify the live support URL. Use a hard
   refresh (`Command-Shift-R`) if the browser still shows the previous version.

### Command line

Clone the deployment repository outside this app repository, copy the changed
files into it, then commit and push:

```sh
git clone https://github.com/urosk/echo-mouse-support.git
cd echo-mouse-support

# Copy changed files from this support-site folder into the clone.

git add index.html privacy.html styles.css app-icon.png mac-app-store-badge.svg .nojekyll README.md
git commit -m "Update support site"
git push origin main
```

Do not create a nested Git repository inside `support-site`.

## App Store Connect

Use the live page as the **Support URL**. Keep
`info@bluepeakmobile.com` current on the page.
