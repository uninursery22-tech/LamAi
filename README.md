# Lam.ai Android project

This is a basic Android project that wraps your existing `Lam_ai.html` chatbot in an Android WebView. It includes a GitHub Actions workflow to build an APK in the cloud.

## Easiest route from a phone (GitHub Actions)

1. Download and unzip `LamAI_Android_Project.zip`.
2. Sign in to GitHub and create a new repository (you can keep it private).
3. Upload the contents of the `LamAI_Android` folder, including the hidden `.github` folder. The `.github/workflows/build-apk.yml` workflow must be included.
4. Open the repository's **Actions** tab and select **Build Lam.ai APK**. Tap **Run workflow** if it has not started automatically.
5. When the run succeeds, open that run and download the **Lam-ai-debug-apk** artifact.
6. Extract the artifact ZIP to find `app-debug.apk`, then open it on your Android phone to install. Android may ask you to allow installs from your browser or file manager; only allow this for files you trust.

## Alternative: Android Studio

1. Install Android Studio from https://developer.android.com/studio on a computer.
2. Open this folder as a project and let Gradle sync.
3. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Find `app-debug.apk` under `app/build/outputs/apk/debug/`.

## Important notes

- The original HTML file is bundled in `app/src/main/assets/Lam_ai.html`.
- This is Android project source, not a precompiled APK. The APK is produced by GitHub Actions or Android Studio.
- Live AI responses require a working API key/configuration in the HTML. Do not publish an APK containing a personal API key; client-side keys can be extracted. For a public app, use a backend that keeps the key private.
- Voice recognition depends on Android/WebView support and may not work on every device.
