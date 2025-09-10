# BongoCat i18n

> Trong lúc tìm hiểu và cài thử [ayangweb/BongoCat](https://github.com/ayangweb/BongoCat), mình nhận thấy **UI và bộ cài đặt chủ yếu là tiếng Trung**.
> Mình thì lại khó hiểu tiếng Trung (hơi bực 😅) nên quyết định **fork về, dịch ra và i18n hóa (đa ngôn ngữ)**.
> Giữ nguyên toàn bộ tính năng gốc, tập trung thêm i18n và bộ cài đặt có chọn ngôn ngữ.

---

## 🌏 English Summary

> While exploring and installing [ayangweb/BongoCat](https://github.com/ayangweb/BongoCat), I found that **most of the UI and installer were in Chinese**.
> I don’t understand Chinese well (a bit frustrated 😅), so I decided to **fork it, translate, and add i18n (multi-language support)**.
> All original features remain intact, focusing on i18n and language selection during installation.

---

## ⬇️ Tải về (chỉ bản Windows) / Download (Windows build only)

- [GitHub Releases](https://github.com/cuonglmptit/bongocat-i18n/releases)

---

## 🎨 Model khác / Other models

> 🇻🇳 Ngoài model mặc định, bạn có thể tải thêm nhiều model khác từ  
> 🇬🇧 Besides the default model, you can download more models from  
> [ayangweb/Awesome-BongoCat](https://github.com/ayangweb/Awesome-BongoCat).

---
## 🏗 Nguồn gốc dự án / Project origins

Khi tìm hiểu về **BongoCat**, mình phát hiện dự án có một lịch sử khá thú vị.
(While researching **BongoCat**, I found that the project has a rather interesting history:)

1. **[HamishDuncanson](https://github.com/HamishDuncanson)**

   - 🇻🇳 Theo chia sẻ của [kuroni](https://github.com/kuroni), Hamish là người đã **tạo ra ý tưởng gốc**:
     🇬🇧 According to [kuroni](https://github.com/kuroni), Hamish was the one who **created the original idea**:
     _"An osu! Bongo Cat overlay with smooth paw movement and simple skinning ability, written in C++."_

2. **[kuroni/bongocat-osu](https://github.com/kuroni/bongocat-osu)**

   - 🇻🇳 Là người Việt, tiếp tục phát triển dự án dựa trên ý tưởng của Hamish.
     🇬🇧 A Vietnamese developer, continued to develop the project based on Hamish’s idea.

3. **[MMmmmoko/Bongo-Cat-Mver](https://github.com/MMmmmoko/Bongo-Cat-Mver)** _(fork từ kuroni)_

   - 🇻🇳 Viết lại nhiều logic, hoạt động như một "decorative operation demo".
     🇬🇧 Rewrote much of the logic, functioning as a "decorative operation demo".
   - 🇻🇳 Chỉ hỗ trợ Windows và hiện đã archive.
     🇬🇧 Only supported Windows and is now archived.

4. **[ayangweb/BongoCat](https://github.com/ayangweb/BongoCat)** _(không phải fork, viết lại từ đầu)_

   - 🇻🇳 Lấy cảm hứng từ MMmmmoko.
     🇬🇧 Inspired by MMmmmoko.
   - 🇻🇳 Viết lại bằng **Tauri**, hỗ trợ đa nền tảng (macOS, Windows, Linux x11).
     🇬🇧 Rewritten with **Tauri**, supporting multiple platforms (macOS, Windows, Linux x11).

5. **[cuonglmptit/bongocat-i18n](https://github.com/cuonglmptit/bongocat-i18n)** _(repo này)_
   - 🇻🇳 Fork từ **ayangweb/BongoCat** để **dịch, i18n hóa UI và installer**, giúp nhiều người dùng hơn có thể tiếp cận.
     🇬🇧 Forked from **ayangweb/BongoCat** to **translate, add i18n for the UI and installer**, making it more accessible to more users.

---

# Instructions

### 🌐 🇻🇳 Thêm ngôn ngữ mới / 🇬🇧 Add a new language

> **🇻🇳** Vì mình không thể dịch hết sang tất cả các ngôn ngữ, bạn có thể dựa vào file tiếng Anh (`en.json`) để dịch sang ngôn ngữ của bạn.  
> **🇬🇧** Since I can't translate into all languages, you can use the English file (`en.json`) as a base and translate it into your language.

1. **🇻🇳** Mở thư mục `assets/locales`.
   **🇬🇧** Open the `assets/locales` folder.

2. **🇻🇳** Copy một file có sẵn (ví dụ: `en.json`) và đổi tên thành mã ngôn ngữ bạn muốn (ví dụ: `fr.json`).
   **🇬🇧** Copy an existing file (e.g., `en.json`) and rename it to the language code you want (e.g., `fr.json`).

3. **🇻🇳** Dịch lại nội dung trong file, ví dụ:
   **🇬🇧** Translate the contents of the file, for example:

   ```json
   {
     "meta": { "name": "English" },
     "menu": {
       "cat": "Cat Settings",
       "general": "General"
     }
   }
   ```

4. **🇻🇳** Lưu file và **khởi động lại ứng dụng** để áp dụng.  
   **🇬🇧** Save the file and **restart the app** to apply.

---

> **🇻🇳** Bạn cũng có thể **tự tải source về**, thêm file JSON ngôn ngữ mới vào `assets/locales` và **build lại** để tạo bộ cài sẵn ngôn ngữ này.
> **🇬🇧** You can also **download the source**, add your new language JSON file into `assets/locales`, and **build again** to create an installer with this language included.

## Ví dụ build lại / Build example:

>### Test:
pnpm install  
pnpm tauri dev  

>### Build:
pnpm install  
pnpm tauri build  

---

## Tính năng chính / Features

- Giữ nguyên các tính năng của **ayangweb/BongoCat** (Keep all original features from **ayangweb/BongoCat**):
  - Đa nền tảng: macOS, Windows, Linux (x11) (Cross-platform: macOS, Windows, Linux (x11))
  - Hỗ trợ model tùy chỉnh (Support for custom models)
  - Chạy offline, không thu thập dữ liệu người dùng (Works offline, no user data collection)
- **Mới:** UI hỗ trợ **đa ngôn ngữ (i18n)** (**New:** UI supports **multi-language (i18n)**)
- **Mới:** Installer (NSIS) có thể chọn ngôn ngữ khi cài đặt (**New:** Installer (NSIS) supports language selection during setup)

> ⚠️ **🇻🇳 Lưu ý:** Bản phát hành chính thức hiện tại chỉ build sẵn cho Windows. Các hệ điều hành khác (macOS, Linux) có thể **tự tải source về, build và test**. Mình không chịu trách nhiệm cho các bản build tự thực hiện.
> 
> ⚠️ **🇬🇧 Note:** Official release currently only builds for Windows. Other operating systems (macOS, Linux) can **download the source, build and test**. I’m not responsible for self-built versions.

---

## License

>### [MIT](./LICENSE)

---

## Credits

- [HamishDuncanson](https://github.com/HamishDuncanson)  
  🇻🇳 Ý tưởng gốc (theo chia sẻ của kuroni)  
  🇬🇧 Original idea (according to kuroni)

- [kuroni](https://github.com/kuroni)  
  🇻🇳 Phát triển bongocat-osu (người Việt 🇻🇳)  
  🇬🇧 Developed bongocat-osu (Vietnamese developer 🇻🇳)

- [MMmmmoko](https://github.com/MMmmmoko)  
  🇻🇳 Tạo Bongo-Cat-Mver (fork từ kuroni)  
  🇬🇧 Created Bongo-Cat-Mver (forked from kuroni)

- [ayangweb](https://github.com/ayangweb)  
  🇻🇳 Viết lại đa nền tảng bằng Tauri  
  🇬🇧 Rewrote as a cross-platform version using Tauri
=======
简体中文| [English](./README.en.md)

![BongoCat](https://socialify.git.ci/ayangweb/BongoCat/image?custom_description=&description=1&font=Source+Code+Pro&forks=1&issues=1&logo=https%3A%2F%2Fgithub.com%2Fayangweb%2FBongoCat%2Fblob%2Fmaster%2Fsrc-tauri%2Fassets%2Flogo-mac.png%3Fraw%3Dtrue&name=1&owner=1&pattern=Floating+Cogs&pulls=1&stargazers=1&theme=Auto)

<div align="center">
  <div>
    <a href="https://github.com/ayangweb/BongoCat/releases">
      <img
        alt="Windows"
        src="https://img.shields.io/badge/-Windows-blue?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB0PSIxNzI2MzA1OTcxMDA2IiBjbGFzcz0iaWNvbiIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHAtaWQ9IjE1NDgiIHdpZHRoPSIxMjgiIGhlaWdodD0iMTI4Ij48cGF0aCBkPSJNNTI3LjI3NTU1MTYxIDk2Ljk3MTAzMDEzdjM3My45OTIxMDY2N2g0OTQuNTEzNjE5NzVWMTUuMDI2NzU3NTN6TTUyNy4yNzU1NTE2MSA5MjguMzIzNTA4MTVsNDk0LjUxMzYxOTc1IDgwLjUyMDI4MDQ5di00NTUuNjc3NDcxNjFoLTQ5NC41MTM2MTk3NXpNNC42NzA0NTEzNiA0NzAuODMzNjgyOTdINDIyLjY3Njg1OTI1VjExMC41NjM2ODE5N2wtNDE4LjAwNjQwNzg5IDY5LjI1Nzc5NzUzek00LjY3MDQ1MTM2IDg0Ni43Njc1OTcwM0w0MjIuNjc2ODU5MjUgOTE0Ljg2MDMxMDEzVjU1My4xNjYzMTcwM0g0LjY3MDQ1MTM2eiIgcC1pZD0iMTU0OSIgZmlsbD0iI2ZmZmZmZiI+PC9wYXRoPjwvc3ZnPg=="
      />
    </a>
    <a href="https://github.com/ayangweb/BongoCat/releases">
      <img
        alt="MacOS"
        src="https://img.shields.io/badge/-MacOS-black?style=flat-square&logo=apple&logoColor=white"
      />
    </a>
    <a href="https://github.com/ayangweb/BongoCat/releases">
      <img
        alt="Linux"
        src="https://img.shields.io/badge/-Linux-yellow?style=flat-square&logo=linux&logoColor=white"
      />
    </a>
  </div>

  <p>
    <a href="./LICENSE">
      <img
        src="https://img.shields.io/github/license/ayangweb/BongoCat?style=flat-square"
      />
    </a>
    <a href="https://github.com/ayangweb/BongoCat/releases/latest">
      <img
        src="https://img.shields.io/github/package-json/v/ayangweb/BongoCat?style=flat-square"
      />
    </a>
    <a href="https://github.com/ayangweb/BongoCat/releases">
      <img
        src="https://img.shields.io/github/downloads/ayangweb/BongoCat/total?style=flat-square"
      />
    </a>
  </p>

  <p>
    <a href="https://hellogithub.com/repository/7d23863fd4be47b39e816193ded385c9" target="_blank">
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://abroad.hellogithub.com/v1/widgets/recommend.svg?rid=7d23863fd4be47b39e816193ded385c9&claim_uid=5ihRVIuTYBmSGtQ&theme=dark" />
        <source media="(prefers-color-scheme: light)" srcset="https://abroad.hellogithub.com/v1/widgets/recommend.svg?rid=7d23863fd4be47b39e816193ded385c9&claim_uid=5ihRVIuTYBmSGtQ&theme=neutral" />
        <img alt="Star History Chart" src="https://abroad.hellogithub.com/v1/widgets/recommend.svg?rid=7d23863fd4be47b39e816193ded385c9&claim_uid=5ihRVIuTYBmSGtQ&theme=neutral" />
      </picture>
    </a>
  </p>
</div>

| macOS                                                                                        | Windows                                                                                        | Linux(x11)                                                                                   |
| -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| ![macOS](https://i0.hdslb.com/bfs/openplatform/dff276b96d49c5d6c431b74b531aab72191b3d87.png) | ![Windows](https://i0.hdslb.com/bfs/openplatform/a4149b753856ee7f401989da902cf3b5ad35b39e.png) | ![Linux](https://i0.hdslb.com/bfs/openplatform/3b49f961819d3ff63b2b80251c1cc13c27e986b0.png) |

## 赞助商

<a href="https://www.toolsetlink.com">
  <img height="54" alt="UpgradeLink" src="https://github.com/user-attachments/assets/6b84fb0f-3f1d-44b5-9932-2298bc999d8d" />
</a>

## 开发背景

本项目的灵感来源于 [MMmmmoko](https://github.com/MMmmmoko) 大佬开发的 [Bongo-Cat-Mver](https://github.com/MMmmmoko/Bongo-Cat-Mver)。它以独特的猫咪互动功能深受用户喜爱，但仅支持 Windows 平台。作为一名深度 macOS 用户，我特别希望在自己的设备上也能使用这款可爱的猫咪，于是我决定开发一个适配 macOS 的版本。

同时，得益于 [Tauri](https://github.com/tauri-apps/tauri) 强大的跨平台能力，本项目不仅支持 macOS，还兼容 Windows 和 Linux(x11)，让更多的用户都能与这只可爱的猫咪互动！

## 下载

- [夸克网盘](https://pan.quark.cn/s/70f2f2663ce1)
- [GitHub Releases](https://github.com/ayangweb/BongoCat/releases)

不确定下载哪一个？请查阅[下载指南](.github/DOWNLOAD_GUIDE.md)。

## 功能介绍

- 适配 macOS、Windows 和 Linux(x11)。
- 根据键盘、鼠标或手柄的操作，同步对应的动作。
- 支持导入自定义模型，自由打造专属猫咪形象。
- 完全开源，代码公开透明，绝不收集任何用户数据。
- 支持离线运行，无需联网，保护用户隐私。

## 模型转换

如果你想将 Bongo-Cat-Mver 应用中的模型转换为兼容 BongoCat 的格式，可以使用以下工具：

🔗 [在线转换](https://bongocat.vteamer.cc)

## 更多模型

你可以在这个仓库中探索、下载更多猫咪模型，或提交你的创作，与大家一起分享：

📦 [Awesome-BongoCat](https://github.com/ayangweb/Awesome-BongoCat)

## 社区交流

<a href="https://qm.qq.com/q/AS3gNv2Vzy">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://i0.hdslb.com/bfs/openplatform/5ad8e4278c525cca6d3b4426c30b6d299d8a9654.png" />
   <source media="(prefers-color-scheme: light)" srcset="https://i0.hdslb.com/bfs/openplatform/599680ad67bc9f9f876f76069c2239e9a85bb54d.png" />
   <img alt="QQ Group" src="https://i0.hdslb.com/bfs/openplatform/599680ad67bc9f9f876f76069c2239e9a85bb54d.png" height="250" />
 </picture>
</a>

## 贡献指南

感谢大家为 BongoCat 做出的宝贵贡献！如果你也希望为 BongoCat 做出贡献，请查阅[贡献指南](.github/CONTRIBUTING.md)。

<a href="https://github.com/ayangweb/BongoCat/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ayangweb/BongoCat" />
</a>

## 历史星标

<a href="https://www.star-history.com/#ayangweb/BongoCat&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=ayangweb/BongoCat&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=ayangweb/BongoCat&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=ayangweb/BongoCat&type=Date" />
 </picture>
</a>
