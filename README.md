Ứng dụng di động giúp sinh viên PTIT tra cứu lịch học, phòng trống và nhận thông báo mới nhất từ nhà trường.
Ghé thăm trang chủ của chúng mình tại CLB Lập trình PTIT.
Các tính năng đã hoàn thành
Tra cứu lịch học theo mã sinh viên
Hỗ trợ xem lịch theo tuần và theo học kỳ
Xem danh sách phòng trống theo tòa nhà
Cảnh báo: Dự án đang trong giai đoạn phát triển, chưa dùng cho mục đích chính thức.
Hướng dẫn cài đặt
Chạy các lệnh sau trong Terminal để khởi chạy dự án:
git clone https://github.com/clb-lap-trinh/smartcampus.git
npm install
npm start
Tiến độ dự án (Task List)
Tra cứu lịch học theo mã sinh viên
Xem danh sách phòng trống theo tòa nhà
Thông báo đẩy (push notification)
Đăng nhập bằng tài khoản trường
Danh sách thư viện
Thư viện
Phiên bản
Mục đích
React Native
0.74
Xây giao diện đa nền tảng iOS/Android
Axios
1.6
Gọi API lấy dữ liệu lịch học
Tài liệu tra cứu: Thuật ngữ API
1. Prompt đặt câu hỏi cho AI (Công thức Prompt 3 phần)
## Tôi là ai / Bối cảnh
Tôi là sinh viên năm nhất vừa tham gia CLB Lập trình, đang làm dự án ứng dụng di động SmartCampus.
## Chủ đề / Nội dung cần xử lý
Tôi cần hiểu rõ thuật ngữ kỹ thuật "API" là gì.
## Yêu cầu
- Giải thích API bằng một ẩn dụ thực tế, dễ hiểu cho người mới học lập trình.
- Nêu rõ vai trò của API trong ứng dụng di động như SmartCampus.
- Trình bày ngắn gọn bằng các gạch đầu dòng rõ ràng.
## Không cần
- Không cần giải thích sâu về các phương thức HTTP (GET, POST, PUT, DELETE) hoặc code minh họa phức tạp.
- Không dùng quá nhiều thuật ngữ chuyên ngành chưa giải thích.
2. Tóm tắt câu trả lời của AI (Chiến lược 3 bước)
API (Application Programming Interface) đóng vai trò là "person phục vụ" trung gian kết nối và truyền dữ liệu giữa ứng dụng di động (giao diện người dùng) và hệ thống máy chủ.
Trong ứng dụng SmartCampus, API giúp app gửi yêu cầu lấy dữ liệu lịch học hoặc danh sách phòng trống từ máy chủ nhà trường và trả kết quả về màn hình điện thoại.
Nhờ có API, ứng dụng frontend không cần truy cập trực tiếp vào cơ sở dữ liệu gốc mà vẫn lấy đủ dữ liệu cần thiết một cách an toàn và tiện lợi.
3. Nội dung chi tiết từ AI
API là gì?
API (Application Programming Interface - Giao diện lập trình ứng dụng) là cầu nối cho phép hai phần mềm hoặc hệ thống máy tính giao tiếp và trao đổi dữ liệu với nhau.
Ẩn dụ thực tế: Khái niệm "Người phục vụ bàn"
Hãy tưởng tượng bạn đi ăn ở nhà hàng:
Bạn (Người dùng / App SmartCampus): Chọn món trên menu.
Nhà bếp (Máy chủ / Database của trường): Nơi chứa và chế biến thức ăn (dữ liệu).
Bồi bàn (API): Lấy yêu cầu món ăn của bạn mang vào bếp, sau đó bê món ăn từ bếp ra bàn cho bạn.
Vai trò của API trong ứng dụng SmartCampus
Tra cứu lịch học: Khi bạn nhập Mã sinh viên trên app, API sẽ gửi mã này lên máy chủ trường, tìm đúng lịch học và trả về hiển thị trên điện thoại.
Bảo mật dữ liệu: App không cần truy cập trực tiếp vào CSDL gốc của nhà trường mà chỉ giao tiếp qua API.
Phân tích lỗi cú pháp và Sửa lỗi (Phần 4)

1. Chỉ ra 2 lỗi cú pháp trong đoạn mã nguồn ban đầu
Lỗi 1 (Cấu trúc Table): Thiếu dòng phân cách tiêu đề cột chứa dấu gạch ngang (ví dụ: | --- | --- |). Trong Markdown, nếu thiếu dòng phân cách này thì trình dịch (Parser) chỉ coi các dòng đó là văn bản thường cách nhau bởi dấu | chứ không thể render thành dạng bảng (Table).
Lỗi 2 (Cú pháp Task List): Thiếu khoảng trắng giữa dấu gạch ngang - và cặp ngoặc vuông [x] / [ ] (viết liền dạng -[x]). Quy tắc chuẩn của Task List bắt buộc phải có ít nhất một khoảng trắng sau dấu gạch ngang (ví dụ: - [x] hoặc - [ ]).
2. Đoạn mã Markdown đã sửa hoàn chỉnh
| Tính năng | Trạng thái |
| :--- | :--- |
| Tra cứu lịch học | Xong |
| Push notification | Đang làm |
- [x] Tra cứu lịch học
- [ ] Push notification
