# AVITECHNO Tiger Quest - Release starter v1.1

Offline Canvas cartoon platform game with generated Web Audio music and SFX, mobile touch controls and AVITECHNO artwork. This is a 2D game, not a native 3D title.

## Browser
Open `www/index.html` in a browser or run `python -m http.server 8080 -d www` and visit http://localhost:8080. Audio starts on PLAY after a user tap.

## GitHub - create separate repo
Create `Avinashsingh011/avitechno-tiger-quest` in GitHub; then from this directory run:

```bash
git init
git add .
git commit -m "Initial AVITECHNO Tiger Quest game and deployment starter"
git branch -M main
git remote add origin https://github.com/Avinashsingh011/avitechno-tiger-quest.git
git push -u origin main
```

Do not commit build signing keys or cloud credentials. GitHub authentication is required.

## AWS Amplify static hosting

1. Open AWS Console -> Amplify -> Create new app -> Deploy without Git.
2. Use `aws-amplify-upload.zip` from the outer download, not this entire source directory.
3. Name the app `avitechno-tiger-quest`, branch `production`, upload and deploy.
4. Verify the generated `amplifyapp.com` URL, music playback after PLAY, touch controls and HTTPS.
5. Optionally add a custom domain in Amplify and configure DNS. Domain and AWS billing require your approval.

Alternatively connect the new GitHub repo to Amplify and use the included `amplify.yml`, which serves `www`.

## Android / Play Store

Install supported Node.js LTS, Java JDK and Android Studio SDK. In this directory:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

In Android Studio, test on real phones, prepare adaptive launcher icons and splash images, set versionCode/versionName, then use Build -> Generate Signed Bundle / APK -> Android App Bundle (.aab). Store the signing/upload key securely and enroll in Play App Signing. Publish with Google Play Console after setting up app name, screenshots, listing, contact information, target audience, content rating, privacy policy and Data safety declarations. Keep target API and Capacitor/Android dependencies updated to current Play requirements. This archive does NOT contain a compiled or signed APK/AAB, and has not been tested on a physical Android device.

If Play Console account is a personal account created after November 13, 2023, you may need at least 12 opted-in testers over 14 continuous days to apply for production access.

## Security / release checklist
- Game has no backend, tracking, advertising SDK or in-app purchasing. Validate all disclosures against the final build.
- Confirm rights to the AVITECHNO brand, mascot and all visuals.
- Obtain store artwork: high-resolution icon, feature graphic and real screenshots.
- Test performance and touch navigation on multiple phone sizes.
- Check the game and age group against Google Play Families policies if targeting children.
- Configure domain, DNS, cloud accounts and signing through your own trusted account consoles.
