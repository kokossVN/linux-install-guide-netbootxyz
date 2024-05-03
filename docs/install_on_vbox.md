# Hướng dẫn cài đặt máy ảo với Oracle Virtual Box


## Chuẩn bị 

- Máy tính cá nhân (hoặc ra net cũng được)
- tối thiểu 2GB RAM (Khuyên dùng 8GB RAM)

## Cài đặt

- Tải từ [trang chủ virtualbox](https://www.virtualbox.org/wiki/Downloads) và cài đặt
  - VirtualBox platform packages (Chọn hệ điều hành phù hợp)
  - VirtualBox Extension Pack (Chọn `All supported platforms`)

- Sau khi cài đặt thành công VirtualBox, Khởi chạy virtual box 

![vbox ui](../image/vbox_ui.png) 

- Chọn new để tạo máy ảo, sau đó đặt các tùy chọn như hình dưới (đặt tên tùy ý)

![vbox install1](../image/vbox_install1.png)

![vbox install2](../image/vbox_install2.png)

- Sau khi `Finish`, chọn `Settings`,chọn tab `System` và làm theo ảnh

![vbox install3](../image/vbox_install3.png)

- để boot vào USB, trước hết ấn `Start`, cancel tất cả các cửa sổ hiện ra và khi màn hình này xuất hiện

![vbox start1](../image/vbox_start_bios1.png) 
- ấn bất kỳ để vào BIOS

![vbox start2](../image/vbox_start_bios2.png) 
- sau đó ấn `Ctrl bên phải` thoát điều khiển máy ảo, ở trên Menu bar chọn `Devices > USB > [chọn usb cài đặt hệ điều hành]`.Sau đó click vào màn BIOS để điều khiển máy ảo, chọn Boot Manager (ở ví dụ này USB cài đặt là AI210 Mass Storage)

![vbox start3](../image/vbox_start_bios3.png) 

- Sau khi màn hình chạy như vậy là thành công,chọn file manjaro và [quay lại hướng dẫn cài đặt manjaro](../README.md) 

![vbox start4](../image/vbox_start_bios4.png) 


### Lưu ý 
tất cả lỗi trong lúc cài đặt có thể hỏi qua phần issue của github hoặc lên google hỏi 🐧
