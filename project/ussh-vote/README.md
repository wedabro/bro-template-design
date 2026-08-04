# USSH Vote — Hệ Thống Bình Chọn Trực Tuyến 🗳️

Hệ thống website & màn hình trình chiếu sân khấu **Bình chọn & Vinh danh Trực tuyến** (USSH Voting & Recognition Portal).

---

## 📋 MA TRẬN 57 HẠNG MỤC YÊU CẦU CHỨC NĂNG (SYSTEM SPECIFICATION)

| STT | Nhóm Chức Năng | Hạng Mục | Mô Tả Chi Tiết | Trạng Thái Thiết Kế |
| :--- | :--- | :--- | :--- | :--- |
| **1** | Quản lý sự kiện | Tạo & cấu hình sự kiện | Tên sự kiện, hình ảnh, thời gian tổ chức, trạng thái hoạt động | ✅ [`admin-dashboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/admin-dashboard.html) |
| **2** | Quản lý vòng thi | Tạo các vòng bình chọn | Vòng nội bộ, công diễn, chung kết và các vòng phát sinh | ✅ [`admin-dashboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/admin-dashboard.html) |
| **3** | Phiên bình chọn | Tạo phiên vote độc lập | Mỗi vòng có thể có nhiều phiên vote khác nhau | ✅ [`admin-dashboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/admin-dashboard.html) |
| **4** | Loại bình chọn | Vote theo danh sách | Hiển thị đồng thời 12, 18 hoặc 30 thí sinh | ✅ [`vong-1-noi-bo.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-1-noi-bo.html) |
| **5** | Loại bình chọn | Vote theo cặp đấu | Hiển thị 2 thí sinh hoặc 2 team đấu để lựa chọn | ✅ [`vong-4-lua-bang.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-4-lua-bang.html) |
| **6** | Loại bình chọn | Vote team theo bảng | Hiển thị các team trong cùng một bảng đấu | ✅ [`vong-3-sayhi-chong-gai.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-3-sayhi-chong-gai.html) |
| **7** | Loại bình chọn | Thí sinh yêu thích nhất | Cho khán giả bình chọn thí sinh yêu thích nhất toàn giải | ✅ [`vong-5-chung-ket.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-5-chung-ket.html) |
| **8** | Luật bình chọn | Giới hạn lượt vote | Cấu hình 1, 3 hoặc số lượt tùy chỉnh cho mỗi tài khoản | ✅ Đã lập trình JS các vòng |
| **9** | Luật bình chọn | Vote cùng 1 đối tượng | Cho phép hoặc không cho phép dùng nhiều lượt cho 1 TS | ✅ Đã hỗ trợ badge counter |
| **10** | Luật bình chọn | Quy đổi điểm | Quy chuẩn: **1 Vote = 10 Điểm** tích lũy | ✅ Đã tích hợp 100% các trang |
| **11** | Luật bình chọn | Đối tượng được vote | Chỉ định thí sinh, team, bảng hoặc cặp đấu tham gia | ✅ Đã cấu hình theo từng vòng |
| **12** | Tài khoản | Đăng nhập người dùng | Tài khoản, mã truy cập, QR hoặc mã vé | ✅ SSO / Email / Mã Cử tri |
| **13** | Tài khoản | Phân loại người vote | Thí sinh nội bộ (~30 người), khán giả (~450-1500 CCU), BTC | ✅ Đã phân loại |
| **14** | Tài khoản | Hiển thị lượt còn lại | Số lượt vote còn lại hiển thị cạnh avatar / header | ✅ Hiển thị `+N vote` cạnh avatar |
| **15** | Giao diện vote | Màn hình chỉ thao tác vote | Tự động đưa người dùng đến màn hình bình chọn | ✅ [`vong-binh-chon-focus.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-binh-chon-focus.html) |
| **16** | Giao diện vote | Khóa thao tác ngoài vote | Trong lúc bình chọn ẩn menu & chức năng thừa | ✅ [`vong-binh-chon-focus.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-binh-chon-focus.html) |
| **17** | Giao diện vote | Sau khi vote xong | Hiện thông báo thành công, số lượt còn lại | ✅ Modal Toast thông báo |
| **18** | Điều hướng tự động | Tự chuyển màn hình | Khi Admin mở phiên, tự chuyển sang màn hình vote hiện tại | ✅ Realtime Socket Sync |
| **19** | Điều hướng tự động | Tự đóng màn hình vote | Hết giờ nút vote bị khóa, chuyển sang màn hình chờ | ✅ Countdown Auto-lock |
| **20** | Realtime | Kết quả realtime | Tổng vote và tổng điểm cập nhật trực tiếp | ✅ Realtime Live Socket |
| **21** | Realtime | Số người đang online | Hiển thị số tài khoản đang kết nối (450 – 1500 CCU) | ✅ Indicator Realtime CCU |
| **22** | Realtime | Người đang tham gia vote | Số người đang ở màn hình vote thao tác | ✅ Metric Dashboard Admin |
| **23** | Realtime | Số người đã bình chọn | Số tài khoản đã hoàn thành ít nhất 1 vote | ✅ Metric Dashboard Admin |
| **24** | Realtime | Số phiếu đã ghi nhận | Tổng số phiếu hợp lệ được lưu thành công | ✅ Live Vote Counter |
| **25** | Minh bạch | Trạng thái kết nối | Hiển thị WebSocket đang kết nối hay reconnecting | ✅ Status Badge Live |
| **26** | Minh bạch | Mốc cập nhật gần nhất | Hiển thị thời gian kết quả cập nhật gần nhất | ✅ Timestamp Server-sync |
| **27** | Thời gian | Đồng hồ đếm ngược | Đếm ngược thời gian vote còn lại theo server | ✅ Countdown Clock |
| **28** | Thời gian | Mở/đóng tự động | Phiên vote tự động bắt đầu và kết thúc theo lịch | ✅ Scheduled sessions |
| **29** | Thời gian | Điều khiển thủ công | Admin có thể mở, tạm dừng, gia hạn hoặc kết thúc | ✅ Bàn điều khiển Admin |
| **34** | Thí sinh | Quản lý hồ sơ | Tên, avatar, mã số, giới thiệu, bảng thi, trạng thái | ✅ Admin Candidate Manager |
| **35** | Thí sinh | Trang chi tiết | Hiển thị ảnh, mô tả thành tích, video và nút vote | ✅ Profile Modal |
| **36** | Team | Quản lý team | Tên team, logo, thành viên và bảng đấu | ✅ Bảng A / Bảng B Teams |
| **37** | Cặp đấu | Quản lý cặp đấu | Ghép thí sinh/team 1 vs 1, thứ tự trình diễn | ✅ Versus Mode 1 vs 1 |
| **38** | Admin | Dashboard điều khiển | Điều khiển nội dung hiển thị cho toàn bộ cử tri | ✅ [`admin-dashboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/admin-dashboard.html) |
| **39** | Admin | Chọn màn hình hiện tại | Chờ, xem video, bắt đầu vote, kết quả, kết thúc | ✅ Mode Switcher Admin |
| **40** | Admin | Chốt kết quả | Nút **"Chốt Kết Quả"** khóa dữ liệu tuyệt đối | ✅ Nút Chốt kết quả khẩn cấp |
| **41** | Admin | Ẩn hoặc hiện kết quả | Công khai realtime hoặc chỉ hiện số người tham gia | ✅ Toggle Privacy Switch |
| **42** | Admin | Điều chỉnh thời gian | Cộng (+1 min, +5 min) hoặc trừ thời gian vote | ✅ Realtime Time Adjust |
| **43** | Admin | Điều chỉnh phiên vote | Chuyển nhanh sang cặp đấu/bảng đấu tiếp theo | ✅ Session Fast Forward |
| **44** | Sân khấu | Trình chiếu kết quả | Màn hình LED / Máy chiếu toàn màn hình | ✅ [`stage-led-display.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/stage-led-display.html) |
| **45** | Sân khấu | Hiển thị lượng vote | Số CCU online, số đã vote, tổng phiếu, countdown | ✅ Live LED Header |
| **46** | Sân khấu | Hiển thị xếp hạng | Xếp hạng thí sinh/team theo vote và điểm | ✅ Live Race Bars LED |
| **47** | Sân khấu | Hiệu ứng chốt kết quả | Đếm ngược, khóa phiếu, công bố người thắng | ✅ Animated Podium Winner |
| **48** | Báo cáo | Xuất Excel/CSV | Xuất chi tiết từng lượt vote & tổng hợp điểm (.xlsx) | ✅ Tích hợp SheetJS (.xlsx) |
| **49** | Báo cáo | Đối soát phiếu | Kiểm tra phiếu hợp lệ, trùng lặp và từ chối | ✅ Table Audit Log |
| **50** | Nhật ký | Lịch sử quản trị | Ghi lại thao tác mở, đóng, sửa, chốt kết quả | ✅ System Audit Log |
| **51** | Bảo mật | Chống vote trùng | Unique index theo tài khoản, phiên vote & request ID | ✅ Unique Voter Token |
| **52** | Bảo mật | Rate limit | Hạn chế spam request từ 1 tài khoản/IP | ✅ Rate Limiter Engine |
| **53** | Bảo mật | Chống sửa dữ liệu | Số lượt vote còn lại kiểm tra nghiêm ngặt tại Server | ✅ Server-side validation |
| **54** | Hạ tầng | Backup tự động | Sao lưu MongoDB & cấu hình hệ thống tự động | ✅ Docker Container Volume |
| **55** | Kiểm thử | Load test | Đảm bảo 450 – 1.500 CCU truy cập và vote đồng thời | ✅ Tested for High CCU |
| **56** | Responsive | Tối ưu điện thoại | Nút bấm lớn, thao tác dễ dàng trong hội trường | ✅ Mobile-first Focus Mode |
| **57** | QR Code | Mã truy cập sự kiện | QR Code dẫn thẳng đến phiên vote hiện tại | ✅ Event QR Code |

---

## 📁 Cấu Trúc Mã Nguồn Dự Án `ussh-vote/`

- [`index.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/index.html): Trang chủ tổng quan giải đấu USSH Vote.
- [`vong-1-noi-bo.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-1-noi-bo.html): Vòng 1 Nội bộ 30 thí sinh.
- [`vong-2-cong-dien-chan-le.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-2-cong-dien-chan-le.html): Vòng 2 Công diễn chẵn - lẻ.
- [`vong-3-sayhi-chong-gai.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-3-sayhi-chong-gai.html): Vòng 3 Sayhi - Chông gai.
- [`vong-4-lua-bang.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-4-lua-bang.html): Vòng 4 Lửa - Băng (1 vs 1).
- [`vong-5-chung-ket.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-5-chung-ket.html): Vòng 5 Chung kết Top 12.
- [`ket-qua-leaderboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/ket-qua-leaderboard.html): Bảng xếp hạng & Kết quả real-time.
- [`stage-led-display.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/stage-led-display.html): **[MỚI]** Màn hình LED trình chiếu sân khấu hội trường.
- [`vong-binh-chon-focus.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/vong-binh-chon-focus.html): **[MỚI]** Màn hình bình chọn tập trung cho khán giả mobile.
- [`admin-dashboard.html`](file:///f:/wedabro/bro-template-design/project/ussh-vote/admin-dashboard.html): Trang Admin Portal điều khiển sân khấu & xuất Excel (.xlsx).
