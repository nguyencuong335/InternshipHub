#09. Kịch bản thử nghiệm

## 1. Mục đích

Tài liệu này xác định các kịch bản thử nghiệm cho hệ thống InternshipHub.

Mục đích của các kịch bản thử nghiệm là giúp BA, Kỹ sư QA, Nhà phát triển và các bên liên quan xác minh rằng hành vi của hệ thống phù hợp với câu chuyện của người dùng, tiêu chí chấp nhận, quy tắc kinh doanh và yêu cầu phần mềm.

## 2. Phạm vi kịch bản thử nghiệm

Tài liệu này bao gồm các kịch bản thử nghiệm chính cho:

- Đăng ký và đăng nhập ứng viên
- Tải hồ sơ ứng viên và CV
- Nộp hồ sơ thực tập
- Theo dõi trạng thái ứng dụng
- Quản lý ứng viên nhân sự
- Cập nhật trạng thái ứng viên
- Lên lịch phỏng vấn
- Phản hồi phỏng vấn
- Bảng điều khiển quản lý tuyển dụng
- Quản lý người dùng và vai trò quản trị viên
- Quyền và kiểm soát truy cập

## 3. Định dạng kịch bản thử nghiệm

| Lĩnh vực | Mô tả |
|---|---|
| ID kiểm tra | ID kịch bản thử nghiệm duy nhất |
| Mô-đun | Khu chức năng đang được thử nghiệm |
| Kịch bản | Những gì cần được kiểm tra |
| Câu chuyện người dùng liên quan | Câu chuyện của người dùng được kết nối với kịch bản |
| Yêu cầu liên quan | Yêu cầu chức năng kết nối với kịch bản |
| Loại bài kiểm tra | Quy tắc Tích cực, Tiêu cực, Quyền, Xác thực hoặc Kinh doanh |
| Kết quả mong đợi | Hành vi dự kiến ​​của hệ thống |

## 4. Kịch bản thử nghiệm

---

## 4.1 Đăng ký và đăng nhập ứng viên

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-001 | Đăng ký ứng viên | Ứng viên đăng ký với thông tin bắt buộc hợp lệ. | Mỹ-01 | FR-01 | Tích cực | Tài khoản ứng viên được tạo thành công. |
| TC-002 | Đăng ký ứng viên | Ứng viên đăng ký bằng email đã tồn tại. | Mỹ-01 | FR-01 | Tiêu cực | Hệ thống hiện thông báo lỗi email đã được đăng ký. |
| TC-003 | Đăng ký ứng viên | Ứng viên để trống các trường bắt buộc trong quá trình đăng ký. | Mỹ-01 | FR-01 | Xác thực | Hệ thống hiển thị thông báo xác thực cho các trường bị thiếu. |
| TC-004 | Đăng nhập | Ứng viên đăng nhập đúng email và mật khẩu. | Mỹ-02 | FR-02 | Tích cực | Ứng viên đã đăng nhập và được chuyển hướng đến bảng điều khiển ứng viên. |
| TC-005 | Đăng nhập | Người dùng đăng nhập sai email hoặc mật khẩu. | Mỹ-02 | FR-02 | Tiêu cực | Hệ thống hiển thị thông báo đăng nhập không hợp lệ. |
| TC-006 | Đăng xuất | Người dùng đã đăng nhập nhấp vào đăng xuất. | Mỹ-02 | FR-02 | Tích cực | Người dùng đã đăng xuất và được chuyển hướng đến trang đăng nhập. |
| TC-007 | Đăng nhập | Người dùng đã bị vô hiệu hóa cố gắng đăng nhập. | Mỹ-02 | FR-02, FR-30 | Giấy phép | Hệ thống ngăn chặn đăng nhập. |

---

## 4.2 Tải lên Hồ sơ Ứng viên và CV

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-008 | Hồ sơ ứng viên | Ứng viên lưu hồ sơ với các thông tin yêu cầu hợp lệ. | Mỹ-03 | FR-03 | Tích cực | Hồ sơ được lưu thành công. |
| TC-009 | Hồ sơ ứng viên | Ứng viên để trống các trường hồ sơ bắt buộc. | Mỹ-03 | FR-03 | Xác thực | Hệ thống hiển thị thông báo xác nhận. |
| TC-010 | Hồ sơ ứng viên | Ứng viên cập nhật hồ sơ hiện có với dữ liệu hợp lệ. | Mỹ-03 | FR-03 | Tích cực | Thông tin hồ sơ cập nhật được lưu. |
| TC-011 | Tải lên CV | Ứng viên tải lên CV PDF hợp lệ có dung lượng dưới 5MB. | Mỹ-04 | FR-04, FR-05 | Tích cực | CV được tải lên thành công. |
| TC-012 | Tải lên CV | Ứng viên tải lên CV DOCX hợp lệ có dung lượng dưới 5MB. | Mỹ-04 | FR-04, FR-05 | Tích cực | CV được tải lên thành công. |
| TC-013 | Tải lên CV | Ứng viên tải lên loại tệp không được hỗ trợ. | Mỹ-04 | FR-05 | Tiêu cực | Hệ thống từ chối tệp và hiển thị các loại tệp được phép. |
| TC-014 | Tải lên CV | Ứng viên upload file CV lớn hơn 5MB. | Mỹ-04 | FR-05 | Xác thực | Hệ thống từ chối tệp và hiển thị giới hạn kích thước tệp. |
| TC-015 | Tải lên CV | Ứng viên thay thế CV hiện có trước khi nộp hồ sơ. | Mỹ-04 | FR-04 | Tích cực | CV cũ được thay thế bằng CV mới. |

---

##4.3 Nộp đơn xin thực tập

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-016 | Nộp hồ sơ | Ứng viên nộp hồ sơ đầy đủ hồ sơ và CV hợp lệ. | Mỹ-05 | FR-06 | Tích cực | Ứng dụng được tạo với trạng thái Đã gửi. |
| TC-017 | Nộp hồ sơ | Ứng viên nộp hồ sơ không kèm CV. | Mỹ-05 | FR-06 | Xác thực | Hệ thống ngăn chặn việc gửi và hiển thị thông báo yêu cầu CV. |
| TC-018 | Nộp hồ sơ | Ứng viên nộp hồ sơ không chọn chương trình thực tập. | Mỹ-05 | FR-06 | Xác thực | Hệ thống ngăn chặn việc gửi và hiển thị thông báo yêu cầu của chương trình. |
| TC-019 | Nộp hồ sơ | Ứng viên nộp đơn vào cùng một chương trình nhiều lần. | Mỹ-05 | FR-06 | Quy tắc kinh doanh | Hệ thống ngăn chặn ứng dụng trùng lặp. |
| TC-020 | Nộp hồ sơ | Ứng viên nộp đơn vào chương trình thực tập khép kín. | Mỹ-05 | FR-06 | Quy tắc kinh doanh | Hệ thống ngăn chặn việc gửi và hiển thị thông báo đã đóng chương trình. |
| TC-021 | Đơn đăng ký đã nộp | Ứng viên xem đơn đăng ký đã nộp của chính mình. | Mỹ-06 | FR-07 | Tích cực | Ứng viên có thể xem thông tin hồ sơ đã nộp. |
| TC-022 | Đơn đăng ký đã nộp | Ứng viên cố gắng xem đơn đăng ký đã nộp của ứng viên khác. | Mỹ-06 | FR-07, NFR-04 | Giấy phép | Hệ thống từ chối truy cập. |

---

## 4.4 Theo dõi trạng thái ứng viên

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-023 | Tình trạng đơn đăng ký | Ứng viên xem trạng thái đơn đăng ký hiện tại. | Mỹ-07 | FR-08 | Tích cực | Trạng thái ứng dụng hiện tại được hiển thị. |
| TC-024 | Tình trạng đơn đăng ký | Ứng viên xem tên chương trình và ngày nộp. | Mỹ-07 | FR-08 | Tích cực | Tên chương trình và ngày gửi được hiển thị. |
| TC-025 | Tình trạng đơn đăng ký | Ứng viên cố gắng xem trạng thái của ứng viên khác. | Mỹ-07 | FR-08, NFR-04 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-026 | Tình trạng đơn đăng ký | Ứng viên xem thông tin phỏng vấn sau khi lên lịch phỏng vấn. | Mỹ-09 | FR-17, FR-18 | Tích cực | Ngày, giờ phỏng vấn và thông tin cuộc họp được hiển thị. |
| TC-027 | Thông báo | Ứng viên nhận được thông báo sau khi cập nhật trạng thái nhân sự. | Mỹ-08 | FR-09 | Tích cực | Ứng viên nhận được thông báo cập nhật trạng thái. |
| TC-028 | Thông báo | Thông báo trạng thái không gửi được. | Mỹ-08 | FR-09 | Tiêu cực | Hệ thống ghi lại thông báo lỗi. |

---

##4.5 Quản lý ứng viên nhân sự

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-029 | Quản lý ứng viên | Nhân sự xem tất cả các ứng dụng đã gửi. | Mỹ-10 | FR-10 | Tích cực | Danh sách ứng viên được hiển thị. |
| TC-030 | Quản lý ứng viên | Nhân sự xem cột danh sách ứng viên. | Mỹ-10 | FR-10 | Tích cực | Tên ứng viên, email, chương trình, trạng thái và ngày nộp đơn được hiển thị. |
| TC-031 | Quản lý ứng viên | Người dùng trái phép cố gắng truy cập trang quản lý ứng viên. | Mỹ-10 | FR-10, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-032 | Tìm kiếm ứng viên | HR tìm kiếm ứng viên theo tên. | Mỹ-11 | FR-11 | Tích cực | Các ứng viên phù hợp sẽ được hiển thị. |
| TC-033 | Tìm kiếm ứng viên | HR tìm kiếm ứng viên qua email. | Mỹ-11 | FR-11 | Tích cực | Các ứng viên phù hợp sẽ được hiển thị. |
| TC-034 | Tìm kiếm ứng viên | Tìm kiếm nhân sự không có kết quả phù hợp. | Mỹ-11 | FR-11 | Tiêu cực | Hệ thống hiển thị thông báo kết quả trống. |
| TC-035 | Bộ Lọc Ứng Viên | Nhân sự lọc ứng viên theo trạng thái. | Mỹ-12 | FR-12 | Tích cực | Chỉ những ứng viên có trạng thái đã chọn mới được hiển thị. |
| TC-036 | Bộ Lọc Ứng Viên | Nhân sự lọc ứng viên theo chương trình thực tập. | Mỹ-12 | FR-12 | Tích cực | Chỉ những ứng viên trong chương trình đã chọn mới được hiển thị. |
| TC-037 | Bộ Lọc Ứng Viên | Nhân sự kết hợp các bộ lọc trạng thái, chương trình và ngày. | Mỹ-12 | FR-12 | Tích cực | Các ứng viên phù hợp với tất cả các bộ lọc sẽ được hiển thị. |
| TC-038 | Chi tiết Ứng viên | HR xem hồ sơ ứng viên và CV. | Mỹ-13 | FR-13 | Tích cực | Hồ sơ ứng viên và CV được hiển thị. |
| TC-039 | Chi tiết Ứng viên | Người dùng trái phép cố gắng xem chi tiết ứng viên. | Mỹ-13 | FR-13, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |

---

## 4.6 Cập nhật trạng thái ứng viên

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-040 | Cập nhật trạng thái | Nhân sự cập nhật trạng thái ứng viên từ Đã gửi đến Sàng lọc. | Mỹ-14 | FR-14, FR-15 | Tích cực | Trạng thái mới được lưu thành công. |
| TC-041 | Cập nhật trạng thái | Nhân sự cập nhật trạng thái bằng cách sử dụng chuyển đổi hợp lệ. | Mỹ-15 | FR-15 | Tích cực | Hệ thống chấp nhận chuyển đổi. |
| TC-042 | Cập nhật trạng thái | Trạng thái cập nhật nhân sự bằng cách sử dụng chuyển đổi không hợp lệ. | Mỹ-15 | FR-15 | Quy tắc kinh doanh | Hệ thống ngăn chặn cập nhật và hiển thị thông báo lỗi. |
| TC-043 | Cập nhật trạng thái | Bộ phận nhân sự cố gắng chuyển trực tiếp ứng viên từ Dự thảo sang Được đề xuất. | Mỹ-15 | FR-15 | Quy tắc kinh doanh | Hệ thống từ chối quá trình chuyển đổi. |
| TC-044 | Cập nhật trạng thái | Nhân sự cập nhật một ứng viên bị từ chối mà không cần phê duyệt. | Mỹ-15 | FR-15 | Quy tắc kinh doanh | Hệ thống ngăn chặn cập nhật. |
| TC-045 | Lịch sử trạng thái | HR cập nhật trạng thái ứng viên thành công. | Mỹ-16 | FR-16 | Tích cực | Trạng thái cũ, trạng thái mới, người cập nhật và thời gian cập nhật đều được ghi lại. |
| TC-046 | Lịch sử trạng thái | Nhân sự xem lịch sử trạng thái trên trang chi tiết ứng viên. | Mỹ-16 | FR-16 | Tích cực | Lịch sử trạng thái được hiển thị. |
| TC-047 | Lịch sử trạng thái | Cập nhật trạng thái không thành công. | Mỹ-16 | FR-16 | Tiêu cực | Bản ghi lịch sử trạng thái không chính xác không được tạo. |
| TC-048 | Cập nhật trạng thái | Trạng thái xem ứng viên sau khi cập nhật nhân sự. | Mỹ-14 | FR-14, FR-08 | Tích cực | Ứng viên nhìn thấy trạng thái mới nhất. |

---

##4.7 Lên lịch phỏng vấn

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-049 | Lên lịch phỏng vấn | Nhân sự lên lịch phỏng vấn với ứng viên hợp lệ, người phỏng vấn, ngày, giờ và thông tin cuộc họp. | Mỹ-18 | FR-17 | Tích cực | Lịch phỏng vấn được tạo thành công. |
| TC-050 | Lên lịch phỏng vấn | Nhân sự lên lịch phỏng vấn mà không chọn người phỏng vấn. | Mỹ-18 | FR-17 | Xác thực | Hệ thống ngăn chặn việc lập kế hoạch và hiển thị thông báo trường bắt buộc. |
| TC-051 | Lên lịch phỏng vấn | Nhân sự lên lịch phỏng vấn cho ứng viên không ở trạng thái Sàng lọc. | Mỹ-18 | FR-17, FR-15 | Quy tắc kinh doanh | Hệ thống ngăn chặn việc lập lịch và hiển thị thông báo trạng thái không hợp lệ. |
| TC-052 | Lên lịch phỏng vấn | Cuộc phỏng vấn được lên lịch thành công. | Mỹ-18 | FR-17 | Tích cực | Trạng thái ứng viên thay đổi thành Đã lên lịch phỏng vấn. |
| TC-053 | Bài tập phỏng vấn | HR phân công người phỏng vấn cho ứng viên. | Mỹ-19 | FR-18 | Tích cực | Người phỏng vấn có thể xem cuộc phỏng vấn được chỉ định. |
| TC-054 | Bài tập phỏng vấn | Nhân sự thay đổi người phỏng vấn được phân công. | Mỹ-19 | FR-18 | Tích cực | Người phỏng vấn cũ mất quyền truy cập và người phỏng vấn mới có quyền truy cập. |
| TC-055 | Bài tập phỏng vấn | Người dùng không phải nhân sự cố gắng chỉ định người phỏng vấn. | Mỹ-19 | FR-18, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-056 | Chi tiết Phỏng vấn | Người phỏng vấn được chỉ định xem chi tiết cuộc phỏng vấn. | Mỹ-20 | FR-20 | Tích cực | Chi tiết phỏng vấn được hiển thị. |

---

## 4.8 Bảng điều khiển và phản hồi của người phỏng vấn

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-057 | Bảng điều khiển dành cho người phỏng vấn | Người phỏng vấn xem các cuộc phỏng vấn được chỉ định. | Mỹ-21 | FR-20 | Tích cực | Chỉ các cuộc phỏng vấn được chỉ định mới được hiển thị. |
| TC-058 | Bảng điều khiển dành cho người phỏng vấn | Người phỏng vấn xem chi tiết cuộc phỏng vấn. | Mỹ-21 | FR-20 | Tích cực | Tên ứng viên, chương trình, ngày, giờ và thông tin cuộc họp được hiển thị. |
| TC-059 | Bảng điều khiển dành cho người phỏng vấn | Người phỏng vấn cố gắng xem cuộc phỏng vấn được giao cho người phỏng vấn khác. | Mỹ-21 | FR-20, NFR-05 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-060 | Hồ sơ ứng viên | Người phỏng vấn được phân công xem hồ sơ ứng viên và CV. | Mỹ-22 | FR-21 | Tích cực | Hồ sơ ứng viên và CV được hiển thị. |
| TC-061 | Hồ sơ ứng viên | Người phỏng vấn chưa được chỉ định cố gắng xem hồ sơ và CV của ứng viên. | Mỹ-22 | FR-21, NFR-05 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-062 | Mẫu phản hồi | Người phỏng vấn được chỉ định gửi phản hồi có cấu trúc đầy đủ. | Mỹ-23 | FR-22, FR-23 | Tích cực | Phản hồi được lưu thành công. |
| TC-063 | Mẫu phản hồi | Người phỏng vấn gửi phản hồi mà không cần đánh giá theo yêu cầu. | Mỹ-23 | FR-23 | Xác thực | Hệ thống ngăn chặn việc gửi và hiển thị thông báo xác thực. |
| TC-064 | Mẫu phản hồi | Người phỏng vấn gửi phản hồi mà không có khuyến nghị. | Mỹ-25 | FR-24 | Xác thực | Hệ thống ngăn chặn việc gửi và hiển thị thông báo yêu cầu đề xuất. |
| TC-065 | Mẫu phản hồi | Người phỏng vấn chưa được chỉ định cố gắng gửi phản hồi. | Mỹ-23 | FR-22, NFR-05 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-066 | Hiển thị phản hồi | Nhân sự xem phản hồi sau khi gửi thành công. | Mỹ-23 | FR-22 | Tích cực | Phản hồi đã gửi sẽ được hiển thị cho bộ phận nhân sự. |
| TC-067 | Khuyến nghị | Người phỏng vấn chọn Đạt đề xuất. | Mỹ-25 | FR-24 | Tích cực | Đề xuất vượt qua được lưu. |
| TC-068 | Khuyến nghị | Người phỏng vấn chọn đề xuất Thất bại. | Mỹ-25 | FR-24 | Tích cực | Đề xuất không thành công đã được lưu. |
| TC-069 | Khuyến nghị | Người phỏng vấn chọn Giữ khuyến nghị. | Mỹ-25 | FR-24 | Tích cực | Giữ khuyến nghị đã được lưu. |

---

## 4.9 Bảng điều khiển và quyết định của người quản lý tuyển dụng

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-070 | Bảng điều khiển đường ống | Người quản lý tuyển dụng xem số lượng ứng viên theo trạng thái. | Mỹ-27 | FR-26 | Tích cực | Số lượng ứng viên theo trạng thái được hiển thị. |
| TC-071 | Bảng điều khiển đường ống | Người quản lý tuyển dụng xem các ứng viên được nhóm theo chương trình thực tập. | Mỹ-27 | FR-26 | Tích cực | Các ứng viên được nhóm theo chương trình. |
| TC-072 | Bảng điều khiển đường ống | Người dùng trái phép truy cập vào bảng thông tin quy trình. | Mỹ-27 | FR-26, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-073 | Phản hồi của ứng viên | Quan điểm của người quản lý tuyển dụng đã gửi phản hồi phỏng vấn. | Mỹ-28 | FR-27 | Tích cực | Phản hồi của ứng viên được hiển thị. |
| TC-074 | Phản hồi của ứng viên | Người quản lý tuyển dụng mở thông tin chi tiết về ứng viên mà không có phản hồi nào được gửi. | Mỹ-28 | FR-27 | Tiêu cực | Hệ thống hiển thị chưa có phản hồi. |
| TC-075 | So Sánh Ứng Viên | Người quản lý tuyển dụng so sánh ít nhất hai ứng viên. | Mỹ-29 | FR-28 | Tích cực | So sánh ứng viên được hiển thị cạnh nhau. |
| TC-076 | So Sánh Ứng Viên | Người quản lý tuyển dụng so sánh ít hơn hai ứng viên. | Mỹ-29 | FR-28 | Xác thực | Hệ thống yêu cầu người dùng chọn ít nhất hai ứng viên. |
| TC-077 | Quyết định cuối cùng | Người quản lý tuyển dụng phê duyệt quyết định đề nghị cuối cùng. | Mỹ-30 | FR-29 | Tích cực | Phê duyệt được ghi lại thành công. |
| TC-078 | Quyết định cuối cùng | Người quản lý không tuyển dụng cố gắng phê duyệt quyết định cuối cùng. | Mỹ-30 | FR-29, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |

---

## 4.10 Kiểm soát quản trị và truy cập

| ID kiểm tra | Mô-đun | Kịch bản | Câu chuyện người dùng liên quan | Yêu cầu liên quan | Loại bài kiểm tra | Kết quả mong đợi |
|---|---|---|---|---|---|---|
| TC-079 | Quản lý người dùng | Quản trị viên tạo một tài khoản người dùng mới với thông tin hợp lệ. | Mỹ-31 | FR-30 | Tích cực | Tài khoản người dùng được tạo thành công. |
| TC-080 | Quản lý người dùng | Quản trị viên cập nhật thông tin người dùng. | Mỹ-31 | FR-30 | Tích cực | Thông tin người dùng cập nhật được lưu. |
| TC-081 | Quản lý người dùng | Quản trị viên vô hiệu hóa tài khoản người dùng. | Mỹ-31 | FR-30 | Tích cực | Người dùng không thể đăng nhập được nữa. |
| TC-082 | Quản lý người dùng | Người dùng không phải quản trị viên cố gắng quản lý tài khoản người dùng. | Mỹ-31 | FR-30, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-083 | Quản lý vai trò | Quản trị viên chỉ định vai trò cho người dùng. | Mỹ-32 | FR-31 | Tích cực | Người dùng nhận được quyền của vai trò được giao. |
| TC-084 | Quản lý vai trò | Quản trị viên thay đổi vai trò của người dùng. | Mỹ-32 | FR-31 | Tích cực | Quyền của người dùng được cập nhật dựa trên vai trò mới. |
| TC-085 | Quản lý vai trò | Người dùng không phải quản trị viên cố gắng chỉ định vai trò. | Mỹ-32 | FR-31, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |
| TC-086 | Quản lý chương trình | Quản trị viên tạo ra một chương trình thực tập với thông tin hợp lệ. | Mỹ-33 | FR-32 | Tích cực | Chương trình thực tập được tạo thành công. |
| TC-087 | Quản lý chương trình | Admin cập nhật chương trình thực tập. | Mỹ-33 | FR-32 | Tích cực | Thông tin chương trình được cập nhật thành công. |
| TC-088 | Quản lý chương trình | Ứng viên nộp đơn vào chương trình thực tập khép kín. | Mỹ-33 | FR-32 | Quy tắc kinh doanh | Hệ thống ngăn chặn việc nộp đơn. |
| TC-089 | Nhật ký hoạt động | Quản trị viên xem trang nhật ký hoạt động. | Mỹ-34 | FR-33 | Tích cực | Các hành động quan trọng của hệ thống được hiển thị. |
| TC-090 | Nhật ký hoạt động | Nhân sự cập nhật trạng thái ứng viên. | Mỹ-34 | FR-33, NFR-06 | Tích cực | Hành động cập nhật trạng thái được ghi lại trong nhật ký hoạt động. |
| TC-091 | Nhật ký hoạt động | Người dùng không phải quản trị viên cố gắng truy cập nhật ký hoạt động. | Mỹ-34 | FR-33, NFR-03 | Giấy phép | Hệ thống từ chối truy cập. |

---

## 5. Kịch bản kiểm tra mức độ ưu tiên cao cho MVP

Các kịch bản kiểm thử sau đây cần được kiểm thử trước tiên vì chúng bao gồm quy trình làm việc cốt lõi của MVP.

| Ưu tiên | ID kiểm tra | Lý do |
|---|---|---|
| Cao | TC-001 | Cần phải đăng ký ứng viên trước khi nộp đơn. |
| Cao | TC-004 | Đăng nhập là cần thiết cho tất cả các tính năng được bảo vệ. |
| Cao | TC-011 | Cần phải tải lên CV để nộp đơn. |
| Cao | TC-016 | Nộp đơn đăng ký là quy trình làm việc cốt lõi của ứng viên. |
| Cao | TC-023 | Theo dõi trạng thái ứng viên là mục tiêu kinh doanh quan trọng. |
| Cao | TC-029 | Nhân sự phải quản lý tất cả các hồ sơ đã nộp. |
| Cao | TC-040 | Cập nhật trạng thái nhân sự là quy trình tuyển dụng cốt lõi. |
| Cao | TC-045 | Lịch sử trạng thái là cần thiết để truy xuất nguồn gốc. |
| Cao | TC-049 | Lập kế hoạch phỏng vấn là cần thiết cho quy trình phỏng vấn. |
| Cao | TC-057 | Người phỏng vấn phải xem các cuộc phỏng vấn được chỉ định. |
| Cao | TC-062 | Phản hồi có cấu trúc là cần thiết cho quyết định tuyển dụng. |
| Cao | TC-079 | Tạo người dùng quản trị hỗ trợ kiểm soát truy cập. |
| Cao | TC-083 | Phân công vai trò hỗ trợ kiểm soát quyền. |

## 6. Luồng thử nghiệm từ đầu đến cuối

Quy trình này kiểm tra xem quy trình tuyển dụng chính có hoạt động từ đầu đến cuối hay không.

| Bước | Diễn viên | Hành động | Kết quả mong đợi |
|---|---|---|---|
| 1 | Ứng viên | Đăng ký tài khoản | Tài khoản ứng viên được tạo. |
| 2 | Ứng viên | Hoàn thiện hồ sơ và upload CV | Hồ sơ và CV được lưu lại. |
| 3 | Ứng viên | Nộp đơn xin thực tập | Trạng thái đơn đăng ký trở thành Đã gửi. |
| 4 | Nhà tuyển dụng nhân sự | Xem đơn đăng ký đã gửi | Ứng viên xuất hiện trong danh sách quản lý ứng viên. |
| 5 | Nhà tuyển dụng nhân sự | Cập nhật trạng thái sàng lọc | Trạng thái ứng viên được cập nhật và ghi lại. |
| 6 | Nhà tuyển dụng nhân sự | Lên lịch phỏng vấn và phân công người phỏng vấn | Cuộc phỏng vấn được tạo và trạng thái ứng viên trở thành Đã lên lịch phỏng vấn. |
| 7 | Người phỏng vấn | Xem cuộc phỏng vấn được chỉ định | Cuộc phỏng vấn xuất hiện trong bảng điều khiển của người phỏng vấn. |
| 8 | Người phỏng vấn | Gửi phản hồi có cấu trúc | Phản hồi được lưu thành công. |
| 9 | Quản lý tuyển dụng | Xem quy trình và phản hồi | Phản hồi của ứng viên có thể được nhìn thấy. |
| 10 | Quản lý tuyển dụng | Phê duyệt quyết định cuối cùng | Quyết định phê duyệt được lưu. |
| 11 | Nhà tuyển dụng nhân sự | Gửi kết quả cuối cùng | Thí sinh nhận được thông báo kết quả cuối cùng. |
| 12 | Ứng viên | Xem trạng thái cuối cùng | Trạng thái cuối cùng được hiển thị chính xác. |

## 7. Danh sách kiểm tra chất lượng kịch bản thử nghiệm

| Mục danh sách kiểm tra | Mô tả |
|---|---|
| Liên kết với yêu cầu | Mỗi kịch bản thử nghiệm ánh xạ tới câu chuyện của người dùng và yêu cầu chức năng. |
| Kết quả mong đợi rõ ràng | Mỗi kịch bản có một hành vi hệ thống được mong đợi rõ ràng. |
| Bao gồm các trường hợp tích cực | Bao gồm các luồng thành công thông thường. |
| Bao gồm các trường hợp tiêu cực | Các hành động không hợp lệ và các trường hợp thất bại được bao gồm. |
| Bao gồm các quy tắc xác nhận | Bao gồm các trường bắt buộc, loại tệp, kích thước tệp và quy tắc trùng lặp. |
| Bao gồm các quy tắc cấp phép | Kiểm soát truy cập và hạn chế dựa trên vai trò được bao gồm. |
| Bao gồm các quy tắc kinh doanh | Chuyển đổi trạng thái, chương trình đóng và quy tắc quyết định cuối cùng được bao gồm. |
| Hỗ trợ thử nghiệm MVP | Các kịch bản thử nghiệm có mức độ ưu tiên cao được xác định. |

##8. BA Ghi chú

Các kịch bản kiểm thử rất quan trọng vì chúng giúp xác nhận rằng các yêu cầu có thể kiểm thử được.

Trong một dự án thực tế, BA làm việc với QA để đảm bảo rằng từng yêu cầu kinh doanh, yêu cầu chức năng, câu chuyện của người dùng và tiêu chí chấp nhận đều có thể được xác minh thông qua thử nghiệm.

Bước tiếp theo là tạo Ma trận truy xuất nguồn gốc yêu cầu để kết nối các yêu cầu kinh doanh, yêu cầu chức năng, câu chuyện của người dùng, tiêu chí chấp nhận và kịch bản thử nghiệm.