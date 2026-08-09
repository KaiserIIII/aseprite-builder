# Aseprite Builder

> Build Aseprite for Windows, macOS, and Ubuntu with a manually triggered GitHub Actions workflow.

## Before you use this repository

Aseprite source code is available under its own license and EULA. Building it for personal use is different from redistributing compiled binaries. Review the upstream [Aseprite EULA](https://github.com/aseprite/aseprite/blob/main/EULA.txt) before running or modifying this workflow.

> Do not publish or share generated Aseprite binaries unless you have the legal right to distribute them. Remove generated GitHub Release assets after downloading your personal build.

## Usage

1. Fork this repository.
2. Open the fork's **Actions** tab.
3. Enable workflows if GitHub asks you to do so.
4. Select **Build and release Aseprite**.
5. Choose **Run workflow** and wait for all requested platform jobs to finish.
6. Download your build from the generated release, then delete the release and its assets when you no longer need them.

![Triggering the workflow](https://github.com/user-attachments/assets/5174f407-4daf-4e28-996e-5efb4f8751cb)

The workflow definition is located at [`.github/workflows/build_and_release.yaml`](.github/workflows/build_and_release.yaml). Build progress and errors are available in the individual Actions job logs.

## Troubleshooting

### Windows: `libcrypto-1_1-x64.dll` is missing

1. Download [OpenSSL 1.1.1w](https://download.firedaemon.com/FireDaemon-OpenSSL/openssl-1.1.1w.zip).
2. Extract `x64/bin/libcrypto-1_1-x64.dll`.
3. Place the DLL in the same directory as `aseprite.exe`.
4. Start Aseprite again.

Only download third-party binaries from sources you trust and verify them when checksums or signatures are available.

## License and attribution

The automation files in this repository are covered by this repository's [LICENSE](LICENSE). Aseprite itself, its source code, and generated binaries remain subject to Aseprite's upstream licensing terms.
