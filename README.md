# EVEW — Android Video Editor Project

- **Repository / Gradle root:** `EVEW`
- **Android app label:** `EVeditor`
- **Application ID / namespace:** `com.evc.app` (preserved)
- **Version:** `0.2.195` (`versionCode 394`)
- **Minimum Android:** API 24
- **Target / Compile SDK:** 35
- **Target ABI:** `armeabi-v7a` (32-bit ARM)

## GitHub Actions / MGit

Workflow: `.github/workflows/android.yml`

- Push and pull-request triggers cover **all branches** (`branches: ["**"]`).
- Manual execution is enabled with `workflow_dispatch`.
- Uses JDK 17, Android SDK 35 / Build Tools 35.0.0, and Gradle 8.9.
- Builds the debug APK. The existing workflow artifact label remains `EVEW-0.2.191-ARM32-debug-apk`; the workflow YAML was intentionally left unchanged.
- The workflow file is included in this ZIP. Make sure the hidden `.github` folder is staged in the first Commit.

## Fresh repository setup

This ZIP intentionally contains **no `.git` directory, Git history, or configured remote**. Extract the archive and open the `EVEW` folder itself in MGit (not its parent and not an extra nested folder). Initialize a new local repository, stage all files including hidden files/folders, then create the first Commit. Create an empty GitHub repository named `EVEW`, add its HTTPS URL as the remote in MGit, and Push the branch.

If the Actions workflow does not start, first verify on GitHub that `.github/workflows/android.yml` exists in the pushed branch and that the first Commit included it. The workflow is not restricted to `main` or `master`.

## Preserved Android identity

The `applicationId`, namespace, source package, and app label are intentionally unchanged. Renaming the repository does not create a different installed Android app.

## Verification status

The archive structure, project metadata, workflow triggers, and documentation/artifact naming were checked. A full Gradle build and on-device test have not been run in this packaging environment; GitHub Actions must confirm compilation and APK generation.
