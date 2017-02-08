
#Bài học Cấu hình Route

====================

##I.Cấu hình cơ bản của Route.
*1. Các thành phần cơ bản:*

+ **Gồm 2 phần như sau:**

	>- Các thành phần bên trong : CPU, ROM, FLASH, NVRAM, RAM.

	>- Các thành phần bên ngoài: WAN, LAN, Console/AUX.

+ **CPU (*đơn vị xử lý trung tâm*).**

	>- Đơn vị xử lý trung tâm thực hiện các lệnh của hệ điều hành: Khởi tạo hệ thống, Định tuyến, Điều kiển các mạng,...

	>- Một Route có thể gồm nhiều CPU.

+ **ROM:**

	>- Là bộ nhớ chỉ đọc nhưng không thể sửa, xóa thông tin trên bộ nhớ này.

	>- Chứa 3 chương trình kiểm tra phần cứng trên Router : **power-on diagnotics**, **a bootstrap program**, and **operating system s
oftware.**

	>- Bên cạnh hệ điều hành chính Router còn có hệ điều hành phụ luôn thường trực nằm trên bộ nhớ ROM.

	>- Chức năng của ROM : kiểm tra phần cứng trong khi Router khởi động lên và tải IOS từ flash vào RAM.

	>- Bộ nhớ ROM không thể xóa đc chỉ có thể thay thế bằng ROM chips trong sockets.

+ **RAM (*Random Access Memory*)**

	>- Các chương trình, phần mềm sẽ đc load vào RAM để xử lý nhanh .

	>- RAM được chia bởi IOS thành 2 phần : **Main & Shared memory**.

	>- Main memony (bộ nhớ chính) sử dụng các chức năng của Router như: running-config, routing tables, switching cache, and ARP tables...

	>- Shared memony (bộ nhớ chia sẻ) dùng để buffer cho tiến trình đg xử lý.

	>- Nội dung của bộ nhớ RAM sẽ mất khi ngắt điện.

	>- Bộ nhớ RAM có thể được nâng cấp.

+ **NVRAM**

	>- Chứa startup configuration.

	>- Không bộ mất nội dung khi tắt router.

+ **Flash**.
	>- Bộ flash tương đương với chức năng của ổ cực trên PC chứa mọi tài nguyên của Router (hệ điều hành chính thức của router IOS).

	>- Bộ flash chứa hệ điều hành dưới dạng nén, khi đưa vào RAM nó sẽ được giải nén.

	>- Những router như 2500 có thể chạy trực tiếp trong flash.

	>- Flash có thể xóa , sửa đc và không bị mất dữ liệu khi ngắt nguồn điện.

+ **Buses**

  >- Đoạn buses để đấu nối giữa CPU và System bus.

+ **Interface**

  >- Dùng để kết nối với môi trường bên ngoài.

  >- Có 3 dạng:LANs(Local area Network), WANs (Wide Area Network), Console/AUX (Management Ports).

###. II. Các lệnh cơ bản trên Route.

**1. Lệnh xuất, nhập :**

- `Router>` (**User EXEC mode**) : không làm được gì hơn

***Lệnh*** : `Router>enable (Enter)`.

- `Router#` (**Privilege mode**) : có thể thực hiện câu lệnh để hiển thị tất cả thông số của Router và đi tới 
bất kì mode nào tiếp theo của Router.

***Lệnh*** : 

              Router#configure terminal (Enter)

              Router(config)#_ (Glogal configuration).

+ **Ví dụ** muốn đk cổng phát 0/0 ta gõ lệnh : 

              Router(config)#interface f0/0

	            Router(config-if)#_  (**Sub mode**)

+ Để trở về bên ngoài sử dụng lệnh : `exit`. Nhưng từ **Privilege mode** ra **User EXEC mode** ta sử dụng lệnh "disable"

**2. Đổi tên Router:**
- Lệnh : **Router(config)#hostname CCNA **

=> `CCNA(config)# `

- Nhập password (enable password)

	              Router(config)#enable password vnpro

**3. Lệnh hiển thị Running-config**

-Lệnh : **Router#show running-config**

                      Building configuration...

                      Current configuration : 708 bytes
                      !
                      version 12.2
                      no service timestamps log datetime msec
                      no service timestamps debug datetime msec
                      no service password-encryption
                      !
                      hostname CCNA
                      !
                      !
                      !
                      enable password ngoclan
                      !
                      !
                      !
                      !
                      !
                      !
                      ip cef
                      no ipv6 cef
                       --More-- 	

**4. Lệnh vòng ngoài**.

Lệnh Console-password:

>Router(config)#line console 0

>Router(config-if)#password cisco

>Router(config-line)#

**5. Mã hóa các password**.

-Lệnh : **Router(config)#service password-encryption**

**6. Lệnh treo khẩu hiệu chào mừng.**

-Lệnh: **Router(config)#banner motd "Welcome to my Router!!!"**

**7. Kiểm tra cổng**

-Lệnh: **Router(config-if)#show ip interface brief**

**8. Gán địa chỉ ip**

-Lệnh: **Router(config-if)#ip address 192.168.1.1 255.255.255.0**

-Đặt địa chỉ ip cho PC: **Router(config-if)#ping 192.168.1.2**

**9. Lưu cấu hình.**

- Lệnh: **Router#copy running-config startup-co**

**10. Xóa cấu hình cũ**
-Lệnh:  **Router#erase startup-config**

**11. Tạo Password mã hóa**
-Lệnh: **Router(config)#enable secret vnpro**
