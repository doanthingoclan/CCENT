# Level 02 : Etheret Lan, Cable

## Bài 3 - Mô hình TCP/IP .
I. Transport Layer
- Tầng Transport của TCP/IP tương đương tầng transport của mô hình OSI có chức năng cung cấp và điều khiển kết nối điểm tới điểm end-to-end và nó có 2 giao thức nổi bật đó là :UDP và TCP.
- Tầng Network của OSI trong TCP/IP tương đương với tầng Ethernet và có giao thức là : IP.
- 2 lớp Data Link and Physical tương đương với lớp Network của mô hình TCP/IP và có giao thức đó là : Ethernet.
- Một số ứng dụng, tính năng và chức năng của tầng Transport trong mô hình TCP/IP :
  + Ghép các phiên truy nhập ứng dụng hay ghép các kết nối trong một đường truyền duy nhất từ đầu cuối đến đầu cuối end-to-end (Session multiplexing) .
  + Phân mạch dữ liệu (Segmentation).
  + Cung cấp cơ chế điều khiển ngược làm cho lượng dung lượng di chuyển hợp lí hơn cho các kết nối đầu cuối nhưng cơ chế này không phải giao thức nào cũng có (giữa UDP and TCP thì chỉ TCP có cơ chế flow control ) và không phải lúc nào cơ chế nào cũng được thi hành mà chỉ khi có yêu cầu .
  + Cung cấp kiểu truyền connection-oriented (truyền theo hướng kết nối) tức là khi 2 máy có ý định truyền dữ liệu cho nhau thì đầu tiền chúng phải thiết lập một kết nối luận ý và có nhiều cơ chế truyền tin cậy được sử dụng kèm theo kết nối luận ý này. Có 2 kiểu truyền tin: connection - oriented dành cho giao thức TCP sử dụng, còn Connectionless là UDP sử dụng.
  + Độ tin cậy đảm bảo dữ liệu được truyền từ điểm này tới điểm kia của hệ thống mạng (when requied)
II . So sánh giữa reliable vs Best-Effort Comparison.
- Reliable: 
  + Kiểu kết nối(Connection Type): Connection - oriented.
  + Loại giao thức (Protocol):TCP
  + Thứ tự (Sequencing):Có
  + Trường hợp sử dụng(Uses): Email, File sharing, Downloading.
  - Best-Effort: 
   + Kiểu kết nối(Connection Type):Connetionless
  + Loại giao thức (Protocol):UDP
  + Thứ tự (Sequencing):Không
  + Trường hợp sử dụng(Uses): Voice streaming, Video streaming.
III. Giao thức UDP (user datagram protocol).
- Là một trong hai loại giao thức nổi tiếng của mô hình OSI và TCP/IP ở lớp transport.
- Cho phép các ứng dụng truy nhập vào lớp network mà không phải thông qua các cơ chế quản lí tin cậy.
- Sử dụng giao thức Connectionless.
- Cung cấp cơ chế kiểm tra giới hạn.
- Cung cấp cơ chế phân phối theo kiểu best-effort (có bao nhiêu gói tin thì đẩy vào đường truyền tất cả các gói tin ấy).
- Không có cơ chế phục hồi dữ liệu.
**Các trường của UDP header** 
|16-bit source port||16-bit destination port|
|16-bit UDP length||16-bit UDP checksum|
|data|

III. Giao thức TCP
- Hoạt động ở tầng transport của mô hình TCP/IP.
- Giúp các ứng dụng truy nhập được vào tầng mạng
- Là giao thức kiểu connection-oriented.
- Hỗ trợ kiểu hoạt động là Full-duplex(là kiểu truyền có thể truyền- nhận cùng 1 thời điểm ).
- Cơ chế kiểm tra lỗi.
- Cơ chế đánh số thứ tự cho cái gói tin để ráp lại cho đúng ở đầu kia.
- Cơ chế báo nhận (Acknowledgement) .
- Cơ chế phục hồi dữ liệu.
**Các trường của TCP header**
|16-Bit source port||16-bit destination port|
|32-bit sequence number|
|32-bit acknowledgement number|
|4-bit header length||resv||ns||cwr||ece||urg||ack||psh||rst||syn||fin||16-bit window size|
|16- bit TCP checksum||16-bit urgent pointer|
|Options|
IV. Ứng dụng của giao thức TCP/IP
- Truyền file : FTP,TFTP,Network file systerm.
- Thư điện tử: SMTP(Simple mail transfer protocol).
- Truy nhập từ xa : Telnet,rlogin.
- Quản lí mạng : SNMP(simple network management protocol).
- Quản lí tên Việt: Domain Name Systerm.
** Cơ chế Mapping layer 3 to layer 4**
|Ver.|IHL|Service Type|packet length|
|Identification|Flag|Frag.Offset|
|Time to Live|Protocol|Header Checksum|
|Source Address|
|Destination Address|
|Options|Padding|
**Mapping Layer 4 to applications**
-FTP sử dụng kết nối TCP port "21".
-Telnet sử dụng kết nối TCP port "23"
-HTTP sử dụng kết nối TCP port "80"
-TFTP sử dụng kết nối UDP port "69"
-SNMP sử dụng kết nối UDP port "161"
-DNS sử dụng kết nối cả hai TCP và UDP port "53".
**Cơ chế bắt tay 3 bước**
-Bước 1: Host A gửi gói tin TCP có SYN được bật lên với số thứ tự được đánh là 100 (SEQ=100 CTL= SYN)
-Bước 2: Gói tin được gửi qua bên host B và khi nhận được gói tin có SYN được bật lên thì nó cũng gửi ngược
lại một gói tin có SYN ,ACK được bật lên (SEQ= 300 ACK = 101 CTL = SYN,ACK)
-Bước 3: Kết nối đã được thiết lập thì host A phải gửi 1 gói tin báo cho host B (SEQ= 101 ACK = 301 CTL = SYN,ACK).
**Cơ chế Flow Control của giao thức TCP**
Giả sử máy A gửi quá nhiều dữ liệu cho máy B , máy B phải Buffer dữ liệu vào trong bộ đệm để xử lí đến lúc bộ đệm đã đầy
thì máy B phải gửi tín hiệu đến máy A stop truyền dữ liệu và máy A nhận được tín hiệu sẽ stop không truyền dữ liệu nữa
và lúc này máy B đg xử lí dần dân Segments trong bộ đệm của nó cho đến khi Buffer trống sau đó máy B sẽ gửi tín hiệu sẵn
sàng qua máy A và tiếp tục truyền lại dữ liệu như ban đầu.

###Bài 4. Ethernet Lan.
**I. Thành phần cơ bản của mạng LAN.

-Computers: PCs, Servers.
-Interconnections: NICs, Media.
-Network devices: Hubs, Switches, Routers.
-Protocols: Ethernet, IP, ARP, DHCP.

**II. Các ứng dụng của mạng LAN**
- Chía sẻ dữ liệu và ứng dụng.
-Chia sẻ những tài nguyên(resources).
-Cung cấp đường kết nối đến 1 mạng khác.
**III. Kích thước mạng LAN.**
- Mạng LAN có thể là 1 mạng có kích thước rất nhỏ như: Mạng SOHO LAN(Small Office Home Office) tượng trưng cho 1 cá thể gồi tại nhà
chỉ gồm 1 or 2 máy tính kết nối với con switch .
- Mạng LAN có thể là mạng có kích thước cực kì lớn như 1 mạng của doanh nghiệp chẳng hạn như: Enterprise LAN. Mạng doah nghiệp này có thể bao gồm routers, switchs và rất nhiều loại PCs, Users,..đấu vời trong 1 hệ thống mạng LAN.
**IV. LAN Standards( Các chuẩn mạng LAN).**
-Tập trung chủ yếu ở 2 lớp OSI: Data Link Layer và Physical Layer
+ Data Link: gồm 2 lớp LLC Sublayer(chuyên lo giao tiếp với hệ thống Layer 3) và MAC SubLayer(chuyên lo truy nhập và điều khiển vào đường truyền vật lý ở phía dưới).
+ Một số chuẩn mạng LAN chạy từ Physical Layer đến hết Data Link Layer còn một số khác chỉ dừng lại ở lớp MAC Sublayer .

https://www.youtube.com/watch?v=TAbvgEuir6w 8:00


























cs

































