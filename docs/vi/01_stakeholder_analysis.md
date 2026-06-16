#01. Phân tích các bên liên quan

## 1. Mục đích

Tài liệu này xác định các bên liên quan chính của hệ thống InternshipHub và giải thích vai trò, nhu cầu, tầm ảnh hưởng và sự tham gia của họ vào dự án.

Phân tích các bên liên quan giúp Nhà phân tích nghiệp vụ hiểu được ai sẽ sử dụng hệ thống, ai sẽ đưa ra quyết định, ai sẽ đưa ra yêu cầu và ai sẽ bị ảnh hưởng bởi giải pháp cuối cùng.

## 2. Danh sách các bên liên quan

| Các bên liên quan | Mô tả | Nhu cầu chính | Ảnh hưởng | Lãi suất |
|---|---|---|---|---|
| Ứng viên | Sinh viên hoặc sinh viên mới tốt nghiệp đăng ký chương trình thực tập. | Gửi hồ sơ, tải CV lên, theo dõi trạng thái hồ sơ, nhận thông tin cập nhật. | Thấp | Cao |
| Nhà tuyển dụng nhân sự | Người quản lý quá trình tuyển dụng. | Sàng lọc ứng viên, cập nhật trạng thái, lên lịch phỏng vấn, gửi kết quả. | Cao | Cao |
| Người phỏng vấn | Một thành viên nhóm kỹ thuật hoặc kinh doanh phỏng vấn ứng viên. | Xem hồ sơ ứng viên, xem xét CV, gửi phản hồi phỏng vấn. | Trung bình | Trung bình |
| Quản lý tuyển dụng | Người đưa ra hoặc phê duyệt quyết định tuyển dụng cuối cùng. | Xem quy trình tuyển dụng, so sánh ứng viên, phê duyệt quyết định. | Cao | Cao |
| Quản trị hệ thống | Người quản lý người dùng, vai trò và cấu hình hệ thống. | Quản lý tài khoản, quyền, chương trình thực tập và nhật ký hoạt động. | Trung bình | Trung bình |
| Nhà phát triển | Người xây dựng hệ thống dựa trên yêu cầu. | Nhận các yêu cầu chức năng và quy tắc kinh doanh rõ ràng. | Trung bình | Cao |
| Kỹ sư QA | Người kiểm tra chất lượng hệ thống. | Nhận các tiêu chí chấp nhận có thể kiểm chứng và các kịch bản kiểm thử. | Trung bình | Cao |

## 3. Mục tiêu của các bên liên quan

| Các bên liên quan | Mục tiêu |
|---|---|
| Ứng viên | Hoàn tất quy trình đăng ký một cách dễ dàng và biết được trạng thái hiện tại. |
| Nhà tuyển dụng nhân sự | Quản lý ứng viên hiệu quả và giảm bớt công việc theo dõi thủ công. |
| Người phỏng vấn | Đánh giá ứng viên bằng cách sử dụng mẫu phản hồi rõ ràng và có cấu trúc. |
| Quản lý tuyển dụng | Đưa ra quyết định tuyển dụng nhanh hơn và tốt hơn dựa trên dữ liệu quy trình. |
| Quản trị hệ thống | Đảm bảo hệ thống được an toàn và người dùng có quyền chính xác. |
| Nhà phát triển | Xây dựng các tính năng chính xác với ít thay đổi yêu cầu hơn. |
| Kỹ sư QA | Kiểm tra hệ thống dựa trên các quy tắc kinh doanh rõ ràng và kết quả mong đợi. |

## 4. Điểm đau của các bên liên quan

| Các bên liên quan | Điểm đau hiện tại |
|---|---|
| Ứng viên | Không biết hồ sơ đã được tiếp nhận, xét duyệt, từ chối hay được chuyển sang vòng tiếp theo. |
| Nhà tuyển dụng nhân sự | Cần theo dõi ứng viên theo cách thủ công bằng bảng tính, email và công cụ trò chuyện. |
| Người phỏng vấn | Có thể nhận thông tin ứng viên muộn hoặc ở định dạng không có cấu trúc. |
| Quản lý tuyển dụng | Không thể dễ dàng xem toàn bộ quy trình tuyển dụng và so sánh ứng viên. |
| Quản trị hệ thống | Cần kiểm soát quyền truy cập vào thông tin nhạy cảm của ứng viên. |
| Nhà phát triển | Có thể nhận được những yêu cầu không rõ ràng nếu quy trình kinh doanh không được ghi chép đầy đủ. |
| Kỹ sư QA | Có thể khó kiểm tra xem tiêu chí chấp nhận có bị thiếu hoặc mơ hồ hay không. |

##5. Ma trận RACI

RACI được sử dụng để làm rõ trách nhiệm trong một dự án.

- R = Chịu trách nhiệm: Người thực hiện công việc.
- A = Accountable: Người có quyết định cuối cùng.
- C = Được tư vấn: Người đưa ra ý kiến.
- I = Informed: Người cần cập nhật.

| Hoạt động | Ứng viên | Nhà tuyển dụng nhân sự | Người phỏng vấn | Quản lý tuyển dụng | Quản trị viên | Nhà phát triển | Kỹ sư QA |
|---|---|---|---|---|---|---|---|
| Nộp đơn | R | Tôi | Tôi | Tôi | Tôi | Tôi | Tôi |
| Sàng lọc CV | Tôi | R/A | Tôi | C | Tôi | Tôi | Tôi |
| Cập nhật trạng thái ứng viên | Tôi | R/A | Tôi | C | Tôi | Tôi | Tôi |
| Lên lịch phỏng vấn | Tôi | R/A | C | Tôi | Tôi | Tôi | Tôi |
| Tiến hành phỏng vấn | Tôi | C | R/A | Tôi | Tôi | Tôi | Tôi |
| Gửi phản hồi | Tôi | Tôi | R/A | C | Tôi | Tôi | Tôi |
| Đưa ra quyết định cuối cùng | Tôi | C | C | R/A | Tôi | Tôi | Tôi |
| Quản lý người dùng và vai trò | Tôi | C | Tôi | Tôi | R/A | Tôi | Tôi |
| Xây dựng tính năng hệ thống | Tôi | C | C | C | C | R/A | C |
| Kiểm tra tính năng hệ thống | Tôi | C | C | C | C | C | R/A |

## 6. Kế hoạch truyền thông với các bên liên quan

| Các bên liên quan | Phương thức giao tiếp | Tần số | Chủ đề chính |
|---|---|---|---|
| Nhà tuyển dụng nhân sự | Phỏng vấn / Hội thảo | Hàng tuần trong quá trình khám phá | Quy trình tuyển dụng, điểm yếu, quy tắc kinh doanh |
| Người phỏng vấn | Phỏng vấn ngắn | Một lần cho mỗi tính năng phản hồi | Luồng phỏng vấn, hình thức đánh giá, tiêu chí phản hồi |
| Quản lý tuyển dụng | Họp đánh giá | Tại cột mốc | Bảng điều khiển quy trình, quy trình ra quyết định, báo cáo |
| Ứng viên | Khảo sát / Đánh giá nguyên mẫu | Một lần trong quá trình xác nhận | Luồng ứng dụng, theo dõi trạng thái, thông báo |
| Nhà phát triển | Hướng dẫn yêu cầu | Mỗi lần chạy nước rút | Yêu cầu chức năng, quy tắc kinh doanh, trường hợp đặc biệt |
| Kỹ sư QA | Kiểm tra đánh giá | Mỗi lần chạy nước rút | Tiêu chí chấp nhận, kịch bản thử nghiệm, kết quả mong đợi |
| Quản trị viên | Phỏng vấn | Một lần trong quá trình khám phá | Vai trò, quyền, cấu hình hệ thống |

##7. BA Ghi chú

Bên liên quan quan trọng nhất trong dự án này là Nhà tuyển dụng nhân sự vì HR quản lý quy trình tuyển dụng chính. Tuy nhiên, trải nghiệm của Ứng viên cũng rất quan trọng vì một trong những mục tiêu kinh doanh là làm cho quy trình tuyển dụng trở nên minh bạch hơn.

BA nên hợp tác chặt chẽ với bộ phận nhân sự để hiểu quy trình hiện tại, sau đó xác nhận quy trình trong tương lai với người phỏng vấn và người quản lý tuyển dụng.