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
















