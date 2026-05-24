# Bộ Prompt cho Giáo viên — Innedu

> Công cụ tương tác giúp giáo viên Việt Nam viết prompt AI tốt hơn cho công việc giảng dạy, thuộc khóa học **"Dạy học Tích cực & AI trong Giáo dục"** do Innedu phát triển.

**Demo trực tuyến:** _[sẽ có sau khi enable GitHub Pages — xem hướng dẫn bên dưới]_

---

## Đây là gì?

Một ứng dụng web một-trang (single-page app) giúp giáo viên học cách viết prompt AI cho công việc giảng dạy. Mỗi prompt được trình bày như một **bài học tương tác** gồm 4 giai đoạn:

1. **Lý thuyết** — Hiểu mục đích sư phạm và cấu trúc 6 thành phần của prompt
2. **Áp dụng** — Điền form các biến số cụ thể của bài học
3. **Kết quả** — Nhận prompt hoàn chỉnh sẵn sàng gửi sang Claude/ChatGPT
4. **Phản hồi** — Đọc đánh giá tự động theo khung **FEED** (Focus–Evidence–Effect–Direction)

Phiên bản hiện tại (v0.2) là bản demo trình bày **8 prompt mẫu trên 6 module** của khóa học. Phiên bản đầy đủ sẽ có khoảng 120 prompt khi hoàn thiện.

## 8 Prompt mẫu trên 6 Module

### Module 1 — Nền tảng Dạy học Tích cực
| Mã | Tên prompt | Độ khó | Thời gian |
|---|---|---|---|
| M1-P01 | Phân tầng câu hỏi theo Thang Bloom | ★☆☆ | 10 phút |
| M1-P02 | Phân biệt mục đích dùng AI: GV hay HS? | ★★☆ | 8 phút |
| M1-P03 | Thiết kế bài học theo quy trình DESIGN-AI | ★★★ | 15 phút |

### Module 2 — AI Literacy & Đạo đức
| Mã | Tên prompt | Độ khó | Thời gian |
|---|---|---|---|
| M2-P01 | Soạn bài giảng AI Literacy cho học sinh | ★★☆ | 12 phút |

### Module 3 — PBL · PrBL · Hợp tác
| Mã | Tên prompt | Độ khó | Thời gian |
|---|---|---|---|
| M3-P01 | Viết Driving Question đạt chuẩn Gold Standard PBL | ★★☆ | 10 phút |

### Module 4 — Flipped · Gamification · IBL
| Mã | Tên prompt | Độ khó | Thời gian |
|---|---|---|---|
| M4-P01 | Thiết kế tiết Lớp đảo ngược (Flipped Classroom) | ★★☆ | 12 phút |

### Module 5 — Design Thinking
| Mã | Tên prompt | Độ khó | Thời gian |
|---|---|---|---|
| M5-P01 | Thiết kế bài học Design Thinking 5 bước | ★★★ | 15 phút |

### Module 6 — Đánh giá FEED
| Mã | Tên prompt | Độ khó | Thời gian |
|---|---|---|---|
| M6-P01 | Viết phản hồi cho bài làm HS theo khung FEED | ★★☆ | 10 phút |

## Đặc điểm kỹ thuật

- **Một file HTML duy nhất** (~110 KB) — toàn bộ HTML, CSS, JavaScript, font, logo SVG đều nhúng vào trong file
- **Không cần backend** — chạy hoàn toàn trên trình duyệt
- **Hoạt động offline** sau lần tải đầu tiên (font Google được cache)
- **Lưu trữ cục bộ** — form data lưu vào `localStorage` của trình duyệt, không gửi đi đâu
- **Mobile-responsive** — hoạt động tốt trên điện thoại với menu hamburger
- **Mọi trình duyệt hiện đại** — Chrome, Edge, Firefox, Safari, kể cả Cốc Cốc

## Cấu trúc file

```
/
├── index.html          ← File chính (GitHub Pages sẽ serve mặc định)
└── README.md           ← File này
```

Không có dependency, không có build step. Có thể tải về và mở trực tiếp bằng trình duyệt (file://...) để dùng offline.

---

## Hướng dẫn deploy lên GitHub Pages

### Yêu cầu chuẩn bị

- Một tài khoản GitHub (miễn phí — đăng ký tại [github.com](https://github.com))
- File `index.html` và `README.md` (file này)

### Bước 1 — Tạo repository

1. Đăng nhập GitHub → bấm dấu **+** góc phải trên → **New repository**
2. Đặt tên repo, ví dụ: `prompt-toolkit` hoặc `bo-prompt-giao-vien`
3. Mô tả ngắn: `Bộ Prompt Tương tác cho Giáo viên - Innedu`
4. Chọn **Public**
5. **KHÔNG** tick "Add a README file" (vì sẽ upload README riêng)
6. Bấm **Create repository**

### Bước 2 — Upload các file

**Cách A — Qua giao diện web (dễ nhất)**:
1. Vào repo vừa tạo
2. Bấm link **"uploading an existing file"** (giữa trang) hoặc **Add file → Upload files**
3. Kéo thả `index.html` và `README.md` vào ô upload
4. Cuộn xuống, gõ commit message: `Khởi tạo bộ prompt v0.2 — 8 prompt trên 6 module`
5. Bấm **Commit changes**

**Cách B — Qua Git command line**:
```bash
git clone https://github.com/USERNAME/prompt-toolkit.git
cd prompt-toolkit
# Copy index.html và README.md vào folder này
git add .
git commit -m "Khởi tạo bộ prompt v0.2"
git push origin main
```

### Bước 3 — Bật GitHub Pages

1. Trong repo, vào tab **Settings** (góc phải trên)
2. Menu trái → cuộn xuống chọn **Pages**
3. Phần **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: chọn `main`, folder `/ (root)`
   - Bấm **Save**
4. Chờ 1–2 phút để GitHub build

### Bước 4 — Lấy URL công khai

Sau khi build xong, quay lại **Settings → Pages**, sẽ thấy dòng:

> **Your site is live at** `https://USERNAME.github.io/REPO-NAME/`

Đây là đường link công khai. Có thể chia sẻ cho đồng nghiệp, Sở GD, các trường khác, hoặc nhúng vào website Innedu.

### Bước 5 (tùy chọn) — Đặt subdomain Innedu

Nếu muốn dùng `prompt.innedu.com.vn`:
1. Vào **Settings → Pages → Custom domain**
2. Nhập domain, bấm **Save**
3. Tại nhà cung cấp tên miền của Innedu, thêm bản ghi DNS `CNAME`:
   - Tên: `prompt`
   - Giá trị: `USERNAME.github.io`
4. Quay lại GitHub, đợi DNS propagate (5–60 phút) và tick **Enforce HTTPS**

---

## Cập nhật nội dung

Khi cần thêm prompt mới hoặc sửa template:

1. Mở `index.html` bằng VSCode/Notepad++/editor bất kỳ
2. Tìm phần `const PROMPTS = { ... }` (gần đầu thẻ `<script>`)
3. Thêm prompt mới theo template hiện có (sao chép cấu trúc của một prompt cũ)
4. Save file
5. Upload lại lên GitHub (cách A hoặc B ở trên)
6. GitHub Pages tự động cập nhật trong 1–2 phút

## Cấu trúc một prompt

Mỗi prompt là một object JavaScript có dạng:

```javascript
'M1-P01': {
  id: 'M1-P01',
  title: 'Tên prompt',
  deck: 'Mô tả ngắn 1-2 câu',
  module: 'Module 1',
  code: 'M1-P01',
  difficulty: 1,           // 1, 2, hoặc 3 (★, ★★, ★★★)
  duration: '10 phút',
  purpose: '...',          // Mục đích sư phạm
  when: '...',             // Khi nào dùng
  foundation: '...',       // Lý thuyết nền
  tags: [...],             // Tag phân loại
  structure: [...],        // 5-6 thành phần cấu trúc prompt
  inputs: [...],           // Các trường form GV điền
  template: ({...}) => `...` // Template prompt sinh ra
}
```

Chi tiết hơn xem các prompt mẫu trong file.

## Câu hỏi thường gặp

**Bộ prompt này có thu thập dữ liệu của giáo viên không?**
Không. Mọi dữ liệu form được lưu trong trình duyệt cục bộ (`localStorage`), không có server nào nhận. Web không có analytics, tracker, hay cookie ngoài chuẩn trình duyệt.

**Có thể chạy offline không?**
Sau lần tải đầu (khi font Google đã cache), về cơ bản có thể chạy offline. Để chắc chắn 100%, tải file về máy và mở trực tiếp.

**Tôi có thể fork và chỉnh sửa cho trường của tôi không?**
Có. Repo public, mọi người được fork. Vui lòng giữ ghi nhận "phát triển bởi Innedu" trong footer.

**Báo lỗi / góp ý ở đâu?**
Mở Issue trong tab **Issues** của repository.

---

## Bản quyền

© 2025 Innedu — Khóa học Dạy học Tích cực & AI trong Giáo dục.

Phần code (HTML/CSS/JS) phát hành dưới giấy phép MIT.
Phần nội dung sư phạm (template prompt, khung FEED, lý thuyết) thuộc bản quyền Innedu, cấp phép sử dụng miễn phí cho mục đích giáo dục phi lợi nhuận.
