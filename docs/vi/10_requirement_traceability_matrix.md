#10. Ma trận truy xuất nguồn gốc yêu cầu

## 1. Mục đích

Tài liệu này xác định Ma trận truy xuất nguồn gốc yêu cầu (RTM) cho hệ thống InternshipHub.

Mục đích của RTM là đảm bảo rằng mọi yêu cầu kinh doanh đều được kết nối với các yêu cầu chức năng, câu chuyện của người dùng, tiêu chí chấp nhận và kịch bản thử nghiệm.

Điều này giúp BA, Nhà phát triển, Kỹ sư QA và các bên liên quan kiểm tra phạm vi yêu cầu và giảm phạm vi bị thiếu.

## 2. Ma trận truy xuất nguồn gốc yêu cầu là gì?

Ma trận truy xuất nguồn gốc yêu cầu là một bảng theo dõi các yêu cầu từ nhu cầu kinh doanh đến thử nghiệm.

Trong dự án này, quy trình truy xuất nguồn gốc là:

```văn bản
Yêu cầu nghiệp vụ → Yêu cầu chức năng → Câu chuyện của người dùng → Tiêu chí chấp nhận → Kịch bản kiểm thử
```

Điều này có nghĩa là mỗi yêu cầu nghiệp vụ phải được hỗ trợ bởi các tính năng hệ thống, câu chuyện của người dùng, tiêu chí chấp nhận và kịch bản thử nghiệm.

## 3. Cấp độ truy xuất nguồn gốc

| Cấp độ | Ý nghĩa | Tài liệu nguồn |
|---|---|---|
| Yêu cầu kinh doanh | Doanh nghiệp cần gì | 04_BRD_business_requirements.md |
| Yêu cầu chức năng | Hệ thống phải làm gì | 05_SRS_software_requirements.md |
| Câu chuyện của người dùng | Yêu cầu từ góc độ người dùng | 06_user_stories_product_backlog.md |
| Tiêu chí chấp nhận | Điều kiện nhận truyện | 07_acceptance_criteria.md |
| Kịch bản thử nghiệm | Kịch bản xác minh yêu cầu | 09_test_scenarios.md |

## 4. Ma trận truy xuất nguồn gốc yêu cầu

| Yêu cầu kinh doanh | Yêu cầu chức năng | Câu chuyện của người dùng | Tiêu chí chấp nhận | Kịch bản thử nghiệm |
|---|---|---|---|---|
| BR-01: Hệ thống cho phép ứng viên nộp hồ sơ thực tập trực tuyến. | FR-01, FR-02, FR-06, FR-07 | US-01, US-02, US-05, US-06 | AC cho US-01, US-02, US-05, US-06 | TC-001 đến TC-007, TC-016 đến TC-022 |
| BR-02: Hệ thống cho phép ứng viên đăng tải CV và thông tin cá nhân. | FR-03, FR-04, FR-05 | US-03, US-04 | AC cho US-03, US-04 | TC-008 tới TC-015 |
| BR-03: Hệ thống cho phép HR xem và quản lý tất cả các hồ sơ đã nộp. | FR-10, FR-11, FR-12, FR-13 | US-10, US-11, US-12, US-13 | AC cho US-10, US-11, US-12, US-13 | TC-029 tới TC-039 |
| BR-04: Hệ thống cho phép HR cập nhật trạng thái tuyển dụng ứng viên. | FR-14, FR-15, FR-16 | US-14, US-15, US-16 | AC cho US-14, US-15, US-16 | TC-040 tới TC-048 |
| BR-05: Hệ thống cho phép nhân sự lên lịch phỏng vấn và phân công người phỏng vấn. | FR-17, FR-18 | US-18, US-19, US-20 | AC cho US-18, US-19, US-20 | TC-049 tới TC-056 |
| BR-06: Hệ thống cho phép người phỏng vấn xem ứng viên được phân công. | FR-20, FR-21, FR-25 | US-21, US-22, US-26 | AC cho US-21, US-22, US-26 | TC-057 tới TC-061 |
| BR-07: Hệ thống sẽ cho phép người phỏng vấn gửi phản hồi phỏng vấn có cấu trúc. | FR-22, FR-23, FR-24 | US-23, US-24, US-25 | AC cho US-23, US-24, US-25 | TC-062 tới TC-069 |
| BR-08: Hệ thống sẽ cho phép người quản lý tuyển dụng xem quy trình tuyển dụng và phản hồi của ứng viên. | FR-26, FR-27, FR-28, FR-29 | US-27, US-28, US-29, US-30 | AC cho US-27, US-28, US-29, US-30 | TC-070 tới TC-078 |
| BR-09: Hệ thống sẽ thông báo cho thí sinh khi trạng thái hồ sơ của họ thay đổi. | FR-09, FR-19 | US-08, US-17 | AC cho US-08, US-17 | TC-027, TC-028, TC-076 đến TC-078 |
| BR-10: Hệ thống sẽ lưu trữ lịch sử trạng thái cho mục đích theo dõi và kiểm tra. | FR-16, FR-33, NFR-06 | US-16, US-34 | AC cho US-16, US-34 | TC-045 đến TC-047, TC-089 đến TC-091 |
| BR-11: Hệ thống sẽ hỗ trợ kiểm soát truy cập dựa trên vai trò cho các loại người dùng khác nhau. | FR-25, FR-30, FR-31, NFR-02, NFR-03, NFR-04, NFR-05 | US-26, US-31, US-32 | AC cho US-26, US-31, US-32 | TC-007, TC-022, TC-025, TC-031, TC-039, TC-055, TC-059, TC-061, TC-065, TC-072, TC-078, TC-082, TC-085, TC-091 |

## 5. Ma trận bao phủ yêu cầu chức năng

| Yêu cầu chức năng | Câu chuyện người dùng liên quan | Kịch bản thử nghiệm liên quan | Tình trạng bảo hiểm |
|---|---|---|---|
| FR-01: Đăng ký ứng viên | Mỹ-01 | TC-001, TC-002, TC-003 | Được bảo hiểm |
| FR-02: Đăng nhập và đăng xuất | Mỹ-02 | TC-004, TC-005, TC-006, TC-007 | Được bảo hiểm |
| FR-03: Tạo và cập nhật hồ sơ | Mỹ-03 | TC-008, TC-009, TC-010 | Được bảo hiểm |
| FR-04: Tải CV lên | Mỹ-04 | TC-011, TC-012, TC-015 | Được bảo hiểm |
| FR-05: Xác thực loại và kích thước tệp CV | Mỹ-04 | TC-013, TC-014 | Được bảo hiểm |
| FR-06: Đăng ký chương trình thực tập | Mỹ-05 | TC-016, TC-017, TC-018, TC-019, TC-020 | Được bảo hiểm |
| FR-07: Xem đơn đăng ký đã gửi | Mỹ-06 | TC-021, TC-022 | Được bảo hiểm |
| FR-08: Xem trạng thái ứng dụng hiện tại | Mỹ-07 | TC-023, TC-024, TC-025 | Được bảo hiểm |
| FR-09: Thông báo trạng thái ứng viên | Mỹ-08 | TC-027, TC-028 | Được bảo hiểm |
| FR-10: HR xem tất cả các đơn đăng ký đã gửi | Mỹ-10 | TC-029, TC-030, TC-031 | Được bảo hiểm |
| FR-11: Nhân sự tìm kiếm ứng viên | Mỹ-11 | TC-032, TC-033, TC-034 | Được bảo hiểm |
| FR-12: Bộ lọc nhân sự | Mỹ-12 | TC-035, TC-036, TC-037 | Được bảo hiểm |
| FR-13: HR xem hồ sơ và CV ứng viên | Mỹ-13 | TC-038, TC-039 | Được bảo hiểm |
| FR-14: HR cập nhật trạng thái ứng viên | Mỹ-14 | TC-040, TC-048 | Được bảo hiểm |
| FR-15: Xác thực chuyển đổi trạng thái | Mỹ-15 | TC-041, TC-042, TC-043, TC-044 | Được bảo hiểm |
| FR-16: Ghi lại các thay đổi trạng thái | Mỹ-16 | TC-045, TC-046, TC-047 | Được bảo hiểm |
| FR-17: Lên lịch phỏng vấn | Mỹ-18 | TC-049, TC-050, TC-051, TC-052 | Được bảo hiểm |
| FR-18: Phân công người phỏng vấn | US-19, US-20 | TC-053, TC-054, TC-055, TC-056 | Được bảo hiểm |
| FR-19: Gửi kết quả đề nghị hoặc từ chối | Mỹ-17 | TC-076, TC-077, TC-078 | Được bảo hiểm |
| FR-20: Xem các cuộc phỏng vấn được chỉ định | Mỹ-21 | TC-057, TC-058, TC-059 | Được bảo hiểm |
| FR-21: Xem hồ sơ và CV ứng viên được phân công | Mỹ-22 | TC-060, TC-061 | Được bảo hiểm |
| FR-22: Gửi phản hồi có cấu trúc | Mỹ-23 | TC-062, TC-065, TC-066 | Được bảo hiểm |
| FR-23: Các trường phản hồi bắt buộc | Mỹ-24 | TC-063 | Được bảo hiểm |
| FR-24: Đề xuất Đạt, Thất bại hoặc Giữ | Mỹ-25 | TC-064, TC-067, TC-068, TC-069 | Được bảo hiểm |
| FR-25: Ngăn người phỏng vấn xem các ứng viên chưa được chỉ định | Mỹ-26 | TC-059, TC-061, TC-065 | Được bảo hiểm |
| FR-26: Xem quy trình tuyển dụng | Mỹ-27 | TC-070, TC-071, TC-072 | Được bảo hiểm |
| FR-27: Xem phản hồi của ứng viên | Mỹ-28 | TC-073, TC-074 | Được bảo hiểm |
| FR-28: So sánh ứng viên | Mỹ-29 | TC-075, TC-076 | Được bảo hiểm |
| FR-29: Phê duyệt quyết định tuyển dụng cuối cùng | Mỹ-30 | TC-077, TC-078 | Được bảo hiểm |
| FR-30: Quản lý tài khoản người dùng | Mỹ-31 | TC-079, TC-080, TC-081, TC-082 | Được bảo hiểm |
| FR-31: Gán vai trò người dùng | Mỹ-32 | TC-083, TC-084, TC-085 | Được bảo hiểm |
| FR-32: Cấu hình chương trình thực tập | Mỹ-33 | TC-086, TC-087, TC-088 | Được bảo hiểm |
| FR-33: Xem nhật ký hoạt động của hệ thống | Mỹ-34 | TC-089, TC-090, TC-091 | Được bảo hiểm |

## 6. Ma trận bao phủ yêu cầu phi chức năng

| Yêu cầu phi chức năng | Khu vực liên quan | Kịch bản thử nghiệm liên quan | Tình trạng bảo hiểm |
|---|---|---|---|
| NFR-01: Danh sách ứng viên sẽ tải trong vòng 3 giây cho tối đa 1.000 bản ghi. | Quản lý ứng viên nhân sự | Kiểm tra hiệu suất sẽ được thêm vào trong phiên bản tương lai | Được che phủ một phần |
| NFR-02: Cần phải xác thực trước các trang được bảo vệ. | Kiểm soát đăng nhập và truy cập | TC-007, TC-031, TC-039, TC-055, TC-072, TC-082, TC-085, TC-091 | Được bảo hiểm |
| NFR-03: Quyền truy cập dữ liệu bị hạn chế bởi vai trò của người dùng. | Kiểm soát truy cập dựa trên vai trò | TC-022, TC-025, TC-031, TC-039, TC-055, TC-059, TC-061, TC-065, TC-072, TC-078, TC-082, TC-085, TC-091 | Được bảo hiểm |
| NFR-04: Ứng viên chỉ có thể xem thông tin ứng tuyển của chính mình. | Tình trạng ứng viên và đơn đăng ký | TC-022, TC-025 | Được bảo hiểm |
| NFR-05: Người phỏng vấn chỉ có thể xem các ứng viên được phân công. | Bảng điều khiển và phản hồi của người phỏng vấn | TC-059, TC-061, TC-065 | Được bảo hiểm |
| NFR-06: Các hành động quan trọng được ghi lại. | Nhật ký hoạt động và lịch sử trạng thái | TC-045, TC-046, TC-089, TC-090 | Được bảo hiểm |
| NFR-07: Hệ thống phải khả dụng 99% trong thời gian tuyển dụng. | Sẵn có | Kiểm tra tính khả dụng sẽ được thêm vào trong phiên bản tương lai | Được che phủ một phần |
| NFR-08: Giao diện người dùng sẽ hoạt động trên trình duyệt trên máy tính để bàn và thiết bị di động. | Khả năng sử dụng và khả năng tương thích | Thử nghiệm đa trình duyệt và phản hồi sẽ được thêm vào trong phiên bản tương lai | Được che phủ một phần |
| NFR-09: Tải lên CV phải hỗ trợ các tệp PDF và DOCX. | Tải lên CV | TC-011, TC-012, TC-013 | Được bảo hiểm |
| NFR-10: Hệ thống sẽ hiển thị thông báo xác thực rõ ràng. | Xác thực | TC-003, TC-009, TC-014, TC-017, TC-018, TC-050, TC-063, TC-064, TC-076 | Được bảo hiểm |

## 7. Phạm vi yêu cầu MVP

MVP tập trung vào quy trình tuyển dụng cốt lõi.

| Khu vực MVP | Yêu cầu kinh doanh | Yêu cầu chức năng | Câu chuyện của người dùng | Kịch bản thử nghiệm | Trạng thái |
|---|---|---|---|---|---|
| Hồ sơ ứng viên | BR-01, BR-02 | FR-01 đến FR-07 | US-01 đến US-06 | TC-001 tới TC-022 | Được bảo hiểm |
| Theo dõi trạng thái ứng viên | BR-09 | FR-08, FR-09 | US-07, US-08 | TC-023 đến TC-028 | Được bảo hiểm |
| Quản lý ứng viên nhân sự | BR-03, BR-04, BR-10 | FR-10 đến FR-16 | US-10 đến US-16 | TC-029 đến TC-048 | Được bảo hiểm |
| Lên lịch phỏng vấn | BR-05 | FR-17, FR-18 | US-18 đến US-20 | TC-049 tới TC-056 | Được bảo hiểm |
| Phản hồi phỏng vấn | BR-06, BR-07 | FR-20 đến FR-25 | US-21 đến US-26 | TC-057 đến TC-069 | Được bảo hiểm |
| Kiểm soát truy cập | BR-11 | FR-25, FR-30, FR-31, NFR-02 đến NFR-05 | US-26, US-31, US-32 | Các trường hợp kiểm tra quyền trên các mô-đun | Được bảo hiểm |

## 8. Phân tích khoảng trống

| ID khoảng cách | Khoảng trống | Tác động | Hành động được đề xuất |
|---|---|---|---|
| GAP-01 | Bài kiểm tra năng lực cho danh sách ứng viên vẫn chưa chi tiết. | Trung bình | Thêm các trường hợp kiểm thử hiệu suất khi kiến ​​trúc kỹ thuật được xác định. |
| GAP-02 | Kiểm tra tính khả dụng vẫn chưa chi tiết. | Trung bình | Xác định giám sát thời gian hoạt động và kiểm tra tính khả dụng trong giai đoạn kỹ thuật sau. |
| GAP-03 | Kiểm tra khả năng phản hồi trên thiết bị di động vẫn chưa chi tiết. | Thấp | Thêm các trường hợp kiểm tra khả năng tương thích giao diện người dùng sau khi nguyên mẫu giao diện người dùng được tạo. |
| GAP-04 | Việc xử lý lỗi gửi thông báo có thể cần chi tiết hơn. | Trung bình | Thêm các yêu cầu thử lại thông báo chi tiết hơn và xử lý lỗi. |
| GAP-05 | Nhiều vòng phỏng vấn không được tính vào MVP hiện tại. | Trung bình | Giữ làm cải tiến trong tương lai trừ khi các bên liên quan xác nhận điều đó là cần thiết. |

## 9. Ví dụ về tác động của thay đổi

Nếu một bên liên quan yêu cầu một tính năng mới, BA sẽ cập nhật RTM.

Ví dụ thay đổi:

```văn bản
Yêu cầu thay đổi: Thêm nhiều vòng phỏng vấn.
```

Tác động:

| Khu vực | Tác động |
|---|---|
| BRD | Thêm hoặc cập nhật yêu cầu kinh doanh cho nhiều vòng phỏng vấn. |
| SRS | Thêm các yêu cầu chức năng để cấu hình và lên lịch vòng phỏng vấn. |
| Câu chuyện của người dùng | Thêm các câu chuyện để lên lịch nhân sự cho nhiều vòng và người phỏng vấn gửi phản hồi cho mỗi vòng. |
| Tiêu chí chấp nhận | Thêm quy tắc Đưa ra–Khi–Thì cho từng vòng phỏng vấn. |
| Kịch bản thử nghiệm | Thêm các trường hợp thử nghiệm cho hành vi ở vòng đầu tiên, vòng thứ hai và vòng cuối cùng. |
| Khung dây | Cập nhật trang đặt lịch phỏng vấn và trang phản hồi. |

## 10. Danh sách kiểm tra chất lượng RTM

| Mục danh sách kiểm tra | Mô tả |
|---|---|
| Mọi BR đều có FR liên quan | Mỗi yêu cầu nghiệp vụ phải kết nối với ít nhất một yêu cầu chức năng. |
| Mỗi FR đều có câu chuyện người dùng liên quan | Mỗi yêu cầu chức năng phải được thể hiện trong hồ sơ tồn đọng. |
| Mọi câu chuyện quan trọng của người dùng đều có tiêu chí chấp nhận | Câu chuyện cốt lõi của người dùng nên có thể kiểm tra được. |
| Mọi yêu cầu cốt lõi đều có kịch bản thử nghiệm | Các yêu cầu MVP phải được QA xác minh. |
| Quy tắc cấp phép có thể theo dõi được | Kiểm soát bảo mật và truy cập sẽ xuất hiện trong các yêu cầu và thử nghiệm. |
| Khoảng trống được ghi lại | Thông tin bị thiếu hoặc một phần phải được ghi lại rõ ràng. |
| RTM được cập nhật sau khi có yêu cầu thay đổi | Những thay đổi về yêu cầu sẽ cập nhật tất cả các tạo phẩm có liên quan. |

##11. BA Ghi chú

Ma trận truy xuất nguồn gốc yêu cầu là một trong những tạo phẩm BA quan trọng nhất vì nó kết nối các mục tiêu kinh doanh với hoạt động và thử nghiệm của hệ thống.

Trong dự án này, RTM cho thấy các yêu cầu chính của InternshipHub bao gồm từ BRD đến SRS, câu chuyện của người dùng, tiêu chí chấp nhận và kịch bản thử nghiệm.

RTM cũng giúp xác định các lỗ hổng, đặc biệt đối với các yêu cầu phi chức năng như hiệu suất, tính khả dụng và kiểm tra giao diện người dùng đáp ứng.

Bước tiếp theo là chuẩn bị các mẫu dự án và tài liệu GitHub để kho lưu trữ trông chuyên nghiệp như một dự án danh mục đầu tư BA.