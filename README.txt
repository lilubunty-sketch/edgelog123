EDGELOG -> APK (needs: Node 18+, JDK 17, Android Studio or Android SDK)

1. npm install
2. npx cap add android
3. npx cap sync android
4. Easiest: npx cap open android  -> in Android Studio: Build > Build APK(s)
   Command line instead:  cd android && ./gradlew assembleDebug
   APK appears at android/app/build/outputs/apk/debug/app-debug.apk

Change appId in capacitor.config.json to your own (e.g. com.yourname.edgelog) before release.
For Play Store you need a signed release build (Build > Generate Signed Bundle / APK).

NO ANDROID STUDIO? BUILD IN THE CLOUD (free):
1. Create a GitHub repo, upload everything in this folder (including the .github folder).
2. Open the Actions tab > "Build APK" > Run workflow.
3. When it finishes (~5 min), open the run and download "edgelog-apk". Unzip it to get app-debug.apk.
4. Send it to your phone and install (allow "install unknown apps").
