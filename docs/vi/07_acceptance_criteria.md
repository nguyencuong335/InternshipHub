#07. Tiêu chí chấp nhận

## 1. Mục đích

Tài liệu này xác định các tiêu chí chấp nhận cho các câu chuyện chính của người dùng trong hệ thống InternshipHub.

Tiêu chí chấp nhận giúp Nhà phân tích kinh doanh, Nhà phát triển, Kỹ sư QA và các bên liên quan đồng ý về ý nghĩa của việc “thực hiện chính xác” đối với mỗi câu chuyện của người dùng.

## 2. Định dạng tiêu chí chấp nhận

Tiêu chí chấp nhận trong tài liệu này sử dụng định dạng Cho trước-Khi-Sau đó.

```văn bản
Cho [điều kiện ban đầu]
Khi [hành động của người dùng hoặc sự kiện hệ thống]
Sau đó [kết quả mong đợi]
```

Định dạng này làm cho các yêu cầu dễ hiểu, phát triển và kiểm tra hơn.

## 3. Danh sách tiêu chí chấp nhận

---

##US-01: Đăng ký ứng viên

**Câu chuyện của người dùng**

Là ứng viên tôi muốn đăng ký tài khoản bằng email và mật khẩu để có thể truy cập vào hệ thống InternshipHub.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đang ở trang đăng ký
Khi tôi nhập email, mật khẩu và thông tin bắt buộc hợp lệ
Sau đó hệ thống tạo tài khoản ứng viên của tôi thành công
```

``` dưa chuột
Vì tôi đang ở trang đăng ký
Khi tôi nhập một email đã tồn tại
Khi đó hệ thống hiện thông báo lỗi email đã được đăng ký
```

``` dưa chuột
Vì tôi đang ở trang đăng ký
Khi tôi để trống các trường bắt buộc
Sau đó hệ thống hiển thị thông báo xác thực cho các trường còn thiếu
```

---

##US-02: Đăng nhập và đăng xuất của ứng viên

**Câu chuyện của người dùng**

Là một ứng cử viên, tôi muốn đăng nhập và đăng xuất để có thể sử dụng tài khoản của mình một cách an toàn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã có tài khoản đã đăng ký
Khi tôi nhập đúng email và mật khẩu
Sau đó, hệ thống đăng nhập và chuyển hướng tôi đến bảng thông tin ứng viên
```

``` dưa chuột
Vì tôi đang ở trang đăng nhập
Khi tôi nhập sai email hoặc mật khẩu
Khi đó hệ thống hiện thông báo đăng nhập không hợp lệ
```

``` dưa chuột
Vì tôi đã đăng nhập
Khi tôi nhấp vào nút đăng xuất
Sau đó hệ thống đăng xuất tôi và chuyển hướng tôi đến trang đăng nhập
```

---

##US-03: Tạo và cập nhật hồ sơ cá nhân

**Câu chuyện của người dùng**

Là ứng viên, tôi muốn tạo và cập nhật hồ sơ cá nhân của mình để HR có thể xem xét thông tin của tôi.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã đăng nhập với tư cách là một ứng cử viên
Khi tôi nhập tất cả thông tin hồ sơ được yêu cầu
Sau đó hệ thống lưu hồ sơ của tôi thành công
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách là một ứng cử viên
Khi tôi để trống các trường hồ sơ bắt buộc
Sau đó hệ thống hiển thị thông báo xác thực cho các trường còn thiếu
```

``` dưa chuột
Vì tôi đã có hồ sơ đã lưu
Khi tôi cập nhật thông tin hồ sơ hợp lệ
Sau đó hệ thống lưu thông tin cập nhật thành công
```

---

##US-04: Tải CV lên

**Câu chuyện của người dùng**

Là ứng viên, tôi muốn tải CV của mình lên để HR có thể đánh giá hồ sơ của tôi.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã đăng nhập với tư cách là một ứng cử viên
Khi tôi tải lên tệp PDF hoặc DOCX có dung lượng dưới 5 MB
Sau đó hệ thống lưu CV và hiển thị thông báo upload thành công
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách là một ứng cử viên
Khi tôi tải lên một tệp không phải là PDF hoặc DOCX
Sau đó hệ thống từ chối file và hiển thị các loại file được phép
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách là một ứng cử viên
Khi tôi tải lên tệp CV lớn hơn 5MB
Sau đó hệ thống từ chối tệp và hiển thị giới hạn kích thước tệp tối đa
```

``` dưa chuột
Vì tôi đã tải CV lên trước khi nộp đơn
Khi tôi tải lên một CV hợp lệ mới
Sau đó hệ thống thay CV cũ bằng CV mới
```

---

##US-05: Nộp hồ sơ

**Câu chuyện của người dùng**

Với tư cách là một ứng viên, tôi muốn đăng ký một chương trình thực tập có sẵn để có thể được xem xét cho vị trí đó.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã hoàn thành hồ sơ của mình và tải lên CV hợp lệ
Khi tôi chọn một chương trình thực tập có sẵn và nộp đơn đăng ký
Sau đó hệ thống tạo một đơn đăng ký mới với trạng thái Đã gửi
```

``` dưa chuột
Vì tôi chưa tải lên CV
Khi tôi cố gắng nộp đơn đăng ký của mình
Sau đó hệ thống ngăn chặn việc gửi và hiển thị thông báo yêu cầu CV
```

``` dưa chuột
Vì tôi đã nộp đơn vào chương trình thực tập tương tự
Khi tôi cố gắng nộp đơn lại
Sau đó hệ thống ngăn chặn việc nộp đơn trùng lặp
```

``` dưa chuột
Vì chương trình thực tập đã kết thúc
Khi tôi cố gắng nộp đơn
Khi đó hệ thống ngăn chặn việc gửi và cho biết chương trình không còn nữa
```

---

##US-06: Xem đơn đăng ký đã gửi

**Câu chuyện của người dùng**

Với tư cách là một ứng cử viên, tôi muốn xem đơn đăng ký đã gửi của mình để có thể kiểm tra thông tin tôi đã cung cấp.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã nộp đơn
Khi tôi mở trang đăng ký đã gửi
Sau đó tôi có thể xem thông tin ứng dụng tôi đã cung cấp
```

``` dưa chuột
Vì tôi là một ứng cử viên
Khi tôi cố gắng xem đơn đăng ký đã gửi của ứng viên khác
Sau đó hệ thống từ chối truy cập
```

``` dưa chuột
Vì tôi đã nộp đơn
Khi tôi mở trang đăng ký đã gửi
Sau đó tôi có thể xem chương trình thực tập, ngày nộp, thông tin hồ sơ và tên tệp CV
```

---

## US-07: Xem trạng thái đơn đăng ký

**Câu chuyện của người dùng**

Với tư cách là một ứng viên, tôi muốn xem trạng thái đơn đăng ký hiện tại của mình để có thể biết tiến độ tuyển dụng của mình.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã nộp đơn
Khi tôi mở trang trạng thái ứng dụng
Sau đó tôi có thể thấy trạng thái đơn đăng ký hiện tại của mình
```

``` dưa chuột
Vì tôi đã nộp đơn
Khi tôi mở trang trạng thái ứng dụng
Sau đó tôi có thể thấy tên chương trình thực tập và ngày nộp đơn
```

``` dưa chuột
Vì tôi là một ứng cử viên
Khi tôi cố gắng xem trạng thái đơn đăng ký của ứng viên khác
Sau đó hệ thống từ chối truy cập
```

``` dưa chuột
Vì cuộc phỏng vấn của tôi đã được lên lịch
Khi tôi mở trang trạng thái ứng dụng
Sau đó tôi có thể xem ngày, giờ phỏng vấn và thông tin cuộc họp
```

---

##US-08: Nhận thông báo trạng thái

**Câu chuyện của người dùng**

Là ứng viên, tôi muốn nhận được thông báo khi trạng thái đơn đăng ký của tôi thay đổi, để tôi không cần phải liên hệ với bộ phận nhân sự theo cách thủ công.

**Tiêu chí chấp nhận**

``` dưa chuột
Do trạng thái đơn đăng ký của tôi được nhân sự cập nhật
Khi cập nhật trạng thái được lưu thành công
Sau đó hệ thống gửi cho tôi thông báo trạng thái
```

``` dưa chuột
Vì địa chỉ email của tôi là hợp lệ
Khi hệ thống gửi thông báo trạng thái
Sau đó tôi nhận được thông báo qua email
```

``` dưa chuột
Do thông báo không thể được gửi
Khi hệ thống phát hiện lỗi gửi
Sau đó hệ thống ghi nhận lỗi để nhân sự hoặc quản trị viên xem xét
```

---

##US-09: Xem thông tin phỏng vấn

**Câu chuyện của người dùng**

Là ứng viên, tôi muốn xem thông tin phỏng vấn khi có lịch phỏng vấn để có thể chuẩn bị kịp thời.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì cuộc phỏng vấn của tôi đã được lên lịch
Khi tôi mở trang trạng thái ứng dụng
Sau đó, tôi có thể xem ngày, giờ phỏng vấn, tên người phỏng vấn và thông tin cuộc họp
```

``` dưa chuột
Vì cuộc phỏng vấn của tôi chưa được lên lịch
Khi tôi mở trang trạng thái ứng dụng
Khi đó hệ thống không hiển thị chi tiết phỏng vấn
```

``` dưa chuột
Nhân sự cập nhật lịch phỏng vấn của tôi
Khi cập nhật được lưu thành công
Sau đó tôi có thể xem thông tin phỏng vấn mới nhất
```

---

## US-10: Xem tất cả đơn đăng ký đã gửi

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn xem tất cả các đơn đăng ký đã gửi để có thể quản lý ứng viên ở một nơi.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi mở trang quản lý ứng viên
Sau đó hệ thống hiển thị danh sách hồ sơ đã nộp
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi danh sách ứng viên được hiển thị
Sau đó, tôi có thể xem tên ứng viên, email, chương trình thực tập, trạng thái và ngày nộp đơn
```

``` dưa chuột
Vì tôi không phải là nhà tuyển dụng nhân sự, người quản lý tuyển dụng hoặc quản trị viên
Khi tôi cố gắng truy cập trang quản lý ứng viên
Sau đó hệ thống từ chối truy cập
```

---

##US-11: Tìm kiếm ứng viên

**Câu chuyện của người dùng**

Là nhà tuyển dụng nhân sự, tôi muốn tìm kiếm ứng viên theo tên, email hoặc chương trình thực tập để có thể tìm được ứng viên một cách nhanh chóng.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi tìm kiếm theo tên ứng viên
Sau đó hệ thống hiển thị các ứng viên có tên trùng với từ khóa tìm kiếm
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi tìm kiếm theo email của ứng viên
Sau đó hệ thống hiển thị các ứng viên có email trùng với từ khóa tìm kiếm
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi không có ứng viên nào khớp với từ khóa tìm kiếm
Sau đó hệ thống hiện thông báo kết quả trống
```

---

##US-12: Lọc ứng viên

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn lọc ứng viên theo trạng thái, chương trình và ngày nộp đơn để có thể quản lý quy trình tuyển dụng một cách hiệu quả.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi lọc ứng viên theo trạng thái
Khi đó hệ thống chỉ hiển thị những ứng viên có trạng thái đã chọn
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi lọc ứng viên theo chương trình thực tập
Sau đó hệ thống chỉ hiển thị những ứng viên đã nộp hồ sơ vào chương trình đã chọn
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi kết hợp các bộ lọc trạng thái, chương trình và ngày áp dụng
Sau đó hệ thống hiển thị các ứng viên phù hợp với tất cả các bộ lọc đã chọn
```

---

##US-13: Xem hồ sơ và CV ứng viên

**Câu chuyện của người dùng**

Là nhà tuyển dụng nhân sự, tôi muốn xem hồ sơ và CV ứng viên để sàng lọc ứng viên một cách chính xác.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi mở trang chi tiết về ứng viên
Sau đó tôi có thể xem thông tin hồ sơ ứng viên
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi mở trang chi tiết về ứng viên
Sau đó tôi có thể xem hoặc tải CV ứng viên
```

``` dưa chuột
Vì tôi không được phép xem thông tin ứng viên
Khi tôi cố gắng mở trang chi tiết về ứng viên
Sau đó hệ thống từ chối truy cập
```

---

##US-14: Cập nhật trạng thái ứng viên

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn cập nhật trạng thái tuyển dụng ứng viên để nguồn ứng viên luôn chính xác.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi cập nhật trạng thái ứng viên từ Đã gửi đến sàng lọc
Sau đó hệ thống lưu trạng thái mới thành công
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi cập nhật trạng thái ứng viên
Sau đó hệ thống ghi lại trạng thái cũ, trạng thái mới, ngày cập nhật, thời gian cập nhật
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi cố gắng cập nhật một ứng viên bằng cách sử dụng chuyển đổi trạng thái không hợp lệ
Khi đó hệ thống ngăn chặn cập nhật và hiển thị thông báo lỗi
```

``` dưa chuột
Với trạng thái ứng viên được cập nhật
Khi cập nhật được lưu thành công
Sau đó, ứng viên có thể xem trạng thái mới nhất trên trang trạng thái
```

---

## US-15: Xác thực chuyển đổi trạng thái

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn hệ thống xác thực các chuyển đổi trạng thái để ngăn chặn những thay đổi trạng thái tuyển dụng không hợp lệ.

**Tiêu chí chấp nhận**

``` dưa chuột
Với một ứng viên đang ở trạng thái Đã gửi
Khi nhân sự cập nhật trạng thái thành Sàng lọc
Sau đó hệ thống chấp nhận chuyển đổi
```

``` dưa chuột
Với một ứng cử viên đang ở trạng thái Dự thảo
Khi nhân sự cố gắng cập nhật trạng thái thành Đã cung cấp
Sau đó hệ thống từ chối quá trình chuyển đổi
```

``` dưa chuột
Cho rằng một ứng viên đang ở trạng thái Bị từ chối
Khi nhân sự cố gắng cập nhật trạng thái mà không được phê duyệt
Sau đó hệ thống ngăn chặn cập nhật
```

---

##US-16: Lịch sử thay đổi trạng thái bản ghi

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn mọi thay đổi trạng thái đều được ghi lại để quá trình tuyển dụng có thể được theo dõi và kiểm tra.

**Tiêu chí chấp nhận**

``` dưa chuột
Đưa ra các cập nhật nhân sự về trạng thái ứng viên
Khi cập nhật được lưu thành công
Sau đó hệ thống ghi lại trạng thái cũ, trạng thái mới, ngày cập nhật, thời gian cập nhật
```

``` dưa chuột
Với một ứng cử viên có lịch sử trạng thái
Khi HR mở trang chi tiết ứng viên
Sau đó nhân sự có thể xem lịch sử trạng thái
```

``` dưa chuột
Do cập nhật trạng thái không thành công
Khi bản cập nhật không được lưu
Khi đó hệ thống không tạo bản ghi lịch sử trạng thái không chính xác
```

---

## US-17: Gửi kết quả đề nghị hoặc từ chối

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn gửi kết quả tuyển dụng hoặc từ chối để ứng viên nhận được kết quả tuyển dụng chính thức.

**Tiêu chí chấp nhận**

``` dưa chuột
Ứng viên đã hoàn tất quá trình tuyển dụng
Khi HR gửi kết quả ưu đãi
Sau đó hệ thống gửi thông báo tuyển dụng tới ứng viên
```

``` dưa chuột
Ứng viên đã hoàn tất quá trình tuyển dụng
Khi HR gửi kết quả từ chối
Sau đó hệ thống gửi thông báo từ chối tới ứng viên
```

``` dưa chuột
Với thông báo kết quả được gửi thành công
Khi ứng viên mở trang trạng thái đơn đăng ký
Sau đó, kết quả cuối cùng được hiển thị chính xác
```

---

##US-18: Lên lịch phỏng vấn

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn đặt lịch phỏng vấn để những ứng viên được chọn có thể chuyển sang giai đoạn phỏng vấn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi chọn ứng viên, người phỏng vấn, ngày phỏng vấn, thời gian phỏng vấn và thông tin cuộc họp
Sau đó hệ thống tạo lịch phỏng vấn thành công
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi cố gắng lên lịch phỏng vấn mà không chọn người phỏng vấn
Sau đó, hệ thống ngăn chặn việc lập lịch và hiển thị thông báo trường bắt buộc
```

``` dưa chuột
Do ứng viên được chọn không ở trạng thái Sàng lọc
Khi tôi cố gắng sắp xếp một cuộc phỏng vấn
Khi đó hệ thống sẽ ngăn việc lập lịch và hiển thị thông báo trạng thái không hợp lệ
```

``` dưa chuột
Cho một cuộc phỏng vấn được lên lịch thành công
Khi lịch trình được tạo
Sau đó, trạng thái ứng viên thay đổi thành Đã lên lịch phỏng vấn
```

---

## US-19: Phân công người phỏng vấn

**Câu chuyện của người dùng**

Là một nhà tuyển dụng nhân sự, tôi muốn phân công người phỏng vấn cho các ứng viên, để mỗi cuộc phỏng vấn đều có một người đánh giá có trách nhiệm.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi chỉ định một người phỏng vấn cho một cuộc phỏng vấn ứng viên
Sau đó, người phỏng vấn có thể xem cuộc phỏng vấn được chỉ định trong bảng điều khiển của họ
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là nhà tuyển dụng nhân sự
Khi tôi thay đổi người phỏng vấn được chỉ định
Khi đó người phỏng vấn cũ không thể xem được cuộc phỏng vấn nữa và người phỏng vấn mới có thể xem nó
```

``` dưa chuột
Vì tôi không phải là nhà tuyển dụng nhân sự
Khi tôi cố gắng chỉ định một người phỏng vấn
Sau đó hệ thống từ chối truy cập
```

---

## US-20: Hiển thị chi tiết cuộc phỏng vấn cho người phỏng vấn

**Câu chuyện của người dùng**

Với tư cách là nhà tuyển dụng nhân sự, tôi muốn những người phỏng vấn được chỉ định hiển thị chi tiết cuộc phỏng vấn để người phỏng vấn có thể chuẩn bị trước cuộc phỏng vấn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì HR đã lên lịch phỏng vấn và chỉ định người phỏng vấn
Khi người phỏng vấn mở bảng thông tin của họ
Sau đó người phỏng vấn có thể xem chi tiết cuộc phỏng vấn
```

``` dưa chuột
Do người phỏng vấn không được chỉ định tham gia phỏng vấn
Khi người phỏng vấn cố gắng mở chi tiết cuộc phỏng vấn
Sau đó hệ thống từ chối truy cập
```

``` dưa chuột
Được nhân sự cập nhật chi tiết cuộc phỏng vấn
Khi người phỏng vấn được chỉ định mở bảng thông tin
Sau đó người phỏng vấn có thể xem chi tiết cuộc phỏng vấn mới nhất
```

---

## US-21: Xem các cuộc phỏng vấn được chỉ định

**Câu chuyện của người dùng**

Với tư cách là người phỏng vấn, tôi muốn xem các cuộc phỏng vấn được chỉ định của mình để biết mình cần phỏng vấn những ứng viên nào.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là người phỏng vấn
Khi tôi mở bảng thông tin phỏng vấn của mình
Sau đó hệ thống chỉ hiển thị các cuộc phỏng vấn được giao cho tôi
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là người phỏng vấn
Khi tôi xem một cuộc phỏng vấn được chỉ định
Sau đó tôi có thể xem tên ứng viên, chương trình thực tập, ngày phỏng vấn, thời gian phỏng vấn và thông tin cuộc họp
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là người phỏng vấn
Khi tôi cố gắng xem một cuộc phỏng vấn được giao cho một người phỏng vấn khác
Sau đó hệ thống từ chối truy cập
```

---

## US-22: Xem hồ sơ và CV ứng viên được chỉ định

**Câu chuyện của người dùng**

Với tư cách là người phỏng vấn, tôi muốn xem hồ sơ và CV ứng viên được giao để có thể chuẩn bị cho cuộc phỏng vấn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi được giao phỏng vấn một ứng viên
Khi tôi mở chi tiết phỏng vấn ứng viên
Sau đó tôi có thể xem tóm tắt hồ sơ ứng viên
```

``` dưa chuột
Vì tôi được giao phỏng vấn một ứng viên
Khi tôi mở chi tiết phỏng vấn ứng viên
Sau đó tôi có thể xem hoặc tải CV ứng viên
```

``` dưa chuột
Vì tôi không được chỉ định vào một ứng cử viên
Khi tôi cố gắng xem hồ sơ hoặc CV của ứng viên
Sau đó hệ thống từ chối truy cập
```

---

## US-23: Gửi phản hồi phỏng vấn có cấu trúc

**Câu chuyện của người dùng**

Với tư cách là người phỏng vấn, tôi muốn gửi phản hồi phỏng vấn có cấu trúc để người quản lý nhân sự và tuyển dụng có thể đưa ra quyết định tốt hơn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi là người phỏng vấn được chỉ định
Khi tôi gửi phản hồi kèm theo xếp hạng, điểm mạnh, điểm yếu và đề xuất bắt buộc
Sau đó hệ thống lưu phản hồi thành công
```

``` dưa chuột
Vì tôi là người phỏng vấn được chỉ định
Khi tôi gửi phản hồi mà không có đánh giá hoặc đề xuất cần thiết
Sau đó, hệ thống ngăn chặn việc gửi và hiển thị thông báo xác thực
```

``` dưa chuột
Vì tôi không được chỉ định tham gia cuộc phỏng vấn ứng viên
Khi tôi cố gắng gửi phản hồi
Sau đó hệ thống từ chối truy cập
```

``` dưa chuột
Đưa ra phản hồi phỏng vấn được gửi thành công
Khi nhân sự xem trang chi tiết ứng viên
Sau đó nhân sự có thể xem phản hồi đã gửi
```

---

## US-24: Cung cấp Xếp hạng, Nhận xét và Đề xuất

**Câu chuyện của người dùng**

Với tư cách là người phỏng vấn, tôi muốn đưa ra đánh giá, nhận xét và đề xuất để phản hồi đó rõ ràng và hữu ích.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đang điền vào mẫu phản hồi
Khi tôi cung cấp tất cả các xếp hạng và đề xuất cần thiết
Sau đó hệ thống cho phép tôi gửi phản hồi
```

``` dưa chuột
Vì tôi đang điền vào mẫu phản hồi
Khi tôi để trống các trường xếp hạng bắt buộc
Sau đó hệ thống hiển thị thông báo xác nhận
```

``` dưa chuột
Vì tôi đang điền vào mẫu phản hồi
Khi tôi thêm nhận xét tùy chọn
Sau đó hệ thống lưu lại các bình luận kèm theo phản hồi
```

---

## US-25: Khuyến nghị Đạt, Thất bại hoặc Giữ

**Câu chuyện của người dùng**

Với tư cách là người phỏng vấn, tôi muốn đề xuất Đạt, Không đạt hoặc Giữ để hành động tuyển dụng tiếp theo dễ dàng quyết định hơn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đang gửi phản hồi phỏng vấn
Khi tôi chọn Đạt làm đề xuất
Sau đó hệ thống lưu Pass làm đề xuất của người phỏng vấn
```

``` dưa chuột
Vì tôi đang gửi phản hồi phỏng vấn
Khi tôi chọn Thất bại làm đề xuất
Sau đó hệ thống lưu Fail làm đề xuất của người phỏng vấn
```

``` dưa chuột
Vì tôi đang gửi phản hồi phỏng vấn
Khi tôi chọn Giữ làm đề xuất
Sau đó hệ thống lưu Giữ làm đề xuất của người phỏng vấn
```

``` dưa chuột
Vì tôi đang gửi phản hồi phỏng vấn
Khi tôi không chọn bất kỳ đề xuất nào
Sau đó, hệ thống ngăn chặn việc gửi và hiển thị thông báo đề xuất bắt buộc
```

---

## US-26: Chỉ truy cập các ứng viên được chỉ định

**Câu chuyện của người dùng**

Với tư cách là người phỏng vấn, tôi chỉ muốn truy cập những ứng viên được chỉ định cho mình để thông tin ứng viên được bảo mật.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là người phỏng vấn
Khi tôi mở danh sách ứng viên được chỉ định
Sau đó hệ thống chỉ hiển thị những ứng viên được phân công cho tôi
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là người phỏng vấn
Khi tôi cố gắng truy cập một ứng viên không được chỉ định cho tôi
Sau đó hệ thống từ chối truy cập
```

``` dưa chuột
Do nhân sự thay đổi người phỏng vấn được chỉ định
Khi tôi không còn được giao cho ứng viên nữa
Sau đó tôi không thể truy cập thông tin ứng viên đó được nữa
```

---

## US-27: Xem quy trình tuyển dụng

**Câu chuyện của người dùng**

Với tư cách là người quản lý tuyển dụng, tôi muốn xem quy trình tuyển dụng để có thể theo dõi tiến độ tuyển dụng.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là người quản lý tuyển dụng
Khi tôi mở bảng thông tin quy trình tuyển dụng
Sau đó tôi có thể xem số lượng ứng viên theo trạng thái
```

``` dưa chuột
Vì tôi đăng nhập với tư cách là người quản lý tuyển dụng
Khi tôi mở bảng thông tin quy trình tuyển dụng
Sau đó tôi có thể thấy các ứng viên được nhóm theo chương trình thực tập
```

``` dưa chuột
Vì tôi không phải là người quản lý tuyển dụng, nhà tuyển dụng nhân sự hay quản trị viên
Khi tôi cố truy cập vào bảng thông tin quy trình tuyển dụng
Sau đó hệ thống từ chối truy cập
```

---

##US-28: Xem phản hồi của ứng viên

**Câu chuyện của người dùng**

Với tư cách là người quản lý tuyển dụng, tôi muốn xem phản hồi của ứng viên để có thể hiểu được đánh giá của người phỏng vấn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là người quản lý tuyển dụng
Khi tôi mở trang chi tiết về ứng viên
Sau đó tôi có thể xem phản hồi phỏng vấn đã gửi
```

``` dưa chuột
Do một ứng viên chưa gửi phản hồi
Khi tôi mở trang chi tiết ứng viên
Khi đó hệ thống báo chưa có phản hồi
```

``` dưa chuột
Vì tôi không được ủy quyền
Khi tôi cố gắng xem phản hồi của ứng viên
Sau đó hệ thống từ chối truy cập
```

---

##US-29: So sánh thí sinh

**Câu chuyện của người dùng**

Với tư cách là người quản lý tuyển dụng, tôi muốn so sánh các ứng viên theo trạng thái, xếp hạng và phản hồi để có thể đưa ra quyết định tuyển dụng tốt hơn.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là người quản lý tuyển dụng
Khi tôi chọn nhiều ứng viên để so sánh
Sau đó, hệ thống sẽ hiển thị trạng thái, xếp hạng và tóm tắt phản hồi của họ cạnh nhau
```

``` dưa chuột
Vì tôi chọn ít hơn hai ứng viên
Khi tôi nhấp vào so sánh
Sau đó hệ thống hiện thông báo yêu cầu tôi chọn ít nhất 2 ứng viên
```

``` dưa chuột
Vì tôi không được ủy quyền
Khi tôi cố gắng sử dụng so sánh ứng viên
Sau đó hệ thống từ chối truy cập
```

---

##US-30: Phê duyệt quyết định tuyển dụng cuối cùng

**Câu chuyện của người dùng**

Với tư cách là người quản lý tuyển dụng, tôi muốn phê duyệt các quyết định tuyển dụng cuối cùng để các đề nghị tuyển dụng đó được kiểm soát trước khi gửi đi.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đăng nhập với tư cách là người quản lý tuyển dụng
Khi tôi chấp thuận quyết định đề nghị cuối cùng
Sau đó hệ thống ghi nhận phê duyệt thành công
```

``` dưa chuột
Do người quản lý tuyển dụng đã phê duyệt quyết định cuối cùng
Khi HR mở trang chi tiết ứng viên
Sau đó HR có thể thấy rằng quyết định đã được phê duyệt
```

``` dưa chuột
Vì tôi không phải là người quản lý tuyển dụng
Khi tôi cố gắng phê duyệt quyết định tuyển dụng cuối cùng
Sau đó hệ thống từ chối truy cập
```

---

## US-31: Quản lý tài khoản người dùng

**Câu chuyện của người dùng**

Với tư cách là quản trị viên hệ thống, tôi muốn tạo, cập nhật và hủy kích hoạt tài khoản người dùng để có thể quản lý quyền truy cập hệ thống.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi tạo tài khoản người dùng mới với thông tin hợp lệ
Sau đó hệ thống tạo tài khoản người dùng thành công
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi cập nhật thông tin của người dùng
Sau đó hệ thống lưu thông tin cập nhật
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi vô hiệu hóa tài khoản người dùng
Khi đó người dùng không thể đăng nhập vào hệ thống được nữa
```

``` dưa chuột
Vì tôi không phải là quản trị viên hệ thống
Khi tôi cố gắng quản lý tài khoản người dùng
Sau đó hệ thống từ chối truy cập
```

---

## US-32: Gán vai trò người dùng

**Câu chuyện của người dùng**

Với tư cách là quản trị viên hệ thống, tôi muốn chỉ định vai trò của người dùng để mỗi người dùng có quyền chính xác.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi chỉ định vai trò cho người dùng
Sau đó người dùng nhận được quyền của vai trò đó
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi thay đổi vai trò của người dùng
Sau đó, quyền truy cập của người dùng sẽ được cập nhật dựa trên vai trò mới
```

``` dưa chuột
Vì tôi không phải là quản trị viên hệ thống
Khi tôi cố gắng phân công vai trò
Sau đó hệ thống từ chối truy cập
```

---

## US-33: Cấu hình các chương trình thực tập

**Câu chuyện của người dùng**

Với tư cách là quản trị viên hệ thống, tôi muốn tạo và cập nhật các chương trình thực tập để bộ phận nhân sự có thể quản lý các chiến dịch tuyển dụng khác nhau.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi tạo một chương trình thực tập với thông tin hợp lệ
Sau đó hệ thống tạo chương trình thành công
```

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi cập nhật một chương trình thực tập
Sau đó hệ thống lưu thông tin chương trình đã cập nhật
```

``` dưa chuột
Do một chương trình thực tập đã kết thúc
Khi một ứng viên cố gắng nộp đơn vào chương trình đó
Sau đó hệ thống ngăn chặn việc nộp đơn
```

---

## US-34: Xem nhật ký hoạt động hệ thống

**Câu chuyện của người dùng**

Với tư cách là quản trị viên hệ thống, tôi muốn xem nhật ký hoạt động của hệ thống để có thể kiểm tra các hành động quan trọng.

**Tiêu chí chấp nhận**

``` dưa chuột
Vì tôi đã đăng nhập với tư cách quản trị viên hệ thống
Khi tôi mở trang nhật ký hoạt động
Sau đó hệ thống hiển thị các thao tác quan trọng của hệ thống
```

``` dưa chuột
Đưa ra một nhà tuyển dụng nhân sự cập nhật trạng thái ứng viên
Khi cập nhật được lưu thành công
Sau đó hành động được ghi lại vào nhật ký hoạt động
```

``` dưa chuột
Vì tôi không phải là quản trị viên hệ thống
Khi tôi cố truy cập trang nhật ký hoạt động
Sau đó hệ thống từ chối truy cập
```

## 4. Danh sách kiểm tra chất lượng tiêu chí chấp nhận

| Mục danh sách kiểm tra | Mô tả |
|---|---|
| Điều kiện rõ ràng | Phần đã cho giải thích tình huống bắt đầu. |
| Hành động rõ ràng | Phần Khi giải thích những gì người dùng hoặc hệ thống làm. |
| Kết quả rõ ràng | Phần Then giải thích kết quả mong đợi. |
| Có thể kiểm tra | QA có thể tạo các trường hợp thử nghiệm từ các tiêu chí chấp nhận. |
| Liên kết với câu chuyện của người dùng | Mỗi tiêu chí chấp nhận thuộc về một câu chuyện của người dùng. |
| Bao gồm các trường hợp tiêu cực | Lỗi quan trọng hoặc trường hợp không hợp lệ được bao gồm. |
| Bao gồm các quy tắc cấp phép | Kiểm soát truy cập được bao gồm khi cần thiết. |
| Trận đấu SRS | Tiêu chí chấp nhận phải phù hợp với yêu cầu chức năng, quy tắc xác thực và quy tắc cấp phép trong SRS. |

##5. BA Ghi chú

Tiêu chí chấp nhận làm cho câu chuyện của người dùng có thể kiểm tra được và giảm sự hiểu lầm giữa các bên liên quan, nhà phát triển và kỹ sư QA.

Trong dự án này, tiêu chí chấp nhận quan trọng nhất tập trung vào xác thực biểu mẫu, quy tắc tải tệp lên, quy tắc chuyển đổi trạng thái, quy tắc lên lịch phỏng vấn, quy tắc gửi phản hồi và kiểm soát quyền truy cập dựa trên vai trò.

Bước tiếp theo là tạo thông số wireframe cho màn hình chính của InternshipHub.