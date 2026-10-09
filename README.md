# k3v.1

Movie and TV watchlist with live data from TMDB: trending, in theaters, coming soon,
real posters, trailers, and every season and episode with air dates.

## You need a free TMDB API key
1. Make a free account at https://www.themoviedb.org
2. Open Settings > API and request a key (choose "Personal use").
3. Paste the key into the app the first time it opens.

## Option A: get the APK (no coding, about 10 minutes)
1. Create a free account at https://github.com and make a new empty repository.
2. Upload everything in this folder to it (choose "uploading an existing file"
   and drag the contents in, including the hidden `.github` folder).
3. Open the **Actions** tab, pick **Build k3v.1 APK**, press **Run workflow**.
4. After a few minutes, open the finished run and download the **k3v.1** artifact.
   Unzip it to get `k3v.1.apk`.
5. Copy the APK to your phone and open it. If asked, allow "Install unknown apps"
   for your file manager or browser.

## Option B: use it without an APK
Host the `www` folder anywhere (GitHub Pages, Netlify, Cloudflare Pages), open the
link in Chrome on your phone, and choose "Install app" / "Add to Home screen".

## Option C: build locally (needs Node 20, Java 17, Android Studio)
    npm install
    npx cap add android
    npx @capacitor/assets generate --android --assetPath assets
    npx cap sync android
    cd android && ./gradlew assembleDebug

The APK is at android/app/build/outputs/apk/debug/app-debug.apk. Rename it to k3v.1.apk.

Data from TMDB. This product uses the TMDB API but is not endorsed or certified by TMDB.
