# Alloy Android SDK Maven Repository

This repository hosts the Maven artifacts for the Alloy Android SDK.

## Current Version: 0.1.0-pre.d178f8 (Prerelease)

⚠️ **This is a prerelease version** - Use for testing only, not recommended for production.

## Installation

Add the Alloy Android SDK to your Android project:

### Gradle (Kotlin DSL)

```kotlin
repositories {
    maven {
        url = uri("https://raw.githubusercontent.com/alloy-ch/rcplus-alloy-android-sdk-maven/v0.1.0-pre.d178f8/")
    }
}

dependencies {
    implementation("com.alloy:android-sdk:0.1.0-pre.d178f8")
}
```

### Gradle (Groovy)

```gradle
repositories {
    maven {
        url 'https://raw.githubusercontent.com/alloy-ch/rcplus-alloy-android-sdk-maven/v0.1.0-pre.d178f8/'
    }
}

dependencies {
    implementation 'com.alloy:android-sdk:0.1.0-pre.d178f8'
}
```

## Available Versions

- **Latest**: 0.1.0-pre.d178f8 (Prerelease)
- **Repository Structure**: This repository uses semantic versioning with git tags for both releases and prereleases

## Version-Specific URLs

Each version of the SDK has its own immutable Maven repository URL:

- **Prerelease**: `https://raw.githubusercontent.com/alloy-ch/rcplus-alloy-android-sdk-maven/v0.1.0-pre.d178f8/`

## Usage

### Quick Start

1. Add the repository and dependency to your `build.gradle.kts`:

```kotlin
repositories {
    google()
    mavenCentral()
    maven {
        url = uri("https://raw.githubusercontent.com/alloy-ch/rcplus-alloy-android-sdk-maven/v0.1.0-pre.d178f8/")
    }
}

dependencies {
    implementation("com.alloy:android-sdk:0.1.0-pre.d178f8")
}
```

2. Add required permissions to your `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

3. Initialize the SDK in your Application class:

```kotlin
class MyApplication : Application() {
    private lateinit var alloySDK: AlloySDK
    
    override fun onCreate() {
        super.onCreate()
        
        alloySDK = AlloySDK(
            context = this,
            tenant = "your-tenant",
            env = "prod", 
            appId = "your-app-id"
        )
    }
    
    fun getAlloySDK(): AlloySDK = alloySDK
}
```

## Requirements

- **Android 5.0 (API level 21) or higher**
- **Kotlin 1.9.0 or higher**
- **Target SDK 34** (Android 14)
- **Google Play Services** (for AAID and App Set ID)

---

**Generated**: 2025-08-26 14:46:34 UTC  
**Version**: 0.1.0-pre.d178f8  
**Type**: Prerelease
