#08. Đặc tả wireframe

## 1. Mục đích

Tài liệu này mô tả wireframe màn hình chính cho hệ thống InternshipHub.

Mục tiêu của đặc tả wireframe này là giúp các bên liên quan, nhà phát triển và kỹ sư QA hiểu được bố cục, các thành phần chính, hành động của người dùng và quy tắc kinh doanh của từng màn hình quan trọng.

Tài liệu này tập trung vào wireframe có độ chính xác thấp và hoạt động của màn hình chức năng, chứ không phải thiết kế giao diện người dùng cuối cùng.

## 2. Phạm vi wireframe

Đặc tả wireframe bao gồm các màn hình sau:

| ID màn hình | Tên màn hình | Người dùng chính |
|---|---|---|
| WF-01 | Trang đăng ký ứng viên | Ứng viên |
| WF-02 | Trang đăng nhập ứng viên | Ứng viên, Nhân sự, Người phỏng vấn, Quản lý tuyển dụng, Quản trị viên |
| WF-03 | Trang Hồ sơ Ứng viên | Ứng viên |
| WF-04 | Trang ứng tuyển thực tập | Ứng viên |
| WF-05 | Trang trạng thái đơn đăng ký của ứng viên | Ứng viên |
| WF-06 | Trang quản lý ứng viên nhân sự | Nhà tuyển dụng nhân sự |
| WF-07 | Trang chi tiết ứng viên | Nhà tuyển dụng nhân sự |
| WF-08 | Trang đặt lịch phỏng vấn | Nhà tuyển dụng nhân sự |
| WF-09 | Bảng điều khiển dành cho người phỏng vấn | Người phỏng vấn |
| WF-10 | Mẫu phản hồi phỏng vấn | Người phỏng vấn |
| WF-11 | Bảng điều khiển quy trình quản lý tuyển dụng | Quản lý tuyển dụng |
| WF-12 | Quản trị viên Trang quản lý người dùng | Quản trị hệ thống |

---

##WF-01: Trang đăng ký thí sinh

### Mục đích

Cho phép ứng viên mới tạo tài khoản trong hệ thống InternshipHub.

### Vai trò của người dùng

ứng viên

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Nhập tên đầy đủ | Ứng viên điền họ tên đầy đủ. |
| Nhập email | Ứng viên nhập địa chỉ email. |
| Nhập mật khẩu | Ứng viên nhập mật khẩu. |
| Xác nhận nhập mật khẩu | Ứng viên xác nhận mật khẩu. |
| Nút Đăng ký | Ứng viên nộp hồ sơ đăng ký. |
| Liên kết đăng nhập | Ứng viên điều hướng đến trang đăng nhập nếu họ đã có tài khoản. |
| Khu vực thông báo xác thực | Hệ thống hiển thị lỗi hoặc thông báo thành công. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| InternshipHub - Đăng ký ứng viên |
+---------------------------------------------------+
| Tên đầy đủ: [________________________] |
| Email: [________________________] |
| Mật khẩu: [________________________] |
| Xác nhận mật khẩu: [________________________] |
|                                                   |
| [ Đăng ký ] |
|                                                   |
| Đã có tài khoản? Đăng nhập |
|                                                   |
| Thông báo xác thực xuất hiện ở đây |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF01-R01 | Cần có tên đầy đủ, email, mật khẩu và xác nhận mật khẩu. |
| WF01-R02 | Email phải theo định dạng email hợp lệ. |
| WF01-R03 | Email phải là duy nhất. |
| WF01-R04 | Mật khẩu và mật khẩu xác nhận phải trùng khớp. |

### Câu chuyện người dùng liên quan

Mỹ-01

---

##WF-02: Trang đăng nhập

### Mục đích

Cho phép người dùng đăng nhập vào hệ thống dựa trên vai trò của họ.

### Vai trò của người dùng

Ứng viên, Nhà tuyển dụng nhân sự, Người phỏng vấn, Trưởng phòng tuyển dụng, Quản trị hệ thống

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Nhập email | Người dùng nhập email. |
| Nhập mật khẩu | Người dùng nhập mật khẩu. |
| Nút đăng nhập | Người dùng gửi mẫu đăng nhập. |
| Khu vực thông báo lỗi | Hệ thống hiển thị thông báo đăng nhập không hợp lệ. |
| Đăng ký liên kết | Ứng viên có thể vào trang đăng ký. |

### Bố cục có độ trung thực thấp

```văn bản
+------------------------------------------+
| InternshipHub - Đăng nhập |
+------------------------------------------+
| Email: [________________________] |
| Mật khẩu: [________________________] |
|                                          |
| [ Đăng nhập ] |
|                                          |
| Ứng cử viên mới? Đăng ký |
|                                          |
| Thông báo lỗi xuất hiện ở đây |
+------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF02-R01 | Email và mật khẩu là bắt buộc. |
| WF02-R02 | Người dùng được chuyển hướng dựa trên vai trò của họ sau khi đăng nhập thành công. |
| WF02-R03 | Đăng nhập không hợp lệ phải hiển thị thông báo lỗi rõ ràng. |
| WF02-R04 | Người dùng bị vô hiệu hóa không thể đăng nhập. |

### Câu chuyện người dùng liên quan

Mỹ-02

---

##WF-03: Trang hồ sơ ứng viên

### Mục đích

Cho phép ứng viên tạo và cập nhật thông tin hồ sơ của mình.

### Vai trò của người dùng

ứng viên

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Nhập tên đầy đủ | Tên đầy đủ của ứng viên. |
| Nhập số điện thoại | Số điện thoại của ứng viên. |
| Đầu Vào Đại Học | Ứng viên đại học. |
| Đầu vào chính | Ứng viên chính. |
| Đầu vào năm tốt nghiệp | Ứng viên dự kiến ​​tốt nghiệp vào năm. |
| Đầu vào liên kết danh mục đầu tư | GitHub, LinkedIn hoặc trang web cá nhân. |
| Nút Lưu | Lưu thông tin hồ sơ. |
| Khu vực thông báo xác thực | Hiển thị thông tin bị thiếu hoặc không hợp lệ. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| Hồ sơ ứng viên |
+---------------------------------------------------+
| Tên đầy đủ: [________________________] |
| Số điện thoại: [________________________] |
| Đại học: [________________________] |
| Thiếu tá: [________________________] |
| Năm tốt nghiệp: [________________________] |
| Liên kết danh mục đầu tư: [________________________] |
|                                                   |
| [ Lưu hồ sơ ] |
|                                                   |
| Thông báo xác thực xuất hiện ở đây |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF03-R01 | Cần có họ tên, số điện thoại, trường đại học, chuyên ngành. |
| WF03-R02 | Ứng viên có thể cập nhật hồ sơ trước khi nộp hồ sơ. |
| WF03-R03 | Ứng viên chỉ có thể chỉnh sửa hồ sơ của chính mình. |

### Câu chuyện người dùng liên quan

Mỹ-03

---

##WF-04: Trang đăng ký thực tập

### Mục đích

Cho phép ứng viên tải lên CV và đăng ký chương trình thực tập có sẵn.

### Vai trò của người dùng

ứng viên

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Chương trình thực tập thả xuống | Ứng viên lựa chọn chương trình thực tập có sẵn. |
| Trường tải lên CV | Ứng viên upload CV PDF hoặc DOCX. |
| Hiển thị tên tệp CV | Hiển thị tên tệp CV đã tải lên. |
| Nút Gửi đơn đăng ký | Ứng viên nộp hồ sơ. |
| Khu vực thông báo xác thực | Hiển thị các trường bị thiếu hoặc lỗi tải lên. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| Đơn xin thực tập |
+---------------------------------------------------+
| Chương trình thực tập: [ Chọn Chương trình v ] |
|                                                   |
| Tải CV lên: [ Chọn File ] |
| Tệp đã tải lên: my_cv.pdf |
|                                                   |
| [Gửi đơn đăng ký] |
|                                                   |
| Thông báo xác thực xuất hiện ở đây |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF04-R01 | Ứng viên phải chọn một chương trình thực tập có sẵn. |
| WF04-R02 | Ứng viên phải upload CV trước khi nộp hồ sơ. |
| WF04-R03 | File CV phải là PDF hoặc DOCX. |
| WF04-R04 | Kích thước file CV không được vượt quá 5MB. |
| WF04-R05 | Ứng viên không thể nộp đơn vào cùng một chương trình nhiều lần. |

### Câu chuyện người dùng liên quan

US-04, US-05, US-06

---

## WF-05: Trang trạng thái đơn đăng ký của ứng viên

### Mục đích

Cho phép ứng viên xem trạng thái đơn đăng ký hiện tại và thông tin phỏng vấn.

### Vai trò của người dùng

ứng viên

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Huy hiệu trạng thái hiện tại | Hiển thị trạng thái ứng dụng hiện tại. |
| Dòng thời gian trạng thái | Hiển thị tiến độ tuyển dụng. |
| Tên chương trình | Hiển thị chương trình thực tập ứng dụng. |
| Ngày gửi | Hiển thị ngày nộp đơn. |
| Mục Thông Tin Phỏng Vấn | Hiển thị ngày, giờ phỏng vấn, người phỏng vấn và liên kết cuộc họp nếu có. |
| Phần kết quả cuối cùng | Hiển thị kết quả đề nghị, từ chối hoặc giữ lại nếu có. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| Tình trạng đơn đăng ký |
+---------------------------------------------------+
| Chương trình: Thực tập sinh phân tích kinh doanh |
| Ngày gửi: 2026-06-16 |
| Tình trạng hiện tại: [ Đã lên lịch phỏng vấn ] |
|                                                   |
| Dòng thời gian: |
| Đã gửi -> Sàng lọc -> Lên lịch phỏng vấn |
|                                                   |
| Thông tin Phỏng vấn |
| Ngày: 2026-06-20 |
| Thời gian: 09:00 sáng |
| Người phỏng vấn: Nguyễn Văn A |
| Liên kết cuộc họp: [ Liên kết mở ] |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF05-R01 | Ứng viên chỉ có thể xem trạng thái đơn đăng ký của chính họ. |
| WF05-R02 | Thông tin phỏng vấn chỉ được hiển thị khi cuộc phỏng vấn được lên lịch. |
| WF05-R03 | Trạng thái mới nhất phải khớp với trạng thái do HR quản lý. |

### Câu chuyện người dùng liên quan

US-07, US-08, US-09

---

##WF-06: Trang quản lý ứng viên nhân sự

### Mục đích

Cho phép nhà tuyển dụng nhân sự xem, tìm kiếm, lọc và quản lý các đơn đăng ký đã gửi.

### Vai trò của người dùng

Nhà tuyển dụng nhân sự

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Hộp Tìm kiếm | Tìm kiếm ứng viên theo tên hoặc email. |
| Bộ lọc trạng thái | Lọc ứng viên theo trạng thái. |
| Bộ lọc chương trình | Lọc ứng viên theo chương trình thực tập. |
| Bộ lọc ngày áp dụng | Lọc theo ngày nộp đơn. |
| Bảng Ứng Viên | Hiển thị danh sách ứng viên. |
| Nút Xem chi tiết | Mở trang chi tiết ứng viên. |
| Cập nhật trạng thái Hành động | Cho phép HR cập nhật trạng thái ứng viên. |
| Lên lịch hành động phỏng vấn | Mở trang lập lịch phỏng vấn. |

### Bố cục có độ trung thực thấp

```văn bản
+------------------------------------------------------------------------------------------------+
| Quản lý ứng viên nhân sự |
+------------------------------------------------------------------------------------------------+
| Tìm kiếm: [________________] Trạng thái: [All v] Chương trình: [All v] Ngày: [____] |
+------------------------------------------------------------------------------------------------+
| Tên ứng viên | Email | Chương trình | Trạng thái | Ngày nộp đơn | Hành động |
|--------------------------------------------------------------------------------|
| Nguyễn Á | a@... | Cử nhân thực tập | Sàng lọc | 2026-06-15 | Xem / Cập nhật |
| Trần B | b@... | Thực tập sinh AI | Đã gửi | 2026-06-16 | Xem / Cập nhật |
+------------------------------------------------------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF06-R01 | Chỉ Nhà tuyển dụng nhân sự, Người quản lý tuyển dụng và Quản trị viên mới có thể xem danh sách ứng viên. |
| WF06-R02 | Chỉ Nhà tuyển dụng nhân sự mới có thể cập nhật trạng thái ứng viên. |
| WF06-R03 | Tìm kiếm và bộ lọc có thể được sử dụng cùng nhau. |
| WF06-R04 | Danh sách ứng viên sẽ hiển thị trạng thái mới nhất. |

### Câu chuyện người dùng liên quan

US-10, US-11, US-12

---

##WF-07: Trang chi tiết ứng viên

### Mục đích

Cho phép bộ phận nhân sự xem xét hồ sơ ứng viên, CV, lịch sử trạng thái và phản hồi.

### Vai trò của người dùng

Nhà tuyển dụng nhân sự

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Mục Hồ sơ Ứng viên | Hiển thị thông tin cá nhân của ứng viên. |
| Mục CV | Cho phép nhân sự xem hoặc tải xuống CV. |
| Phần thông tin ứng dụng | Hiển thị chương trình, trạng thái, ngày áp dụng. |
| Phần Cập Nhật Trạng Thái | Cho phép HR cập nhật trạng thái ứng viên. |
| Bảng lịch sử trạng thái | Hiển thị các thay đổi trạng thái. |
| Phần phản hồi phỏng vấn | Hiển thị phản hồi đã gửi nếu có. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| Chi tiết Ứng viên |
+---------------------------------------------------+
| Họ tên: Nguyễn Văn A |
| Email: nguyenvana@email.com |
| Đại học: UIT |
| Chuyên ngành: Công nghệ thông tin |
| Chương trình: Cử nhân thực tập |
| Tình trạng hiện tại: Đang sàng lọc |
|                                                   |
| CV: [ Xem CV ] [ Tải CV ] |
|                                                   |
| Cập nhật trạng thái: [ Chọn trạng thái v ] [ Lưu ] |
|                                                   |
| Lịch sử trạng thái |
| Trạng thái cũ | Trạng thái mới | Cập nhật bởi | Thời gian |
|                                                   |
| Phản hồi phỏng vấn |
| Phản hồi sẽ xuất hiện ở đây sau cuộc phỏng vấn |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF07-R01 | Nhân sự có thể xem hồ sơ ứng viên và CV. |
| WF07-R02 | Nhân sự chỉ có thể cập nhật trạng thái ứng viên thông qua các chuyển đổi được phép. |
| WF07-R03 | Mọi thay đổi trạng thái phải được lưu trong lịch sử trạng thái. |
| WF07-R04 | Phản hồi được hiển thị sau khi người phỏng vấn gửi nó. |

### Câu chuyện người dùng liên quan

US-13, US-14, US-15, US-16

---

##WF-08: Trang đặt lịch phỏng vấn

### Mục đích

Cho phép nhân sự lên lịch phỏng vấn và phân công người phỏng vấn.

### Vai trò của người dùng

Nhà tuyển dụng nhân sự

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Thông tin ứng viên | Hiển thị thông tin ứng viên đã chọn. |
| Người phỏng vấn thả xuống | HR chọn người phỏng vấn. |
| Công cụ chọn ngày phỏng vấn | HR chọn ngày phỏng vấn. |
| Công cụ chọn thời gian phỏng vấn | HR chọn thời gian phỏng vấn. |
| Đầu vào liên kết cuộc họp | HR nhập link hoặc địa điểm họp trực tuyến. |
| Nút Lưu lịch biểu | Tạo lịch phỏng vấn. |
| Khu vực thông báo xác thực | Hiển thị trường bắt buộc hoặc thông báo trạng thái không hợp lệ. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| Lên lịch phỏng vấn |
+---------------------------------------------------+
| Ứng viên: Nguyễn Văn A |
| Chương trình: Cử nhân thực tập |
| Tình trạng hiện tại: Đang sàng lọc |
|                                                   |
| Người phỏng vấn: [ Chọn Người phỏng vấn v ] |
| Ngày: [ YYYY-MM-DD ] |
| Thời gian: [ HH:MM ] |
| Cuộc họp: [________________________] |
|                                                   |
| [ Lưu lịch trình ] |
|                                                   |
| Thông báo xác thực xuất hiện ở đây |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF08-R01 | Bộ phận nhân sự chỉ có thể lên lịch phỏng vấn cho những ứng viên ở trạng thái Sàng lọc. |
| WF08-R02 | Người phỏng vấn, ngày, giờ và thông tin cuộc họp là bắt buộc. |
| WF08-R03 | Sau khi lên lịch, trạng thái ứng viên sẽ trở thành Đã lên lịch phỏng vấn. |
| WF08-R04 | Người phỏng vấn được chỉ định có thể xem chi tiết cuộc phỏng vấn. |

### Câu chuyện người dùng liên quan

US-18, US-19, US-20

---

##WF-09: Bảng điều khiển dành cho người phỏng vấn

### Mục đích

Cho phép người phỏng vấn xem cuộc phỏng vấn được chỉ định của họ.

### Vai trò của người dùng

Người phỏng vấn

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Danh sách phỏng vấn được chỉ định | Hiển thị các cuộc phỏng vấn được giao cho người phỏng vấn. |
| Tên ứng viên | Hiển thị tên ứng viên. |
| Tên chương trình | Hiển thị chương trình thực tập. |
| Ngày giờ phỏng vấn | Hiển thị lịch trình. |
| Thông tin cuộc họp | Hiển thị liên kết cuộc họp hoặc vị trí. |
| Nút phản hồi mở | Mở biểu mẫu phản hồi. |

### Bố cục có độ trung thực thấp

```văn bản
+------------------------------------------------------------------------------------------------+
| Bảng điều khiển dành cho người phỏng vấn |
+------------------------------------------------------------------------------------------------+
| Tên ứng viên | Chương trình | Ngày | Thời gian | Cuộc họp | Hành động |
|--------------------------------------------------------------------------------|
| Nguyễn Á | Cử nhân thực tập | 20-06-2026 | 09:00 | Liên kết gặp gỡ | Phản hồi mở |
| Trần B | Thực tập sinh AI | 21-06-2026 | 14:00 | Liên kết gặp gỡ | Phản hồi mở |
+------------------------------------------------------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF09-R01 | Người phỏng vấn chỉ có thể xem các cuộc phỏng vấn được chỉ định. |
| WF09-R02 | Người phỏng vấn chỉ có thể xem hồ sơ ứng viên và CV của các cuộc phỏng vấn được chỉ định. |
| WF09-R03 | Người phỏng vấn có thể mở mẫu phản hồi cho các cuộc phỏng vấn được chỉ định. |

### Câu chuyện người dùng liên quan

US-21, US-22, US-26

---

##WF-10: Phiếu phản hồi phỏng vấn

### Mục đích

Cho phép người phỏng vấn gửi phản hồi có cấu trúc sau cuộc phỏng vấn.

### Vai trò của người dùng

Người phỏng vấn

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Tóm tắt ứng viên | Hiển thị thông tin ứng viên và chương trình. |
| Trường đánh giá kỹ thuật | Người phỏng vấn đánh giá khả năng kỹ thuật. |
| Trường đánh giá truyền thông | Người phỏng vấn đánh giá sự giao tiếp. |
| Lĩnh vực thế mạnh | Người phỏng vấn nhập điểm mạnh của ứng viên. |
| Lĩnh vực Điểm yếu | Người phỏng vấn đi vào điểm yếu của ứng viên. |
| Khuyến nghị thả xuống | Đạt, Thất bại hoặc Giữ. |
| Trường nhận xét | Ghi chú bổ sung tùy chọn. |
| Nút Gửi phản hồi | Lưu phản hồi. |

### Bố cục có độ trung thực thấp

```văn bản
+---------------------------------------------------+
| Mẫu phản hồi phỏng vấn |
+---------------------------------------------------+
| Ứng viên: Nguyễn Văn A |
| Chương trình: Cử nhân thực tập |
|                                                   |
| Đánh giá kỹ thuật: [ 1 2 3 4 5 ] |
| Đánh giá truyền thông: [ 1 2 3 4 5 ] |
|                                                   |
| Điểm mạnh: |
| [____________________________________________] |
|                                                   |
| Điểm yếu: |
| [____________________________________________] |
|                                                   |
| Khuyến nghị: [ Đạt/Không đạt/Giữ v] |
| Bình luận: |
| [____________________________________________] |
|                                                   |
| [Gửi phản hồi] |
+---------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF10-R01 | Chỉ người phỏng vấn được chỉ định mới có thể gửi phản hồi. |
| WF10-R02 | Cần phải có đánh giá kỹ thuật, đánh giá truyền thông, điểm mạnh, điểm yếu và đề xuất. |
| WF10-R03 | Khuyến nghị phải là Đạt, Thất bại hoặc Giữ. |
| WF10-R04 | Phản hồi đã gửi sẽ hiển thị cho Người quản lý nhân sự và tuyển dụng. |

### Câu chuyện người dùng liên quan

US-23, US-24, US-25

---

## WF-11: Bảng thông tin quy trình quản lý tuyển dụng

### Mục đích

Cho phép người quản lý tuyển dụng xem tiến trình tuyển dụng và phản hồi của ứng viên.

### Vai trò của người dùng

Người quản lý tuyển dụng

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Số lượng ứng viên theo trạng thái | Hiển thị số lượng ứng cử viên trong mỗi giai đoạn. |
| Bộ lọc chương trình | Lọc theo chương trình thực tập. |
| Bảng lộ trình ứng viên | Hiển thị các ứng cử viên và tình trạng hiện tại của họ. |
| Tóm tắt phản hồi | Hiển thị đề xuất của người phỏng vấn. |
| So Sánh Ứng Viên Hành Động | Cho phép so sánh ứng viên. |
| Phê duyệt Quyết định Hành động | Cho phép phê duyệt quyết định tuyển dụng cuối cùng. |

### Bố cục có độ trung thực thấp

```văn bản
+------------------------------------------------------------------------------------------------+
| Bảng điều khiển quy trình quản lý tuyển dụng |
+------------------------------------------------------------------------------------------------+
| Chương trình: [ Tất cả chương trình v ] |
|                                                                                |
| Đã gửi: 20 | Chiếu: 12 | Phỏng vấn: 8 | Đã cung cấp: 3 | Bị từ chối: 5 |
+------------------------------------------------------------------------------------------------+
| Ứng viên | Chương trình | Trạng thái | Đánh giá | Khuyến nghị | Hành động |
|--------------------------------------------------------------------------------|
| Nguyễn Á | Cử nhân thực tập | Đã Hoàn Thành Phỏng Vấn | 4,5 | Vượt qua | Xem / Phê duyệt |
| Trần B | Thực tập sinh AI | Giữ | 3,8 | Giữ | Xem / So sánh |
+------------------------------------------------------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF11-R01 | Người quản lý tuyển dụng có thể xem quy trình và phản hồi. |
| WF11-R02 | Người quản lý tuyển dụng không thể trực tiếp chỉnh sửa hồ sơ ứng viên. |
| WF11-R03 | Việc so sánh ứng viên cần ít nhất hai ứng viên được chọn. |
| WF11-R04 | Ưu đãi cuối cùng phải được phê duyệt trước khi bộ phận nhân sự gửi thông báo ưu đãi. |

### Câu chuyện người dùng liên quan

US-27, US-28, US-29, US-30

---

##WF-12: Trang quản lý người dùng Admin

### Mục đích

Cho phép quản trị viên hệ thống quản lý tài khoản và vai trò của người dùng.

### Vai trò của người dùng

Quản trị hệ thống

### Thành phần chính

| Thành phần | Mô tả |
|---|---|
| Danh sách người dùng | Hiển thị tất cả người dùng hệ thống. |
| Hộp Tìm kiếm | Tìm kiếm người dùng theo tên hoặc email. |
| Bộ lọc vai trò | Lọc người dùng theo vai trò. |
| Tạo nút người dùng | Mở biểu mẫu tạo người dùng. |
| Chỉnh sửa hành động của người dùng | Cập nhật thông tin người dùng. |
| Vô hiệu hóa hành động của người dùng | Vô hiệu hóa tài khoản người dùng. |
| Hành động phân công vai trò | Gán hoặc thay đổi vai trò của người dùng. |

### Bố cục có độ trung thực thấp

```văn bản
+------------------------------------------------------------------------------------------------+
| Quản trị viên Quản lý người dùng |
+------------------------------------------------------------------------------------------------+
| Tìm kiếm: [________________] Vai trò: [ Tất cả các vai trò v ] [ Tạo người dùng ] |
+------------------------------------------------------------------------------------------------+
| Tên | Email | Vai trò | Trạng thái | Hành động |
|--------------------------------------------------------------------------------|
| Nhân sự A | hra@company.com | Nhà tuyển dụng nhân sự | Đang hoạt động | Chỉnh sửa/Thay đổi vai trò/Vô hiệu hóa |
| B | b@company.com | Người phỏng vấn | Đang hoạt động | Chỉnh sửa/Thay đổi vai trò/Vô hiệu hóa |
+------------------------------------------------------------------------------------------------+
```

### Quy tắc kinh doanh

| ID quy tắc | Quy tắc |
|---|---|
| WF12-R01 | Chỉ Quản trị viên hệ thống mới có thể quản lý người dùng và vai trò. |
| WF12-R02 | Người dùng bị vô hiệu hóa không thể đăng nhập. |
| WF12-R03 | Mỗi người dùng phải có ít nhất một vai trò. |
| WF12-R04 | Thay đổi vai trò phải cập nhật quyền của người dùng. |

### Câu chuyện người dùng liên quan

US-31, US-32, US-33, US-34

---

## 3. Danh sách kiểm tra đánh giá wireframe

| Mục danh sách kiểm tra | Mô tả |
|---|---|
| Xóa mục đích màn hình | Mỗi màn hình đều có một mục tiêu rõ ràng. |
| Xóa vai trò người dùng | Mỗi màn hình xác định ai sử dụng nó. |
| Bao gồm các trường bắt buộc | Các trường quan trọng được liệt kê. |
| Bao gồm các hành động chính | Các nút và hành động của người dùng được xác định. |
| Bao gồm các quy tắc kinh doanh | Các quy tắc và hạn chế được ghi lại. |
| Câu chuyện người dùng liên quan được liên kết | Mỗi màn hình ánh xạ tới câu chuyện của người dùng. |
| Quy tắc cấp phép được xem xét | Màn hình nhạy cảm bao gồm các quy tắc truy cập. |

##4. BA Ghi chú

Đặc tả wireframe giúp BA truyền đạt hành vi mong đợi của màn hình trước khi bắt đầu phát triển.

Đối với vai trò BA Thực tập sinh hoặc Fresher, wireframe không cần phải hoàn hảo về mặt hình ảnh. Điểm quan trọng là chứng tỏ rằng BA hiểu luồng người dùng, dữ liệu được yêu cầu, quy tắc kinh doanh và hành vi ở cấp độ màn hình.

Bước tiếp theo là tạo kịch bản thử nghiệm từ câu chuyện của người dùng, tiêu chí chấp nhận và quy tắc kinh doanh.