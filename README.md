# EVEW — Android Video Editor Project

- **Repository / Gradle root:** `EVEW`
- **Android app label:** `EVEW`
- **Application ID / namespace / Kotlin package:** `com.evew.app`
- **Version:** `0.2.199` (`versionCode 398`)
- **Minimum Android:** API 24
- **Target / Compile SDK:** 35
- **Target ABI:** `armeabi-v7a` (32-bit ARM)

## Project structure and separation

All Kotlin sources are under `app/src/main/java/com/evew/app/`. No legacy `com/evc/app` source directory is included. The app ID and namespace remain `com.evew.app`; output storage and temporary-file naming remain EVEW-specific. The app does not generate `_Info.txt` in Download.

## GitHub Actions / MGit

Workflow: `.github/workflows/android.yml`

The existing workflow file is included **unchanged**. It uses JDK 17, Android SDK 35 / Build Tools 35.0.0, and Gradle 8.9. Push and pull-request triggers cover all branches, and manual execution is enabled. The existing artifact label in the workflow has not been edited.

## Fresh repository setup

This ZIP contains no `.git` directory, Git history, or configured remote. Extract the archive and open the `EVEW` folder itself in MGit. Initialize the repository, stage all files including the hidden `.github` folder, commit, then configure the intended GitHub remote and push.

## Verification status

The archive was checked for a single current Kotlin source location, package/namespace consistency, absence of legacy `com/evc/app` paths, and duplicate file contents. A full Gradle build and on-device test have **not** been run in this packaging environment; GitHub Actions must confirm compilation and APK generation.
