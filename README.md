# URBANIQ AI 2.0 — Smart Civic Intelligence Platform

A responsive, zero-build civic-tech web application with a redesigned premium command-center interface. The update focuses on visual design and interaction polish while retaining the existing Citizen Portal, complaint tracking, Leaflet map, Admin Dashboard, Innovation Centre, Firebase Authentication and Cloud Firestore integration.

## Files
- `index.html` — complete application and responsive animated interface.
- `firebase-config.js` — Firebase Web configuration for project `urbantiq-ai`.
- `firestore.rules` — Firestore access rules used by this project.

## Before publishing
1. In Firebase Console, open project `urbantiq-ai`.
2. Enable **Cloud Firestore** and **Authentication → Email/Password**.
3. Open Firestore → Rules and publish the contents of `firestore.rules`.
4. Confirm your Firebase Web app config in `firebase-config.js`.

## Deploy (the ZIP is not deployed automatically)
### Cloudflare Pages — Direct Upload
1. Open https://dash.cloudflare.com/ and sign in.
2. Go to **Workers & Pages → Create → Pages → Direct Upload**.
3. Upload `URBANIQ-AI-2.0-Redesigned.zip` and deploy.
4. Open the generated Pages URL and test sign-in and a sample complaint.

### GitHub Pages
1. Extract the ZIP.
2. Upload `index.html`, `firebase-config.js`, and `firestore.rules` to the root of your repository.
3. In GitHub, open **Settings → Pages**, select your branch and root folder, and save.
4. Wait for the Pages URL to become available.

## Important notes
- The visual redesign does not itself deploy the site or prove that Firebase writes are working. Test a signed-in sample complaint after publishing.
- The Firebase Web API key is client-side project configuration, not a service-account private key. Never upload service-account JSON or passwords to a public repository.
- The current app uses a client-side role switch for presentation. Do not treat that switch as secure administrator authorization in a public production deployment; implement server-verified admin claims before exposing privileged operations.
- The current Firestore rules allow public reads so the civic tracker/map can read complaint records. Review whether the fields stored in complaint documents are appropriate for public display before using real citizen data.
