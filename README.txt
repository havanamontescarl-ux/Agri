AGROFORESTRY TREE MONITORING & GPS-BASED STUDENT TRACKING SYSTEM
================================================================

FILES
- index.html       Main page
- style.css        Design
- game.js          Main application logic (kept this filename to match your starter project)
- firebase.js      Firebase connection settings
- firestore.rules  Firestore database security rules

IMPORTANT: THIS PROJECT NEEDS FIREBASE SETUP
1. Open https://console.firebase.google.com and create a Firebase project.
2. Add a Web App and copy the Firebase configuration.
3. Open firebase.js and replace every PASTE_YOUR... value with your real Firebase config.
4. In Firebase Authentication, enable Email/Password.
5. Create a Cloud Firestore database.
6. Open Firestore Rules and publish the contents of firestore.rules.
7. Run the project using a local web server or HTTPS. GPS usually does not work from a plain file:// page.
   If your mobile coding app has a Preview/Run button, use its web preview. Allow location permission.

ROLE FEATURES
- Student: sign in and voluntarily share GPS while the field activity is active.
- Instructor: view the latest location shared by student accounts.
- Forestry Personnel: register trees, capture tree GPS, update alive/dead status, and delete records.
- Admin: overview, student tracking, tree records, and monitoring.

GPS NOTES
- Student tracking is permission-based and only updates while the page is open and sharing is active.
- This is latest-location reporting, not guaranteed background tracking.
- Tree GPS captures the phone's current location at the tree registration point.
- Location accuracy depends on the phone, GPS signal, and environment.
- Use only with informed consent and during authorized school field activities.

OFFLINE NOTES
- Firestore IndexedDB persistence is enabled where supported. Cached data and pending writes may work offline
  and sync when the device reconnects. First login and first-time data loading require internet.
- Browser GPS may require internet/HTTPS even though GPS hardware can sometimes determine location offline.

SECURITY WARNING
- The registration form lets a user choose a role to make classroom testing easy.
- Do NOT deploy publicly like this. For production, remove public role selection and let an administrator
  assign roles through a trusted backend or Firebase Admin SDK. Never put service-account keys in frontend code.
