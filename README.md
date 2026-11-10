# Minimal Key — GitHub APK build project

Build the Android APK with GitHub Actions without installing Android Studio.

## Steps

1. Create a repository on GitHub named `Minimal-Key`.
2. Extract this ZIP.
3. Upload **all contents inside the `MinimalKey_GitHub` folder** to the root of your GitHub repository. Include the hidden `.github` folder and its `workflows/build.yml` file.
4. Commit the files to the `main` branch.
5. Open the repository's **Actions** tab.
6. Choose **Build Minimal Key APK**. If no run started automatically, select **Run workflow**.
7. Wait for the workflow to finish successfully.
8. Open the completed workflow run and find **Artifacts** near the bottom.
9. Download `Minimal-Key-debug-APK` and extract it. The APK is `app-debug.apk`.
10. Transfer the APK to your Android phone and install it. Allow installation from the browser/file manager if Android asks.

If GitHub's mobile app does not offer file upload, open github.com in your phone browser and enable **Desktop site**. Upload the extracted files there.

## What the workflow does

- Sets up Java 17 and Android SDK platform 35.
- Downloads Gradle 8.9.
- Runs `gradle assembleDebug`.
- Publishes the debug APK as a GitHub Actions artifact.

## Project status

This is an early MVP/source project, not a production-ready keyboard. A successful build only confirms that the source compiles; it does not guarantee that every feature works correctly on every Android device. Test it before using it for sensitive typing.

The current MVP includes an English QWERTY keyboard, number row, basic keypress animation, spacebar cursor movement, and basic appearance/height preferences. Some requested customization features still need further implementation. The app has no internet permission and is designed not to transmit typed text.
