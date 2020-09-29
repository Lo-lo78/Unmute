# NVDA Bật âm thanh

* Tác giả: Oleksandr Gryshchenko
* Phiên bản: 1.0
* Tải về [phiên bản chính thức][1]

Add-on này kiểm tra trạng thái âm thanh hệ thống của Windows khi khởi động NVDA.
Nếu nhận thấy rằng âm thanh bị tắt thì add-on sẽ  bật nó lên.

## Các thay đổi

### Phiên bản 1.0. Thực hiện tính năng
Add-on sử dụng một module của bên thứ ba [Windows Sound Manager][2].

## Tùy biến NVDA Bật âm thanh
Bạn có thể tạo bản sao (clone) cho add-on này để thực hiện các tùy biến cho nó.

### Các thư viện phụ thuộc của bên thứ ba
Chúng có thể được cài đặt với pip:
- markdown
- scons
- python-gettext

### Để đóng gói và phân phối add-on:
1. Mở một ứng dụng dòng lệnh, điều hướng đến thư mục gốc của kho add-on này
2. Gõ lệnh **scons**. Gói add-on sẽ được tạo ở thư mục hiện tại nếu không có lỗi xảy ra.

[1]: https://github.com/grisov/Unmute/releases/download/v1.0/unmute-1.0.nvda-addon
[2]: https://github.com/Paradoxis/Windows-Sound-Manager