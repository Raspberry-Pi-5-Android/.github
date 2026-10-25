# Android (AOSP) for Raspberry Pi 5

A board support package (BSP) that runs **AOSP Android** on the **Raspberry Pi 5**, built from AOSP,
the official Raspberry Pi kernel and firmware, and upstream open source projects such as Mesa.

> **Status: public preview, work in progress.** It boots and is usable, but it is not a finished
> product yet.

<!-- TODO: photo or GIF of the Pi 5 running Android -->

## Android versions

Each Android version lives on its own branch with the same name in every repository.

| Android | Branch | Latest release | Status |
|---|---|---|---|
| 15 (AOSP `android-15.0.0_r1`) | `android-15` | `v0.9.0` | Work in progress |

## Android 15 at a glance

**Works**
- Boots from microSD to the home screen, 64-bit only
- GPU acceleration with Mesa: OpenGL ES 3.1 and Vulkan 1.3
- Raspberry Pi kernel 6.12, built reproducibly from source
- Ethernet, Wi-Fi and Bluetooth audio
- USB keyboard and mouse

**Not yet**
- SELinux is permissive and storage is not encrypted
- Only the `userdebug` build variant
- No Google apps or Play Store
- No ready-to-flash image yet (planned for `v1.0.0`)

The full feature list, known issues, and build and flash instructions are in the repositories below.

## Repositories

| Repository | Contents |
|---|---|
| [`android_device_rpi_rpi5`](https://github.com/Raspberry-Pi-5-Android/android_device_rpi_rpi5) | Device configuration: product and board setup, init scripts, HALs, feature list |
| [`android_vendor_rpi_rpi5`](https://github.com/Raspberry-Pi-5-Android/android_vendor_rpi_rpi5) | Vendor files: firmware configuration, Mesa GPU drivers, Wi-Fi and Bluetooth firmware |
| [`android_kernel_rpi_bcm2712`](https://github.com/Raspberry-Pi-5-Android/android_kernel_rpi_bcm2712) | Kernel, device trees and modules, with the script that builds them |
| [`android_external_minigbm`](https://github.com/Raspberry-Pi-5-Android/android_external_minigbm) | AOSP graphics buffer allocator with Raspberry Pi 5 support |
| [`android_local_manifest`](https://github.com/Raspberry-Pi-5-Android/android_local_manifest) | Adds these repositories to an AOSP checkout — start here to build |

## License and disclaimer

Every component keeps the license of its source (Apache 2.0 for AOSP, GPL-2.0 for the kernel, MIT
for Mesa, and the vendor licenses of the wireless firmware); details are in each repository.

This is a personal project, not affiliated with or endorsed by Google or Raspberry Pi Ltd.
Android is a trademark of Google LLC; Raspberry Pi is a trademark of Raspberry Pi Ltd.
