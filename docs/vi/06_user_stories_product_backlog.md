#06. Câu chuyện của người dùng và tồn đọng sản phẩm

## 1. Mục đích

Tài liệu này chuyển đổi các yêu cầu phần mềm từ SRS thành câu chuyện của người dùng và sắp xếp chúng thành tồn đọng sản phẩm.

Việc tồn đọng sản phẩm giúp nhóm hiểu những gì nên xây dựng, ai cần từng tính năng, tại sao tính năng này có giá trị và tầm quan trọng của mỗi mục đối với lần phát hành đầu tiên của InternshipHub.

## 2. Phạm vi tồn đọng

Hồ sơ tồn đọng này bao gồm quy trình tuyển dụng cốt lõi của InternshipHub:

- Nộp hồ sơ ứng viên
- Theo dõi trạng thái ứng viên
- Quản lý ứng viên nhân sự
- Lên lịch phỏng vấn
- Phản hồi phỏng vấn
- Hỗ trợ quyết định tuyển dụng của người quản lý
- Kiểm soát quản trị và truy cập

## 3. Định dạng câu chuyện của người dùng

Tất cả các câu chuyện của người dùng đều tuân theo định dạng này:

```văn bản
Với tư cách là [vai trò người dùng], tôi muốn [mục tiêu], để có [giá trị doanh nghiệp].
```

Ví dụ:

```văn bản
Với tư cách là một ứng viên, tôi muốn xem trạng thái đơn đăng ký của mình để có thể biết tiến độ tuyển dụng của mình.
```

## 4. Phương pháp ưu tiên

Việc tồn đọng này sử dụng phương pháp ưu tiên MoSCoW.

| Ưu tiên | Ý nghĩa |
|---|---|
| Phải | Cần thiết cho phiên bản có thể sử dụng đầu tiên |
| Nên | Quan trọng nhưng có thể được phát hành sau các tính năng cốt lõi |
| Có thể | Rất vui nếu thời gian và nguồn lực cho phép |
| Sẽ không | Không có trong phiên bản này |

## 5. Danh sách sử thi

| ID sử thi | Tên sử thi | Mô tả |
|---|---|---|
| EP-01 | Hồ sơ ứng viên | Đăng ký ứng viên, đăng nhập, hồ sơ, tải lên CV và nộp hồ sơ |
| EP-02 | Theo dõi trạng thái ứng viên | Ứng viên xem trạng thái đơn đăng ký và nhận thông tin cập nhật |
| EP-03 | Quản lý ứng viên nhân sự | Chế độ xem, tìm kiếm, lọc, sàng lọc và cập nhật ứng viên về nhân sự |
| EP-04 | Lên lịch phỏng vấn | HR lên lịch phỏng vấn và phân công người phỏng vấn |
| EP-05 | Phản hồi phỏng vấn | Người phỏng vấn xem các ứng viên được chỉ định và gửi phản hồi có cấu trúc |
| EP-06 | Quyết định tuyển dụng | Người quản lý tuyển dụng xem xét quy trình, phản hồi và quyết định cuối cùng |
| EP-07 | Kiểm soát quản trị và truy cập | Quản trị viên quản lý người dùng, vai trò, chương trình và quyền |

## 6. Tồn đọng sản phẩm

### EP-01: Hồ sơ ứng tuyển

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-01 | Là ứng viên tôi muốn đăng ký tài khoản bằng email và mật khẩu để có thể truy cập vào hệ thống InternshipHub. | Phải | FR-01 | Bản nháp |
| Mỹ-02 | Là một ứng cử viên, tôi muốn đăng nhập và đăng xuất để có thể sử dụng tài khoản của mình một cách an toàn. | Phải | FR-02 | Bản nháp |
| Mỹ-03 | Là ứng viên, tôi muốn tạo và cập nhật hồ sơ cá nhân của mình để HR có thể xem xét thông tin của tôi. | Phải | FR-03 | Bản nháp |
| Mỹ-04 | Là ứng viên, tôi muốn tải CV của mình lên để HR có thể đánh giá hồ sơ của tôi. | Phải | FR-04, FR-05 | Bản nháp |
| Mỹ-05 | Với tư cách là một ứng viên, tôi muốn đăng ký một chương trình thực tập có sẵn để có thể được xem xét cho vị trí đó. | Phải | FR-06 | Bản nháp |
| Mỹ-06 | Với tư cách là một ứng cử viên, tôi muốn xem đơn đăng ký đã gửi của mình để có thể kiểm tra thông tin tôi đã cung cấp. | Phải | FR-07 | Bản nháp |

### EP-02: Theo dõi trạng thái ứng viên

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-07 | Với tư cách là một ứng viên, tôi muốn xem trạng thái đơn đăng ký hiện tại của mình để có thể biết tiến độ tuyển dụng của mình. | Phải | FR-08 | Bản nháp |
| Mỹ-08 | Là ứng viên, tôi muốn nhận được thông báo khi trạng thái đơn đăng ký của tôi thay đổi, để tôi không cần phải liên hệ với bộ phận nhân sự theo cách thủ công. | Nên | FR-09 | Bản nháp |
| Mỹ-09 | Là ứng viên, tôi muốn xem thông tin phỏng vấn khi có lịch phỏng vấn để có thể chuẩn bị kịp thời. | Nên | FR-17, FR-18 | Bản nháp |

### EP-03: Quản lý ứng viên nhân sự

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-10 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn xem tất cả các đơn đăng ký đã gửi để có thể quản lý ứng viên ở một nơi. | Phải | FR-10 | Bản nháp |
| Mỹ-11 | Là nhà tuyển dụng nhân sự, tôi muốn tìm kiếm ứng viên theo tên, email hoặc chương trình thực tập để có thể tìm được ứng viên một cách nhanh chóng. | Phải | FR-11 | Bản nháp |
| Mỹ-12 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn lọc ứng viên theo trạng thái, chương trình và ngày nộp đơn để có thể quản lý quy trình tuyển dụng một cách hiệu quả. | Phải | FR-12 | Bản nháp |
| Mỹ-13 | Là nhà tuyển dụng nhân sự, tôi muốn xem hồ sơ và CV ứng viên để sàng lọc ứng viên một cách chính xác. | Phải | FR-13 | Bản nháp |
| Mỹ-14 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn cập nhật trạng thái tuyển dụng ứng viên để nguồn ứng viên luôn chính xác. | Phải | FR-14 | Bản nháp |
| Mỹ-15 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn hệ thống xác thực các chuyển đổi trạng thái để ngăn chặn những thay đổi trạng thái tuyển dụng không hợp lệ. | Phải | FR-15 | Bản nháp |
| Mỹ-16 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn mọi thay đổi trạng thái đều được ghi lại để quá trình tuyển dụng có thể được theo dõi và kiểm tra. | Phải | FR-16 | Bản nháp |
| Mỹ-17 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn gửi kết quả tuyển dụng hoặc từ chối để ứng viên nhận được kết quả tuyển dụng chính thức. | Nên | FR-19 | Bản nháp |

### EP-04: Lên lịch phỏng vấn

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-18 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn đặt lịch phỏng vấn để những ứng viên được chọn có thể chuyển sang giai đoạn phỏng vấn. | Phải | FR-17 | Bản nháp |
| Mỹ-19 | Là một nhà tuyển dụng nhân sự, tôi muốn phân công người phỏng vấn cho các ứng viên, để mỗi cuộc phỏng vấn đều có một người đánh giá có trách nhiệm. | Phải | FR-18 | Bản nháp |
| Mỹ-20 | Với tư cách là nhà tuyển dụng nhân sự, tôi muốn những người phỏng vấn được chỉ định hiển thị chi tiết cuộc phỏng vấn để người phỏng vấn có thể chuẩn bị trước cuộc phỏng vấn. | Phải | FR-18, FR-20 | Bản nháp |

### EP-05: Phản hồi phỏng vấn

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-21 | Với tư cách là người phỏng vấn, tôi muốn xem các cuộc phỏng vấn được chỉ định của mình để biết mình cần phỏng vấn những ứng viên nào. | Phải | FR-20 | Bản nháp |
| Mỹ-22 | Với tư cách là người phỏng vấn, tôi muốn xem hồ sơ và CV ứng viên được giao để có thể chuẩn bị cho cuộc phỏng vấn. | Phải | FR-21 | Bản nháp |
| Mỹ-23 | Với tư cách là người phỏng vấn, tôi muốn gửi phản hồi phỏng vấn có cấu trúc để người quản lý nhân sự và tuyển dụng có thể đưa ra quyết định tốt hơn. | Phải | FR-22 | Bản nháp |
| Mỹ-24 | Với tư cách là người phỏng vấn, tôi muốn đưa ra đánh giá, nhận xét và đề xuất để phản hồi đó rõ ràng và hữu ích. | Phải | FR-23 | Bản nháp |
| Mỹ-25 | Với tư cách là người phỏng vấn, tôi muốn đề xuất Đạt, Không đạt hoặc Giữ để hành động tuyển dụng tiếp theo dễ dàng quyết định hơn. | Phải | FR-24 | Bản nháp |
| Mỹ-26 | Với tư cách là người phỏng vấn, tôi chỉ muốn truy cập những ứng viên được chỉ định cho mình để thông tin ứng viên được bảo mật. | Phải | FR-25 | Bản nháp |

### EP-06: Quyết định tuyển dụng

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-27 | Với tư cách là người quản lý tuyển dụng, tôi muốn xem quy trình tuyển dụng để có thể theo dõi tiến độ tuyển dụng. | Nên | FR-26 | Bản nháp |
| Mỹ-28 | Với tư cách là người quản lý tuyển dụng, tôi muốn xem phản hồi của ứng viên để có thể hiểu được đánh giá của người phỏng vấn. | Nên | FR-27 | Bản nháp |
| Mỹ-29 | Với tư cách là người quản lý tuyển dụng, tôi muốn so sánh các ứng viên theo trạng thái, xếp hạng và phản hồi để có thể đưa ra quyết định tuyển dụng tốt hơn. | Có thể | FR-28 | Bản nháp |
| Mỹ-30 | Với tư cách là người quản lý tuyển dụng, tôi muốn phê duyệt các quyết định tuyển dụng cuối cùng để các đề nghị tuyển dụng đó được kiểm soát trước khi gửi đi. | Nên | FR-29 | Bản nháp |

### EP-07: Kiểm soát quản trị và truy cập

| ID câu chuyện | Câu chuyện của người dùng | Ưu tiên | FR liên quan | Trạng thái |
|---|---|---|---|---|
| Mỹ-31 | Với tư cách là quản trị viên hệ thống, tôi muốn tạo, cập nhật và hủy kích hoạt tài khoản người dùng để có thể quản lý quyền truy cập hệ thống. | Phải | FR-30 | Bản nháp |
| Mỹ-32 | Với tư cách là quản trị viên hệ thống, tôi muốn chỉ định vai trò của người dùng để mỗi người dùng có quyền chính xác. | Phải | FR-31 | Bản nháp |
| Mỹ-33 | Với tư cách là quản trị viên hệ thống, tôi muốn tạo và cập nhật các chương trình thực tập để bộ phận nhân sự có thể quản lý các chiến dịch tuyển dụng khác nhau. | Nên | FR-32 | Bản nháp |
| Mỹ-34 | Với tư cách là quản trị viên hệ thống, tôi muốn xem nhật ký hoạt động của hệ thống để có thể kiểm tra các hành động quan trọng. | Nên | FR-33 | Bản nháp |

## 7. MVP tồn đọng

MVP chỉ nên bao gồm những tính năng quan trọng nhất cần thiết cho phiên bản có thể sử dụng đầu tiên.

| Khu vực MVP | Câu chuyện của người dùng đi kèm | Lý do |
|---|---|---|
| Hồ sơ ứng viên | US-01, US-02, US-03, US-04, US-05, US-06 | Ứng viên phải có khả năng tạo và gửi đơn đăng ký. |
| Theo dõi trạng thái ứng viên | Mỹ-07 | Ứng viên phải có khả năng nhìn thấy tiến trình nộp đơn. |
| Quản lý ứng viên nhân sự | US-10, US-11, US-12, US-13, US-14, US-15, US-16 | Nhân sự phải có khả năng quản lý quy trình tuyển dụng. |
| Lên lịch phỏng vấn | US-18, US-19, US-20 | Nhân sự phải có khả năng lên lịch phỏng vấn và phân công người phỏng vấn. |
| Phản hồi phỏng vấn | US-21, US-22, US-23, US-24, US-25, US-26 | Người phỏng vấn phải có khả năng đánh giá ứng viên. |
| Kiểm soát truy cập cơ bản | US-31, US-32 | Hệ thống phải bảo vệ thông tin ứng viên. |

## 8. Kế hoạch phát hành

| Phát hành | Mục tiêu | Câu chuyện của người dùng |
|---|---|---|
| Phát hành 1 | Quy trình tuyển dụng MVP | US-01 đến US-07, US-10 đến US-16, US-18 đến US-26, US-31, US-32 |
| Bản phát hành 2 | Thông báo ứng viên và thông báo kết quả | US-08, US-09, US-17 |
| Bản phát hành 3 | Bảng thông tin quản lý tuyển dụng và hỗ trợ ra quyết định | US-27, US-28, US-29, US-30 |
| Phát hành 4 | Cải thiện cấu hình quản trị và kiểm tra | US-33, US-34 |

## 9. Ghi chú phụ thuộc

| ID phụ thuộc | Phụ thuộc |
|---|---|
| DEP-01 | Ứng viên phải tạo một tài khoản trước khi nộp đơn. |
| DEP-02 | Ứng viên phải tải lên CV hợp lệ trước khi nộp hồ sơ. |
| DEP-03 | Bộ phận nhân sự phải sàng lọc ứng viên trước khi lên lịch phỏng vấn. |
| DEP-04 | Nhân sự phải chỉ định một người phỏng vấn trước khi có thể gửi phản hồi phỏng vấn. |
| DEP-05 | Phản hồi phỏng vấn phải được gửi trước khi có quyết định tuyển dụng cuối cùng. |
| DEP-06 | Vai trò của người dùng phải được cấu hình trước khi kiểm soát truy cập có thể hoạt động chính xác. |

##10. Định nghĩa sẵn sàng

Câu chuyện của người dùng đã sẵn sàng để phát triển khi:

| Tiêu chí | Mô tả |
|---|---|
| Xóa vai trò người dùng | Câu chuyện xác định ai cần tính năng này. |
| Mục tiêu rõ ràng | Câu chuyện giải thích những gì người dùng muốn làm. |
| Xóa giá trị | Câu chuyện giải thích tại sao tính năng này lại hữu ích. |
| Yêu cầu liên quan | Câu chuyện được liên kết với ít nhất một yêu cầu chức năng. |
| Tiêu chí chấp nhận | Truyện có tiêu chí chấp nhận rõ ràng. |
| Không có câu hỏi mở quan trọng | Sự mơ hồ quan trọng đã được làm rõ. |

## 11. Định nghĩa Hoàn thành

Một câu chuyện của người dùng được thực hiện khi:

| Tiêu chí | Mô tả |
|---|---|
| Tính năng được triển khai | Hành vi mong đợi được xây dựng. |
| Tiêu chí chấp nhận được thông qua | Tất cả các tiêu chí chấp nhận đều được thỏa mãn. |
| Xác thực được xử lý | Các quy tắc xác nhận bắt buộc được thực hiện. |
| Đã kiểm tra quyền | Kiểm soát truy cập hoạt động chính xác. |
| Được kiểm tra bởi QA | Kịch bản thử nghiệm được thông qua. |
| Được đánh giá bởi các bên liên quan | BA, Product Owner hoặc người dùng doanh nghiệp xác nhận kết quả. |

##12. BA Ghi chú

Câu chuyện của người dùng giúp BA truyền đạt các yêu cầu theo cách lấy người dùng làm trung tâm. Chúng giúp nhóm dễ dàng hiểu được ai cần tính năng này, người dùng muốn làm gì và tại sao tính năng này lại quan trọng.

Trong dự án này, các câu chuyện của người dùng có mức độ ưu tiên cao nhất liên quan đến hồ sơ ứng viên, quản lý ứng viên nhân sự, lên lịch phỏng vấn, phản hồi có cấu trúc và kiểm soát truy cập.

Bước tiếp theo là viết tiêu chí chấp nhận cho các câu chuyện của người dùng đã chọn để mỗi câu chuyện trở nên rõ ràng và có thể kiểm tra được.