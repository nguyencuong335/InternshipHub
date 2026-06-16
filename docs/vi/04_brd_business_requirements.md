#04. Tài liệu yêu cầu nghiệp vụ

## 1. Mục đích

Tài liệu này xác định các yêu cầu kinh doanh đối với hệ thống InternshipHub.

Mục đích của BRD này là mô tả doanh nghiệp cần gì, tại sao hệ thống lại cần thiết, ai sẽ được hưởng lợi từ hệ thống và giải pháp phải tuân theo những quy tắc kinh doanh nào.

## 2. Vấn đề kinh doanh

Quy trình tuyển dụng thực tập sinh hiện tại được phân chia thành email, bảng tính, công cụ trò chuyện và ghi chú thủ công. Điều này gây khó khăn cho HR trong việc theo dõi trạng thái ứng viên, lên lịch phỏng vấn, thu thập phản hồi và cung cấp thông tin cập nhật kịp thời cho ứng viên.

Khi số lượng người đăng ký tăng lên, quy trình trở nên khó quản lý hơn, kém minh bạch hơn và dễ xảy ra lỗi hơn.

## 3. Mục tiêu kinh doanh

| ID mục tiêu | Mục tiêu kinh doanh | Thước đo thành công |
|---|---|---|
| BO-01 | Tập trung quản lý hồ sơ thực tập trong một hệ thống. | Nhân sự có thể quản lý tất cả các ứng viên từ một bảng điều khiển. |
| BO-02 | Giảm công việc theo dõi thủ công cho nhân sự. | Nhân sự sử dụng ít bảng tính và ghi chú thủ công hơn. |
| BO-03 | Cải thiện tính minh bạch về trạng thái ứng viên. | Ứng viên có thể xem trạng thái đơn đăng ký hiện tại của họ. |
| BO-04 | Chuẩn hóa phản hồi phỏng vấn. | Người phỏng vấn sử dụng một mẫu phản hồi có cấu trúc. |
| BO-05 | Cải thiện khả năng hiển thị quyết định tuyển dụng. | Người quản lý tuyển dụng có thể xem đường dẫn và phản hồi của ứng viên. |
| BO-06 | Cải thiện khả năng truy xuất nguồn gốc của quá trình tuyển dụng. | Lịch sử trạng thái và các hành động quan trọng được lưu trữ trong hệ thống. |

## 4. Yêu cầu kinh doanh

| ID yêu cầu | Yêu cầu kinh doanh | Ưu tiên | Chủ sở hữu |
|---|---|---|---|
| BR-01 | Hệ thống cho phép ứng viên nộp hồ sơ thực tập trực tuyến. | Phải | Nhà tuyển dụng nhân sự |
| BR-02 | Hệ thống cho phép ứng viên đăng tải CV và thông tin cá nhân. | Phải | Nhà tuyển dụng nhân sự |
| BR-03 | Hệ thống sẽ cho phép nhân sự xem và quản lý tất cả các đơn đăng ký đã gửi. | Phải | Nhà tuyển dụng nhân sự |
| BR-04 | Hệ thống sẽ cho phép HR cập nhật trạng thái tuyển dụng ứng viên. | Phải | Nhà tuyển dụng nhân sự |
| BR-05 | Hệ thống sẽ cho phép bộ phận nhân sự lên lịch phỏng vấn và phân công người phỏng vấn. | Phải | Nhà tuyển dụng nhân sự |
| BR-06 | Hệ thống sẽ cho phép người phỏng vấn xem các ứng viên được chỉ định. | Phải | Người phỏng vấn |
| BR-07 | Hệ thống sẽ cho phép người phỏng vấn gửi phản hồi phỏng vấn có cấu trúc. | Phải | Người phỏng vấn |
| BR-08 | Hệ thống sẽ cho phép người quản lý tuyển dụng xem quy trình tuyển dụng và phản hồi của ứng viên. | Nên | Quản lý tuyển dụng |
| BR-09 | Hệ thống sẽ thông báo cho thí sinh khi trạng thái hồ sơ của họ thay đổi. | Nên | Nhà tuyển dụng nhân sự |
| BR-10 | Hệ thống sẽ lưu trữ lịch sử trạng thái cho mục đích theo dõi và kiểm tra. | Phải | Nhà tuyển dụng nhân sự |
| BR-11 | Hệ thống sẽ hỗ trợ kiểm soát truy cập dựa trên vai trò cho các loại người dùng khác nhau. | Phải | Quản trị hệ thống |

## 5. Quy tắc kinh doanh

| ID quy tắc | Quy tắc kinh doanh |
|---|---|
| QUY TẮC-01 | Ứng viên không thể nộp đơn nếu không có thông tin cá nhân và CV cần thiết. |
| QUY TẮC-02 | Một ứng viên chỉ có thể xem trạng thái đơn đăng ký của chính họ. |
| QUY TẮC-03 | Chỉ HR Recruiter mới có thể cập nhật trạng thái tuyển dụng ứng viên. |
| QUY TẮC-04 | Chỉ Nhà tuyển dụng nhân sự mới có thể lên lịch phỏng vấn và phân công người phỏng vấn. |
| QUY TẮC-05 | Người phỏng vấn chỉ có thể xem các ứng viên được chỉ định cho họ. |
| QUY TẮC-06 | Phản hồi của người phỏng vấn là cần thiết trước khi đưa ra quyết định tuyển dụng cuối cùng. |
| QUY TẮC-07 | Mọi thay đổi trạng thái của ứng viên phải được ghi lại trạng thái cũ, trạng thái mới, được cập nhật bởi và thời gian cập nhật. |
| QUY TẮC-08 | Người quản lý tuyển dụng có thể xem danh sách ứng viên nhưng không thể chỉnh sửa trực tiếp thông tin hồ sơ ứng viên. |
| QUY TẮC-09 | Các ứng viên bị từ chối không thể được chuyển trực tiếp sang Được cung cấp mà không có sự chấp thuận của người quản lý nhân sự. |

## 6. Giả định

| ID giả định | Giả định |
|---|---|
| A-01 | Ứng viên sẽ nộp đơn thông qua hệ thống InternshipHub. |
| A-02 | HR Recruiter chịu trách nhiệm quản lý trạng thái ứng viên. |
| A-03 | Người phỏng vấn sẽ gửi phản hồi thông qua hệ thống sau khi phỏng vấn. |
| A-04 | Người quản lý tuyển dụng sẽ sử dụng thông tin bảng điều khiển để hỗ trợ các quyết định tuyển dụng. |
| A-05 | Email sẽ được sử dụng làm kênh thông báo chính. |

## 7. Ràng buộc

| ID ràng buộc | Ràng buộc |
|---|---|
| C-01 | Phiên bản đầu tiên của hệ thống chỉ nên tập trung vào quy trình tuyển dụng cốt lõi. |
| C-02 | Hệ thống không nên bao gồm sàng lọc CV dựa trên AI trong phiên bản đầu tiên. |
| C-03 | Hệ thống không được bao gồm các tính năng trả lương hoặc giới thiệu nhân viên. |
| C-04 | Dữ liệu cá nhân của ứng viên phải được bảo vệ bằng biện pháp kiểm soát truy cập dựa trên vai trò. |
| C-05 | Tải lên CV phải hỗ trợ các định dạng tài liệu phổ biến như PDF và DOCX. |

## 8. Thước đo thành công

| ID số liệu | Số liệu thành công | Mục tiêu |
|---|---|---|
| M-01 | Nỗ lực theo dõi bảng tính thủ công | Giảm 50% |
| M-02 | Tin nhắn hỏi thăm tình trạng ứng viên | Giảm 40% |
| M-03 | Tỷ lệ hoàn thành phản hồi phỏng vấn | Ít nhất 95% |
| M-04 | Thời gian trung bình từ khi nộp đơn đến khi sàng lọc | Giảm 30% |
| M-05 | Độ chính xác cập nhật trạng thái ứng viên | Ít nhất 95% |

## 9. Phạm vi

### Trong phạm vi

- Nộp hồ sơ ứng viên
- Tải hồ sơ ứng viên và CV
- Sàng lọc ứng viên nhân sự
- Quản lý trạng thái ứng viên
- Lên lịch phỏng vấn
- Gửi phản hồi của người phỏng vấn
- Tổng quan về quy trình tuyển dụng người quản lý
- Thông báo trạng thái ứng viên
- Theo dõi lịch sử trạng thái
- Kiểm soát truy cập dựa trên vai trò

### Ngoài phạm vi

- Sàng lọc CV dựa trên AI
- Kiểm tra mã hóa trực tuyến
- Quản lý tiền lương
- Tiếp nhận nhân viên
- Tích hợp với các hệ thống HRM bên ngoài
- Thực hiện đầy đủ ở cấp độ sản xuất

##10. BA Ghi chú

BRD này tập trung vào nhu cầu cấp độ doanh nghiệp chứ không phải chi tiết triển khai kỹ thuật.

Các yêu cầu kinh doanh quan trọng nhất là nộp đơn đăng ký ứng viên, quản lý trạng thái nhân sự, lên lịch phỏng vấn, phản hồi có cấu trúc và theo dõi trạng thái ứng viên.

Bước tiếp theo là chuyển các yêu cầu kinh doanh này thành các yêu cầu phần mềm chi tiết hơn trong tài liệu SRS.