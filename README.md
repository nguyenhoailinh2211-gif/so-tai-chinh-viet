# Sổ Tài Chính

Web app quản lý chi tiêu cá nhân, kinh doanh và ghi chú bằng tiếng Việt.

## Chạy trên máy

```bash
npm install
npm run dev
```

## Deploy GitHub + Vercel

1. Tạo repository mới trên GitHub.
2. Trong thư mục dự án, chạy `git init`, `git add .`, `git commit -m "Initial app"` rồi `git push` lên repository.
3. Vào Vercel, chọn **Add New → Project**, import repository GitHub.
4. Vercel tự nhận diện Vite. Build command: `npm run build`; Output directory: `dist`.
5. Nhấn **Deploy** để nhận tên miền `.vercel.app` miễn phí.

## Dữ liệu và realtime

Phiên bản hiện tại lưu dữ liệu bằng LocalStorage nên dữ liệu không mất khi F5 hoặc đóng trình duyệt. Các tab của cùng trình duyệt tự đồng bộ tức thì qua sự kiện `storage`.

Để nhiều người dùng xem và cập nhật dữ liệu realtime qua Internet, cần kết nối thêm Supabase hoặc Firebase, kèm xác thực người dùng và cơ sở dữ liệu dùng chung. LocalStorage không thể đồng bộ dữ liệu giữa thiết bị/người dùng khác nhau.
