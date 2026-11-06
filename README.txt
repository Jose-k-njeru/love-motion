LOVE MOTION — VOLUME 1
Where Love Becomes an Experience

CONTENTS
- index.html: responsive romantic website and Firebase client.
- firestore.rules: starter Firestore security rules.

SETUP

1. CREATE A FIREBASE PROJECT
   - Go to https://console.firebase.google.com/
   - Create a project and add a Web App.
   - Copy the Firebase Web App configuration.
   - In index.html, replace each YOUR_* placeholder in firebaseConfig.

2. ENABLE AUTHENTICATION
   - Firebase Console > Authentication > Sign-in method.
   - Enable Email/Password.
   - Enable Anonymous.
   - Add your website domain to Authentication > Settings > Authorized domains.

3. CREATE FIRESTORE
   - Firebase Console > Firestore Database > Create database.
   - Open Rules, replace the rules with firestore.rules, and Publish.

4. HOST THE WEBSITE
   - Host index.html on an HTTPS host (Firebase Hosting, GitHub Pages, or another static host).
   - Do not open it as a file:// page; Firebase authentication requires a hosted origin.
   - The creator shares a link with a #love/UNIQUE_ID fragment for their page.

IMPORTANT VOLUME 1 LIMITATIONS
- The website does not upload or distribute music files yet. A music file stored only on the creator's phone cannot play for the recipient. Cloud Storage upload and playback are future work.
- Photo uploads, video backgrounds, creator dashboard history, premium payments, premium access enforcement, email/SMS notifications, and anniversary reminders are not implemented.
- Recipient recognition uses sessionStorage for the current browser session only. It is not durable across devices or all browser sessions.
- Recipient phone numbers are collected but not verified.
- The creator's WhatsApp number is stored in the public couple document so the recipient's browser can open WhatsApp. Only use a number you are comfortable sharing with people who receive your link.
- WhatsApp opens a prefilled message; the recipient must press Send.
- Premium tiers are display-only. No payments are taken.
- The NO button moves away from pointer/touch; YES remains stationary. No music is bundled in this release.
- The date choice is saved before WhatsApp opens.

SECURITY BEFORE PUBLIC LAUNCH
- Treat these rules as a starter baseline and test them with Firebase Emulator / Rules Playground.
- Enable Firebase App Check and consider abuse controls/rate limiting.
- Publish a privacy notice describing collection of names and phone numbers, and provide a deletion-request process.
- Never put service-account keys, private API secrets, or admin credentials in index.html.
- Firebase web config is not a secret; access control comes from Authentication and Firestore Rules.
- Current rules deny deleting couple records and deny editing registrations/date choices.
- Public page reads expose the creator name, letter, and WhatsApp number to anyone who has the page link. The page link is shareable, not a private vault.

This is a starter implementation. Test thoroughly before using real personal information.
