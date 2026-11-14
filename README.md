# Claude Certification Quiz

Ứng dụng luyện thi **Claude Developer & Architect** chạy hoàn toàn trên trình duyệt — một file HTML duy nhất, không cần backend, không cần build.

## Tính năng

- **98 câu hỏi** trắc nghiệm 4 đáp án, ngưỡng đậu 70%
- 2 chế độ: **Practice mode** (xem giải thích ngay) và **Exam mode** (thi thử)
- Tùy chọn xáo trộn câu hỏi và đáp án
- Giới hạn thời gian: 30 / 45 / 60 / 90 phút, có đồng hồ đếm ngược
- Bảng điều hướng câu hỏi (question palette) hiển thị trạng thái đã trả lời / đúng / sai
- Màn hình kết quả chi tiết kèm phần ôn tập từng câu
- Lưu cài đặt và số lần hoàn thành bằng `localStorage`

## Chạy local

Mở trực tiếp `index.html` bằng trình duyệt, hoặc dùng static server bất kỳ:

```powershell
npx serve .
```

## Deploy lên Vercel

Repo này là static site thuần — Vercel tự nhận diện, không cần cấu hình thêm.

**Cách 1: Import qua dashboard**

1. Push code lên GitHub (đã có remote `origin`).
2. Vào [vercel.com/new](https://vercel.com/new) → chọn repo `claude-certification-quiz`.
3. Framework Preset: **Other** · Build Command: *(để trống)* · Output Directory: *(để trống)*.
4. Bấm **Deploy** — Vercel sẽ serve `index.html` tại root.

**Cách 2: Vercel CLI**

```powershell
npm i -g vercel
vercel        # deploy preview
vercel --prod # deploy production
```

## Cấu trúc

```text
index.html   # Toàn bộ ứng dụng (HTML + CSS + JS + ngân hàng câu hỏi)
README.md
```
