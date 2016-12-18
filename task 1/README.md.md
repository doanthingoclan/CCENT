# CCENT
===================================
##I.Introduction (Giới thiệu).

**1. Chứng chỉ Cisco (Cisco certification Overview).**

* Được chia ra làm 5 bậc :
  
  >-Bậc 1 (Entry): bậc cho người mới bắt đầu học và học theo chứng chỉ CCENT
 
  >-Bậc 2 (Associate) :  học theo các chứng chỉ như CCNA,CCNAS,CCNA Wireless,...

  >-Bậc 3 (Professional) : gồm những chứng chỉ như CCNP,CCIP,CCVP,CCDP,..

  >-Bậc 4 (Expert) :người hiểu rõ công nghệ và biết cách áp dụng công nghệ  : CCIE R&S, CCIE SP, CCDE,...

  >-Bậc 5 (Architect): chứng chỉ cao nhất trong Cisco như Cisco Certified Architect.

* Làm thế nào để học những chứng chỉ trên ???

**Offline**

  >+ Ði đến các trung tâm nhưng có những hạn chế như : trung tâm thường giá cao mặc dù được tương tác với cấu hình thật và giảng viên tuy nhiên các thiết bị thường rất lỗi thời.
  
**Self-study ( Tự học )**

  >- Được nhưng khó nếu bạn không thực sự master được nền tảng CCNA. 
Online

  >- Có rất nhiều trang wed cung cấp dịch vụ online như Udemy, INE, via Skype,...Và đây là phương pháp phổ biến trên thế giới bởi vì :
  
  >+ Chi phí cho 1 khóa học rẻ hơn 
  
  >+ Tự do trong thời gian học và có video cho ta review lại bài sau khi học.
  
  > Mặc dù vậy nhưng nó cũng có những hạn chế : với những khóa học chưa thuần thúy thì ta sẽ khó khan trong việc tương tác trực tiếp với giáo viên mà phải thông qua email và chờ reply comment. 
  
  >** Và tất nhiên muốn học những khóa học trên thì ta phải biết tiếng anh để nghe được bài giảng **
  
**Làm thế nào để chọn công việc để khớp với chứng chỉ theo học ???**
  
  > Có 3 lựa chọn :
  
  >++ P/a 1 :Chọn những công ti chuyên tích hợp hệ thống (Systerm Intergration) (SI) , đây là nơi tạo điều kiện cho ta có thể tiếp xúc nhiều công nghệ, nhiều hang, nhiều dự án khác nhau, học được nhiều kiến thức mới khác nhau (thích hơp cho những người sau khi học xong chứng chỉ).
  
  >++ P/a 2 : Chọn những công ti chuyên cung cấp dịch vụ Internet (ISP) : đây là nơi có những hệ thống mạng rất lớn và sử dụng rất nhiều thiết bị, ta có thể làm NOC (Network Operating Center) kiểm tra hệ thống khi nào xảy ra sự cố, tắc nghẽn để can thiệp or có thể làm Solution Engineer đưa ra những giải pháp sử lý sự cố nhưng thực tế các công ti như Viettel,VNP sẽ thuê SI để làm công việc này.
  
  >++ P/a 3 : Làm Admin cho những doanh nghiệp và công việc chủ yếu là quản trị hệ thống, mạng, máy in,… Đây là công việc ít cung cấp kiến thức cho chúng ta nhất.
  
 **Tiếp tục học và phát triển .**
  
  >- Học CCNP (tối thiểu).
  
  >- Xin công việc làm (**SI** or **NOC**).
  
  >- Trong quá trình đó thì tiếp tục học thêm những chứng chỉ khác
  
**Xây dựng phòng lab tại nhà .**
  
  >- Packet Tracer:hạn chế là support ít câu lệnh và không đủ để học CCIP nhưng đây là phần mềm dễ sử dụng và tích hợp được nhiều thứ. 
  
  >- GNS3( www.gns3.com ): tốn rất nhiều tài nguyên CPU/RAM.
  
  >-Cisco IOU (routereflector.com): tốn  tài nguyên ít và đây là phần mềm tốt nhất để thực hành .
  
-Unified Networking Lab  ( www.unetlab.com ) : có thể tích hợp được rất nhiều hang và là best oftion nhưng cần một máy tính khỏe ít nhất là 16GB. 

  * **Những nguồn tài nguyên**
  
  >- Youtube: https://www.youtube.com/user/nguyenshin .
  >- INE blog :  http://blog.ine.com .
  >- CareerCert:  http://www.careercert.info .

###II . Mạng căn bản

**1.	Như  thế nào là mạng ?**

   > Mạng là một hệ thống đường truyền kết nối với nhau để đảm bảo sự truyền tin cho các thiết bị khác nhau , những thành phần khác nhau giữa các hệ thống như một người dùng cố định sử dụng di động giữa một trụ sở chính vào các chi tiết của doanh nghiệp thông qua một đám mây internet và là hệ thống cho các thiết bị có thể truyền tin được với nhau.
    
**2.	Chức năng chia sẻ tài nguyên của một hệ thống mạng.**

  >-	Chia sẻ dữ liệu và ứng dụng (Data & applications).

  >-	Chia sẻ những tài nguyên (resources).

  >-	Chia sẻ lưu trữ mạng (Network storage).

  >-	Chia sẻ Backup devices.

**3.	Những ứng dụng đời sống phổ biến.**

  >-	Email (Outlook.POP3,Yahoo ,…)

  >-	Web brower (IE,Firefox , …)

  >-	Instant messaging (Yahoo , IM, Microsoft Messenger,…)

  >-	Collaboration (Whiteboard, Netmeeting, WebEx,… )

  >-	Databases (file servers)

**4.	Đặc tính kỹ thuật của mạng.**

  >-	Speed

  >-	Cost

  >-	Security

  >-	Availability

  >-	Scalability

  >-	Reliability

  >-	Topology

**5.	Sơ đồ đấu với vật (Physical Topology): Bus, Ring, Star.**

•	Bus Topology : Các thiết bị cùng nhau đấu với 1 đường truyền, khi một máy gửi tín hiệu vào trong đường truyền thì tất cả các thiết bị đều nhận được tín hiệu này.

•	Star topology : Các thiết bị muốn gửi tín hiệu với nhau phải thông qua Center point trước.

•	Extended – star topology : Sơ đồ có tính phục hồi cao hơn sơ đồ Star thông thường 

•	Ring topology : Các thiết bị đấu nhau và truyền đi theo 1 đường vòng tròn.

•	Dual – Ring : Có tình phục hồi cao hơn Ring thông thường .

•	Full –Mesh topology : từ một đường truyền có thể đến tất cả các thiết bị còn lại trong hệ thống, có thể chịu lỗi cực kì cao nhưng rất đắt tiền tồn kém .

•	Partical – mesh topology : dạng đơn giản của Full –Mesh topology để giảm bớt chi phí hơn .

####III.  Mô hình OSI.

**1.	Host là gì ?** là một thực thể mạng có khả năng truyền được các ứng dụng .

**2.	Các mô hình :**

-**Older model **:

  >-	Độc quyền .
  
  >-	Các ứng dụng và phần mềm cài đặt trên các máy này chỉ được cung cấp bởi một nhà cung cấp duy nhất.
  
•	**Standards-based model.**

  >-	Mô hình cho phép 1 thiết bị có thể sử dụng nhiều phần mềm của nhiều hãng khác nhau.

  >-	Mô hình phân lớp : Gồm có 7 lớp công việc : Physical, Data Link, Network, Transport, Session , Presentation, Application. Nhờ chia công việc theo từng lớp sẽ giúp giảm bớt sự phức tạp, chuẩn hóa được giao diện dòng sản phẩm, đảm bảo sự tương thích về mặt công nghệ, thúc đẩy kỹ thuật model hóa, thúc đẩy mạnh mẽ công nghệ mạng ngày nay và cuối cùng là đơn giản cho việc dạy and học .

**3.	Mô hình OSI (Open Systerm Interconnection)** là một mô hình cực kì nổi tiếng được phát thảo từ năm 1977 và được hoàn thiện vào năm 1984, mô hình chia công việc thành 7 lớp: Physical, Data Link, Network, Transport, Session , Presentation, Application 

  >•	**Physical (lớp vật lý)** : quy định đường truyền vật lí về cơ , điện , quang, các thủ tục chức năng để truyền 1 dòng bit qua đường truyền vật lý cụ thể nào đó.
  
  >•	**Data Link :** cung cấp, điều khiển việc truy nhập đường truyền vật lý và giao tiếp với đường truyền Network bên trên. 
  
  >•	**Network**: xác định đường truyền tối ưu nhất và định nghĩa các giao thức định tuyến, quy đinh địa chỉ logic (ID) cho hệ thống đường truyền của chúng ta. 
  
  >•	**Transport:** quản lí kết nối đầu - cuối (end-to-end) ; xử lí các truyền tải giữa hosts; đảm bảo rằng dữ liệu được truyền đáng tin cậy; đảm bảo các thiết lập, duy trì và kết thúc các đường mạch ảo ; cung cấp các cơ chế dò lỗi tin cậy, phục hồi thông tin bằng cách điều khiển flow.
  
  >•	**Session**: lớp đứng ra tổ chức các kết nối cho các ứng dụng.
  
  >•	**Presentation:** đảm bảo dữ liệu đầu này sẽ đọc được ở đầu kia; định dạng lại, cấu trúc dữ liệu; thương lượng các cú pháp truyền dữ liệu cho ứng dụng; cung cấp cơ chế mã hóa.
  
  >•	**Application:** Cung cấp các ứng dụng, dịch vụ mạng (như là electronic mail, file transfer and terminal emailation); cung cấp các cơ chế xác thực cho người dùng.
  
#####IV. Mô hình TCP/IP: 

  > Gồm 4 lớp , sử dụng những tên khác nhau từ lớp 3 đến lớp 7 và gộp chung từ lớp 5 đến lớp 7 thành 1 lớp đơn.
  
  
                                                          
                                                        ^^  HẾT ^^

