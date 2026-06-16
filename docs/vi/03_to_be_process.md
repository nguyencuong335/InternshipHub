#03. Phân tích quy trình TO-BE

## 1. Mục đích

Tài liệu này mô tả quy trình tuyển dụng thực tập sinh trong tương lai sau khi triển khai hệ thống InternshipHub.

Mục tiêu của phân tích TO-BE là thiết kế quy trình làm việc tốt hơn nhằm giải quyết các điểm yếu trong quy trình AS-IS.

## 2. Tóm tắt quy trình trong tương lai

Trong quá trình tương lai, InternshipHub sẽ được sử dụng như một hệ thống tập trung để quản lý đơn đăng ký thực tập, trạng thái ứng viên, lên lịch phỏng vấn, phản hồi của người phỏng vấn và quyết định tuyển dụng.

Thay vì sử dụng nhiều công cụ riêng biệt như email, bảng tính và ứng dụng trò chuyện, HR có thể quản lý quy trình tuyển dụng trong một hệ thống.

## 3. Các bước quy trình SẼ ĐƯỢC

| Bước | Diễn viên | Hoạt động tương lai | Hỗ trợ hệ thống |
|---|---|---|---|
| 1 | Ứng viên | Tạo tài khoản và nộp đơn | Đơn đăng ký |
| 2 | Ứng viên | Tải lên CV và thông tin cá nhân | Tải lên hồ sơ và CV |
| 3 | Hệ thống | Xác thực thông tin bắt buộc | Xác thực mẫu |
| 4 | Nhà tuyển dụng nhân sự | Xem ứng dụng mới | Bảng thông tin ứng viên |
| 5 | Nhà tuyển dụng nhân sự | Sàng lọc hồ sơ ứng viên | Trang chi tiết ứng viên |
| 6 | Nhà tuyển dụng nhân sự | Cập nhật trạng thái ứng viên | Quản lý trạng thái |
| 7 | Hệ thống | Gửi thông báo trạng thái cho ứng viên | Thông báo qua email |
| 8 | Nhà tuyển dụng nhân sự | Lên lịch phỏng vấn và phân công người phỏng vấn | Lên lịch phỏng vấn |
| 9 | Người phỏng vấn | Xem cuộc phỏng vấn được phân công và hồ sơ ứng viên | Bảng điều khiển của người phỏng vấn |
| 10 | Người phỏng vấn | Gửi phản hồi có cấu trúc | Mẫu phản hồi |
| 11 | Quản lý tuyển dụng | Đánh giá hệ thống ứng viên và phản hồi | Bảng điều khiển đường ống |
| 12 | Quản lý tuyển dụng | Đưa ra hoặc phê duyệt quyết định cuối cùng | Quản lý quyết định |
| 13 | Nhà tuyển dụng nhân sự | Gửi kết quả đề nghị hoặc từ chối | Thông báo kết quả |
| 14 | Hệ thống | Lưu trữ lịch sử trạng thái và nhật ký hoạt động | Nhật ký kiểm tra |

## 4. Những cải tiến chính từ AS-IS sang TO-BE

| Vấn đề AS-IS | Cải tiến TO-BE |
|---|---|
| Dữ liệu ứng viên được lưu trữ ở nhiều nơi. | Dữ liệu ứng viên được tập trung vào một hệ thống. |
| Nhân sự cập nhật trạng thái ứng viên theo cách thủ công trong bảng tính. | Nhân sự cập nhật trạng thái trực tiếp trên hệ thống. |
| Ứng viên không biết tình trạng hiện tại. | Ứng viên có thể xem trạng thái đơn đăng ký. |
| Lịch phỏng vấn được thực hiện thông qua trò chuyện hoặc email. | Nhân sự có thể đặt lịch phỏng vấn trên hệ thống. |
| Phản hồi được gửi ở các định dạng khác nhau. | Người phỏng vấn gửi mẫu phản hồi có cấu trúc. |
| Người quản lý tuyển dụng thiếu khả năng hiển thị quy trình. | Người quản lý tuyển dụng có thể xem bảng điều khiển và đường dẫn ứng viên. |
| Không có lịch sử trạng thái rõ ràng. | Hệ thống lưu trữ lịch sử trạng thái và nhật ký hoạt động. |

## 5. Luồng trạng thái ứng viên trong tương lai

Luồng trạng thái ứng viên phải là:

```văn bản
Bản nháp → Đã gửi → Sàng lọc → Lên lịch phỏng vấn → Đã hoàn thành cuộc phỏng vấn → Đề nghị / Từ chối / Giữ lại