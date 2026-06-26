# Asterion — Professional Astrology Academy

App học bài tương tác (lesson navigator), single-page HTML, không cần backend — chỉ cần host tĩnh (static hosting). Cho phép thêm "Custom Lesson / Notes" cá nhân, lưu trực tiếp trong trình duyệt.

**Live demo sau khi deploy:** `https://<username>.github.io/<repo-name>/`

---

## 📁 Cấu trúc file

```
.
├── index.html      ← Toàn bộ app (HTML/CSS/JS gộp 1 file, dùng CDN cho Tailwind + Font Awesome + Google Fonts)
└── README.md        ← File này
```

> File gốc của bạn đã được đổi tên thành `index.html` — bắt buộc để GitHub Pages tự nhận làm trang chủ.

---

## 🚀 Hướng dẫn Deploy — Repo mới, Pages từ root (/)

### Cách A — Qua Git CLI

```bash
# 1. Tạo repo mới trên GitHub.com (nút "New repository"), KHÔNG tick "Add README"
#    → ví dụ đặt tên: asterion-astrology-academy

# 2. Trong thư mục chứa 2 file index.html + README.md:
git init
git add .
git commit -m "Initial commit: Asterion Astrology Academy"
git branch -M main
git remote add origin https://github.com/<username>/asterion-astrology-academy.git
git push -u origin main
```

### Cách B — Qua giao diện web (không cần terminal)

1. **github.com → New repository** → đặt tên → **Create repository** (để trống, không tick README).
2. Trong repo vừa tạo, chọn **"uploading an existing file"**.
3. Kéo-thả `index.html` và `README.md` vào → **Commit changes**.

### Bật GitHub Pages

1. Repo → **Settings → Pages**.
2. **Build and deployment → Source**: chọn **Deploy from a branch**.
3. **Branch**: `main` — **Folder**: **`/ (root)`** → **Save**.
4. Đợi 1–2 phút → link xuất hiện dạng `https://<username>.github.io/asterion-astrology-academy/`.

---

## ⚠️ Lưu ý kỹ thuật quan trọng — về localStorage

App này dùng `localStorage` (bộ nhớ lưu trong trình duyệt) để lưu các "Custom Lesson" bạn tự thêm. Điều này có nghĩa là:

- Ghi chú chỉ lưu **trên một trình duyệt, một thiết bị cụ thể** — không tự đồng bộ giữa điện thoại và laptop, không lưu trên "cloud" của GitHub.
- Nếu bạn xóa cache/cookies của trình duyệt, hoặc dùng **Incognito/Private mode**, ghi chú đã thêm sẽ **mất hoàn toàn**.
- Đây là hành vi đúng của `localStorage` — không phải lỗi của trang web.

> 💡 Nếu sau này bạn muốn ghi chú đồng bộ được giữa nhiều thiết bị, sẽ cần nâng cấp sang lưu trữ phía server (database) — đây là một bước nâng cấp riêng, không tự động có với GitHub Pages (vì Pages chỉ host file tĩnh, không chạy backend).

---

## 📘 Từ vựng kỹ thuật / Technical Vocabulary

| English | Phát âm (Oxford US) | Nghĩa tiếng Việt |
|---|---|---|
| Repository (repo) | /rɪˈpɑːzɪˌtɔːri/ | Kho lưu trữ mã nguồn |
| Deploy | /dɪˈplɔɪ/ | Triển khai |
| localStorage | /ˈloʊkəl ˈstɔːrɪdʒ/ | Bộ nhớ lưu trữ cục bộ trong trình duyệt |
| Static hosting | /ˈstætɪk ˈhoʊstɪŋ/ | Dịch vụ lưu trữ trang web tĩnh |
| Branch | /bræntʃ/ | Nhánh trong Git |
| Root (folder) | /ruːt/ | Thư mục gốc |

---

*Tạo cho mục đích học tập cá nhân — Asterion Professional Astrology Academy.*
