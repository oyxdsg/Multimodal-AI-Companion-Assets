# Multimodal-AI-Companion · 动画资源包

[DeskPet / Multimodal-AI-Companion](https://github.com/oyxdsg/Multimodal-AI-Companion) 的**动画资源**。

**为什么单独一个仓库**：素材有 248MB，放进源码仓库会让 `git clone` 从 3.7MB 涨到 250MB。
放这里，源码仓库保持轻量 —— **只克隆源码也能跑**（静态形象启动，功能完全一致，只是不动）。

## 里面有什么

- **17 个动作 / 1663 帧 PNG**（248MB）：侧面、哭泣、坐下、坐地上生气、害羞、开心、思考、惊讶、打滚、正面、站着睡着、背面、起身、跳舞、跳跃、转向
- 位移类动作额外带 `traj.json`（跳跃记 `dy`、打滚记 `dx+dy`，播放时施加回去以还原真实位移）
- `ACTIONS.md` / `actions.json`：动作清单（帧数、体积、是否有轨迹）

## 怎么用

1. 到 [Releases](../../releases) 下载 **`deskpet-animation-assets-v1.0.0.zip`**（约 247MB）
2. 解压到源码仓库的 **`desktop-pet/assets/`** 目录（zip 内就是 `<动作>/frame_0000.png` 这层结构，直接覆盖即可）
3. 重启桌宠 → 动作动画生效

解压后目录形如：

```
desktop-pet/assets/
├── README.md          （源码仓库自带，不要删）
├── _static/idle.png   （源码仓库自带：无动画时的静态形象）
├── 正面/frame_0000.png …
├── 思考/frame_0000.png …
├── 打滚/frame_0000.png … + traj.json
└── …
```

> 也可以只解压你需要的几个动作 —— 程序**按动作 key 缺失就回退静态图**，不会崩。

## 自己做素材

不想用这套？用 [`deskpet-tools/`](https://github.com/oyxdsg/Multimodal-AI-Companion/tree/main/deskpet-tools)
把自己的绿幕视频转成动作、打包成角色包，放进 `desktop-pet/skins/` 即可在设置 →「皮肤」切换。

## 许可

⚠️ **本仓库内容不适用 MIT。**

动画素材描绘的是**他人原创的角色形象** —— 原创 OC「溟月」@上善无形，
女仆版二次设计 @ZipZipPipe（B 站）。据两位作者公开声明，该形象以
**CC BY-NC-SA 4.0** 开放二次创作：

- 必须**署名**原作者；
- **禁止商业使用**；
- 衍生作品须**相同方式共享**。

完整条款与建议署名格式见 [`LICENSE`](LICENSE) 与 [`NOTICE.md`](NOTICE.md)。

想用不受该协议约束的素材：用
[`deskpet-tools/`](https://github.com/oyxdsg/Multimodal-AI-Companion/tree/main/deskpet-tools)
从自己的素材制作角色包。
