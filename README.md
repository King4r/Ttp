# Uncover Android app

Uncover is an idea workbench for app, robot, and engineering projects. It includes structured templates, project status, milestones, a progress indicator, a 15-minute sprint prompt, check-ins, and JSON import/export.

## Build an APK through GitHub Actions
1. Create a new GitHub repository, for example `uncover-app`.
2. Upload the contents of this folder to the repository root (the `.github` folder must be included).
3. Open the repository's **Actions** tab and select **Build Uncover APK**. If prompted, enable workflows.
4. Run the workflow with **Run workflow**, or push to `main`/`master`.
5. Open the completed workflow run, scroll to **Artifacts**, and download `uncover-debug-apk`. Inside is `app-debug.apk`.
6. Transfer the APK to your Android device and install it. Android may ask you to allow installation from that source.

## Local build (optional)
Requires JDK 17, Gradle 8.x, and Android SDK platform 35. Run `gradle assembleDebug`; APK output is `app/build/outputs/apk/debug/app-debug.apk`.

## Data & limitations
This prototype saves ideas locally on the device using WebView local storage. It does not include accounts, cloud sync, team collaboration, or automatic backups. Use **Data → Export all ideas** regularly. The included APK is a debug build intended for testing; before public Play Store distribution, add a proper release signing setup, privacy policy, and testing.
