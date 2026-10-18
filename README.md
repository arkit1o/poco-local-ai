# POCO Local AI

Starter project for an Android on-device AI chat using `llama.rn`. It does not require a paid API key. The language model is a separate GGUF file and runs locally on the phone.

## Important status
This is **source code, not a finished APK**. The first Android build must be checked in GitHub Actions, and native-library compatibility may require adjustments. No model is bundled in this archive.

## Upload to GitHub
1. Open https://github.com/arkit1o/poco-local-ai
2. Tap **Add file** → **Upload files**.
3. Extract this ZIP first, then upload the *contents* of the `poco-local-ai` folder (not the ZIP itself).
4. Tap **Commit changes**.
5. Open the **Actions** tab and select **Build Android APK**. If GitHub asks to enable Actions, enable it.
6. When the workflow finishes, open the run and download the `poco-local-ai-debug-apk` artifact.

## Model
You need a compatible `.gguf` model separately. Start with a small 1B–3B instruct model quantized to Q4_K_M; check its licence and confirm the file is from a trusted source. Keep in mind RAM and storage limits. This starter UI currently has a model-path input and chat shell; model loading / file selection can need device-specific adjustments before it runs end-to-end.

## Build workflow
The GitHub Actions workflow runs Expo prebuild and Gradle to create a debug APK. A successful workflow is not guaranteed until the first run is tested; review the build log if it fails.
