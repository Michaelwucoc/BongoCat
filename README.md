# 🐾 BongoCat i18n

> Trong lúc tìm hiểu và cài thử [ayangweb/BongoCat](https://github.com/ayangweb/BongoCat), mình nhận thấy **UI và bộ cài đặt chủ yếu là tiếng Trung**.
> Mình thì lại khó hiểu tiếng Trung (hơi bực 😅) nên quyết định **fork về, dịch ra và i18n hóa (đa ngôn ngữ)**.
> Giữ nguyên toàn bộ tính năng gốc, tập trung thêm i18n và bộ cài đặt có chọn ngôn ngữ.

👉 [Tải bản release tại đây](https://github.com/cuonglmptit/bongocat-i18n/releases)

---

## 🌏 English Summary

> While exploring and installing [ayangweb/BongoCat](https://github.com/ayangweb/BongoCat), I found that **most of the UI and installer were in Chinese**.
> I don’t understand Chinese well (a bit frustrated 😅), so I decided to **fork it, translate, and add i18n (multi-language support)**.
> All original features remain intact, focusing on i18n and language selection during installation.

👉 [Download release here](https://github.com/cuonglmptit/bongocat-i18n/releases)

---

## 🏗 Nguồn gốc dự án / Project origins

Khi tìm hiểu về **BongoCat**, mình phát hiện dự án có một lịch sử khá thú vị:

1. **[HamishDuncanson](https://github.com/HamishDuncanson)**

   - Theo chia sẻ của [kuroni](https://github.com/kuroni), Hamish là người đã **tạo ra ý tưởng gốc**:
     _"An osu! Bongo Cat overlay with smooth paw movement and simple skinning ability, written in C++."_

2. **[kuroni/bongocat-osu](https://github.com/kuroni/bongocat-osu)**

   - Là người Việt, tiếp tục phát triển dự án dựa trên ý tưởng của Hamish.

3. **[MMmmmoko/Bongo-Cat-Mver](https://github.com/MMmmmoko/Bongo-Cat-Mver)** _(fork từ kuroni)_

   - Viết lại nhiều logic, hoạt động như một "decorative operation demo".
   - Chỉ hỗ trợ Windows và hiện đã archive.

4. **[ayangweb/BongoCat](https://github.com/ayangweb/BongoCat)** _(không phải fork, viết lại từ đầu)_

   - Lấy cảm hứng từ MMmmmoko.
   - Viết lại bằng **Tauri**, hỗ trợ đa nền tảng (macOS, Windows, Linux x11).

5. **[cuonglmptit/bongocat-i18n](https://github.com/cuonglmptit/bongocat-i18n)** _(repo này)_
   - Fork từ **ayangweb/BongoCat** để **dịch, i18n hóa UI và installer**, giúp nhiều người dùng hơn có thể tiếp cận.

---

## ✨ Tính năng chính / Features

- Giữ nguyên các tính năng của **ayangweb/BongoCat**:
  - Đa nền tảng: macOS, Windows, Linux (x11)
  - Hỗ trợ model tùy chỉnh
  - Chạy offline, không thu thập dữ liệu người dùng
- **Mới:** UI hỗ trợ **đa ngôn ngữ (i18n)**
- **Mới:** Installer (NSIS) có thể chọn ngôn ngữ khi cài đặt

---

## ⬇️ Tải về / Download

- [GitHub Releases](https://github.com/cuonglmptit/bongocat-i18n/releases)

---

## 📜 License

Dự án phát hành dưới giấy phép [MIT](./LICENSE).

---

## 🙏 Credits

- [HamishDuncanson](https://github.com/HamishDuncanson) – ý tưởng gốc (theo chia sẻ của kuroni)
- [kuroni](https://github.com/kuroni) – phát triển bongocat-osu (người Việt 🇻🇳)
- [MMmmmoko](https://github.com/MMmmmoko) – tạo Bongo-Cat-Mver (fork từ kuroni)
- [ayangweb](https://github.com/ayangweb) – viết lại đa nền tảng bằng Tauri
