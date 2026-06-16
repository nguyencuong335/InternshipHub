#02. Phân tích quy trình AS-IS

## 1. Mục đích

Tài liệu này mô tả quy trình tuyển dụng thực tập sinh hiện tại trước khi triển khai hệ thống InternshipHub.

Mục tiêu của phân tích AS-IS là hiểu quy trình làm việc hiện tại, xác định các bước thủ công, tìm điểm yếu và khám phá các cơ hội cải tiến.

## 2. Tóm tắt quy trình hiện tại

Hiện tại, quy trình tuyển dụng thực tập sinh được quản lý thông qua các công cụ khác nhau như email, bảng tính, ứng dụng trò chuyện và ghi chú thủ công.

Quá trình này có thể hoạt động khi số lượng ứng viên ít. Tuy nhiên, khi số lượng đơn đăng ký tăng lên, bộ phận nhân sự có thể gặp khó khăn trong việc theo dõi trạng thái ứng viên, lên lịch phỏng vấn, thu thập phản hồi và gửi thông tin cập nhật kịp thời.

## 3. Các bước xử lý AS-IS

| Bước | Diễn viên | Hoạt động hiện tại | Công cụ được sử dụng |
|---|---|---|---|
| 1 | Ứng viên | Gửi CV hoặc điền đơn ứng tuyển | Email / Biểu mẫu Google |
| 2 | Nhà tuyển dụng nhân sự | Tải CV ứng viên | Email / Google Drive |
| 3 | Nhà tuyển dụng nhân sự | Thêm thông tin ứng viên vào tệp theo dõi | Bảng tính Excel / Google |
| 4 | Nhà tuyển dụng nhân sự | Sàng lọc hồ sơ ứng viên theo cách thủ công | CV / Bảng tính |
| 5 | Nhà tuyển dụng nhân sự | Liên hệ ứng viên cho bước tiếp theo | Email / Zalo / Đội |
| 6 | Nhà tuyển dụng nhân sự | Lên lịch phỏng vấn với người phỏng vấn | Trò chuyện / Lịch / Email |
| 7 | Người phỏng vấn | Đánh giá CV ứng viên trước khi phỏng vấn | Email / Thư mục dùng chung |
| 8 | Người phỏng vấn | Tiến hành phỏng vấn | Họp trực tuyến / Ngoại tuyến |
| 9 | Người phỏng vấn | Gửi phản hồi tới HR | Trò chuyện / Email / Bảng tính |
| 10 | Nhà tuyển dụng nhân sự | Cập nhật trạng thái ứng viên theo cách thủ công | Bảng tính |
| 11 | Quản lý tuyển dụng | Đánh giá ứng viên được lựa chọn | Bảng tính / tóm tắt nhân sự |
| 12 | Nhà tuyển dụng nhân sự | Gửi kết quả cuối cùng cho ứng viên | Email / Trò chuyện |

## 4. Điểm đau

| ID điểm đau | Điểm đau | Tác động |
|---|---|---|
| PP-01 | Thông tin ứng viên được lưu trữ ở nhiều nơi. | Nhân sự có thể bị mất thông tin hoặc mất nhiều thời gian tìm kiếm hơn. |
| PP-02 | Trạng thái ứng viên được cập nhật thủ công. | Trạng thái có thể trở nên lỗi thời hoặc không chính xác. |
| PP-03 | Lịch phỏng vấn được thực hiện thông qua trò chuyện hoặc email. | Xung đột về thời gian hoặc thiếu thông tin có thể xảy ra. |
| PP-04 | Phản hồi phỏng vấn không được chuẩn hóa. | Người quản lý nhân sự và tuyển dụng có thể khó so sánh các ứng viên. |
| PP-05 | Ứng viên không biết tình trạng hồ sơ hiện tại. | Trải nghiệm của ứng viên trở nên không rõ ràng và căng thẳng. |
| PP-06 | Người quản lý tuyển dụng không thể nhìn thấy rõ ràng quy trình tuyển dụng. | Quyết định tuyển dụng cuối cùng có thể chậm hơn. |
| PP-07 | Không có lịch sử trạng thái rõ ràng. | Thật khó để kiểm tra xem ai đã thay đổi cái gì và khi nào. |

## 5. Nguyên nhân cốt lõi

| ID nguyên nhân gốc | Nguyên nhân gốc rễ |
|---|---|
| RC-01 | Không có hệ thống tập trung để quản lý tuyển dụng. |
| RC-02 | Nhân sự phụ thuộc nhiều vào bảng tính và cập nhật thủ công. |
| RC-03 | Việc giao tiếp với ứng viên không được tự động hóa. |
| RC-04 | Phản hồi phỏng vấn không tuân theo một định dạng cố định. |
| RC-05 | Dữ liệu tuyển dụng không được kết nối giữa các bên liên quan. |

## 6. Cơ hội cải tiến

| ID cơ hội | Cơ hội cải tiến |
|---|---|
| OP-01 | Tạo cơ sở dữ liệu ứng viên tập trung. |
| OP-02 | Cho phép HR quản lý trạng thái ứng viên trên hệ thống. |
| OP-03 | Thêm lịch phỏng vấn và phân công người phỏng vấn. |
| OP-04 | Tạo một mẫu phản hồi có cấu trúc cho người phỏng vấn. |
| OP-05 | Cho phép ứng viên xem trạng thái đơn đăng ký của họ. |
| OP-06 | Cung cấp bảng thông tin quy trình tuyển dụng cho người quản lý tuyển dụng. |
| OP-07 | Lưu trữ lịch sử trạng thái để kiểm tra và theo dõi. |

##7. BA Ghi chú

Quy trình AS-IS cho thấy vấn đề chính không chỉ nằm ở việc thiếu một tính năng. Vấn đề thực sự là quy trình tuyển dụng bị phân mảnh trên nhiều công cụ.

Do đó, hệ thống trong tương lai nên tập trung vào tính tập trung, minh bạch, tiêu chuẩn hóa và theo dõi.