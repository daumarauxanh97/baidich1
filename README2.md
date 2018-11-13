## Hướng dẫn cho git

## "flight rules" là gì?

Một bản hướng dẫn cho phi hành gia(bây giờ lập trình viên sử dụng git)nói về nên làm gì khi mọi chuyện tồi tệ.

Flight Rules là kinh nghiệm xương máu được ghi chép vào sổ sách mà liệt kê,từng bước một,phải làm gì nếu X xảy ra và tại sao.
Về cơ bản, chúng là các quy trình vận hành tiêu chuẩn cụ thể theo từng kịch bản cụ thể. 

NASA đã thu thập những lôi lẫm,tai họa và giải pháp kẻ từ đầu năm 1960,khi mà Mercury-era ground teams bắt đầu thu thập  "lessons learned" vào một bản tóm tắt mà bây giờ hàng nghìn trường hợp còn mơ hồ từ hỏng động cơ và tới thất bại tới trục trặc máy tính. Và cách giải quyết của bọn họ

## Quy ước cho văn bản này


Vì mục đích rõ ràng, tất cả các ví dụ trong tài liệu này sử dụng tùy chỉnh bash để chỉ ra nhánh hiện tại và có hay không có các thay đổi theo giai đoạn Nhánh được đặt trong dấu ngoặc đơn và dấu * bên cạnh tên chi nhánh cho biết các thay đổi được tùy chỉnh.

Tất cả các lệnh sẽ hoạt động với phiên bản thấp nhất là 2.13.0. Bạn nên ghé thăm trang web git để cập nhật thêm phiên bản git cục bộ.

## Mục lục được khởi tạo bằng DocToc

- [Kho lưu trữ](Kho lưu trữ)
- [Tôi muốn bắt đầu một kho lưu trữ cục bộ](#Tôi muốn bắt đầu một kho lưu trữ cục bộ)
- [Tôi muốn sao lưu một kho lưu trữ từ xa](Tôi muốn sao lưu một kho lưu trữ từ xa)
- [Cập nhập thay đổi](Cập nhập thay đổi)
- [Tôi vừa commit điều gì?](Tôi vừa commit điều gì?)
