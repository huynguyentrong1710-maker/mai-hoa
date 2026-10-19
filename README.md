# the Meal — Sandbox cài đặt & kiểm thử

Trang web **demo tương tác một file HTML** dùng để thuyết trình quy trình cài đặt và thử nghiệm hệ thống the Meal. Giao diện hỗ trợ desktop và điện thoại; không cần cài máy chủ.

## Cách chạy

1. Giải nén `theMeal_Website_Testing.zip`.
2. Mở `index.html` bằng Chrome, Edge hoặc trình duyệt hiện đại.
3. Vào **Cài đặt môi trường** → **Khởi tạo tất cả**. Chức năng cũng cho phép bật từng phân hệ và nạp dữ liệu riêng.
4. Chọn vai trò ở góc trên bên phải để thực hành theo kịch bản. Khi cần, bấm **Nhật ký kiểm thử** để xem tiêu chí PASS/PENDING và tải báo cáo JSON.
5. Dữ liệu thao tác được lưu bằng bộ nhớ trình duyệt (`localStorage`, nếu trình duyệt cho phép). Nút **Đặt lại sandbox** sẽ xóa dữ liệu demo.

## Quy trình trình diễn gợi ý

### Kịch bản 01 — Người dùng & AI Scanner
- Chọn vai trò **Người dùng**.
- Vào **Người dùng & AI Scanner** → lưu hồ sơ để xem BMI, TDEE, calo khuyến nghị, macro.
- Chọn ảnh thực phẩm (tùy chọn), chọn món trong danh mục mẫu và nhấn **Phân tích món ăn (demo)**.
- Lưu bữa ăn, quan sát Health Score; thử báo cáo món ăn sai.
- Thử trợ lý Miu và nút kết nối các thiết bị ảo.

### Kịch bản 02 — Tủ lạnh thông minh
- Vào **Tủ lạnh thông minh** → nhấn **Nạp nhanh 7 thực phẩm** → **Thử thêm sản phẩm thứ 8**.
- Xem thông báo chặn của Freemium; nhấn **Nâng cấp Premium (demo)** để thử thêm.
- Nhấn **Bảo quản** trên một thực phẩm để xem hướng dẫn, sau đó **Gợi ý thực đơn & danh sách mua sắm**.

### Kịch bản 03 — Chuyên gia & Khóa học
- Chuyển vai trò **Chuyên gia**, tải một file chứng chỉ giả lập và gửi hồ sơ.
- Chuyển vai trò **Quản trị viên**, vào **Quản trị & Kiểm duyệt** để duyệt hồ sơ.
- Trở về **Chuyên gia**, gõ đúng tên đăng ký và xác nhận hợp đồng hợp tác mô phỏng.
- Đăng khóa học giá **500.000đ**: phí đăng **10% = 50.000đ**.
- Chuyển vai trò **Người dùng**, tạo hợp đồng 3 bên, ký xác nhận rồi thanh toán demo: hoa hồng **2% = 10.000đ**.

### Kịch bản 04 — Admin
- Chuyển vai trò **Quản trị viên**.
- Xử lý báo cáo AI Scanner và cập nhật giá trị dinh dưỡng cơ sở.
- Duyệt hoặc từ chối bài viết cộng đồng.
- Vào **Nhật ký kiểm thử** xem 12 tiêu chí hoàn tất. Tải báo cáo JSON khi cần.

## Dữ liệu có sẵn

`data/themeal-5120-mock-records.csv` chứa **5.120 dòng sinh từ 32 món ăn cơ sở, 16 mức khẩu phần và 10 mã biến thể cho mỗi mức**. Đây là **dữ liệu tổng hợp giả lập**, không phải 5.120 món ăn độc lập và không phải bảng thành phần dinh dưỡng chuẩn hóa. Web có chức năng xuất lại file CSV từ trang Cài đặt.

## Giới hạn và an toàn

- **Không có backend/database thật, API AI, thị giác máy tính, thiết bị IoT/Bluetooth, cổng thanh toán hoặc chữ ký số có giá trị pháp lý.** Tất cả là mô phỏng hoạt động và trạng thái client-side.
- Dữ liệu BMI, năng lượng và macro chỉ là ước lượng để minh họa, không sử dụng để chẩn đoán, điều trị hoặc đưa lời khuyên y tế cá nhân.
- Không nhập thông tin cá nhân nhạy cảm hoặc tải lên tài liệu thật vì bản demo chưa triển khai hệ thống bảo mật, xác thực và quản trị dữ liệu cấp sản xuất.
- Đây là **nguyên mẫu minh họa dựa theo yêu cầu**; không phải phần mềm hay trang chính thức do the Meal phát hành.
