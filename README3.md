
## Mục Lục
1. HTML
2. CSS
3. Fonts
4. Images
5. JavaScript
6. Server (trong tiến trình)
7. JS Frameworks (trong tiến trình)


## Giới thiệu


Hiệu năng là một chủ đề lớn, nhưng không phải lúc nào cũng là chủ đề "back-end" hoặc "admin": Đó cũng là một phần trách nhiệm của Front-end nữa Danh sách kiểm tra hiệu suất Front-End là một Checklist đầy đủ các yếu tố tiên quyết cần phải kiểm tra hoặc ít nhất là nhận thức được, như một nhà phát triển Front-End và áp dụng cho dự án của bạn (cá nhân và chuyên nghiệp).


## Làm thế nào để sử dụng ?


Đối với mỗi quy tắc, bạn sẽ có một đoạn giải thích lý do tại sao quy tắc này quan trọng và các bạn có thể khắc phục nó. Để biết thêm thông tin chi tiết, bạn nên tìm các liên kết trỏ tới 🛠 tools, 📖 articles hoặc 📹 medias để có thể hoàn thành Checklist.

Tất cả các mục trong Checklist kiểm tra hiệu suất mặt trước là những yếu tố cần thiết để đạt được điểm hiệu suất cao nhất nhưng bạn sẽ tìm thấy chỉ thị để giúp bạn ưu tiên một số quy tắc khác. Có 3 mức độ ưu tiên:

LOW có nghĩa là danh mục con ưu tiên thấp.


MEDIUM có nghĩa là danh mục được ưu tiên mức trung bình, bạn nên xử lý và sắp xếp những danh mục con này


HIGH có nghĩa là danh mục con được ưu tiên cao. Bạn không thể tránh tuân thủ theo những quy tắc đó và cần thực hiện những phương pháp để sửa chữa.


## Hiệu năng tools


Danh sách công cụ bạn nên sử dụng để kiểm thử màn hinh, website hoặc ứng dụng của bạn


🛠 WebPagetest - Kiểm tra tối ưu hóa hiệu suất và tối ưu hóa trang web

🛠 ☆ Dareboost: Kiểm tra tốc độ trang web và phân tích trang web (sử dụng phiếu giảm giá WPCDD20 cho -20%)


🛠 Treo: Giám sát tốc độ load trang


🛠 GTmetrix | Tốc độ trang web và tối ưu hóa hiệu suất


🛠 Thông tin chi tiết về tốc độ trang


🛠 Kiểm tra tốc độ trang web-Pingdom


📖 Làm cho trang web nhanh hơn | Google Developers


🛠 Sitespeed.io - Chào mừng bạn đến với thế giới web diệu kỳ


🛠 Calibre


🛠 Kiểm tra tốc độ trang web | Kiểm tra hiệu suất Web »Dotcom-Tools


🛠 Giám sát thời gian hoạt động của máy chủ và trang web - Pingdom (Liên kết đăng ký miễn phí)


🛠 Uptime Robot


🛠 SpeedCurve: Giám sát hiệu suất front-end


🛠 Công cụ PWMetrics - CLI và lib để thu thập số liệu hiệu suất


🛠 Varvy - Tối ưu hóa tốc độ trang


🛠 Lighthouse - Google


🛠 Tiện ích mở rộng trình duyệt Checkbot - Kiểm tra các phương pháp hay nhất về hiệu suất web


🛠 Công cụ Lab vàng | Kiểm tra trực tuyến để giúp tăng tốc các trang web nặng


## Tài liệu tham khảo


📹 Chi phí của JavaScript - YouTube (phiên bản text)


AddyOsmani.com - Bắt đầu Lập ngân sách Hiệu suất


📖 Bắt đầu với phân tích hiệu suất thời gian chạy | Google Developers


📖 Trạng thái của Web | 2018_01_01


📖 Độ nặng của trang không quan trọng


📖 Hiệu năng Checklist Front-End 2018 [PDF, Apple Pages]


📖 Thiết kế cho hiệu suất Cân nặng thẩm mỹ và tốc độ - Bởi Lara Callender Hogan [eBook, In]


📖 Varvy - Thuật ngữ hiệu suất Web


📖 fabkrum / web-performance-resources: Cập nhật bộ sưu tập tài nguyên hiệu suất web có giá trị


📖 Checkbot - Các phương pháp hay nhất về tốc độ web


🛠 Công cụ lũy tiến - Danh sách các công cụ của bên thứ ba được xây dựng bởi cộng đồng có thể được sử dụng để cải thiện hiệu suất trang


## HTML


HTML được rút gọn: trung bình Mã HTML được rút gọn, các chú thích, khoảng trắng và các dòng mới sẽ bị xóa khỏi các tệp khi xuất bản.


Lý do :


Xóa tất cả các khoảng trống, nhận xét và ngắt những câu không cần thiết sẽ giảm kích thước HTML của bạn và tăng tốc thời gian tải trang web của bạn và rõ ràng làm giảm tải xuống cho người dùng của bạn.


Như thế nào :


Hầu hết các khung công tác đều có các plugin để tạo điều kiện tối giản hóa các trang web. Bạn có thể sử dụng một loạt các mô-đun NPM có thể thực hiện công việc cho bạn một cách tự động.


🛠 Trình chỉnh sửa HTML | Giảm bớt code


🛠 Công cụ nén HTML trực tuyến


📖 Thử nghiệm với trình chỉnh sửa HTML - Sự tiêu diệt hoàn hảo


Xóa các nhận xét không cần thiết: Đảm bảo rằng các nhận xét được xóa khỏi các trang của bạn.


🛠 remove-html-comments - npm

Loại bỏ các thuộc tính không cần thiết: Gõ các thuộc tính như type = "text / javascript" hoặc type = "text / css".


<!-- Before HTML5 -->
<script type="text/javascript">
    // JavaScript code
</script>

<!-- Today -->
<script>
    // JavaScript code
</script>


Lý do: Các thuộc tính type không cần thiết vì HTML5 như text / css và text / javascript là các giá trị mặc định. Code không sử dụng sẽ bị xóa khi không được trang web hoặc ứng dụng của bạn sử dụng .


Bằng cách : Đảm bảo rằng tất cả các thẻ <link> và <script> của bạn không có thuộc tính type nào.
  
  
📖 Thẻ Script | CSS-Tricks

  
Luôn đặt thẻ CSS trước thẻ JavaScript: Và nhớ đảm bảo rằng CSS của bạn luôn được tải trước khi có mã JavaScript.


<!-- Not recommended -->
<script src="jquery.js"></script>
<script src="foo.js"></script>
<link rel="stylesheet" href="foo.css"/>

<!-- Recommended -->
<link rel="stylesheet" href="foo.css"/>
<script src="jquery.js"></script>
<script src="foo.js"></script>


Lý do: thẻ css tags được đặt trước Javascript sẽ giúp tăng tốc thời gian hiển thị của trình duyệt.


Bằng cách: Đảm bảo rằng <link> và <style> trong <head> của bạn luôn ở trước <script>.
  

📖 Các kiểu Order và script của bạn cho pagespeed


Giảm thiểu số iframe: Chỉ sử dụng iframe nếu bạn không có khả năng kỹ thuật nào khác. Cố gắng tránh ifram nhiều nhất có thể.


⬆ Về đầu trang.
