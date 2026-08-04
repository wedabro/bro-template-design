# Bro Template Design 🎨

Tổng hợp các **UI/UX Project Templates** được thiết kế & phát triển nhanh dành cho các hệ thống website, web apps và cổng thông tin.

---

## 📁 Danh Sách Dự Án (Project Catalog)

Tất cả các dự án mẫu được quản lý trong thư mục [`project/`](file:///f:/wedabro/bro-template-design/project):

| STT | Tên Dự Án | Thư Mục | Mô Tả | Trạng Thái |
| :--- | :--- | :--- | :--- | :--- |
| **01** | **USSH Vote** | [`project/ussh-vote/`](file:///f:/wedabro/bro-template-design/project/ussh-vote) | Hệ thống Bình chọn & Vinh danh Trực tuyến (Voting & Recognition Portal) | 🟡 Đang thiết kế |

---

## 🚀 Hướng Dẫn Thêm Dự Án Mới

Để khởi tạo thêm dự án thiết kế mới trong kho lưu trữ này:

1. Tạo thư mục mới theo tên dự án trong `project/`:
   ```bash
   mkdir project/<ten-du-an>
   ```
2. Khởi tạo file `README.md` trong thư mục dự án để mô tả yêu cầu thiết kế và kiến trúc các trang.
3. Cập nhật danh sách bảng trên tại file `README.md` root.

---

## 🛠️ Quy Chuẩn Đóng Gói & Thiết Kế

- **Design Aesthetics**: Giao diện hiện đại, sử dụng gradient hài hòa, hỗ trợ Dark/Light Mode, micro-animations và Typography chuẩn.
- **Docker-First Policy**: Mọi dịch vụ chạy ứng dụng phải được container hóa qua `docker-compose`.
- **Environment Variables**: Cấu hình linh hoạt qua file `.env`, tuyệt đối không hard-code endpoint hay credentials.
