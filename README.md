<h1 align="center">Golden Launcher</h1>

<img src="https://github.com/Golden-Launcher-Org/Golden-Android/blob/main/app_pojavlauncher/src/main/assets/pojavlauncher.png" align="left" width="130" height="130" alt="Golden Launcher logo">

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Golden-Launcher-Org/Golden-Android)
![GitHub Downloads](https://img.shields.io/github/downloads/Golden-Launcher-Org/Golden-Android/total)
![Platform](https://img.shields.io/badge/platform-Android-gold?style=flat)
![Min SDK](https://img.shields.io/badge/minSdk-26-gold?style=flat)
![Android CI](https://github.com/Golden-Launcher-Org/Golden-Android/workflows/Android%20CI/badge.svg)
[![Discord](https://img.shields.io/discord/YOUR_DISCORD_ID?color=FFD700&logo=discord&logoColor=white&label=&style=flat)](https://discord.gg/YOUR_INVITE)

Golden is a gold-themed fork of [Golden Launcher](https://github.com/Golden-Launcher-Org/Golden-Android) that lets you play Minecraft: Java Edition on your Android devices with a sleek, customized experience.

## Table of Contents

* [Introduction](#introduction)
* [Getting Golden](#getting-golden)
* [Building](#building)
    * [Quick Build (Recommended)](#quick-build-recommended)
    * [Detailed Build](#detailed-build)
* [Features](#features)
* [Known Issues](#known-issues)
* [Contributing](#contributing)
* [Support](#support)
* [License](#license)
* [Credits & Dependencies](#credits--dependencies)

## Introduction

* Golden is a Minecraft: Java Edition launcher for Android based on [Golden Launcher](https://github.com/Golden-Launcher-Org/Golden-Android), [Amethyst Launcher](https://github.com/AngelAuraMC/Amethyst-Android), [PojavLauncher](https://github.com/PojavLauncherTeam/PojavLauncher) and [Boardwalk](https://github.com/zhuowei/Boardwalk).
* This launcher supports nearly all Minecraft versions from rd-132211 to 26.x snapshots (including Combat Test versions).
* Modding via Forge and Fabric are fully supported.
* Customized with a gold theme and landscape support for an enhanced mobile experience.
* This repository contains the source code for Android.

## Getting Golden

You can get Golden via three methods:

1. **Nightly Builds:** Download the latest artifact from [Nightly.link](https://nightly.link/Golden-Launcher-Org/Golden-Android/workflows/android/main?preview)
2. **Releases:** Download the latest prebuilt app [from Releases](https://github.com/Golden-Launcher-Org/Golden-Android/releases/)
3. **Build from Source:** Follow the [building instructions](#building) below.

## Building

### Quick Build (Recommended)

The easiest way to build Golden is to use the pre-built JREs provided by our CI.

1. Clone the repository: `git clone --recursive https://github.com/Golden-Launcher-Org/Golden-Android.git`
2. Build the launcher: `./gradlew :app_pojavlauncher:assembleDebug` (Use `gradlew.bat` on Windows)

The built APK will be located in `app_pojavlauncher/build/outputs/apk/debug/`.

### Detailed Build

If you need more control over the build process, follow these steps:

1. **Java Runtime Environment (JRE):** Download the `jre8-pojav` artifact from AngelAuraMCs [CI auto builds](https://github.com/AngelAuraMC/openjdk-build-multiarch/actions). This package contains pre-built JREs for all supported architectures. If you need to build the JRE yourself, follow the instructions in the [android-openjdk-build-multiarch](https://github.com/AngelAuraMC/openjdk-build-multiarch) repository.

2. **LWJGL:** The build instructions for the custom LWJGL are available in the [LWJGL repository](https://github.com/AngelAuraMC/lwjgl3).

3. **Language List:** Because languages are auto-added by Crowdin, you need to run the language list generator before building. In the project directory, run:
   * Linux/macOS:
     ```bash
     chmod +x scripts/languagelist_updater.sh
     bash scripts/languagelist_updater.sh
     ```
   * Windows:
     ```batch
     scripts\languagelist_updater.bat
     ```

4. **Build GLFW stub:** `./gradlew :jre_lwjgl3glfw:build`

5. **Build the launcher:** `./gradlew :app_pojavlauncher:assembleDebug` (Replace `gradlew` with `gradlew.bat` on Windows).

## Features

✨ **Gold-Themed UI** - A sleek, customized gold aesthetic throughout the launcher
📱 **Landscape Support** - Full landscape layout support for tablets and rotated devices
🎮 **Full Version Support** - Play from ancient versions to the latest snapshots
🔧 **Modding Ready** - Forge and Fabric support built-in
📦 **Resource & Shader Packs** - Integrated pack managers and downloaders
🌍 **Multi-Language** - Community translations via Crowdin
⚡ **High Performance** - Optimized rendering with multiple renderer options

## Known Issues

See Golden's [issue tracker](https://github.com/Golden-Launcher-Org/Golden-Android/issues) for a list of known issues and their current status.

## Contributing

We welcome contributions! Feel free to:
- Report bugs via [issue tracker](https://github.com/Golden-Launcher-Org/Golden-Android/issues)
- Submit pull requests for improvements
- Join our Discord community for discussions

## Support

For support, questions, or just to hang out, join our [Discord server](https://discord.gg/YOUR_INVITE)

## License

Golden is licensed under [GNU LGPLv3](https://github.com/Golden-Launcher-Org/Golden-Android/blob/main/LICENSE).

## Credits & Dependencies

**Upstream Projects:**
* [Golden Launcher](https://github.com/Golden-Launcher-Org/Golden-Android): [LGPL-3.0 license](https://github.com/Golden-Launcher-Org/Golden-Android/blob/main/LICENSE)
* [Amethyst Launcher](https://github.com/AngelAuraMC/Amethyst-Android/): [LGPL-3.0 license](https://github.com/AngelAuraMC/Amethyst-Android/blob/v3_openjdk/LICENSE)
* [PojavLauncher](https://github.com/PojavLauncherTeam/PojavLauncher): [GLGPL](https://github.com/PojavLauncherTeam/PojavLauncher/blob/v3_openjdk/LICENSE)
* [Boardwalk](https://github.com/zhuowei/Boardwalk) (JVM Launcher): Unknown License/[Apache License 2.0](https://github.com/zhuowei/Boardwalk/blob/master/LICENSE) or GNU GPLv2.

**Core Dependencies:**
* [MojoLauncher](https://github.com/MojoLauncher/MojoLauncher/): [LGPL-3.0 license](https://github.com/MojoLauncher/MojoLauncher/blob/main/LICENSE)
* [FCL-team](https://github.com/FCL-Team/FoldCraftLauncher/): [GPL-3.0 license](https://github.com/FCL-Team/FoldCraftLauncher/blob/main/LICENSE)
* [GL4ES](https://github.com/AngelAuraMC/gl4es): [MIT License](https://github.com/ptitSeb/gl4es/blob/master/LICENSE)
* [Krypton Wrapper](https://github.com/BZLZHH/NG-GL4ES): [MIT License](https://github.com/BZLZHH/NG-GL4ES/blob/main/LICENSE)
* [MobileGlues](https://github.com/MobileGL-Dev/MobileGlues): [LGPL-2.1 License](https://github.com/MobileGL-Dev/MobileGlues/blob/dev-es/LICENSE)
* [ANGLE](https://chromium.googlesource.com/angle/angle): [All Rights Reserved](app_pojavlauncher/src/main/assets/licenses/ANGLE_LICENSE)
* [OpenJDK](https://github.com/AngelAuraMC/openjdk-multiarch-jdk8u): [GNU GPLv2 License](https://openjdk.java.net/legal/gplv2+ce.html)
* [LWJGL3](https://github.com/AngelAuraMC/lwjgl3): [BSD-3 License](https://github.com/LWJGL/lwjgl3/blob/master/LICENSE.md)
* [LWJGLX](https://github.com/AngelAuraMC/lwjglx): unknown license
* [Mesa 3D Graphics Library](https://gitlab.freedesktop.org/mesa/mesa): [MIT License](https://docs.mesa3d.org/license.html)
* [bhook](https://github.com/bytedance/bhook): [MIT license](https://github.com/bytedance/bhook/blob/main/LICENSE)
* [libepoxy](https://github.com/anholt/libepoxy): [MIT License](https://github.com/anholt/libepoxy/blob/master/COPYING)
* [virglrenderer](https://github.com/AngelAuraMC/virglrenderer): [MIT License](https://gitlab.freedesktop.org/virgl/virglrenderer/-/blob/master/COPYING)
* [OpenAL-Soft](https://github.com/kcat/openal-soft): [GNU GPLv2](app_pojavlauncher/src/main/assets/licenses/OPENAL-SOFT_GPL2)
  * [oboe](https://github.com/google/oboe): [Apache License 2.0](app_pojavlauncher/src/main/assets/licenses/OBOE_APACHE2)
  * [pfffft](https://bitbucket.org/jpommier/pffft/src/master/): [ARR](app_pojavlauncher/src/main/assets/licenses/PFFFT_LICENSE)
* [SDL3](https://github.com/libsdl-org/SDL): [zlib License](https://github.com/libsdl-org/SDL/blob/main/LICENSE.txt)
* [sdl2-compat](https://github.com/libsdl-org/sdl2-compat): [zlib License](https://github.com/libsdl-org/sdl2-compat/blob/main/LICENSE.txt)
* [Android Support Libraries](https://android.googlesource.com/platform/prebuilts/maven_repo/android/+/master/NOTICE.txt): [Apache License 2.0](https://android.googlesource.com/platform/prebuilts/maven_repo/android/+/master/NOTICE.txt)

**Thanks to:**
* [MCHeads](https://mc-heads.net) for Minecraft avatars
* [Modrinth](https://api.modrinth.com/), [CurseForge](https://docs.curseforge.com/rest-api/) and [McLo.gs](https://api.mclo.gs) for free APIs
* The Minecraft Android launcher community for continued support and feedback
