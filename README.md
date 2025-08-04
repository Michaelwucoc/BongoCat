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
> **🇬🇧 Note:** Official release currently only builds for Windows. Other operating systems (macOS, Linux) can **download the source, build and test**. I’m not responsible for self-built versions.

---

## License

>### [MIT](./LICENSE).

---

## Credits

- [HamishDuncanson](https://github.com/HamishDuncanson) – 🇻🇳 ý tưởng gốc (theo chia sẻ của kuroni)
  🇬🇧 original idea (according to kuroni)
- [kuroni](https://github.com/kuroni) – 🇻🇳 phát triển bongocat-osu (người Việt 🇻🇳)
  🇬🇧 developed bongocat-osu (Vietnamese developer 🇻🇳)
- [MMmmmoko](https://github.com/MMmmmoko) – 🇻🇳 tạo Bongo-Cat-Mver (fork từ kuroni)
  🇬🇧 created Bongo-Cat-Mver (forked from kuroni)
- [ayangweb](https://github.com/ayangweb) – 🇻🇳 viết lại đa nền tảng bằng Tauri
  🇬🇧 rewrote as a cross-platform version using Tauri
