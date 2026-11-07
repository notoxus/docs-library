# **Chương 9: Kết nối Internet**

**TRONG CHƯƠNG NÀY**

* Hiểu các phương pháp kết nối Internet phổ biến  
* Biết rõ phần cứng của bạn  
* Kết nối với Nhà cung cấp Dịch vụ Internet (ISP) của bạn  
* Hiểu đủ về TCP/IP để trở nên "nguy hiểm"

Bạn có thể đã được kết nối với Internet nếu bạn đang sử dụng một máy tính được kết nối với mạng LAN (Mạng cục bộ) và bạn đã cấu hình mạng trong quá trình cài đặt. Để kiểm tra xem bạn có kết nối hay không, hãy mở một trình duyệt web và thử truy cập vào một trang web bên ngoài (chẳng hạn như www.gnu.org). Nếu nó hoạt động, bạn đã lên mạng thành công\! Bạn không cần phải đọc chương này nữa. Nếu không, hãy đọc tiếp nhé.

## **Lớp Vỡ lòng về Kết nối Internet (Internet Connectivity 101\)**

Đừng để các nhà cung cấp dịch vụ tốc độ cao làm bạn nản lòng trong việc sử dụng Linux với dịch vụ của họ. Chỉ vì họ không trực tiếp hỗ trợ Linux không có nghĩa là công nghệ đó không hoạt động với Linux. TCP/IP (bộ quy tắc giao thông dành cho Internet) ban đầu được phát triển cho hệ điều hành UNIX, và Linux chính là hậu duệ của nó.

Nếu bạn đang khởi động kép (dual-boot) với Windows, ISP của bạn có thể giúp bạn cài đặt kết nối băng thông rộng trên Windows, và sau đó bạn có thể tự mày mò để kết nối Linux khi có thời gian và hứng thú. Dưới đây là các loại kết nối phổ biến mà bạn có thể gặp:

* **Cable modems (Modem cáp):** Khi bạn đăng ký dịch vụ Internet cáp, kỹ thuật viên lắp đặt thường cung cấp cho bạn một thiết bị đặc biệt, gọi là modem cáp, gắn vào cáp đồng trục truyền hình và kết nối với máy tính của bạn thông qua cổng cáp mạng (Ethernet).  
* **DSL modems (Modem DSL):** Đường dây thuê bao kỹ thuật số (DSL) sử dụng đường dây điện thoại hiện có của bạn để truyền dữ liệu tốc độ cao. Giống như cáp, modem DSL thường kết nối với PC của bạn qua cổng Ethernet.  
* **Mạng không dây (Wi-Fi/Wireless):** Ngày nay, hầu hết các modem cáp và DSL đều đi kèm với bộ định tuyến không dây (wireless router) tích hợp, cho phép bạn kết nối máy tính xách tay hoặc máy tính để bàn với Internet mà không cần cắm cáp vật lý.  
* **Mạng di động (Cellular):** Nếu bạn đang di chuyển, bạn có thể sử dụng điện thoại thông minh làm điểm phát sóng (hotspot) hoặc sử dụng USB 4G/5G để kết nối mạng.

## **Biết rõ Phần cứng của Bạn (Knowing Your Hardware)**

Để kết nối với mạng, PC của bạn cần có phần cứng giao tiếp mạng phù hợp. May mắn thay, hầu hết các máy tính hiện đại đều được tích hợp sẵn những thứ này trên bo mạch chủ:

* **Card Giao diện Mạng (Network Interface Card \- NIC):** Đây là cổng cắm cáp mạng (thường được gọi là cổng Ethernet hoặc cổng RJ-45). Nếu bạn đang sử dụng kết nối có dây, đây là nơi bạn sẽ cắm sợi cáp từ modem hoặc router vào.  
* **Bộ điều hợp Không dây (Wireless Adapter):** Hầu hết các máy tính xách tay và nhiều máy tính để bàn hiện nay đều có card Wi-Fi tích hợp. Linux hỗ trợ hàng ngàn loại card Wi-Fi khác nhau, vì vậy trong hầu hết các trường hợp, hệ thống sẽ tự động nhận diện thiết bị của bạn.

**MẸO:** Nếu Linux không nhận diện được card Wi-Fi của bạn (thường xảy ra với các dòng máy tính xách tay quá mới hoặc sử dụng chip độc quyền), bạn có thể cần cắm tạm dây mạng Ethernet để tải trình điều khiển (driver) không dây từ kho phần mềm.

## **Kết nối với Mạng của Bạn (Connecting to Your Network)**

Bất kể bạn đang sử dụng GNOME, KDE Plasma hay Xfce, Linux đều xử lý các kết nối mạng thông qua một công cụ chạy ngầm tuyệt vời có tên là **NetworkManager**. NetworkManager giúp việc kết nối vào mạng trở nên dễ dàng chỉ với vài cú nhấp chuột, giống hệt như trên Windows hoặc macOS.

### **Kết nối Mạng Có dây (Wired Connections)**

Mạng có dây là phương pháp dễ nhất để kết nối trong Linux. Trong 99% các trường hợp, bạn chỉ cần lấy một đầu cáp Ethernet cắm vào máy tính, và đầu còn lại cắm vào bộ định tuyến (router) hoặc modem của bạn.

NetworkManager sẽ tự động phát hiện kết nối cáp, yêu cầu bộ định tuyến cung cấp địa chỉ IP thông qua quá trình DHCP (tôi sẽ giải thích điều này sau), và đưa bạn lên mạng trong vòng chưa đầy năm giây. Bạn sẽ thấy biểu tượng mạng trên thanh bảng điều khiển (panel) chuyển thành hình hai máy tính hoặc một sơ đồ mạng nhỏ.

### **Kết nối Mạng Không dây (Wireless Connections)**

Kết nối Wi-Fi cần bạn thao tác thêm một chút, nhưng vẫn rất đơn giản:

1. **Nhấp vào biểu tượng mạng** trên bảng điều khiển (thường nằm ở góc trên bên phải trong GNOME, hoặc góc dưới bên phải trong KDE/Xfce).  
2. **Đảm bảo Wi-Fi đã được bật.**  
3. **Chọn mạng Wi-Fi (SSID) của bạn** từ danh sách các mạng khả dụng.  
4. **Nhập mật khẩu (Passphrase/Security Key)** khi được nhắc.  
5. Nhấp vào **Connect** (Kết nối).

Sau khi kết nối thành công, biểu tượng mạng sẽ chuyển thành hình các vạch sóng Wi-Fi quen thuộc. NetworkManager sẽ ghi nhớ mật khẩu này để tự động kết nối lại vào những lần sau.

## **Hiểu đủ về TCP/IP để trở nên "Nguy hiểm"**

Đôi khi, mọi thứ không hoạt động trơn tru theo cách tự động, hoặc có thể bạn chỉ tò mò muốn biết đằng sau hậu trường mạng máy tính diễn ra như thế nào. Giao thức TCP/IP có thể là một chủ đề phức tạp (người ta viết cả những cuốn sách dày cộp về nó), nhưng bạn chỉ cần nắm được một vài thuật ngữ cơ bản sau đây để tự tin làm chủ mạng của mình.

* **Địa chỉ IP (IP Address):** Giống như địa chỉ nhà của bạn, mọi thiết bị trên mạng đều cần một địa chỉ IP duy nhất để giao tiếp. Trong mạng gia đình, nó thường có dạng 192.168.1.x hoặc 10.0.0.x.  
* **Mặt nạ mạng con (Subnet Mask):** Đây là một dãy số cho máy tính biết phần nào của địa chỉ IP là "địa chỉ đường" (địa chỉ mạng) và phần nào là "số nhà" (địa chỉ máy). Giá trị phổ biến nhất là 255.255.255.0.  
* **Cổng mặc định (Default Gateway):** Đây là địa chỉ IP của bộ định tuyến (router) nhà bạn. Bất kỳ khi nào PC của bạn muốn gửi dữ liệu ra ngoài Internet (thay vì chỉ gửi cho các máy trong nhà), nó sẽ gửi dữ liệu đó đến Cổng mặc định để router xử lý.  
* **DNS (Hệ thống phân giải tên miền):** Máy tính chỉ hiểu các con số (Địa chỉ IP), nhưng con người lại thích dùng tên (như www.google.com). Máy chủ DNS hoạt động như một danh bạ điện thoại, dịch tên miền mà bạn gõ thành địa chỉ IP mà máy tính có thể kết nối.  
* **DHCP (Giao thức cấu hình máy chủ động):** Đây là phép màu giúp bạn không phải tự tay nhập tất cả các thông số trên. Khi bạn kết nối vào mạng, PC của bạn sẽ hét lên: *"Này, ai cho tôi một địa chỉ IP với\!"* và bộ định tuyến (đóng vai trò máy chủ DHCP) sẽ tự động phân bổ IP, Subnet Mask, Gateway và DNS cho bạn.

### **Khắc phục sự cố mạng cơ bản**

Nếu bạn không thể truy cập Internet, đây là một vài công cụ dòng lệnh cực kỳ hữu ích mà các chuyên gia Linux thường dùng:

1. **ping:** Lệnh này gửi một gói dữ liệu nhỏ đến một máy chủ khác để xem nó có phản hồi hay không.  
   Hãy mở Terminal và gõ: ping 8.8.8.8 (đây là máy chủ DNS của Google). Nếu bạn thấy các dòng trả về hiển thị thời gian (time=xx ms), nghĩa là bạn CÓ kết nối Internet. Nhấn Ctrl+C để dừng lệnh.  
2. **ip addr:** Lệnh này hiển thị địa chỉ IP hiện tại của các card mạng trên máy bạn. Hãy tìm card không dây (thường bắt đầu bằng wl... như wlan0) hoặc card có dây (thường bắt đầu bằng en... như eth0 hoặc enp3s0).

## **Các Trang web Hữu ích (Useful Sites)**

Sau khi đã lên mạng, bạn sẽ muốn biết mình có thể tìm kiếm sự trợ giúp và các chương trình Linux ở đâu. Dưới đây là một số trang web bạn có thể thấy hữu ích khi cần trợ giúp, có thắc mắc, hoặc muốn khám phá sâu hơn về thế giới Linux. Một số trang có thể hơi "đậm chất kỹ thuật", nhưng rồi bạn sẽ dần quen với chúng thôi\!

Bạn cũng có thể muốn cập nhật máy tính của mình (xem Chương 15), cài đặt phần mềm mới (cũng ở Chương 15), và suy nghĩ thêm về bảo mật hệ thống (xem Chương 18\) để bảo vệ bản thân khỏi những kẻ xấu và các chương trình độc hại.

Các trang web hữu ích bao gồm:

* **www.linuxsecurity.com:** Một nơi hơi "mọt sách" (nhưng cực kỳ hữu ích) để bạn theo dõi những gì đang diễn ra trong thế giới bảo mật Linux.  
* **www.linuxquestions.org:** Tôi đã nhắc đến trang web này ở một phần khác trong sách, nhưng nó xứng đáng được nhắc lại. Đây là nơi tụ tập phổ biến của những người có câu hỏi cần giải đáp, và cả những người thích giúp người khác tìm ra câu trả lời.  
* **tldp.org (The Linux Documentation Project):** Chứa vô số tài liệu trợ giúp được viết cho nhiều trình độ người dùng khác nhau.  
* **www.slashdot.org:** Nơi tụ tập của các siêu trùm công nghệ (uber-geek hangout). Đáng tiếc là văn hóa ở đây đôi khi khá gay gắt, nhưng nó cung cấp rất nhiều liên kết đến các bài báo trực tuyến thú vị. Cách tốt nhất là bạn chỉ nên vào đây để đọc báo; hãy *bỏ qua* các cuộc cãi vã trong phần bình luận\!

Ngoài những gợi ý này, hãy luôn nhớ rằng công cụ tìm kiếm yêu thích của bạn (như Google hay DuckDuckGo) cũng có thể cực kỳ đắc lực khi bạn cần giải quyết vấn đề.