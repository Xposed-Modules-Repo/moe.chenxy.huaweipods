<div align="center">

<img src="https://github.com/user-attachments/assets/e8a3df6b-6e67-485a-ae1c-018ac24e87d4" width="120" height="120" style="border-radius: 24px;" alt="HuaweiPods Icon"/>

# HuaweiPods

**让华为耳机接入小米 HyperOS 的系统体验**

[![Android 15+](https://img.shields.io/badge/Android-15%2B-3DDC84?style=flat-square&logo=android&logoColor=white)](https://www.android.com/)
[![HyperOS](https://img.shields.io/badge/ROM-HyperOS-FF6900?style=flat-square)](https://hyperos.mi.com/)
[![LSPosed](https://img.shields.io/badge/Framework-LSPosed-6F42C1?style=flat-square)](https://github.com/LSPosed/LSPosed)

[项目主页](https://github.com/Nshpiter/HuaweiPods) ·
[使用文档](https://github.com/Nshpiter/HuaweiPods/blob/main/docs/guide/getting-started.md) ·
[问题反馈](https://github.com/Nshpiter/HuaweiPods/issues) ·
QQ群 `1022359908`

**简体中文** · **[English](README_EN.md)**

</div>

HuaweiPods 是一个面向小米 / Redmi HyperOS 设备的 Xposed 模块，将华为耳机接入系统蓝牙详情页、连接弹窗、超级岛与融合设备中心。

## 支持型号

当前统一版已集成下列 14 个型号，所有型号使用同一个 APK，不再按型号单独分发测试包。

| 型号 | 状态 | 当前能力 |
| --- | --- | --- |
| HUAWEI FreeBuds 3 | 稳定 | 电量、降噪开关、9 档降噪空间方向、双击手势与系统界面集成 |
| HUAWEI FreeBuds 4E | 扩展支持 | 电量、降噪 / 关闭与轻度 / 均衡两档降噪、状态回读、左右耳双击与按住、佩戴检测、轻滑音量说明、3 种官方音效和官方配色图片 |
| HUAWEI FreeBuds 5 | 扩展支持 | 电量、降噪 / 关闭与状态回读、智慧动态 / 轻度 / 均衡三档降噪、佩戴检测、4 种官方音效、高清音质与低时延自动保持；手势设置待补充 |
| HUAWEI FreeBuds 5i | 扩展支持 | 电量、通透 / 降噪 / 关闭与状态回读、智慧动态 / 轻度 / 均衡 / 深度四档降噪、左右耳双击、佩戴检测、4 种官方音效、高清音质、低时延自动保持与官方配色图片；长按和滑动设置待补充 |
| HUAWEI FreeBuds 6i | 扩展支持 | 电量、通透 / 降噪 / 关闭、4 档降噪、通透人声模式、双击 / 三击手势、4 种官方音效、10 段自定义均衡器、低时延自动保持与专属图片 |
| HUAWEI FreeBuds Pro 3 | 扩展支持 | 电量、三态控制与状态回读、4 档降噪、通透人声模式、长按 / 捏合 / 滑动手势与低时延自动保持 |
| HUAWEI FreeBuds Pro 4 | 基础支持 | 电量、降噪 / 关闭两态控制；暂不支持降噪状态回读与手势设置 |
| HUAWEI FreeBuds Pro 5 | 基础支持 | 电量、通透 / 降噪 / 关闭与状态回读、低时延自动保持；降噪等级和手势待补充 |
| HUAWEI FreeBuds 7i | 扩展支持 | 电量、通透 / 降噪 / 关闭与状态回读、4 档降噪、双击 / 三击 / 长按 / 滑动音量、佩戴检测、头动控制、空间音频、4 种官方音效、10 段自定义均衡器、高清音质、低时延自动保持、双设备列表管理与官方配色图片 |
| HUAWEI FreeClip | 基础支持 | 左右耳与充电盒电量；不提供传统主动降噪 |
| HUAWEI FreeClip 2 | 扩展支持 | 电量、双击 / 三击 / 滑动手势、空间音频、低时延自动保持及部分佩戴和音频设置；不支持传统主动降噪 |
| HUAWEI FreeArc | 扩展支持 | 左右耳与充电盒电量、双击 / 三击 / 按住 / 滑动手势、5 种官方音效、10 段自定义均衡器与官方配色图片；不支持传统主动降噪 |
| 华为智能眼镜（第一代） | 基础支持 | 左右镜腿电量与系统界面集成；不提供主动降噪 |
| HUAWEI Eyewear 2 | 基础支持 | 左右镜腿电量、双击 / 滑动手势与低时延自动保持；不提供主动降噪 |

“基础支持”和“扩展支持”机型仍建议继续进行真机回归；表中未列出的官方功能不代表已经支持。

## 主要功能

- 在系统蓝牙详情页显示电量及机型支持的控制项
- 接入 HyperOS 连接弹窗、超级岛和融合设备中心
- 按机型提供主动降噪、通透模式、降噪等级及手势设置
- 耳机被改名或无法自动识别时，可按蓝牙地址手动选择型号
- 支持应用内检查更新，并在覆盖安装后重启相关作用域

## 使用要求

- 小米或 Redmi 设备
- HyperOS，Android 15 及以上
- LSPosed API 101 及以上

## 快速开始

1. 安装 HuaweiPods，并在 LSPosed 中启用模块。
2. 勾选 `com.android.bluetooth`、`com.android.settings`、`com.milink.service` 和 `com.xiaomi.bluetooth`。
3. 在 HuaweiPods 内重启相关作用域，或重启手机。
4. 连接支持的设备后，即可在模块与系统界面中查看已接入能力。

需要适配其他华为耳机或参与真机复测，可加入 QQ 群 `1022359908`；可复现问题请提交至 [GitHub Issues](https://github.com/Nshpiter/HuaweiPods/issues)。

## 致谢

- [OppoPods](https://github.com/1812z/OppoPods) by 1812z（HuaweiPods 直接基于）
- [OppoPods](https://github.com/Leaf-lsgtky/OppoPods) by Leaf-lsgtky（上游原始项目）
- [HyperPods](https://github.com/Art-Chen/HyperPods) by Art_Chen
- [HyperIsland](https://github.com/1812z/HyperIsland) by 1812z（更新与首次引导交互参考）
- [Miuix](https://github.com/YuKongA/miuix)

## 许可证

[GPL-3.0](LICENSE)
