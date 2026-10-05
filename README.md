# 自制桌宠分享包

包含天爱星、七海千秋、蕾姆三只桌宠的完整动画资源，可按需安装或整包分享。

| 天爱星 | 七海千秋 | 蕾姆 | Monokuma | DeepSeek(大肥鱼) |
| :---: | :---: | :---: | :---: | :---: |
| ![天爱星静态预览](预览/天爱星.png) | ![七海千秋静态预览](预览/七海千秋.png) | ![蕾姆静态预览](预览/蕾姆.png) | ![蕾姆静态预览](预览/黑白熊.png) | ![蕾姆静态预览](预览/大肥鱼.png) |
| `pets/basori-tiara/` | `pets/hualing/` | `pets/rem/` | `pets/monokuma` | `pets/da_fei_yu` | 

## 适用范围

用于支持 **v2 自定义桌宠格式**的 Codex / ChatGPT 桌面客户端。每只桌宠均包含 `pet.json` 和透明背景动画精灵图；精灵图为 **1536 × 2288 像素、8 列 × 11 行**，配置中保留 `spriteVersionNumber: 2`。

天爱星、七海千秋使用 WebP，蕾姆使用 PNG，两种格式都是完整的动画资源。本包不能作为独立程序运行。

## 安装

如果下载的是 ZIP，请先完整解压。只需将 `pets` 内想要使用的桌宠文件夹复制到客户端的 `pets` 目录。

### Windows

1. 按 **Win + R**，输入 `%USERPROFILE%\.codex` 并回车。在其中找到或新建 `pets` 文件夹。若 `.codex` 不存在，先打开 `%USERPROFILE%`，新建 `.codex`，再在里面新建 `pets`。
2. 将本包 `pets` 内的 `basori-tiara`、`hualing`、`rem` 文件夹复制进去，可以只选一只。
3. 检查层级，例如蕾姆应为：

   ```text
   C:\Users\你的用户名\.codex\pets\rem\pet.json
   C:\Users\你的用户名\.codex\pets\rem\spritesheet.png
   ```

### macOS

在访达中按 **Command + Shift + G**，打开 `~/.codex/pets/`，再将需要的桌宠文件夹复制进去。目录不存在时，可先在终端执行：

```sh
mkdir -p ~/.codex/pets
```

### 自定义位置与启用

如果设置了 `CODEX_HOME` 环境变量，请安装到 **该目录下的 `pets`**。Windows PowerShell 可用 `$env:CODEX_HOME` 查看；无输出时通常使用上述默认位置。

复制后，打开客户端的 **设置 → Pets / 桌宠**，或个人菜单中的 **Pets**，选择“天爱星”“七海千秋”或“蕾姆”。如果界面有 **Refresh / 刷新**，可先点击刷新；未出现时重新打开选择界面，或完全退出客户端再启动。在支持的版本中，可用 `/pet` 或 **Show pet / 显示桌宠**打开桌宠。界面名称可能随版本变化。

**请复制桌宠文件夹本身**，避免出现 `.codex/pets/pets/rem` 这样的多余层级。目标位置已有同名文件夹时，请先备份，再决定是否替换。

## 文件结构

```text
（今天忙完就更新）
自制桌宠分享包/
├── README.md
├── pets/
│   ├── basori-tiara/         # 天爱星
│   │   ├── pet.json
│   │   └── spritesheet.webp
│   ├── hualing/              # 七海千秋
│   │   ├── pet.json
│   │   └── spritesheet.webp
│   └── rem/                  # 蕾姆
│       ├── pet.json
│       └── spritesheet.png
└── 预览/
    ├── 天爱星.png
    ├── 七海千秋.png
    └── 蕾姆-动作预览.png
```

文件夹名对应桌宠的内部 ID，请保留现有名称；`hualing` 在客户端显示为“七海千秋”。

## 常见问题

- **桌宠没有出现：** 检查目录是否多嵌套一层、`pet.json` 和对应精灵图是否齐全、是否设置了 `CODEX_HOME`，并确认客户端支持 v2 桌宠。必要时更新客户端后重新打开桌宠设置。
- **图片无法识别或动画错位：** 保留 `spriteVersionNumber: 2` 和 `spritesheetPath`，不要缩放、裁切或重排精灵图，也不要只改扩展名或用预览图替换精灵图。
- **能否直接上传到网页版：** 本包按桌面版 v2 格式整理。官方网页版说明列出的上传规格为 1536 × 1872，与本包不同，因此本包不作为网页版直接上传包使用。桌面版自定义桌宠也不会自动同步到网页版。
- **如何移除：** 先切换到其他桌宠，再将对应桌宠文件夹移出客户端的 `pets` 目录，重新打开桌宠设置或重启客户端。

## 分享

可将本文件夹完整压缩为 ZIP，或把其中的内容上传到 GitHub 仓库。保留 `pets`、`预览` 与本 README 的相对位置，朋友下载并解压后即可按上述步骤安装，无需提供个人客户端的其他配置文件。

参考：[OpenAI 官方 Pets 文档](https://learn.chatgpt.com/docs/pets)。本包的安装结构与现有资源按本地 v2 格式契约核对。
