# WAXTIX

A mobile-first social platform implemented as a static HTML site. It deploys to Render Static Sites or GitHub Pages without a build step.

## Features
- Reels-style home feed
- News feed
- Media upload preview (demo only)
- Firebase Realtime Database chat integration
- Profile page
- Responsive dark interface

## Run locally
Open `index.html`, or run `python -m http.server 8000` in this folder and visit http://localhost:8000.

## Deploy to Render
1. Push the contents of this folder to the root of a GitHub repository.
2. In Render, choose **New + → Static Site** and connect the repository.
3. Leave **Build Command** blank (or use `echo "No build required"` if required).
4. Set **Publish Directory** to `.`.
5. Deploy.

The included `render.yaml` can also be used as a Blueprint.

## Deploy to GitHub Pages
1. Push the files to a GitHub repository.
2. Open **Settings → Pages**.
3. Choose **Deploy from a branch**, select `main` and `/ (root)`.
4. Save and wait for the Pages URL.

## Firebase production setup
The frontend uses the Realtime Database URL from the supplied source. Confirm that this Firebase project belongs to you. Configure secure database rules and authentication before production use; do not enable unrestricted public writes. If Firebase is unavailable or writes are rejected, the interface falls back to local demo behavior.

## Current demo limitations
- Media upload is a **UI preview/demo**. It does not upload files to cloud storage. Configure Firebase Storage (or another provider), security rules, and upload code before calling it live.
- Translation uses sample text; no translation API is connected.
- Authentication and authorization are not configured in this starter project.

## Structure
```text
waxtix/
├── index.html
├── README.md
└── render.yaml
```
