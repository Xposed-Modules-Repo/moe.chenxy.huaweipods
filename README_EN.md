<div align="center">

<img src="https://github.com/user-attachments/assets/e8a3df6b-6e67-485a-ae1c-018ac24e87d4" width="120" height="120" style="border-radius: 24px;" alt="HuaweiPods Icon"/>

# HuaweiPods

**Huawei audio device integration for Xiaomi HyperOS**

[![Android 15+](https://img.shields.io/badge/Android-15%2B-3DDC84?style=flat-square&logo=android&logoColor=white)](https://www.android.com/)
[![HyperOS](https://img.shields.io/badge/ROM-HyperOS-FF6900?style=flat-square)](https://hyperos.mi.com/)
[![LSPosed](https://img.shields.io/badge/Framework-LSPosed-6F42C1?style=flat-square)](https://github.com/LSPosed/LSPosed)

[Source repository](https://github.com/Nshpiter/HuaweiPods) ·
[Setup guide](https://github.com/Nshpiter/HuaweiPods/blob/main/docs/guide/getting-started.md) ·
[Issue tracker](https://github.com/Nshpiter/HuaweiPods/issues) ·
QQ group `1022359908`

**English** · **[Simplified Chinese](README.md)**

</div>

HuaweiPods is an Xposed module for Xiaomi and Redmi devices running HyperOS. It integrates supported Huawei audio devices with the system Bluetooth detail page, connection popup, Super Island, and Fusion Device Center.

## Supported models

The unified build supports the 14 models below in one APK. Model-specific test APKs are no longer distributed.

| Model | Status | Integrated capabilities |
| --- | --- | --- |
| HUAWEI FreeBuds 3 | Stable | Battery, ANC on/off, nine-position spatial ANC dial, double-tap gestures, and system UI integration |
| HUAWEI FreeBuds 4E | Extended support | Battery, ANC/off with Light/Balanced levels and readback, left/right double-tap and press-and-hold, wear detection, fixed swipe-volume guidance, three official sound presets, and official color images |
| HUAWEI FreeBuds 5 | Extended support | Battery, ANC/off readback, Smart/Light/Balanced ANC levels, wear detection, four official sound presets, high-quality audio and low-latency auto-apply; gesture settings remain pending |
| HUAWEI FreeBuds 5i | Extended support | Battery, transparency/ANC/off readback, Smart/Light/Balanced/Deep ANC levels, left/right double-tap, wear detection, four official sound presets, high-quality audio, low-latency auto-apply, and official color images; long-press and swipe settings remain pending |
| HUAWEI FreeBuds 6i | Extended support | Battery, transparency/ANC/off, four ANC levels, voice transparency, double/triple-tap gestures, four official sound presets, a 10-band custom EQ, low-latency auto-apply, and dedicated images |
| HUAWEI FreeBuds Pro 3 | Extended support | Battery, three-mode control and readback, four ANC levels, voice transparency, long-press/pinch/swipe gestures, and low-latency auto-apply |
| HUAWEI FreeBuds Pro 4 | Basic support | Battery and ANC/off; no verified ANC state readback or gesture settings |
| HUAWEI FreeBuds Pro 5 | Basic support | Battery, transparency/ANC/off, state readback, and low-latency auto-apply; ANC levels and gestures remain pending |
| HUAWEI FreeBuds 7i | Extended support | Battery, transparency/ANC/off readback, four ANC levels, double/triple-tap, long-press and swipe-volume gestures, wear detection, head-motion control, spatial audio, four sound presets, a 10-band custom EQ, high-quality audio, low-latency auto-apply, dual-device list management, and official color images |
| HUAWEI FreeClip | Basic support | Left/right/case battery; no traditional ANC |
| HUAWEI FreeClip 2 | Extended support | Battery, double/triple-tap and swipe gestures, spatial audio, low-latency auto-apply, and selected wearing/audio settings; no traditional ANC |
| HUAWEI FreeArc | Extended support | Left/right/case battery, double/triple-tap, press-and-hold and swipe gestures, five official sound presets, a 10-band custom EQ, and official color images; no traditional ANC |
| HUAWEI Eyewear (1st generation) | Basic support | Left/right temple battery and system UI integration; no ANC |
| HUAWEI Eyewear 2 | Basic support | Left/right temple battery, double-tap/swipe gestures, and low-latency auto-apply; no ANC |

Models marked Basic or Extended still benefit from real-device regression testing. Official features not listed in the table should not be assumed to work.

## Features

- Battery and model-specific controls in the system Bluetooth detail page
- HyperOS connection popup, Super Island, and Fusion Device Center integration
- Model-aware ANC, transparency, ANC level, and gesture controls
- Manual model selection by Bluetooth address for renamed or unrecognized devices
- In-app update checks and scoped-process restart after an update

## Requirements

- Xiaomi or Redmi device
- HyperOS based on Android 15 or newer
- LSPosed API 101 or newer

## Quick start

1. Install HuaweiPods and enable it in LSPosed.
2. Select `com.android.bluetooth`, `com.android.settings`, `com.milink.service`, and `com.xiaomi.bluetooth` as scopes.
3. Restart the scoped processes from HuaweiPods, or reboot the phone.
4. Connect a supported device and use the integrated features from HuaweiPods or the system UI.

For additional model adaptation or device testing, join QQ group `1022359908`. Reproducible problems can be reported through [GitHub Issues](https://github.com/Nshpiter/HuaweiPods/issues).

## Credits

- [OppoPods](https://github.com/1812z/OppoPods) by 1812z — the fork HuaweiPods was directly adapted from
- [OppoPods](https://github.com/Leaf-lsgtky/OppoPods) by Leaf-lsgtky — the original upstream project
- [HyperPods](https://github.com/Art-Chen/HyperPods) by Art_Chen
- [HyperIsland](https://github.com/1812z/HyperIsland) by 1812z — interaction reference for update checks and onboarding
- [Miuix](https://github.com/YuKongA/miuix)

## License

[GPL-3.0](LICENSE)
