# Netboot.xyz Installation guide (Vietnamese)


### Hướng dẫn cài hệ điều hành qua mạng (áp dụng cho linux :v)

#### Chuẩn bị:
- Docker ( ưu tiên linux :v )
- [dhcp-netboot.xyz](https://github.com/samdbmg/dhcp-netboot.xyz): docker [netboot.xyz](https://netboot.xyz) sử dụng qua DHCP
- Máy ảo ( có pxe/network boot  )

#### Cài đặt: 
##### Máy chủ
- Sử dụng ufw để mở tưởng lửa các port như sau :

```bash
sudo ufw allow proto udp from any to any port 67
sudo ufw allow proto udp from any to any port 69
sudo ufw allow proto udp from any to any port 4011
sudo ufw allow proto tcp from any to any port 80
```
- Sử dụng lệnh docker để chạy máy ảo 
```bash
docker run --net=host --cap-add=NET_ADMIN -e DHCP_RANGE_START=192.168.0.1 samdbmg/dhcp-netboot.xyz
``` 
*ở phần DHCP_RANGE_START là 3 dãy số đầu của `ip a ` xxx.xxx.xxx.1* (vd 192.168.1.1)

##### Máy khách
- Kết nối chung mạng với máy chủ 
- Khởi động máy và boot vào chế độ Pxe/Network Boot 
![PXE frist Start](image/pxe_frist_boot.png) 
- Trong hướng dẫn này sẽ cài Manjaro Gnome, ở Menu netboot chọn Live CD - Manjaro - Manjaro Gnome
![Manjaro LiveCD](./image/in_live_cd.png) 

