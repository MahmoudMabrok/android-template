# Clean architecture kotlin template 🤖

[![Use this template](https://img.shields.io/badge/from-Clean--Architecture--Template-brightgreen?logo=github)](https://github.com/AbdElraoufSabri/android-template/generate) ![Pre Merge Checks](https://github.com/AbdElraoufSabri/android-template/workflows/Pre%20Merge%20Checks/badge.svg)  ![License](https://img.shields.io/github/license/AbdElraoufSabri/android-template.svg) ![Language](https://img.shields.io/github/languages/top/AbdElraoufSabri/android-template?color=blue&logo=kotlin)

A simple **Github template** that lets you create an **Android/Kotlin** project and be up and running in a **few seconds**, Which is suitable for **Clean architecture projects**.

This template is focused on delivering a project with **static analysis** and **continuous integration** already in place.

## How to use 👣

Just click on [![Use this template](https://img.shields.io/badge/-Use%20this%20template-brightgreen)](https://github.com/cortinico/kotlin-android-template/generate) button to create a new repo starting from this template.

Once created don't forget to update the:
- [App ID](buildSrc/src/main/java/Coordinates.kt)
- AndroidManifest: 
  - [UI Module](ui/src/main/AndroidManifest.xml)
  - [Presentation Module](presentation/src/main/AndroidManifest.xml)
  - [Data Module](data/src/main/AndroidManifest.xml)
  - [Device Module](device/src/main/AndroidManifest.xml)
- Package of the source files

## Features 🎨
Someone said features? I heared you, I'll find you 😂😂

- **100% Kotlin-only template**.
- JetPack Compose `1.0.0-alpha11`.
- All layers of clean architecture (UI, Presentation, Domain, Data, Device) you may also add (Remote and Cache as needed).
- Sample Espresso, Instrumentation & JUnit tests.
- 100% Gradle Kotlin DSL setup.
- Dependency versions managed via `buildSrc`.
- CI Setup with GitHub Actions.
- Kotlin Static Analysis via `ktlint` and `detekt`.
- Publishing Ready.
- Issues Template (bug report + feature request).
- Pull Request Template.

## Gradle Setup 🐘

This template is using [**Gradle Kotlin DSL**](https://docs.gradle.org/current/userguide/kotlin_dsl.html) as well as the [Plugin DSL](https://docs.gradle.org/current/userguide/plugins.html#sec:plugins_block) to setup the build.

Dependencies are centralized inside the [Dependencies.kt](buildSrc/src/main/java/Dependencies.kt) file in the `buildSrc` folder. This provides convenient auto-completion when writing your gradle files.

## Static Analysis 🔍

This template is using [**ktlint**](https://github.com/pinterest/ktlint) with the [ktlint-gradle](https://github.com/jlleitschuh/ktlint-gradle) plugin to format your code. To reformat all the source code as well as the buildscript you can run the `ktlintFormat` gradle task.

This template is also using [**detekt**](https://github.com/detekt/detekt) to analyze the source code, with the configuration that is stored in the [detekt.yml](config/detekt/detekt.yml) file (the file has been generated with the `detektGenerateConfig` task).

## CI ⚙️

This template is using [**GitHub Actions**](https://github.com/AbdElraoufSabri/android-template/actions) as CI. You don't need to setup any external service and you should have a running CI once you start using this template.

There are currently the following workflows available:
- [Validate Gradle Wrapper](.github/workflows/gradle-wrapper-validation.yml) - Will check that the gradle wrapper has a valid checksum
- [Pre Merge Checks](.github/workflows/pre-merge.yaml) - Will run the `build`, `check` and `publishToMavenLocal` tasks. 

## Publishing 🚀

The template is setup to be **ready to publish** a library/artifact on a Maven Repository. If you're using JitPack, you don't need any further configuration and you can just configure the repo on JitPack. If you're using another repository (MavenCentral/JCenter/etc.), you need to specify the publishing coordinates.

## Contributing 🤝

Feel free to open a issue or submit a pull request for any bugs/improvements.


## Original Repo

This is just a modification to the great work of [**cortinico**](https://github.com/cortinico) and the [**original repo**](https://github.com/cortinico/kotlin-android-template). I have customized the repo to my needs for further improvements.
