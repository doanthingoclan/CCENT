# Chia IP.

======================

**I. Sự chuyển đổi giữa hệ nhị phân và hệ thập phân:**

-	Hệ nhị phân (Bindy): 0;1 .

-	Hệ thập phân (Decimal) : 0 đến 9.

  >+ Muốn chuyển từ decimal sang bindy ta lấy số trong decimal chia đôi, chia đôi liên tục từ đó ta sử dụng kết quả chia để viết ra 
bindy cần tính.
  >+ Muốn chuyển ngược lại ta thứ tự đánh số các bits từ phải sang trái bắt đầu từ 0 đến n rồi ta thực hiện phép tính tổng các lũy 
thừa 2 mũ số đếm thứ tự nhân cho các số trong bindy từ trái sáng phải.

**II.	Các giá trị lũy thừa của 2 ( 2^n ).**

2^0= 1		

2^1= 2

2^2= 4

2^3= 8

2^4= 16

2^5= 32

2^6= 64

2^7= 128

2^8= 256

2^9= 512

2^10= 1024

2^11= 2048

2^12= 4096

2^16= 65536

       Cho ta n bit nhị phân thì có thể tạo ra được 2^n số nhị phân n-bit chạy từ 00000…..00000( n-bit 0 ) đến 1111……1111
       ( n-bit 1 )và ta có các giá trị thập phân tương ứng là 0 đến 2^n - 1.

**III.Bảng:**
- ***Bảng 1***:

00000000 -> 0

10000000 -> 128

11000000 -> 192

11100000 -> 224

11110000 -> 240

11111000 -> 248

11111100 -> 252

11111110 -> 254

11111111 -> 255

-	***Bảng 2***: Gọi n là số bit mượn thì bước nhay được tính bằng công thức 2^ (8-n).

|Số bit mượn|1      |2      |3      |4      |5      |6     |7     |8     |
| --------- | :---: | :---: | :---: | :---: | :---: |:---: |:---: |----: |
|Số bước nhảy|128      |64     |32     |16     |8    |4     |2     |1     |

***IP HEADER***

|Ver. & IHL &Service Type|Packet Length|
|  -------------------  |:----------------|
|Identification		  |Flag & Flag. Offset|
|Time to Live & Protocol|Header Checksum|
|Scurce Address|
|Destination Address|
|Options |Padding|

**IV.	Cấu trúc địa chỉ IP:**

-	Địa chỉ IP là dãy số nhị phân dài tổng cộng 32 Bits (10000011011011000111101011001100) và chia làm hai phần ( NETWORK & HOST) 
phần NETWORK sẽ định danh cho cả mạng máy tính của nó , phần HOST sẽ định dang từng HOST cụ thể trong mạng ấy.

-	Địa chỉ IP thường được viết thành từng cụm 8 Bits:

|10000011 |01101100 |01111010 | 11001100 |
| ------ | :-----: | :-----: | :------|

-	Từng cụm sẽ không được sử dụng dưới dạng nhị phân mà ngta sẽ đổi dưới dạng là thập phân và được ngăn cách với nhau bằng dấu chấm .

|131|.|108|.|122|.|204|
|----|:---:|:---:|:---:|:----:|:---:|:----|

-	Các bits phần mạng không được phép đồng thời bằng 0.

-	Nếu tất cả bit phần HOST =0 thì đó là địa chỉ mạng

-	Nếu tất cả bit phần HOST =1 thì đó là địa chỉ quảng bá ( boardcast ).

**V.	Các lớp địa chỉ IP.**

|N      |H      |H      |H      |
| ----- | :----: |:-----:|:-----|
|N      |N      |H      |H      |
|N      |N      |N      |H      |

***Class A***: (8 BITS đầu định danh phần mạng; 24 bits sau định đanh phần host)
                  
|NETWORK|HOST |HOST|HOST|
| ----- | :----: |:-----:|:-----|
|#Bits  |1       |7		   |24    |
|       |0       |NETWORK#|HOST#|

>-	Một mạng lớp A sẽ chạy từ 1.0.0.0 đến 127.0.0.0, lớp A có 8 bits đầu là phần mạng và 24 bits sau là phần HOST vậy mỗi mạng lớp A
có 2^24 -2 host.
                  
>-	Một mạng lớp A sẽ chạy từ 1.0.0.0 đến 127.0.0.0 trong đó mạng 127.0.0.0 không được dùng trong các HOST mà được sử dụng 
loopback network do đó địa chỉ mạng sử dụng được : 1.0.0.0 đến 126.0.0.0 ( 126 mạng )
                  
***Class B:***
                  
|NETWORK|NETWORK |HOST   | HOST |
| ----- | :----: |:-----:|:-----|
                  
>-	Một địa chỉ IP lớp B sẽ có 2 bits đầu luôn luôn được giữ cứng là 0 & 1, còn 14 bits sẽ chạy tự do đê định danh cho toàn bộ mạng 
                  của địa chỉ IP lớp B.
                  
>-	Trong lớp B chạy từ 128.0.0.0 đến 191.255.0.0 có 2^14 địa chỉ mạng.
                  
>-	Phần host : 16 bits, một mạng lớp B có 2^16 -2 host.
                  
***Class C:***
                  
|  NETWORK  |   NETWORK  |  NETWORK  |    HOST  |
| --------- | :--------: |:---------:|:---------|

>-	Địa chỉ mạng chạy từ 192.0.0.0 đến 223.255.255.0 và có tất cả 2^21 mạng trong lớp C
                  
>-	Phần host : 8 bits. Một mạng lớp C có 2^8 -2 = 254 host.
                  
**Địa chir IP lớp D**
                  
>-	Địa chỉ : 224.0.0.0 đến 239.255.255.255
                  
>-	Địa chỉ multicast.
                  
>-	Ví dụ: 224.0.0.5 dùng cho OSPF
                  
> 224.0.0.9 dùng cho RIPv2
                  
 **Địa chỉ lớp E :**
                  
>-	Từ 240.0.0.0 trở đi
                  
>-	Dự phòng
                  
**Địa chỉ quảng bá (broadcast)**
                  
>-	Direct . VD: 192.168.1.255
                  
>-	Local . VD: 255.255.255.255
                  
**Địa chỉ IP: Private và Public**
                  
>-	Trong LAN: Private
                  
>Internet:Public
                  
>-	Dải địa chỉ private (RFC 1918):
                  
  >o	Lớp A: 10.x.x.x
                  
  >o	Lớp B: 172.16.x.x đến 172.31.x.x
                  
  >o	Lớp C: 192.168.x.x
                  
>-	NAT: chuyển đổi từ private sang public và ngược lại.
                  
>-	Ý nghĩa của địa chỉ private: bảo tồn địa chỉ IP.
                  
- **Subnet-mask** là một dãy nhị phân dài 32 bits được dùng để đem với địa chỉ IP để xác định địa chỉ mạng của địa chỉ IP ấy.
                  
- Số Prefix – length: A.B.C.D/ n(Số bits mạng trong địa chỉ IP).
                  
                  
                  
                                                                  ~~END~~



