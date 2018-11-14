## Hướng dẫn cho git

## "flight rules" là gì?

Một bản hướng dẫn cho phi hành gia(bây giờ lập trình viên sử dụng git)nói về nên làm gì khi mọi chuyện tồi tệ.

Flight Rules là kinh nghiệm xương máu được ghi chép vào sổ sách mà liệt kê,từng bước một,phải làm gì nếu X xảy ra và tại sao.
Về cơ bản, chúng là các quy trình vận hành tiêu chuẩn cụ thể theo từng kịch bản cụ thể. 

NASA đã thu thập những lôi lẫm,tai họa và giải pháp kẻ từ đầu năm 1960,khi mà Mercury-era ground teams bắt đầu thu thập  "lessons learned" vào một bản tóm tắt mà bây giờ hàng nghìn trường hợp còn mơ hồ từ hỏng động cơ và tới thất bại tới trục trặc máy tính. Và cách giải quyết của bọn họ

## Quy ước cho văn bản này


Vì mục đích rõ ràng, tất cả các ví dụ trong tài liệu này sử dụng tùy chỉnh bash để chỉ ra nhánh hiện tại và có hay không có các thay đổi theo giai đoạn Nhánh được đặt trong dấu ngoặc đơn và dấu * bên cạnh tên chi nhánh cho biết các thay đổi được tùy chỉnh.

Tất cả các lệnh sẽ hoạt động với phiên bản tối thiểu là 2.13.0. Ghé thăm website git để cập nhật phiên bản git của bạn.

## Mục lục được khởi tạo bằng DocToc

## Repositories

Tôi muốn tạo một Repository cục bộ

Tôi muốn sao lưu Repository từ bên ngoài

Thay đổi các Commit

Tôi vừa commit điều gì?

Tôi viết sai trong một tin nhắn commit

Tôi commit với tên bị sai và email đã định cấu hình

Tôi muốn xóa một file từ lần commit trước đó

Tôi muốn xóa commit lần gần nhất

Xóa commit tùy ý

Tôi thử đẩy commit đã sủa đổi lên một remote,nhưng nhận được thông báo lỗi

Tôi vô tình thực hiện khôi phục cài đặt và tôi muốn lấy lại những gì tôi đã thay đổi

Tôi vô tình commit và hợp nhất chúng với nhau

Tôi vô tình commit vầ đẩy lên file chứa dữ liệu nhạy cảm

## Staging

Tôi cần thêm nhãn thay đổi theo giai đoạn vào commit trước đó

Tôi muốn stage một phần của file mới nhưng không phải cả file

Tôi muốn thay đổi một file ở 2 commit khác nhau

Tôi muốn stage cái thay đổi chưa được stage của tôi và bỏ stage cái thay đổi đã được stage

Thay đổi chưa được stage

Tôi muốn rời thay đổi chưa được stage của tôi xang một branch mới

Tôi muốn rơi thay đổi chưa được stage của tôi xang một branch khác đã tồn tại

Tôi muốn loại bỏ những thay đổi cục bộ chưa được commit(stage và chưa được stage)

Tôi muốn loại bỏ cụ thể một thay đổi chưa được stage

Tôi muốn loại bỏ cụ thể một file chưa được stage

Tôi chỉ muốn loại bỏ  thay đổi cục bộ chưa được stage

Tôi muốn loại bỏ tất cả file untracked

Tôi muốn bỏ satge một file đã được stage

## Branches

Tôi muốn liệt kê tất cả các branch

Tạo một brach từ một commit

Tôi lấy nhầm/đẩy nhầm branch

Tôi muốn loại bỏ commit cục bộ để brach giốn cái trên server

Tôi commit vào master thay vì brach mới

Tôi muốn giữ cả file từ một ref-ish khác

Tôi đã commit vài lần trên cùng một brach mà nó nên ở trên branch khác

Tôi vô tình xóa branch của tôi

Tôi muốn xóa một branch

Tôi muốn xóa nhiều branch 

Tôi muốn đổi tôi một branch

Tôi muốn kiểm tra một branch bên ngoài mà người khác đang làm

Tôi muốn tạo một branch bên ngoài từ cái branch cục bộ

Tôi muốn đặt branch bên ngoài đồng bội với branch cục bộ của tôi

Tôi muốn đặt HEAD của tôi 
