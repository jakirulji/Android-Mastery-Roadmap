# Android Mastery Roadmap

A dark, neon-accented, installable PWA for learning Android development and internals in 30-minute daily sessions. Built with Bengali explanations and free English documentation.

## Features

- 42 lessons across 7 milestones: Linux, ADB, Kotlin, Android internals/security, root/recovery, AOSP/custom ROMs, kernel/debugging.
- Daily 30-minute rhythm: 10 minutes learning, 15 minutes practice, 5 minutes recap.
- Hands-on labs, knowledge-check quiz, free resource library, timer and notes.
- Local-first progress stored in browser localStorage.
- JSON export/import backup.
- Optional GitHub sync to a private Gist using GitHub OAuth Device Flow.
- Service worker and web manifest for PWA installation/offline shell.
- GitHub Actions deployment to GitHub Pages.

## GitHub Pages deployment

1. Open repository Settings → Pages.
2. Set Build and deployment source to GitHub Actions.
3. The workflow .github/workflows/deploy.yml deploys the repository root after pushes to main.
4. Wait for the Deploy Android Mastery PWA workflow to succeed. The URL appears in repository Pages settings.

## Optional GitHub progress sync

The app uses GitHub OAuth Device Flow and the Gists API. It creates a private Gist for progress.

1. Create a GitHub OAuth App under GitHub → Settings → Developer settings → OAuth Apps.
2. Set the homepage URL to your published Pages URL and enable Device Flow in the OAuth App settings.
3. Enter the OAuth App public Client ID in the app when prompted.
4. Approve the device code on GitHub. The app requests the gist scope only.
5. Keep the Gist private. The access token is held in memory for the current page session and is not stored in localStorage or committed to this repository. You may need to authorize again after reload.

Important: this is a static PWA, so the public OAuth Client ID is not a secret. Never add an OAuth client secret or personal access token to this repository or browser code. Use HTTPS for OAuth. Review the GitHub authorization prompt before approving access.

## Progress and privacy

- Local progress and notes stay in the browser until you export, clear browser data, or reset the app.
- Export a JSON backup before switching browsers or clearing data.
- GitHub sync stores progress in a private Gist after authorization. Do not store secrets in lab notes.
- Redact device identifiers and personal data from logs before sharing.

## Learning approach

Each lesson is designed for about 30 minutes. Read official documentation, run a safe lab, then write a short recap. Do not flash partitions or run destructive commands as beginner exercises. Check the exact device codename, Android version, firmware and maintainer instructions before device modifications.

## Tech

Plain HTML, CSS and JavaScript. No build step or paid dependency required.