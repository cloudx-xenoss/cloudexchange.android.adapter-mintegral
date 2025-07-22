## 🚀 CloudX Mintegral Adapter Installation Guide

### 📦 Compatibility

#### 🧩 Language Compatibility
- **Kotlin version**: Built with `1.9.22`
    - Host apps should use Kotlin `1.9.0+`
- **Java compatibility**: Compiled to Java 8 bytecode (`jvmTarget = 1.8`)
    - Fully compatible with Java-based host apps (no Kotlin required)

#### 📱 Android Compatibility
- **Minimum SDK version**: `21`
- **Compile SDK version**: `35`
    - Host apps must set `minSdkVersion >= 21` to use the adapter.

#### 🛠️ Build Compatibility
- **Gradle version**: `8.5`
- **Android Gradle Plugin**: `8.2.2`
    - Host apps using AGP `8.0+` and Gradle `8.0+` are fully supported.

---

### 1. Add Maven Central Repository

In your project’s `settings.gradle` or `settings.gradle.kts`  
(You likely already have this by default):

```kotlin
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
    }
}
```

---

### 2. Add Adapter Dependency

In your app/module `build.gradle` or `build.gradle.kts`:

```kotlin
dependencies {
    implementation("io.cloudx.adapter:adapter-mintegral:<latest-version>")
}
```

> Replace `<latest-version>` with the desired version (e.g., `0.0.1`).

---

### 3. Sync and Build

* Sync your project in Android Studio.
* The Mintegral Adapter will be downloaded automatically from Maven Central.

✅ **That’s it! You’re ready to use the CloudX Mintegral Adapter.**

---

### ➕ Related Adapters

You may also integrate other CloudX Adapters:

- [Google Adapter](https://github.com/cloudx-xenoss/cloudexchange.android.adapter-google)
- [CloudX Adapter](https://github.com/cloudx-xenoss/cloudexchange.android.adapter-cloudx)
- [Meta Adapter](https://github.com/cloudx-xenoss/cloudexchange.android.adapter-meta)

> Visit each link for setup guides and available versions.
