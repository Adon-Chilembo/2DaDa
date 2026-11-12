# 2DaDa

A fast tap-sequence game for Android. Each round starts by tapping **1**. After that, tap **da** twice before each of the next numbers, in order, before the timer runs out. You get through 5 chapters, and each one is set against a different scene from Zambia:

1. The flag of Zambia
2. Mosi-oa-Tunya (Victoria Falls)
3. Sunset on the Zambezi River
4. South Luangwa: elephants at dusk
5. The African fish eagle, Zambia's national bird

## Rewards

Clearing chapters and rounds unlocks rewards, which you can browse in the **Rewards** screen on the welcome page:

- **Themes:** collect the Zambia scenes and use one as your welcome-page background.
- **Number designs:** Classic, Copper, Malachite, Chitenge and Flag colours.

Progress is saved on the device.

## Project layout

- `www/index.html`: the whole game (HTML, CSS and JS, with the scenes drawn as inline SVG)
- `www/fonts/`: bundled fonts, so the app works offline
- `android/`: the native Android project (Capacitor)

## Build the APK

Requires Node.js and Android Studio.

```bash
npm install
npx cap sync android
cd android && ./gradlew assembleDebug
```

The APK is written to `android/app/build/outputs/apk/debug/app-debug.apk`.

To test a specific chapter in a browser, serve `www/` and open `index.html?chapter=3`.
