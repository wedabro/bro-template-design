# USSH Vote — Hệ Thống Bình Chọn Trực Tuyến 🗳️

Dự án thiết kế giao diện (Template Design) cho **Hệ thống Bình chọn & Vinh danh Trực tuyến** (USSH Voting Portal).

---

## 🎯 Mục Tiêu Thiết Kế

- **Ấn tượng thị giác**: Giao diện trẻ trung, hiện đại, uy tín, phù hợp với môi trường giáo dục/sinh viên và các sự kiện vinh danh lớn.
- **Trải nghiệm người dùng (UX)**: Thao tác bình chọn nhanh chóng, minh bạch, trực quan trên cả thiết bị di động (Mobile-first) và máy tính (Desktop).
- **Tính năng nổi bật**: Đếm ngược sự kiện, bảng xếp hạng thời gian thực (Real-time Leaderboard), xác thực cử tri chống gian lận vote.

---

## 📐 Kiến Trúc & Thiết Kế Các Trang (Page Layout Specifications)

### 1. Trang Chủ (Landing Page / Home)
- **Header Navigation**:
  - Logo trường/sự kiện, Menu điều hướng (Trang chủ, Hạng mục, Bảng xếp hạng, Thể lệ, Trợ giúp).
  - Nút "Đăng nhập / Xác thực".
- **Hero Section**:
  - Banner hình ảnh/video hiệu ứng sống động của sự kiện bình chọn.
  - Tiêu đề lớn (Headline) + Tagline truyền cảm hứng.
  - Đồng hồ đếm ngược (Countdown Timer) đóng/mở cổng bình chọn.
  - Nút Call-to-Action (CTA): **"Bình Chọn Ngay"** (Scroll mượt xuống danh sách hạng mục).
- **Khối Hạng Mục Bình Chọn (Categories Grid)**:
  - Danh sách các bảng/hạng mục (ví dụ: *Gương mặt Trẻ Tiêu biểu*, *Cán bộ Hội Xuất sắc*, *Cuộc thi Tài năng*...).
- **Khối Thống Kê Thời Gian Thực (Live Metrics Counter)**:
  - Số liệu thống kê động: *Tổng lượt bình chọn*, *Số ứng viên*, *Số lượt truy cập*.
- **Thể Lệ & Mốc Thời Gian (Rules & Timeline)**:
  - Các mốc mở/đóng cổng vote, điều kiện bình chọn hợp lệ.
- **Footer**:
  - Thông tin Ban tổ chức, Bản quyền, Liên hệ hỗ trợ & Các kênh Truyền thông/Social Media.

---

### 2. Trang Danh Sách Ứng Viên & Hạng Mục (Candidate Catalog)
- **Thanh Lọc & Tìm Kiếm (Filter Bar)**:
  - Dropdown lọc theo Khoa / Viện / Đơn vị.
  - Tab chuyển đổi giữa các Hạng mục bình chọn.
  - Ô tìm kiếm ứng viên theo Tên hoặc Mã số ứng viên.
- **Grid Danh Sách Ứng Viên (Candidate Cards Grid)**:
  - Card thiết kế hiệu ứng Hover/Glassmorphism:
    - Ảnh chân dung chất lượng cao.
    - Tên ứng viên, Mã số, Khoa/Đơn vị.
    - Badge hiển thị số lượt vote hiện tại.
    - Nút **"Bình chọn"** (bình chọn nhanh) & Nút **"Xem thông tin"** (mở trang chi tiết).

---

### 3. Trang Chi Tiết Ứng Viên (Candidate Profile)
- **Profile Header**:
  - Avatar khổ lớn, Tên đầy đủ, Danh hiệu/Hạng mục ứng cử.
  - Tổng số lượt bình chọn nhận được & Thứ hạng hiện tại trong bảng đấu.
- **Khối Giới Thiệu & Thành Tích (Bio & Accomplishments)**:
  - Bài viết giới thiệu bản thân / Câu nói yêu thích.
  - Danh sách thành tích nổi bật, giải thưởng, dự án cá nhân (dạng Timeline hoặc Bullet point sinh động).
- **Bộ Bộ Bộ Thư Viện Ảnh/Video (Media Gallery)**:
  - Carousel hình ảnh hoạt động, video giới thiệu ấn tượng.
- **Khu Vực Bình Chọn & Gửi Lời Chúc (Voting Form & Messages)**:
  - Nút bình chọn lớn kèm hiệu ứng thả tim/pháo hoa khi click.
  - Khung gửi lời chúc/cổ vũ công khai cho ứng viên (Message Wall).

---

### 4. Trang Bảng Xếp Hạng & Kết Quả (Real-time Leaderboard)
- **Top 3 Vinh Danh (Podium Section)**:
  - Khối Podium thiết kế nổi bật cho 3 ứng viên dẫn đầu (Hạng 1, 2, 3) với vương miện/badge đặc biệt.
- **Biểu Đồ Kết Quả (Interactive Chart)**:
  - Biểu đồ thanh (Bar chart) trực quan hóa khoảng cách số vote giữa các ứng viên.
- **Bảng Xếp Hạng Đầy Đủ (Full Ranking Table)**:
  - Bảng danh sách chi tiết: Thứ hạng, Avatar, Tên, Đơn vị, Số vote, Tỷ lệ % vote.
  - Phân trang hoặc hiệu ứng cuộn vô tận (Infinite Scroll).

---

### 5. Trang Xác Thực & Đăng Nhập (Auth & Voter Verification Modal)
- **Xác Thực Cử Tri (Voter Authentication)**:
  - Form nhập Mã số sinh viên / Email nhà trường (SSO Google / Office 365) hoặc Xác thực mã OTP.
  - Đảm bảo cơ chế: **1 Cử tri - 1 Lượt vote / ngày / hạng mục**.
- **Thông Báo Trạng Thái Bình Chọn**:
  - Modal thông báo thành công (Success Modal) kèm nút Chia sẻ (Share Facebook/Zalo) để lan tỏa cho ứng viên.
  - Thông báo khi đã hết lượt vote trong ngày.

---

### 6. Trang Quản Trị Hệ Thống (Admin Dashboard UI)
- **Dashboard Tổng Quan**:
  - Biểu đồ lưu lượng truy cập, tốc độ tăng trưởng lượt vote theo giờ/ngày.
- **Quản Lý Sự Kiện & Hạng Mục**:
  - Bật/Tắt cổng bình chọn khẩn cấp, chỉnh sửa thể lệ, cấu hình thời gian.
- **Quản Lý Danh Sách Ứng Viên**:
  - Thêm mới, chỉnh sửa thông tin, tải lên hình ảnh/thành tích ứng viên.
- **Giám Sát & Xuất Báo Cáo**:
  - Phát hiện các bất thường (Spam vote / Bot IP), lọc lượt vote hợp lệ.
  - Export báo cáo kết quả ra file Excel / PDF chính thức.

---

## 🎨 Định Hướng UI/UX & Design System

- **Màu sắc chủ đạo**:
  - Primary: Burgundy Red / Deep Navy (Thể hiện tính chính thống, trang trọng của USSH).
  - Accent: Vibrant Gold / Bright Amber (Dành cho hiệu ứng vinh danh, top 1, nút vote CTA).
  - Background: Clean Light Mode hoặc Sleek Modern Dark Mode.
- **Typography**: Font chữ hiện đại, rõ ràng (ví dụ: *Inter*, *Be Vietnam Pro* hoặc *Outfit*).
- **Responsive**: Tối ưu 100% giao diện cho Smartphone, Tablet và Desktop.
