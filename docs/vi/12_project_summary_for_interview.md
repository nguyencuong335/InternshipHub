#12. Tóm tắt dự án để phỏng vấn

## 1. Quảng cáo chiêu hàng dự án

**InternshipHub** là một nền tảng quản lý tuyển dụng dựa trên web được thiết kế dành riêng cho vòng đời thực tập. Nó hợp lý hóa và tự động hóa quy trình đăng ký ứng viên, xác thực tự động, sàng lọc nhân sự, lên lịch phỏng vấn, thu thập phản hồi và phê duyệt tuyển dụng cuối cùng. Bằng cách cung cấp một hệ thống hồ sơ duy nhất, nó thay thế các công cụ giao tiếp rời rạc và bảng tính thủ công, giảm khối lượng công việc hành chính và cải thiện chất lượng tuyển dụng.

## 2. Vấn đề kinh doanh

Trước khi có hệ thống này, công ty đã quản lý tuyển dụng thực tập sinh thông qua các chuỗi email rời rạc, ứng dụng trò chuyện và bảng tính theo dõi. Điều này gây ra một số điểm khó khăn khi vận hành:
- **Kém hiệu quả:** Bộ phận nhân sự theo dõi thủ công trạng thái ứng viên và lên lịch phỏng vấn, gây ra chi phí quản trị cao.
- **Tính minh bạch thấp:** Ứng viên không có cách nào để theo dõi trạng thái đơn đăng ký của mình, dẫn đến yêu cầu về trạng thái quá mức.
- **Phản hồi không có cấu trúc:** Người phỏng vấn gửi phản hồi qua trò chuyện hoặc email ở nhiều định dạng khác nhau, khiến việc so sánh các kỹ năng của ứng viên một cách khách quan trở nên khó khăn.
- **Kho chứa thông tin:** Người quản lý tuyển dụng không có bảng điều khiển trung tâm để xem dữ liệu về nguồn ứng viên, gây ra sự chậm trễ trong các quyết định tuyển dụng.
- **Khả năng kiểm tra kém:** Không tồn tại nhật ký lịch sử về các thay đổi trạng thái ứng viên để theo dõi hiệu suất của nhà tuyển dụng hoặc đảm bảo tuân thủ quy trình.

## 3. Các bên liên quan chính

- **Ứng viên:** Gửi đơn đăng ký, tải CV lên và xem cập nhật trạng thái đơn đăng ký.
- **Nhà tuyển dụng nhân sự:** Quản lý hồ sơ, sàng lọc hồ sơ, lên lịch phỏng vấn, phân công người phỏng vấn và xử lý việc chuyển đổi trạng thái ứng viên.
- **Người phỏng vấn:** Xem xét hồ sơ ứng viên được chỉ định, tiến hành phỏng vấn và gửi phản hồi có cấu trúc (xếp hạng, nhận xét, đề xuất).
- **Người quản lý tuyển dụng:** Giám sát quy trình tuyển dụng, so sánh các ứng viên và ký kết các quyết định tuyển dụng cuối cùng.
- **Quản trị viên hệ thống:** Quản lý tài khoản người dùng, định cấu hình vai trò và quyền cũng như duy trì siêu dữ liệu của chương trình thực tập.

## 4. Yêu cầu chính

Giải pháp được cấu trúc thành năm mô-đun cốt lõi:
1. **Mô-đun ứng viên:** Đăng ký/đăng nhập tài khoản, tạo hồ sơ, tải lên tệp CV có xác thực (PDF/DOCX, <=5MB) và gửi đơn đăng ký.
2. **Mô-đun tuyển dụng nhân sự:** Bảng điều khiển ứng dụng với tìm kiếm/bộ lọc, cập nhật trạng thái với xác thực chuyển tiếp, lên lịch phỏng vấn và phân phối đề nghị/từ chối.
3. **Mô-đun người phỏng vấn:** Bảng điều khiển về ứng viên được chỉ định, người xem CV ứng viên và biểu mẫu phản hồi có cấu trúc (đánh giá về kỹ thuật/giao tiếp, nhận xét, đề xuất).
4. **Mô-đun quản lý tuyển dụng:** Bảng điều khiển tổng quan về quy trình, công cụ so sánh ứng viên và quy trình phê duyệt tuyển dụng.
5. **Mô-đun quản trị:** Quản lý người dùng/vai trò, cấu hình chương trình thực tập và trình xem nhật ký kiểm tra.

## 5. Quy trình AS-IS và TO-BE

- **AS-IS (Quy trình thủ công):** Ứng dụng email của ứng viên -> Nhân sự tải CV xuống và ghi vào bảng tính theo cách thủ công -> Nhân sự liên hệ với ứng viên theo cách thủ công để lên lịch phỏng vấn -> Tiến hành phỏng vấn -> Người phỏng vấn gửi văn bản phản hồi qua email/Slack -> Nhân sự cập nhật bảng tính theo cách thủ công -> Người quản lý tuyển dụng đưa ra quyết định cuối cùng dựa trên các cuộc thảo luận đặc biệt -> Nhân sự gửi thông báo cuối cùng theo cách thủ công.
- **TO-BE (Quy trình do hệ thống điều khiển):** Ứng viên đăng ký trên cổng thông tin -> Ứng viên tải CV lên -> Hệ thống xác thực loại/kích thước tệp và tạo đơn đăng ký -> Nhân sự xem xét hồ sơ ứng viên trong hệ thống -> Nhân sự lên lịch phỏng vấn và phân công người phỏng vấn trong ứng dụng -> Hệ thống tự động gửi thông báo -> Người phỏng vấn gửi biểu mẫu phản hồi có cấu trúc trong ứng dụng -> Người quản lý tuyển dụng xem quy trình và phản hồi tổng hợp để đưa ra quyết định -> Hệ thống ghi lại lịch sử trạng thái và giúp nhân sự gửi các đề nghị/từ chối cuối cùng.

## 6. Phần khó nhất

Khía cạnh thách thức nhất của dự án này là xác định **Quy tắc chuyển đổi trạng thái ứng viên** và thực thi **Ma trận quyền** tương ứng.
- **Thách thức:** Buộc ứng viên chỉ chuyển đổi trạng thái trong vòng đời đã được phê duyệt (ví dụ: ngăn nhà tuyển dụng chuyển ứng viên từ "Bản nháp" trực tiếp sang "Đã lên lịch phỏng vấn" hoặc từ "Bị từ chối" sang "Được đề nghị" mà không có sự cho phép thích hợp).
- **Giải pháp:** Tôi đã vạch ra các chuyển đổi trạng thái thành ma trận chuyển đổi trạng thái và viết Quy tắc xác thực cụ thể (VR-07 đến VR-10). Sau đó, tôi đã tạo Ma trận quyền chi tiết hiển thị chính xác những hành động tính năng mà mỗi vai trò người dùng có thể thực hiện, đảm bảo Kiểm soát truy cập dựa trên vai trò (RBAC) nghiêm ngặt.

## 7. Những điều tôi học được

Thông qua dự án này, tôi đã củng cố kỹ năng phân tích kinh doanh toàn diện của mình:
- **Luồng logic:** Đã học cách cấu trúc các yêu cầu một cách hợp lý, truy tìm từ các vấn đề kinh doanh cấp cao cho đến các thông số chức năng, câu chuyện của người dùng, tiêu chí chấp nhận và kịch bản thử nghiệm.
- **Thông số kỹ thuật có cấu trúc:** Hiểu rằng các yêu cầu phải rõ ràng, có thể kiểm tra và không có sự mơ hồ (ví dụ: sử dụng kích thước tệp cụ thể như "5 MB" hoặc các quy tắc chuyển đổi trạng thái nghiêm ngặt) để tránh sai lệch với nhà phát triển và QA.
- **Khả năng truy xuất nguồn gốc:** Nhận thấy tầm quan trọng đặc biệt của Ma trận truy xuất nguồn gốc yêu cầu (RTM) để đảm bảo rằng mọi mục tiêu kinh doanh đều được giải quyết theo yêu cầu chức năng, ánh xạ tới câu chuyện của người dùng và được xác minh bằng các kịch bản thử nghiệm.

## 8. Tôi sẽ trình bày dự án này như thế nào trong một cuộc phỏng vấn

1. **Bắt đầu với "Tại sao" (Giá trị Kinh doanh):** Tôi sẽ định hình dự án bằng cách giải thích vấn đề kinh doanh trước tiên—việc tuyển dụng thủ công đã gây ra sự chậm trễ, chi phí quản trị cao và trải nghiệm ứng viên kém như thế nào.
2. **Tìm hiểu về phương pháp luận:** Tôi sẽ mô tả quy trình của mình từ xác định các bên liên quan và lập mô hình AS-IS đến chuyển các nhu cầu kinh doanh sang BRD và SRS.
3. **Làm nổi bật các thành phần chính:** Tôi sẽ trình bày cách tôi phân tách các yêu cầu chức năng thành các câu chuyện của người dùng Agile với các tiêu chí chấp nhận Cho trước khi nào rõ ràng và cách tôi cộng tác với QA bằng cách xác định các kịch bản thử nghiệm.
4. **Thể hiện giải pháp xung đột/sự phức tạp:** Tôi sẽ sử dụng các quy tắc chuyển đổi trạng thái và ma trận quyền làm ví dụ về cách tôi giải quyết logic kinh doanh phức tạp và chuyển nó thành các quy tắc rõ ràng để phát triển.
5. **Tóm tắt bằng kết quả:** Tôi sẽ kết luận bằng cách chỉ ra các số liệu thành công (ví dụ: giảm 50% nỗ lực theo dõi thủ công và cải thiện độ chính xác của cập nhật trạng thái lên 95%).