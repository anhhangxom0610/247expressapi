# 247Express API

[![N|Solid](https://247post.vn/static/images/logo_red.png)](https://247post.vn/static/images/logo_red.png)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Hướng dẫn chi tiết các bước tích hợp API 247
  # Các bước tích hợp
 Bước 1: Đăng nhập lấy ClientID và Token theo API đăng nhập. Username và Password đăng nhập sẽ được cấp khi là khách hàng của 247. 
 
 Bước 2: Lấy danh sách các ClientHubID, đấy chính là danh sách mã định danh (ID) của các địa chỉ gửi hàng của khách hàng. Khi tạo đơn hàng cần gửi, phải điền đúng mã định danh (ClientHubID) tương ứng với địa chỉ gửi hàng đi của đơn hàng đó. 
 
Bước 3: Lấy danh sách dịch vụ chính đã được đăng ký bởi khách hàng. 

Bước 4: Lấy danh sách các dịch vụ giá trị gia tăng mà khách hàng có thể sử dụng. 

Bước 5: Tạo đơn hàng sử dụng API tạo đơn hàng với các thông tin cần thiết sau: 

ClientID và Token lấy ở bước 1 
ClientHubId lấy ở bước 2 
Dịch vụ chính/dịch vụ giá trị gia tăng lấy bước 3 và 4 (nếu sử dụng).

# Cập nhật!

  - 15/10/2020: 247Express triển khai hỗ trợ api trên nền tảng nodejs

### Cài đặt

-Yêu cầu nền tảng từ Nodejs 6+. Hỗ trợ với các framework: ReactJS, Angular, VueJS
```sh
$ npm install 247express --save
```

### API

247Express hỗ trợ các API dưới đây:

| API | Mô tả |
| ------ | ------ |
| clientLogin | Đăng nhập|
| getServiceTypes | Lấy danh sách dịch vụ chính |
| getServices | Lấy danh sách dịch vụ gia tăng |
| getClientHubs | Lấy danh sách điểm gửi hàng |
| updateOrder | Cập nhật vận đơn |
| cancelOrder | Hủy vận đơn |
| getOrderImages | Lấy ảnh vận đơn |
| getPrice | Tính giá vận đơn |
| createOrder | Tạo vận đơn |
| createClientHub | Tạo điểm gửi hàng |
| tracking | Track vận đơn |

#### Example
Đăng nhập:
```sh
import {clientLogin} from '247express';
.....
var response = await clientLogin({
     UserName:"TXN-KH18-0059",
      Password:"456123@" 
});
```

### Mọi thắc mắc và yêu cầu hỗ trợ vui lòng gửi về địa chỉ sau

 - https://247post.vn
 - Email: tech@247post.vn
 - Hotline: 19006980

License
----
MIT
