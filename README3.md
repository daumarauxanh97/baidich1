
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


## CSS


Rút gọn [cao] Tất cả các tệp CSS được rút gọn, nhận xét, khoảng trắng và dòng mới sẽ bị xóa khỏi tệp khi được upload.


Lý do: Khi các tệp CSS được rút gọn, nội dung được tải nhanh hơn và ít dữ liệu hơn được gửi đến máy khách. Điều quan trọng là luôn luôn giảm thiểu các tệp CSS trong quá trình sản xuất. Nó có lợi cho người dùng vì nó là dành cho tất cả những doanh nghiệp muốn giảm chi phí băng thông và sử dụng tài nguyên thấp hơn.

Bằng cách: Sử dụng công cụ giảm thiểu những file tự động trước hoặc trọng khi sản phẩm của bạn được phát triển


🛠 cssnano: A một mô đun rút gọn theo hệ sinh thái PostCSS. - cssnano


🛠 @neutrinojs/style-minify - npm


🛠 Công cụ nén css trực tuyến


Nối: các tệp CSS trung bình được nối trong một tệp duy nhất (Không phải lúc nào cũng hợp lệ cho HTTP / 2).


<!-- Not recommended -->
<link rel="stylesheet" href="foo.css"/>
<link rel="stylesheet" href="bar.css"/>

<!-- Recommended -->
<link rel="stylesheet" href="foobar.css"/>



Lý do: Nếu bạn vẫn sử dụng HTTP/1, bạn có thể vẫn cần nối những file của bạn, nó sẽ ít chính xác hơn so với khi bạn sử dụng máy chủ HTTP/2 (kiểm thử nên được thực hiện)


Bằng cách: Sử dụng công cụ online hoặc bất kỳ plugin hoặc trong khi bạn xây dựng hoặc phát triển nối lại những file của ban.


- Đảm bảo đằng project của bạn khi nối sẽ không bị gãy đoạn hoặc dang dở.


📖 HTTP: Tối ưu hóa phân phối ứng dụng - Mạng trình duyệt hiệu suất cao (O'Reilly)


📖 Các phương pháp hay nhất về hiệu năng trong kỷ nguyên HTTP / 2


Không chặn: tệp CSS cần phải không bị chặn để ngăn DOM lấy thời gian tải.


<link rel="preload" href="global.min.css" as="style" onload="this.rel='stylesheet'">
<noscript><link rel="stylesheet" href="global.min.css"></noscript>


Lý do: Tệp CSS có thể chặn tải trang và trì hoãn hiển thị trang của bạn. Sử dụng preload thực sự có thể tải các tệp CSS trước khi trình duyệt bắt đầu hiển thị nội dung của trang.


🛠 loadCSS bởi nhóm filament


📖 Ví dụ về tải trước CSS bằng cách sử dụng loadCSS


📖 Tải trước nội dung với rel = "preload"


📖 Tải trước: Điều gì là tốt nhất? - Tạp chí Smashing


Độ dài của các lớp CSS: Độ dài của các lớp học của bạn có thể có tác động (nhẹ) trên các tệp HTML và CSS của bạn .

Lý do: Ngay cả các tác động hiệu suất có thể bị tranh chấp, đưa ra quyết định về chiến lược đặt tên liên quan đến dự án của bạn có thể có tác động đáng kể đến khả năng bảo trì của stylesheets. Nếu bạn đang sử dụng BEM, trong một số trường hợp, bạn có thể kết thúc với các lớp có nhiều ký tự hơn mức cần thiết. Việc lựa chọn một cách khôn ngoan tên cũng như không gian tên của bạn luôn là điều quan trọng và cấp thiết nhất.


Bằng cách : Đặt giới hạn về số lượng ký tự có thể thú vị đối với một số người, nhưng Chắc chắn rằng bạn có thể đã phá vỡ trang web của bạn vì trong các thành phần có thể giúp giảm số lượng lớp (như khai báo) và độ dài của class.


🛠 Dài so với lớp ngắn · jsPerf


CSS không sử dụng: phương tiện Xóa các bộ chọn CSS không sử dụng.


Lý do: Việc xóa bộ chọn CSS không được sử dụng có thể giảm kích thước tệp của bạn và sau đó tăng tốc tải nội dung của bạn.


Bằng cách: ⁃ ⚠️ Luôn kiểm tra xem CSS khung bạn muốn sử dụng chưa có mã reset  / chuẩn hóa chưa. Đôi khi bạn có thể không cần mọi thứ nằm trong tệp reset  / chuẩn hóa của bạn.

🛠 UnCSS Online


🛠 PurifyCSS


🛠 PurgeCSS


🛠 Chrome DevTools Coverage


CSS Critical: CSS Critical ("trong màn hình đầu tiên") thu thập tất cả CSS được sử dụng để hiển thị phần hiển thị của trang. Nó được nhúng trước khi gọi CSS chính của bạn và giữa <style> </ style> trong một dòng đơn (nó sẽ được rút gọn nếu có thể).


Lý do: Inlining CSS quan trọng giúp tăng tốc độ hiển thị của các trang web làm giảm số lượng yêu cầu đến máy chủ.


Bằng cách: Tạo CSS quan trọng với các công cụ trực tuyến hoặc sử dụng một plugin giống như plugin mà Addy Osmani đã phát triển.


📖 Hiểu Critical CSS


🛠 Bình luận của Addy Osmani trên GitHub tự động hóa điều này.


📖 Inlining Critical CSS cho hiệu suất web tốt hơn 


🛠 Trình tạo đường dẫn Critical CSS - Ưu tiên nội dung trong màn hình đầu tiên :: SiteLocity


📖 Giảm kích thước nội dung trong màn hình đầu tiên

CSS được nhúng hoặc nội tuyến: (high) Tránh sử dụng CSS nhúng hoặc nội tuyến bên trong <body> của bạn (Không hợp lệ cho HTTP / 2)

Lý do: Một trong những lý do là vì đó là một phương pháp hay để phân tách nội dung khỏi thiết kế. Nó cũng giúp bạn có một mã dễ bảo trì hơn và giữ cho trang web của bạn có thể truy cập được. Nhưng liên quan đến hiệu suất, nó đơn giản chỉ vì nó làm giảm kích thước tập tin của các trang HTML của bạn và thời gian tải.

Bằng cách : Luôn sử dụng biểu định kiểu bên ngoài hoặc nhúng CSS trong <head> của bạn (và thực hiện theo các quy tắc hiệu suất CSS khác)
    
   
📖 Quan sát thực tiễn tốt nhất của CSS: Tránh các kiểu nội tuyến CSS


Phân tích độ phức tạp của stylesheets : Phân tích bảng định kiểu của bạn có thể giúp bạn đánh dấu các vấn đề dư thừa và bộ chọn CSS trùng lặp.


Lý do: Đôi khi bạn có thể có lỗi thừa hoặc lỗi xác thực trong CSS, phân tích các tệp CSS của bạn và xóa những thứ phức tạp này có thể giúp bạn tăng tốc các tệp CSS (vì trình duyệt của bạn sẽ đọc nhanh hơn) 


Bằng cách: CSS của bạn nên được tổ chức, bằng cách sử dụng một bộ tiền xử lý CSS có thể giúp bạn với điều đó. Một số công cụ trực tuyến được liệt kê bên dưới cũng có thể giúp bạn phân tích và sửa mã của bạn.


🛠 TestMyCSS | Tối ưu hóa và kiểm tra hiệu suất CSS


🛠 Thống kê CSS


🛠 macbre / analysis-css: Bộ chọn CSS complexity và phân tích hiệu suất


🛠 Dự án Wallace giống như Thống kê CSS nhưng lưu trữ số liệu thống kê theo thời gian để bạn có thể theo dõi các thay đổi của mình


⬆ Trở về đầu trang

## Fonts

- :book: A Book Apart, Webfont Handbook
Định dạng webfont:Bạn đang sử dụng WOFF2 trên trang web hay ứng dụng của bạn

_Tại sao_

>Theo như google định dạng nén WOFF 2.0 Web Font cung cấp mức tăng trung bình 30% so với WOFF 1.0. Thật tốt khi sử dụng WOFF 2.0, WOFF 1.0 làm dự phòng và TTF.

_Làm như thế nào_

>Kiểm tra trước khi mua phông chữ mới xem nhà cung cấp cung cấp cho bạn định dạng WOFF2. Nếu bạn đang sử dụng phông chữ miễn phí, bạn luôn có thể sử dụng Font Squirrel để tạo tất cả các định dạng bạn cần.
  - :book: WOFF 2.0 –Hiểu biết thêm về thế hệ tiếp theo Web Font Format và chuyển đổi TTF xang WOFF2
  
  - 🛠  Tự tạo @font-face Kits » Font Squirrel
  
  - 🛠  IcoMoon App - Icon Font, SVG, PDF & PNG Generator
  
  - :book: Using @font-face | CSS-Tricks
  
  - :book: Can I use... WOFF2
  
### Sử dụng `preconnect` để load fonts nhanh hơn [medium] 
  
  
  
  
