# Elora Android prototype

This is an Android app **source project**, not a compiled APK. GitHub Actions builds a debug-signed installable APK using JDK 17, Gradle 8.9 and AGP 8.7.3.

## Capabilities
- Local chat history persisted on device
- Basic scripted offline response mode (NOT an offline language model)
- Optional OpenAI-compatible HTTPS chat completions endpoint and API key (provider may charge)

Not yet implemented: true local AI inference, advanced memory retrieval, character editor, autonomous evolution, adult-mode controls, or polished UI. The API key is stored in ordinary Android SharedPreferences, not encrypted; do not use a valuable production key. Use only a trusted endpoint.

## Build without Android Studio
1. Create a GitHub repository and upload the contents of this project, including the hidden `.github/workflows/android.yml` directory. On a phone, uploading many individual files can be difficult; using GitHub's web UI or an integrated GitHub connector may help.
2. Open the repository's **Actions** tab and select **Build Elora APK**, then **Run workflow**. A push to main also starts a build.
3. When the workflow succeeds, open its run and download the **Elora-Android-APK** artifact. Unzip the artifact to obtain `app-debug.apk`.
4. Open `app-debug.apk` on the Samsung device and approve **Install unknown apps** for the app used to open it if Android asks.

Debug signing is for personal testing, not public app distribution. No build was run in this chat environment.
