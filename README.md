# BigBlueButton mobile SDK: Android Maven repository

Static Maven repository for the Android AAR of the
[BigBlueButton mobile SDK](https://github.com/ahmad-bbbb/bigbluebutton-mobile-sdk):
`org.bigbluebutton.bbb:meeting-sdk-fused-release`. Gradle downloads single files from it; there is
no need to clone it.

```kotlin
// settings.gradle.kts
dependencyResolutionManagement {
  repositories {
    google()
    mavenCentral()
    maven {
      url = uri("https://raw.githubusercontent.com/ahmad-bbbb/bigbluebutton-mobile-sdk-maven/main")
      content { includeGroup("org.bigbluebutton.bbb") }
    }
  }
}
```

```kotlin
// app/build.gradle.kts
dependencies {
  implementation("org.bigbluebutton.bbb:meeting-sdk-fused-release:0.2.0")
}
```

The rest of the host-app setup (packaging rules, Guava, minification, permissions, code) is in the
[Android guide](https://github.com/ahmad-bbbb/bigbluebutton-mobile-sdk/blob/main/android/README.md).
Flutter apps get this repository automatically through the `bbb_meeting_sdk` plugin. Published
versions: [`org/bigbluebutton/bbb/meeting-sdk-fused-release/`](org/bigbluebutton/bbb/meeting-sdk-fused-release/).

License: LGPL-3.0 (see [LICENSE](LICENSE)).
