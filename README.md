# Expo Android Build Failure: AGP Version Incompatibility

This repository demonstrates a common issue encountered when building Android apps with Expo CLI: incompatibility between different versions of the Android Gradle Plugin (AGP).  The problem often arises from conflicting versions specified in various Gradle files within the Android project.

## Problem

Expo's Android build process relies on a specific version range of AGP. Mismatches between the AGP version declared in `gradle-wrapper.properties`, project-level `build.gradle`, and module-level `build.gradle` files can lead to build failures.

The error messages can be cryptic and don't always clearly point to the version conflict.  This example shows how subtle differences in versions can cause the build to break.

## Solution

The solution involves careful examination of the AGP versions used across all Gradle files.  Ensure all versions are compatible with each other and with the version recommended or used by Expo for your project.  Sometimes, updating Gradle files to use the latest compatible AGP versions resolves the conflict.  In other cases, it might be required to downgrade specific dependencies.