# Netboot.xyz Installation guide (Vietnamese)


### Hướng dẫn cài hệ điều hành qua mạng (áp dụng cho linux :v)

#### Chuẩn bị:
- Docker ( ưu tiên linux :v )
- [dhcp-netboot.xyz](https://github.com/samdbmg/dhcp-netboot.xyz): docker [netboot.xyz](https://netboot.xyz) sử dụng qua DHCP
- Máy ảo ( có pxe/network boot  )

#### Cài đặt: 

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

 *ở phần DHCP_RANGE_START là địa chỉ của router mạng (có thể là 192.168.1.1 hoặc 192.168.0.1)*  
