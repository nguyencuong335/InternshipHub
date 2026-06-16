#05. Đặc tả yêu cầu phần mềm

## 1. Mục đích

Tài liệu này mô tả các yêu cầu phần mềm đối với hệ thống InternshipHub.

Mục đích của SRS này là chuyển đổi các yêu cầu kinh doanh thành các yêu cầu chức năng rõ ràng, yêu cầu phi chức năng, vai trò của người dùng, quy tắc xác thực và hành vi của hệ thống.

Tài liệu này giúp các nhà phát triển hiểu những gì cần xây dựng và giúp các kỹ sư QA hiểu những gì cần kiểm tra.

## 2. Phạm vi sản phẩm

InternshipHub là một hệ thống quản lý tuyển dụng thực tập sinh dựa trên web.

Hệ thống hỗ trợ ứng viên, nhà tuyển dụng nhân sự, người phỏng vấn, người quản lý tuyển dụng và quản trị hệ thống trong việc quản lý quy trình nộp đơn thực tập từ khi nộp đơn đến quyết định tuyển dụng cuối cùng.

## 3. Vai trò của người dùng

| Vai trò | Mô tả |
|---|---|
| Ứng viên | Người dùng đăng ký các chương trình thực tập và theo dõi trạng thái đơn đăng ký. |
| Nhà tuyển dụng nhân sự | Người dùng quản lý hồ sơ, sàng lọc ứng viên, lên lịch phỏng vấn và cập nhật trạng thái ứng viên. |
| Người phỏng vấn | Người dùng đánh giá các ứng viên được chỉ định và gửi phản hồi phỏng vấn. |
| Quản lý tuyển dụng | Người dùng xem xét hệ thống ứng viên và phê duyệt các quyết định tuyển dụng cuối cùng. |
| Quản trị hệ thống | Người dùng quản lý người dùng hệ thống, vai trò, quyền và chương trình thực tập. |

## 4. Yêu cầu chức năng

### 4.1 Mô-đun ứng viên

| ID yêu cầu | Yêu cầu chức năng | Ưu tiên |
|---|---|---|
| FR-01 | Hệ thống cho phép thí sinh đăng ký tài khoản bằng email và mật khẩu. | Phải |
| FR-02 | Hệ thống sẽ cho phép thí sinh đăng nhập và đăng xuất. | Phải |
| FR-03 | Hệ thống cho phép ứng viên tạo và cập nhật hồ sơ cá nhân của mình. | Phải |
| FR-04 | Hệ thống cho phép ứng viên upload file CV. | Phải |
| FR-05 | Hệ thống sẽ xác nhận loại tệp CV và kích thước tệp. | Phải |
| FR-06 | Hệ thống sẽ cho phép ứng viên đăng ký một chương trình thực tập có sẵn. | Phải |
| FR-07 | Hệ thống sẽ cho phép thí sinh xem hồ sơ đã nộp của mình. | Phải |
| FR-08 | Hệ thống sẽ cho phép ứng viên xem trạng thái đơn đăng ký hiện tại của họ. | Phải |
| FR-09 | Hệ thống sẽ thông báo cho thí sinh khi trạng thái hồ sơ của họ thay đổi. | Nên |

### 4.2 Module tuyển dụng nhân sự

| ID yêu cầu | Yêu cầu chức năng | Ưu tiên |
|---|---|---|
| FR-10 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự xem tất cả các hồ sơ đã nộp. | Phải |
| FR-11 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự tìm kiếm ứng viên theo tên, email hoặc chương trình thực tập. | Phải |
| FR-12 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự lọc ứng viên theo trạng thái, chương trình và ngày nộp đơn. | Phải |
| FR-13 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự xem hồ sơ và CV của ứng viên. | Phải |
| FR-14 | Hệ thống cho phép nhà tuyển dụng nhân sự cập nhật tình trạng tuyển dụng ứng viên. | Phải |
| FR-15 | Hệ thống sẽ xác nhận việc chuyển đổi trạng thái ứng viên. | Phải |
| FR-16 | Hệ thống sẽ ghi lại mọi thay đổi trạng thái của ứng viên. | Phải |
| FR-17 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự lên lịch phỏng vấn. | Phải |
| FR-18 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự phân công người phỏng vấn cho ứng viên. | Phải |
| FR-19 | Hệ thống sẽ cho phép nhà tuyển dụng nhân sự gửi kết quả đề nghị hoặc từ chối. | Nên |

### 4.3 Mô-đun Người phỏng vấn

| ID yêu cầu | Yêu cầu chức năng | Ưu tiên |
|---|---|---|
| FR-20 | Hệ thống sẽ cho phép người phỏng vấn xem các cuộc phỏng vấn được chỉ định của họ. | Phải |
| FR-21 | Hệ thống cho phép người phỏng vấn xem hồ sơ và CV ứng viên được phân công. | Phải |
| FR-22 | Hệ thống sẽ cho phép người phỏng vấn gửi phản hồi phỏng vấn có cấu trúc. | Phải |
| FR-23 | Hệ thống sẽ yêu cầu người phỏng vấn đưa ra đánh giá, nhận xét và đề xuất. | Phải |
| FR-24 | Hệ thống sẽ cho phép người phỏng vấn đề xuất Đạt, Không đạt hoặc Giữ. | Phải |
| FR-25 | Hệ thống sẽ ngăn người phỏng vấn xem các ứng viên không được phân công. | Phải |

### 4.4 Mô-đun quản lý tuyển dụng

| ID yêu cầu | Yêu cầu chức năng | Ưu tiên |
|---|---|---|
| FR-26 | Hệ thống sẽ cho phép người quản lý tuyển dụng xem quy trình tuyển dụng. | Nên |
| FR-27 | Hệ thống sẽ cho phép người quản lý tuyển dụng xem phản hồi của ứng viên. | Nên |
| FR-28 | Hệ thống sẽ cho phép người quản lý tuyển dụng so sánh các ứng viên theo trạng thái, xếp hạng và phản hồi. | Có thể |
| FR-29 | Hệ thống sẽ cho phép người quản lý tuyển dụng phê duyệt các quyết định tuyển dụng cuối cùng. | Nên |

### 4.5 Mô-đun quản trị

| ID yêu cầu | Yêu cầu chức năng | Ưu tiên |
|---|---|---|
| FR-30 | Hệ thống sẽ cho phép quản trị viên tạo, cập nhật và hủy kích hoạt tài khoản người dùng. | Phải |
| FR-31 | Hệ thống sẽ cho phép quản trị viên phân công vai trò người dùng. | Phải |
| FR-32 | Hệ thống cho phép quản trị viên tạo và cập nhật các chương trình thực tập. | Nên |
| FR-33 | Hệ thống sẽ cho phép quản trị viên xem nhật ký hoạt động của hệ thống. | Nên |

## 5. Yêu cầu phi chức năng

| ID yêu cầu | Yêu cầu phi chức năng | Danh mục | Ưu tiên |
|---|---|---|---|
| NFR-01 | Hệ thống sẽ tải danh sách ứng viên trong vòng 3 giây cho tối đa 1.000 bản ghi. | Hiệu suất | Nên |
| NFR-02 | Hệ thống sẽ yêu cầu xác thực trước khi người dùng truy cập các trang được bảo vệ. | An ninh | Phải |
| NFR-03 | Hệ thống sẽ hạn chế quyền truy cập dữ liệu dựa trên vai trò của người dùng. | An ninh | Phải |
| NFR-04 | Ứng viên chỉ có thể xem thông tin ứng tuyển của chính mình. | An ninh | Phải |
| NFR-05 | Người phỏng vấn chỉ có thể xem các ứng viên được chỉ định cho họ. | An ninh | Phải |
| NFR-06 | Hệ thống sẽ ghi lại các hành động quan trọng như cập nhật trạng thái, lên lịch phỏng vấn và gửi phản hồi. | Kiểm toán | Phải |
| NFR-07 | Hệ thống phải khả dụng 99% trong thời gian tuyển dụng. | Sẵn có | Nên |
| NFR-08 | Giao diện người dùng hệ thống sẽ hoạt động trên trình duyệt máy tính để bàn và thiết bị di động. | Khả năng sử dụng | Nên |
| NFR-09 | Tải lên CV phải hỗ trợ các tệp PDF và DOCX. | Khả năng tương thích | Phải |
| NFR-10 | Hệ thống sẽ hiển thị thông báo xác thực rõ ràng khi dữ liệu nhập của người dùng không hợp lệ. | Khả năng sử dụng | Phải |

## 6. Yêu cầu về dữ liệu

### 6.1 Dữ liệu hồ sơ ứng viên

| Lĩnh vực | Bắt buộc | Mô tả |
|---|---|---|
| Tên đầy đủ | Có | Họ và tên ứng viên |
| Email | Có | Địa chỉ email của ứng viên |
| Số điện thoại | Có | Số liên lạc của ứng viên |
| Đại học | Có | Ứng viên đại học |
| Thiếu tá | Có | Ứng viên chuyên ngành |
| Năm tốt nghiệp | Không | Năm tốt nghiệp dự kiến ​​|
| Tệp CV | Có | File CV ứng viên |
| Liên kết danh mục đầu tư | Không | GitHub, LinkedIn hoặc trang web cá nhân |
| Chương trình ứng dụng | Có | Chương trình thực tập do ứng viên lựa chọn |

### 6.2 Dữ liệu ứng dụng

| Lĩnh vực | Bắt buộc | Mô tả |
|---|---|---|
| ID ứng dụng | Có | Mã định danh ứng dụng duy nhất |
| ID ứng viên | Có | Ứng viên được liên kết với ứng dụng |
| ID chương trình | Có | Chương trình thực tập |
| Tình trạng đơn đăng ký | Có | Tình trạng tuyển dụng hiện tại |
| Ngày nộp đơn | Có | Ngày ứng viên nộp hồ sơ |
| Ngày cập nhật lần cuối | Có | Lần cập nhật trạng thái cuối cùng |
| Cập nhật bởi | Có | Người dùng đã cập nhật ứng dụng |

### 6.3 Dữ liệu phản hồi phỏng vấn

| Lĩnh vực | Bắt buộc | Mô tả |
|---|---|---|
| ID phỏng vấn | Có | Mã định danh phỏng vấn duy nhất |
| ID ứng viên | Có | Ứng viên đang được phỏng vấn |
| ID người phỏng vấn | Có | Người phỏng vấn được chỉ định |
| Đánh giá kỹ thuật | Có | Điểm đánh giá kỹ thuật |
| Đánh giá truyền thông | Có | Điểm đánh giá truyền thông |
| Điểm mạnh | Có | Điểm mạnh của ứng viên |
| Điểm yếu | Có | Điểm yếu của ứng viên |
| Khuyến nghị | Có | Đạt, Thất bại hoặc Giữ |
| Bình luận | Không | Ý kiến ​​bổ sung của người phỏng vấn |

## 7. Luồng trạng thái ứng viên

Hệ thống sẽ hỗ trợ luồng trạng thái ứng viên sau:

```văn bản
Bản nháp → Đã gửi → Sàng lọc → Lên lịch phỏng vấn → Đã hoàn thành phỏng vấn → Được đề nghị
                                                               ↘ Bị từ chối
                                                               ↘ Giữ
```

## 8. Quy tắc chuyển trạng thái

| Tình trạng hiện tại | Trạng thái tiếp theo được phép |
|---|---|
| Bản nháp | Đã gửi |
| Đã gửi | Sàng lọc, Bị từ chối |
| Sàng lọc | Lên lịch phỏng vấn, bị từ chối |
| Đã lên lịch phỏng vấn | Cuộc phỏng vấn đã hoàn thành, bị từ chối |
| Đã Hoàn Thành Phỏng Vấn | Được cung cấp, Từ chối, Giữ |
| Giữ | Được đề nghị, bị từ chối |
| Cung cấp | Không có trạng thái tiếp theo |
| Bị từ chối | Không có trạng thái tiếp theo theo mặc định |

## 9. Ma trận quyền

| Tính năng | Ứng viên | Nhà tuyển dụng nhân sự | Người phỏng vấn | Quản lý tuyển dụng | Quản trị viên |
|---|---|---|---|---|---|
| Nộp đơn | Có | Không | Không | Không | Không |
| Xem trạng thái của chính mình | Có | Không | Không | Không | Không |
| Xem tất cả ứng viên | Không | Có | Không | Có | Có |
| Cập nhật trạng thái ứng viên | Không | Có | Không | Không | Không |
| Lên lịch phỏng vấn | Không | Có | Không | Không | Không |
| Xem cuộc phỏng vấn được chỉ định | Không | Không | Có | Không | Không |
| Gửi phản hồi phỏng vấn | Không | Không | Có | Không | Không |
| Xem bảng điều khiển đường ống | Không | Có | Không | Có | Có |
| Quản lý người dùng và vai trò | Không | Không | Không | Không | Có |
| Cấu hình chương trình thực tập | Không | Không | Không | Không | Có |

## 10. Quy tắc xác thực

| ID quy tắc | Quy tắc xác thực |
|---|---|
| VR-01 | Tên đầy đủ của ứng viên không được để trống. |
| VR-02 | Email của ứng viên phải tuân theo định dạng email hợp lệ. |
| VR-03 | Số điện thoại của ứng viên không được để trống. |
| VR-04 | Cần có file CV trước khi nộp hồ sơ. |
| VR-05 | File CV phải là PDF hoặc DOCX. |
| VR-06 | Kích thước file CV không được vượt quá 5MB. |
| VR-07 | Ứng viên không thể nộp đơn vào cùng một chương trình thực tập nhiều lần. |
| VR-08 | Bộ phận nhân sự không thể lên lịch phỏng vấn nếu không chọn ứng viên, người phỏng vấn, ngày và giờ. |
| VR-09 | Người phỏng vấn không thể gửi phản hồi nếu không có đánh giá và đề xuất. |
| VR-10 | Hệ thống phải từ chối truy cập trái phép dựa trên vai trò của người dùng. |

## 11. Xử lý lỗi

| Trường hợp lỗi | Hành vi hệ thống |
|---|---|
| Người dùng gửi biểu mẫu chưa đầy đủ | Hệ thống hiển thị thông báo xác thực trường bắt buộc. |
| Người dùng tải lên loại tệp CV không được hỗ trợ | Hệ thống từ chối tệp và hiển thị các loại tệp được phép. |
| Ứng viên cố gắng truy cập vào ứng dụng của ứng viên khác | Hệ thống từ chối truy cập. |
| Người phỏng vấn cố gắng xem ứng viên chưa được chỉ định | Hệ thống từ chối truy cập. |
| HR chọn chuyển đổi trạng thái không hợp lệ | Hệ thống ngăn chặn cập nhật và hiển thị thông báo lỗi. |
| Phản hồi phỏng vấn thiếu các trường bắt buộc | Hệ thống ngăn chặn việc gửi và hiển thị thông báo xác thực. |

## 12. Câu hỏi mở

| ID câu hỏi | Câu hỏi mở |
|---|---|
| OQ-01 | Ứng viên có được phép chỉnh sửa hồ sơ đã nộp không? |
| OQ-02 | Nhân sự có thể xuất dữ liệu ứng viên sang Excel không? |
| OQ-03 | Hệ thống có nên hỗ trợ nhiều vòng phỏng vấn không? |
| OQ-04 | Ứng viên nên chỉ nhận email hay cả email và thông báo trong hệ thống? |
| OQ-05 | Người quản lý tuyển dụng nên phê duyệt mọi lời đề nghị hay chỉ những chương trình được chọn? |

##13. BA Ghi chú

SRS này chuyển đổi các yêu cầu kinh doanh thành các yêu cầu phần mềm chi tiết.

Các phần quan trọng nhất để phát triển và thử nghiệm là yêu cầu chức năng, yêu cầu phi chức năng, ma trận cấp phép, quy tắc xác thực, quy tắc chuyển đổi trạng thái và xử lý lỗi.