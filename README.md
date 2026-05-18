# Google News RSS Android WebView

Android wrapper for the existing `google_news` FastAPI web interface.

## Configure URL

Edit `gradle.properties`:

```properties
GOOGLE_NEWS_WEB_URL=http://193.124.24.115/
```

Use `10.0.2.2` for the Android emulator when the FastAPI service runs on the same Ubuntu host.
For a real phone, set a reachable IP address or domain. If the service is exposed directly on port `8100`, use:

```properties
GOOGLE_NEWS_WEB_URL=http://193.124.24.115:8100/
```

## Build

Install JDK 17 and Android SDK command-line tools, then run:

```bash
export ANDROID_HOME=/path/to/android-sdk
export ANDROID_SDK_ROOT=/path/to/android-sdk
./gradlew assembleDebug
```

The debug APK will be created at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

This project includes a Gradle Wrapper pinned to Gradle 8.10.2, so the old
system `gradle` package is not required.
