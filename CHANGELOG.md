# Changelog

All notable changes to this project will be documented in this file.

## [1.0.37-patch1] - 2026-06-15

### Changed

* Updated plugin compatibility metadata to support newer Android Studio and IntelliJ Platform releases.
* Modified the IDE build compatibility range in `META-INF/plugin.xml`:

  ```xml
  <idea-version since-build="242" until-build="270.*" />
  ```
* Increased the maximum supported build version from `255.*` to `270.*`.

### Technical Details

* Extracted `profiler.jar` from the plugin distribution package.
* Updated `META-INF/plugin.xml` inside the JAR.
* Repackaged the modified `profiler.jar`.
* Rebuilt the final `profiler-1.0.37.zip` distribution package.

### Compatibility

* Added support for:

    * Android Studio Quail 1 (2026.1.1 Patch)
    * Build: `AI-261.23567.138`
    * IntelliJ Platform 261-based IDEs

### Fixed

* Resolved plugin installation failure caused by the restrictive compatibility definition:

  ```xml
  until-build="255.*"
  ```
* Plugin can now be installed successfully using **Settings → Plugins → Install Plugin from Disk...** on supported Android Studio versions.

### Notes

* No functional changes were made to plugin features or runtime behavior.
* This release only updates IDE compatibility metadata.
