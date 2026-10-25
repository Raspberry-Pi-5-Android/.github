# Android (AOSP) for Raspberry Pi 5

A board support package (BSP) that runs **AOSP Android** on the **Raspberry Pi 5**, built from AOSP,
the official Raspberry Pi kernel and firmware, and upstream open source projects.

## Android versions

| Android | Branch | Latest release | Status |
|---|---|---|---|
| 15 (`AOSP android-15.0.0_r1`) | `android-15` | `v0.9.0` | Work in progress |

## Features
 
- Boots from microSD to the home screen (64-bit)
- GPU acceleration: OpenGL ES 3.1 and Vulkan 1.3
- Ethernet, Wi-Fi and Bluetooth audio
- USB keyboard and mouse
## Limitations
 
- SELinux permissive, storage not encrypted
- `userdebug` build only
- No Google apps

## Repositories

| Repository | Contents |
|---|---|
| [`android_device_rpi_rpi5`](https://github.com/Raspberry-Pi-5-Android/android_device_rpi_rpi5) | Device configuration |
| [`android_vendor_rpi_rpi5`](https://github.com/Raspberry-Pi-5-Android/android_vendor_rpi_rpi5) | Vendor files, GPU drivers, firmware |
| [`android_kernel_rpi_bcm2712`](https://github.com/Raspberry-Pi-5-Android/android_kernel_rpi_bcm2712) | Kernel, device trees, modules |
| [`android_external_minigbm`](https://github.com/Raspberry-Pi-5-Android/android_external_minigbm) | Graphics buffer allocator |
| [`android_local_manifest`](https://github.com/Raspberry-Pi-5-Android/android_local_manifest) | Local manifest for building |

## License and disclaimer

Each component keeps the license of its source. Personal project, not affiliated with Google or
Raspberry Pi Ltd. Android is a trademark of Google LLC; Raspberry Pi is a trademark of
Raspberry Pi Ltd.
