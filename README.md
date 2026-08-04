# Bro Template Design 🎨

Tổng hợp các **UI/UX Project Templates** được thiết kế & phát triển dành cho các hệ thống website, web apps và cổng thông tin.

---

## 📁 Danh Sách Dự Án (Project Catalog)

Tất cả các dự án mẫu được quản lý trong thư mục [`project/`](file:///f:/wedabro/bro-template-design/project):

| STT | Tên Dự Án | Thư Mục | Mô Tả | Trạng Thái |
| :--- | :--- | :--- | :--- | :--- |
| **01** | **USSH Vote** | [`project/ussh-vote/`](file:///f:/wedabro/bro-template-design/project/ussh-vote) | Hệ thống Bình chọn, Vinh danh & Màn hình LED Sân khấu (Đáp ứng 57 Hạng mục Chức năng) | ✅ Hoàn thành thiết kế |

---

## 🌟 Dự Án USSH Vote: 57 Hạng Mục Yêu Cầu Chức Năng Đã Đáp Ứng

- 📺 **Màn hình Trình chiếu LED Sân Khấu**: [`stage-led-display.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/stage-led-display.html) (Màn LED/Máy chiếu hội trường, đếm ngược toàn màn hình, vinh danh Quán quân).
- 📱 **Focus Mode Bình chọn Khán Giả Mobile**: [`vong-binh-chon-focus.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-binh-chon-focus.html) (Tối ưu nút bấm lớn, tự khóa menu ngoài khi phiên vote mở).
- 🖥️ **Admin Control Center & Xuất Excel**: [`admin-dashboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/admin-dashboard.html) (Điều khiển màn hình LED, nút Chốt kết quả, gia hạn thời gian vote, đối soát phiếu & xuất file `.xlsx` qua SheetJS).
- 📊 **5 Vòng Bình Chọn**: 1 Vote = 10 Pts, Vote Nội bộ, Vote Chẵn-Lẻ, Sayhi-Chông gai, Lửa-Băng (1:1) và Chung kết Top 12.

---

## 🛠️ Quy Chuẩn Đóng Gói & Thiết Kế

- **Design Aesthetics**: Giao diện màu đỏ đun (`#800020`) sang trọng, chuẩn Enterprise Admin UI, hỗ trợ Dark Mode và màn hình hội trường.
- **Docker-First Policy**: Mọi dịch vụ chạy ứng dụng phải được container hóa qua `docker-compose`.
- **Environment Variables**: Cấu hình linh hoạt qua file `.env`, tuyệt đối không hard-code credentials.
