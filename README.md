
## 🚀 CloudX Mintegral Adapter Installation Guide
### Prerequisite: Get a GitHub Token
* Go to [GitHub PAT Settings](https://github.com/settings/tokens).
* Generate a new token with read:packages permission.
* Use your GitHub username and token in the credentials block below.


### 1. Add Adapter Repositories
Add this Maven repository in your project’s `settings.gradle` or `settings.gradle.kts` file **inside** the `dependencyResolutionManagement.repositories` block:
```
maven {
    url = uri("https://maven.pkg.github.com/cloudx-xenoss/cloudxchange.android.adapter-mintegral")
    credentials {
        username = "<GITHUB_USERNAME>"
        password = "<GITHUB_TOKEN>"
    }
}
```
*You can use environment variables or Gradle properties if preferred, but for quick setup just put your username/token here (not recommended for open source repos).*

### 2. Add Adapter Dependencies
In your app/module `build.gradle` (or `build.gradle.kts`):
```
dependencies {
    implementation("com.cloudx.adapter:adapter-mintegral:v<latest-verion>")
}
```

*Replace* *`v<latest-version>`* *with the adapter version you want to use.*

### 3. Sync and Build
* Sync your project in Android Studio.
* CloudX Mintegral adapter will be automatically downloaded from GitHub Packages.
