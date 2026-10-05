# Aseprite Builder

[简体中文](README_zh.md)

A fork of [a1393323447/aseprite-builder](https://github.com/a1393323447/aseprite-builder) for building Aseprite through GitHub Actions. The current build matrix runs on Windows; the workflow also contains dependency and build branches for macOS and Linux.

## Build workflow

The [workflow](.github/workflows/build_and_release.yaml) resolves an upstream Aseprite release, prepares Skia, generates Ninja build files with CMake, and packages the executable as a portable ZIP.

It can be triggered manually with `workflow_dispatch`. Changes to `BuildLog.md` on `main` also trigger a build.

## Usage

1. Fork the repository and enable GitHub Actions.
2. Open **Actions → Build and release Aseprite**.
3. Select **Run workflow**.
4. Inspect the job logs and resulting release assets.

A build uses the platform matrix declared in the workflow. macOS and Linux need to be added to that matrix before those jobs will run.

## Licensing

The automation files use the repository's [MIT license](LICENSE). Aseprite and its compiled binaries are subject to the upstream [Aseprite EULA](https://github.com/aseprite/aseprite/blob/main/EULA.txt). Check redistribution rights before sharing generated release assets.
