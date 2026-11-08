# **Chương 4: Khám phá Máy tính để bàn GNOME**

**TRONG CHƯƠNG NÀY**

* Lịch sử của máy tính để bàn GNOME  
* Khám phá màn hình nền  
* Tùy chỉnh màn hình nền của bạn  
* Cài đặt các tính năng trợ năng

Một số người thích mô tả Linux như một hệ điều hành được xây dựng bởi những kẻ mọt sách (nerd), dành riêng cho những kẻ mọt sách. Điều này gieo rắc viễn cảnh rằng bạn phải gõ những dòng lệnh bí ẩn để làm bất cứ việc gì trên máy tính. Tuy nhiên, điều đó hoàn toàn sai sự thật\! Linux hỗ trợ một số môi trường máy tính để bàn đồ họa cung cấp giao diện thân thiện với người dùng nhất hiện có cho máy tính cá nhân.

Mặc dù vậy, điều có thể hơi khó hiểu là không có một màn hình đồ họa tiêu chuẩn duy nhất nào cho Linux. Linux có đầy rẫy sự lựa chọn, và điều đó không đâu rõ ràng hơn trong thế giới đồ họa máy tính để bàn. Trong Chương 4, 5 và 6, tôi sẽ đề cập đến các môi trường máy tính để bàn đồ họa Linux phổ biến nhất được sử dụng bởi các bản phân phối Linux thịnh hành. Chương này bắt đầu cuộc thảo luận bằng việc khám phá máy tính để bàn GNOME.

## **Lịch sử của GNOME**

Máy tính để bàn GNOME (GNU Network Object Model Environment) \- như bạn có thể nghi ngờ từ tên gọi của nó \- là một phần của dự án GNU, nổi tiếng với việc tạo và hỗ trợ nhiều gói mã nguồn mở được sử dụng trong Linux (xem Chương 1). Phiên bản ban đầu của GNOME trở nên phổ biến vì nó là màn hình mặc định được sử dụng bởi Red Hat Linux, một trong những bản phân phối Linux thương mại đầu tiên. Kể từ đó, nó đã được nhiều bản phân phối Linux khác áp dụng, bao gồm cả Ubuntu.

Tuy nhiên, lịch sử của GNOME không phải lúc nào cũng trải đầy hoa hồng. Mặc dù phiên bản gốc của GNOME rất phổ biến, nhưng vào năm 2011, nhóm phát triển GNOME đã thực hiện một thay đổi lớn trong phiên bản 3\.

Thay vì môi trường máy tính để bàn đồ họa tiêu chuẩn mà hầu hết mọi người đã dần yêu thích và cảm thấy thoải mái, GNOME 3 kết hợp một mô hình hoàn toàn mới cho máy tính để bàn đồ họa — sử dụng một giao diện nhất quán giữa các thiết bị khác nhau, chẳng hạn như máy tính xách tay, máy tính bảng và điện thoại di động. Bất kể bạn sử dụng màn hình GNOME 3 trên loại thiết bị nào, trải nghiệm người dùng của bạn đều giống nhau.

Thiết kế mới đạt được điều này bằng cách ít chú trọng hơn vào các giao diện người dùng khó thao tác trên thiết bị di động (chẳng hạn như chọn mục từ các menu thả xuống dài ngoằng) và chú trọng nhiều hơn vào các giao diện người dùng mà bạn có thể cuộn và nhấp chuột (chẳng hạn như chọn mục từ danh sách các biểu tượng). Mặc dù điều này giúp mọi thứ dễ dàng hơn cho người dùng máy tính bảng và điện thoại di động, nhưng nó lại bị coi là một sự bất tiện đối với người dùng máy tính để bàn và laptop. Phiên bản mới của GNOME đã khiến thế giới Linux rơi vào tình trạng hoang mang, và thậm chí còn tạo ra một số môi trường máy tính để bàn đồ họa mới dựa trên phiên bản GNOME gốc (như bạn có thể thấy trong Chương 6).

Tuy nhiên, theo thời gian, mọi người trở nên thoải mái hơn với mô hình máy tính để bàn đằng sau GNOME 3, và hiện tại nó đã được (hầu hết) chấp nhận trong thế giới Linux. Các phần sau đây sẽ đi qua các điểm chính của màn hình GNOME 3 và cách bạn có thể tùy chỉnh mọi thứ theo ý thích của mình.

**MẸO:** Giao diện người dùng của máy tính để bàn đồ họa GNOME 3 hiện được gọi là GNOME Shell. Điều này có thể gây ra đôi chút nhầm lẫn, và bạn có thể thấy thuật ngữ GNOME 3 và GNOME Shell được sử dụng thay thế cho nhau trong các tài liệu và sách. Tôi thích chỉ sử dụng GNOME 3 để không nhầm lẫn nó với các màn hình GNOME gốc hoặc giao diện dòng lệnh (command line shell).

## **Mổ xẻ Máy tính để bàn GNOME**

Sự đơn giản đã trở thành dấu ấn của môi trường máy tính để bàn GNOME 3\. Không có bất kỳ menu dài ngoằng nào để bạn phải chọn lọc, bạn cũng không cần phải đào bới qua các thư mục để tìm kiếm tệp, nhưng việc làm quen với giao diện mới có thể mất chút thời gian. Phần này hướng dẫn các tính năng cơ bản của màn hình GNOME 3 để bạn có thể tự mình điều hướng.

### **Trình đơn (Menu) đâu rồi\!**

Ở trên cùng của màn hình GNOME 3 là một bảng điều khiển (được gọi là thanh trên cùng \- top bar). Khi màn hình nền mở ra lần đầu, nó chỉ chứa ba lựa chọn menu (như Hình 4-1).

Ba mục menu đó là:

* **Activities** (Hoạt động)  
* **Calendar and notifications** (Lịch và thông báo)  
* **System menu** (Menu hệ thống)

Các phần sau đây sẽ xem xét chi tiết những gì mỗi menu này chứa đựng.

### **Menu Activities (Hoạt động)**

Menu Activities là cách bạn truy cập vào các ứng dụng của mình và kiểm tra trạng thái của bất kỳ ứng dụng nào đang chạy. Bạn có thể mở menu Activities bằng ba phương pháp khác nhau:

* Nhấp vào mục menu **Activities** trên thanh trên cùng.  
* Di chuyển con trỏ chuột của bạn lên góc trên cùng bên trái của màn hình (một số bản phân phối Linux, chẳng hạn như Ubuntu, đã vô hiệu hóa tính năng này).  
* Nhấn phím **Super** trên bàn phím của bạn (chính là phím có logo Windows trên các PC).

Khi bạn mở menu Activities, bạn sẽ thấy bố cục tổng quan hoạt động (activities overview) như được hiển thị trong Hình 4-2.

Khu vực tổng quan hoạt động cung cấp một điểm dừng chân duy nhất để truy cập tất cả các ứng dụng của bạn và xem trạng thái của bất kỳ ứng dụng nào đang chạy trên màn hình. Nó bao gồm ba mục chính:

* Thanh **dash** (thanh công cụ)  
* Tổng quan cửa sổ (windows overview)  
* Bộ chọn không gian làm việc (workspace selector)

Tôi sẽ đi sâu hơn vào khu vực tổng quan hoạt động trong phần "Khám phá Tổng quan Hoạt động" ở phần sau.

### **Menu Lịch (Calendar)**

Mục menu Calendar (nằm ở giữa thanh trên cùng) tạo ra đúng như những gì bạn mong đợi — một cuốn lịch, như Hình 4-3. Nhưng đợi đã, vẫn còn nữa\!

Bên trái của cuốn lịch là khu vực thông báo. Khu vực thông báo hiển thị bất kỳ sự kiện lịch sắp tới nào mà bạn đã lên lịch. GNOME 3 cho phép bạn đồng bộ hóa lịch của mình với lịch trực tuyến từ nhiều ứng dụng phổ biến, chẳng hạn như Google, Facebook và Microsoft, cung cấp một cách tuyệt vời để xem tất cả các sự kiện lịch của bạn ở cùng một nơi\!

Bên cạnh việc theo dõi các cuộc hẹn của bạn, khu vực thông báo cũng hiển thị bất kỳ thông báo nào do hệ thống tạo ra, chẳng hạn như khi có bản nâng cấp và bản vá lỗi khả dụng để cài đặt, hoặc liệu hệ thống của bạn sắp hết dung lượng ổ đĩa hay không. Thanh trượt **Do Not Disturb** (Không làm phiền) cho phép bạn vô hiệu hóa các thông báo hệ thống bật lên trên màn hình của mình.

### **Menu hệ thống (System menu)**

Ở góc ngoài cùng bên phải của thanh trên cùng là menu hệ thống. Menu hệ thống hiển thị các biểu tượng cho biết trạng thái của một số tính năng trên hệ thống của bạn, tùy thuộc vào phần cứng nào có sẵn trên máy. Menu này có khả năng tùy chỉnh rất cao và thường hơi khác nhau giữa các bản phân phối Linux. Các tùy chọn menu hệ thống có thể bao gồm:

* Trạng thái kết nối mạng  
* Trạng thái card âm thanh  
* Cài đặt độ sáng màn hình  
* Trạng thái pin  
* Trạng thái của người dùng đang đăng nhập  
* Các tùy chọn khởi động lại

Để truy cập các tùy chọn menu này, hãy nhấp vào biểu tượng mũi tên hướng xuống trong menu hệ thống. Một menu thả xuống chứa các tùy chọn hệ thống sẽ xuất hiện, như Hình 4-4.

Nếu PC của bạn có card âm thanh, bạn có thể điều chỉnh âm lượng hoặc tắt tiếng loa, và nếu PC của bạn có màn hình có thể thay đổi độ sáng, cũng sẽ có cài đặt để điều chỉnh độ sáng màn hình ở đây.

Tiếp theo, bạn sẽ thấy một menu cho phép bạn quản lý kết nối mạng của mình (nếu có). Nếu PC của bạn sử dụng kết nối mạng không dây, một menu thả xuống cho phép bạn chọn mạng không dây để kết nối, cùng với các cài đặt mạng khác. Nếu PC của bạn sử dụng kết nối mạng có dây, bạn sẽ thấy các tùy chọn để vô hiệu hóa kết nối mạng và thay đổi cài đặt mạng. Có rất nhiều thứ cần giải quyết khi nói đến cài đặt mạng, vì vậy tôi sẽ đi sâu hơn vào vấn đề đó trong Chương 9\.

Là một phần của menu hệ thống, hầu hết các bản phân phối Linux đều bao gồm một tùy chọn để truy cập cài đặt hệ thống — thường là tùy chọn menu **Settings** (Cài đặt) hoặc dưới dạng một biểu tượng ở dưới cùng của menu hệ thống. Khi bạn chọn bất kỳ tùy chọn nào, hộp thoại Cài đặt Hệ thống (như Hình 4-5) sẽ xuất hiện. Nó cho phép bạn tùy chỉnh trải nghiệm màn hình nền theo ý thích của mình. Tôi sẽ thảo luận thêm về điều này trong phần "Tùy chỉnh Không gian của Bạn" ở phần sau của chương này.

Cũng trong menu hệ thống là tùy chọn để quản lý tài khoản người dùng hiện đang đăng nhập. Một số bản phân phối Linux tùy chỉnh tùy chọn này, do đó kết quả của bạn có thể khác với những gì được hiển thị trong Hình 4-4. Trong Ubuntu, bạn chỉ có thể khóa màn hình cho người dùng hiện tại (Lock). Fedora Linux cho phép bạn đăng xuất (Log Out) từ menu này, hoặc đi tới hộp thoại Settings cho tài khoản người dùng.

Ở dưới cùng của menu hệ thống là tùy chọn để tắt nguồn hoặc đăng xuất khỏi hệ thống. Tùy chọn menu tắt nguồn cung cấp một menu khác, cho phép bạn chọn khởi động lại (restart), tắt máy (shut down) hoặc tạm ngưng hệ thống (suspend).

### **Menu ứng dụng (Application menu)**

Mặc dù tôi đã đề cập rằng theo mặc định chỉ có ba menu hiển thị trên thanh trên cùng, nhưng đôi khi menu thứ tư sẽ xuất hiện. Khi bạn khởi chạy một ứng dụng trên màn hình GNOME 3, một menu riêng xuất hiện ở thanh trên cùng. Đây là menu ứng dụng, chứa các tùy chọn liên quan đến ứng dụng đó. Thay vì đặt menu ứng dụng vào thanh tiêu đề cửa sổ của ứng dụng, GNOME 3 lại đặt nó ở thanh trên cùng, tách biệt với cửa sổ ứng dụng. Điều này có thể cần chút thời gian để làm quen.

Các tùy chọn có sẵn trong menu ứng dụng khác nhau tùy thuộc vào ứng dụng mà bạn đang mở trên màn hình nền. Hầu hết các ứng dụng đều cung cấp các tùy chọn cho phép bạn mở một cửa sổ mới của ứng dụng hoặc thoát khỏi cửa sổ hiện tại. Một số ứng dụng cũng cung cấp các tính năng dành riêng cho ứng dụng đó.

### **Màn hình nền (The desktop)**

Trong nhiều môi trường máy tính để bàn đồ họa, màn hình nền là vua. Thường thì hầu hết mọi việc bạn làm đều diễn ra từ một biểu tượng trên màn hình nền. Có một ứng dụng yêu thích? Tạo một biểu tượng trên màn hình để khởi chạy nó. Có một tệp mà bạn cần mở hàng ngày? Tạo một biểu tượng trên màn hình để mở nó. Cắm một thẻ USB mới vào? Hệ thống tự động tạo một biểu tượng trên màn hình nền để truy cập nó.

Mô hình GNOME 3 đã thay đổi điều đó một chút. Các biểu tượng trên màn hình nền không còn là cách ưa thích để khởi chạy ứng dụng, lưu trữ tệp hoặc truy cập phương tiện có thể tháo rời. Trên thực tế, nhiều bản phân phối Linux thậm chí không thèm tạo bất kỳ biểu tượng nào trên màn hình nền theo mặc định\! Tuy nhiên, nếu bạn gặp khó khăn trong việc phá bỏ những thói quen cũ, GNOME 3 vẫn cho phép bạn tạo và sử dụng các biểu tượng trên màn hình nền.

Bản phân phối Linux Ubuntu tạo hai biểu tượng máy tính để bàn theo mặc định:

* **Thư mục Home:** Mở chương trình quản lý tệp (Files) và mặc định trỏ đến thư mục Home của tài khoản người dùng.  
* **Thư mục Thùng rác (Trash):** Mở chương trình quản lý tệp và mặc định trỏ đến thư mục Trash của tài khoản người dùng.

Bạn có thể làm một vài điều từ màn hình nền. Nhấp chuột phải vào vùng trống trên màn hình nền và một menu bật lên sẽ mở ra (như Hình 4-6).

Menu bật lên trên màn hình nền cung cấp cho bạn một vài lựa chọn khác nhau:

* **New Folder:** Tạo một thư mục mới bên dưới thư mục Desktop của tài khoản người dùng của bạn.  
* **Paste:** Dán bất kỳ tệp hoặc thư mục nào đã sao chép ra màn hình.  
* **Show Desktop in Files:** Mở thư mục Desktop bằng chương trình quản lý tệp (Files) (xem Chương 8).  
* **Open in Terminal:** Mở thư mục Desktop bằng giao diện dòng lệnh Terminal (xem Chương 16).  
* **Change Background:** Sửa đổi hình ảnh được sử dụng cho hình nền màn hình.  
* **Display Settings:** Thay đổi cài đặt hướng và độ phân giải cho màn hình.  
* **Settings:** Truy cập công cụ cài đặt Hệ thống.

Điều này cung cấp cho bạn quyền truy cập nhanh vào một số cài đặt hệ thống liên quan đến màn hình nền, như được mô tả ở phần "Tùy chỉnh Không gian của Bạn".

**MẸO:** Nhiều màn hình đồ họa cho phép bạn tạo tệp mới bằng cách nhấp chuột phải vào màn hình, thật không may GNOME 3 không nằm trong số đó. Nếu muốn tạo biểu tượng cho tệp trên màn hình nền của mình, bạn cần lưu trữ tệp đó trong thư mục Desktop, nằm trong thư mục Home của bạn, bằng cách sử dụng chương trình quản lý tệp (Files).

## **Khám phá Tổng quan Hoạt động (Activities Overview)**

Khu vực tổng quan hoạt động là thứ đã thay thế hệ thống menu Ứng dụng được sử dụng trong các phiên bản GNOME cũ hơn, và là nguyên nhân khiến GNOME 3 gây ra nhiều tranh cãi. Mặc dù nó được thiết kế để dễ dàng điều hướng xung quanh, cấu trúc và bố cục tổng thể có thể gây nhầm lẫn, đặc biệt nếu bạn đã quen sử dụng hệ thống menu cũ. Phần này hướng dẫn ba tính năng của tổng quan hoạt động: thanh dash, tổng quan cửa sổ và bộ chọn không gian làm việc.

### **Thanh dash**

Dash là một tập hợp các biểu tượng ứng dụng xuất hiện ở phía bên trái của tổng quan hoạt động theo mặc định. Một số bản phân phối Linux đã chọn hiển thị dash theo mặc định, do đó nó xuất hiện trên màn hình nền mà bạn không cần phải làm gì cả (như Hình 4-7).

Các bản phân phối Linux khác đã chọn giữ thanh dash như một phần của phần tổng quan hoạt động, vì vậy bạn cần nhấp vào tùy chọn menu **Activities** trên thanh trên cùng để xem nó.

Dù bằng cách nào, khi dash xuất hiện, nó chứa một số biểu tượng, như được giải thích trong các phần tiếp theo.

#### **Mục Yêu thích (Favorites)**

Mặc dù các bậc cha mẹ không nên thiên vị, nhưng người dùng Linux thì thường xuyên làm vậy. Thanh dash cung cấp một khu vực nơi bạn có thể đặt các biểu tượng khởi chạy các ứng dụng yêu thích của mình, giúp bạn dễ dàng bắt đầu các ứng dụng thường dùng.

Hầu hết các bản phân phối Linux cung cấp một số ít các ứng dụng mặc định dưới dạng danh sách yêu thích để giúp bạn bắt đầu mọi thứ. Trong Ubuntu, các ứng dụng yêu thích là:

* Trình duyệt web Firefox  
* Ứng dụng email Thunderbird  
* Chương trình quản lý tệp (Files)  
* Trình phát âm thanh RhythmBox  
* LibreOffice Writer để xử lý văn bản  
* Ứng dụng Phần mềm Ubuntu (Ubuntu software)  
* Hướng dẫn trợ giúp màn hình Ubuntu

Nhấp vào một biểu tượng yêu thích sẽ khởi chạy ứng dụng tương ứng. Nhấp chuột phải vào một biểu tượng yêu thích sẽ tạo ra một menu với các tùy chọn mặc định sau:

* Mở một cửa sổ mới cho ứng dụng.  
* Các tùy chọn dành riêng cho ứng dụng, chẳng hạn như mở cửa sổ duyệt web riêng tư cho Firefox, hoặc tạo tài liệu mới cho Writer.  
* Xóa biểu tượng yêu thích khỏi thanh dash (Remove from Favorites).

Một số ứng dụng cung cấp các tùy chọn bổ sung trong menu dash để bạn có thể kiểm soát các tính năng bên trong ứng dụng trực tiếp từ biểu tượng dash, trong khi những ứng dụng khác thì không. Bạn cần tham khảo tài liệu của ứng dụng cụ thể đó để xem bạn có sẵn những tùy chọn nào.

#### **Các ứng dụng đang chạy**

Bên cạnh các biểu tượng cho các ứng dụng yêu thích của bạn, dash cũng hiển thị các biểu tượng cho bất kỳ ứng dụng máy tính để bàn nào hiện đang chạy. Khi một ứng dụng đang hoạt động, một dấu chấm sẽ xuất hiện bên cạnh biểu tượng ứng dụng trong dash.

Nhấp chuột phải vào biểu tượng của một ứng dụng đang chạy và một menu nhỏ bật lên cung cấp một số lựa chọn về những gì bạn có thể làm:

* Mở cửa sổ ứng dụng, hoặc một cửa sổ cụ thể của ứng dụng nếu ứng dụng đó có nhiều hơn một cửa sổ đang mở.  
* Mở một cửa sổ mới cho ứng dụng.  
* Thêm ứng dụng vào dash làm mục yêu thích (Add to Favorites) nếu nó chưa phải là mục yêu thích.

Khi bạn thoát khỏi một ứng dụng, biểu tượng của nó sẽ tự động biến mất khỏi dash (trừ khi nó là một ứng dụng được đánh dấu là yêu thích).

#### **Phương tiện có thể tháo rời**

Khi bạn cắm một thiết bị phương tiện có thể tháo rời (chẳng hạn như đĩa DVD hoặc thẻ USB) vào PC, một biểu tượng sẽ xuất hiện trong dash cho thiết bị đó (như Hình 4-8).

Nhấp vào biểu tượng thiết bị để mở cửa sổ Files nhằm xem nội dung của thiết bị tháo rời. Khi bạn đã sẵn sàng tháo thiết bị, hãy nhấp chuột phải vào biểu tượng thiết bị và chọn tùy chọn menu **Eject** (Đẩy ra).

#### **Biểu tượng tổng quan ứng dụng**

Khi bạn nhấp vào biểu tượng tổng quan ứng dụng trong dash (biểu tượng dạng lưới ở dưới cùng của dash), bạn sẽ thấy phần tổng quan ứng dụng ở giữa màn hình nền (như Hình 4-9).

Khu vực tổng quan ứng dụng hiển thị biểu tượng cho tất cả các ứng dụng máy tính để bàn hiện được cài đặt. Bạn có thể cuộn xuống khu vực tổng quan ứng dụng để xem các trang bổ sung nếu có nhiều biểu tượng hơn. Ở dưới cùng của khu vực tổng quan ứng dụng là các tùy chọn để hiển thị tất cả các biểu tượng ứng dụng (All) hoặc chỉ các biểu tượng ứng dụng được sử dụng thường xuyên (Frequent). Việc chọn các ứng dụng được sử dụng thường xuyên sẽ thu hẹp các biểu tượng ứng dụng xuống chỉ còn các ứng dụng bạn đã sử dụng gần đây.

Trong khu vực tổng quan ứng dụng, hãy nhấp vào biểu tượng của ứng dụng để khởi chạy nó trên màn hình. Nếu bạn muốn thêm ứng dụng vào khu vực yêu thích trên dash, hãy nhấp chuột phải vào biểu tượng trong tổng quan ứng dụng và chọn **Add to Favorites**.

**MẸO:** Rất có thể tính năng linh hoạt nhất của tổng quan ứng dụng là hộp văn bản Tìm kiếm (Search) ở trên cùng. Hộp văn bản Tìm kiếm cho phép bạn tìm kiếm không chỉ các ứng dụng mà còn cả các tài liệu nằm trong các thư mục. Đây là một công cụ tuyệt vời để tìm kiếm các tài liệu bị thất lạc\!

### **Khu vực tổng quan cửa sổ (Windows overview)**

Ở giữa phần tổng quan hoạt động là tổng quan cửa sổ. Tổng quan cửa sổ cung cấp quyền truy cập nhanh để quản lý các ứng dụng đang hoạt động trên màn hình. Nó hiển thị một tập hợp các hình ảnh thu nhỏ của tất cả các cửa sổ ứng dụng hiện đang chạy trên màn hình. Khi bạn nhấp vào hình thu nhỏ của một ứng dụng trong tổng quan cửa sổ, ứng dụng đang chạy trên màn hình sẽ được đưa lên phía trước. Bạn cũng có thể chấm dứt một ứng dụng máy tính để bàn đang chạy bằng cách nhấp vào vòng tròn màu đỏ xuất hiện ở góc trên cùng bên phải của hình thu nhỏ khi bạn di chuột qua hình thu nhỏ.

Một hộp văn bản tìm kiếm cũng nằm ở trên cùng của khu vực tổng quan cửa sổ (tham khảo Hình 4-2). Cũng giống như trong khu vực tổng quan ứng dụng, ở đây bạn có thể nhập tên ứng dụng, tên tệp hoặc tên tài nguyên để tìm kiếm trên hệ thống của mình. Khi bạn nhập, GNOME sẽ tìm kiếm một nhóm vị trí được thiết lập trước để tìm các ứng dụng và tệp phù hợp, đồng thời hiển thị danh sách các kết quả phù hợp trong khu vực tìm kiếm. Khi bạn thấy những gì mình đang tìm kiếm, chỉ cần nhấp vào biểu tượng của nó để khởi chạy nó. Đây là một cách tuyệt vời để truy cập các tệp mà bạn đã "chôn giấu" trong các thư mục của mình\!

**MẸO:** Bên cạnh tổng quan cửa sổ, còn có một cách khác để chuyển đổi giữa các ứng dụng đang chạy trên màn hình nền:

1. Nhấn phím **Super** (phím Windows trên PC Windows) và phím **Tab**.  
   Trình chuyển đổi cửa sổ xuất hiện ở giữa màn hình nền, hiển thị biểu tượng cho từng ứng dụng hiện đang chạy trên màn hình.  
2. Giữ phím **Super** và nhấn phím **Tab** để chuyển đổi giữa các ứng dụng đang chạy.  
   Nhả phím **Super** khi bạn làm nổi bật ứng dụng mà bạn muốn chuyển sang.

Sau khi bạn mở trình chuyển đổi cửa sổ bằng tổ hợp phím **Super \+ Tab**, bạn có thể chọn chuyển sang ứng dụng nào trực tiếp bằng cách dùng chuột nhấp vào biểu tượng ứng dụng đó.

### **Làm việc với không gian làm việc (Workspaces)**

Ở góc ngoài cùng bên phải của tổng quan hoạt động là bộ chọn không gian làm việc (workspace selector). Một khái niệm đã xuất hiện từ khá lâu là tính năng màn hình ảo (virtual desktop). Màn hình ảo cho phép bạn xác định các khu vực màn hình riêng biệt và mở các cửa sổ ứng dụng trong các màn hình riêng biệt đó. Điều đó cho phép bạn nhóm các ứng dụng lại với nhau và chuyển đổi màn hình nền thay vì có nhiều cửa sổ mở trên cùng một màn hình.

GNOME 3 triển khai các màn hình ảo, nhưng có một chút thay đổi. Các không gian làm việc (workspaces) là một phần của cùng một màn hình nền; chúng chỉ đặt các cửa sổ ứng dụng thành các nhóm riêng biệt để giúp bạn quản lý chúng dễ dàng hơn. Bạn kiểm soát điều này bằng cách sử dụng bộ chọn không gian làm việc.

Khi bạn mở tổng quan hoạt động lần đầu, bộ chọn không gian làm việc bị thu nhỏ về kích thước, nhưng nếu bạn di con trỏ chuột qua khu vực đó, nó sẽ xuất hiện toàn bộ (như Hình 4-10).

Theo mặc định, Ubuntu tạo một không gian làm việc duy nhất và đặt bất kỳ ứng dụng nào bạn bắt đầu vào không gian làm việc đó. Bạn có thể di chuyển một ứng dụng sang một không gian làm việc mới bằng cách làm theo các bước sau:

1. Mở tổng quan hoạt động (activities overview).  
2. Nhấp và giữ hình thu nhỏ của ứng dụng trong khu vực tổng quan cửa sổ mà bạn muốn di chuyển. Con trỏ chuột sẽ biến thành hình bàn tay.  
3. Kéo hình thu nhỏ của ứng dụng đến khu vực bộ chọn không gian làm việc. Khi bạn di chuyển con trỏ bàn tay đến bộ chọn không gian làm việc, một cửa sổ không gian làm việc mới sẽ xuất hiện trong bộ chọn.  
4. Thả hình thu nhỏ của ứng dụng vào khu vực không gian làm việc mới.

Sau khi bạn có ứng dụng trong hai hoặc nhiều không gian làm việc, bạn có thể dễ dàng chuyển đổi xem không gian làm việc nào đang hoạt động trên màn hình nền của mình. Có hai phương pháp để làm điều đó:

* Mở tổng quan hoạt động, sau đó chọn không gian làm việc từ bộ chọn không gian làm việc.  
* Từ màn hình nền, nhấn phím **Super \+ Page Down** để chuyển sang không gian làm việc thấp hơn tiếp theo, hoặc phím **Super \+ Page Up** để chuyển sang không gian làm việc cao hơn tiếp theo trong vòng quay.

Nếu bạn là một người làm việc đa nhiệm thực thụ và có nhiều ứng dụng mở trên màn hình nền, điều này cung cấp một cách dễ dàng để giúp giữ mọi thứ ngăn nắp\!

## **Tùy chỉnh Không gian của Bạn**

Tôi đã đề cập ở đầu chương này rằng Linux rất nổi tiếng về việc cung cấp các lựa chọn khi nói đến môi trường máy tính để bàn đồ họa. Điều tôi chưa đề cập là ngay cả sau khi bạn chọn một màn hình nền cụ thể để sử dụng, bạn vẫn có rất nhiều lựa chọn để tùy chỉnh trải nghiệm màn hình của mình.

Điều này được thực hiện với các tùy chọn cài đặt máy tính để bàn trong công cụ Settings (Cài đặt) chung của GNOME 3\. Bạn có thể truy cập công cụ Settings bằng cách nhấp chuột phải vào một vùng trống trên màn hình nền và chọn **Settings**, hoặc bằng cách chọn tùy chọn **Settings** trong menu hệ thống đã thảo luận ở phần "Trình đơn (Menu) đâu rồi\!" trước đó.

Bạn có thể tùy chỉnh rất nhiều thứ bằng công cụ Settings. Hiện tại, tôi chỉ thảo luận về các cài đặt khác nhau liên quan đến màn hình nền mà bạn có thể sử dụng để tùy chỉnh trải nghiệm màn hình GNOME 3 của mình.

### **Hình nền (Background)**

Các nhà phát triển của mỗi bản phân phối Linux đều chọn một hình ảnh nền màn hình mặc định để giúp xác định bản phân phối của họ. Fedora sử dụng một phối màu cách điệu khác nhau cho mỗi bản phát hành, trong khi Ubuntu sử dụng một số loại hình ảnh cách điệu của loài động vật mà bản phát hành được đặt tên theo.

Tuy nhiên, bạn không bị bó buộc với những hình nền màn hình đó. Bạn có thể dễ dàng thay đổi hình nền máy tính của mình; chỉ cần làm theo các bước sau:

1. Mở tùy chọn **Background** trong công cụ Settings. (Bạn có thể thực hiện việc này bằng cách nhấp chuột phải vào màn hình nền và chọn **Change Background**. Hoặc, nếu bạn đang ở trong công cụ Settings, hãy chọn Background ở menu bên trái).  
2. Cuộn qua các hình ảnh có sẵn và chọn một. Mỗi bản phân phối Linux sẽ chọn bộ hình ảnh riêng của mình để bao gồm theo mặc định. Nếu bạn có hình ảnh riêng muốn sử dụng, hãy nhấp vào nút **Add Picture** ở trên cùng của công cụ Settings.

**MẸO:** Mỗi người dùng trên hệ thống có thể chọn hình nền máy tính của riêng mình, vì vậy nếu bạn phải chia sẻ PC của mình với người khác, bạn sẽ không bị mắc kẹt khi phải dán mắt vào bức ảnh về thú cưng yêu thích của người kia cả ngày\!

### **Giao diện (Appearance)**

Bạn không chỉ có thể thay đổi hình nền máy tính mà còn có thể thay đổi màu sắc được sử dụng trong chính các cửa sổ ứng dụng. Từ công cụ Settings, nhấp vào tùy chọn **Appearance** ở menu bên trái. Cửa sổ Appearance sẽ xuất hiện (như Hình 4-11).

Trong phần Window Colors (Màu Cửa sổ), tùy chọn Appearance cho phép bạn đặt độ đổ bóng của các cửa sổ ứng dụng: Chọn sáng (light), tiêu chuẩn (standard) hoặc tối (dark).

Bên dưới đó là một số cài đặt bạn có thể thay đổi để kiểm soát thanh dash (được gọi là dock trong phần Settings). Nếu bản phân phối Linux của bạn hiển thị dash trên màn hình nền, bạn có thể chọn tự động ẩn nó (auto-hide) khi một ứng dụng muốn chuyển sang chế độ toàn màn hình. Tính năng này cho phép các ứng dụng đẩy thanh dash ra khỏi đường đi và chiếm toàn bộ khu vực xem của màn hình nền.

Từ đây, bạn cũng có thể thay đổi kích thước của các biểu tượng ứng dụng xuất hiện trong dash (cả các ứng dụng yêu thích và ứng dụng đang chạy), cũng như đặt cạnh của màn hình nơi dash xuất hiện khi bạn mở phần tổng quan hoạt động (trái, phải, trên cùng hoặc dưới cùng).

### **Màn hình (Displays)**

Việc cố gắng làm cho màn hình đồ họa hoạt động với vô số các loại card video và màn hình khác nhau có thể là một cơn ác mộng. Hầu hết các bản phân phối Linux đều cố gắng hết sức để tự động phát hiện card video và màn hình của bạn tại thời điểm cài đặt và thiết lập độ phân giải màn hình, nhưng chúng không phải lúc nào cũng chính xác hoặc không nhận ra thiết lập phần cứng cụ thể của bạn. Nếu trường hợp đó xảy ra, tập lệnh cài đặt thường dự phòng về một cài đặt mặc định, cài đặt này có thể không tối ưu cho thiết lập của bạn.

Nếu đó là trường hợp của bạn, vẫn còn hy vọng vì bạn có thể tùy chỉnh cài đặt hiển thị cho màn hình GNOME 3\. Trong công cụ Settings, hãy nhấp vào mục **Displays** ở menu bên trái, và bạn sẽ thấy các tùy chọn khác nhau mà bạn có thể thay đổi cho màn hình của mình (như Hình 4-12).

Những gì bạn thấy ở đây chủ yếu phụ thuộc vào thiết lập màn hình của bạn. Tối thiểu, bạn sẽ thấy ba tùy chọn để thay đổi:

* **Orientation (Hướng):** Cách màn hình được định hướng liên quan đến bàn phím. Với màn hình phẳng, bạn có rất nhiều tùy chọn gắn kết \- chẳng hạn như đặt màn hình nằm nghiêng sang một bên. Nếu đúng như vậy, bạn có thể thay đổi hướng màn hình thành Dọc (Portrait) ở đây. Nếu màn hình của bạn phải được gắn lộn ngược, chỉ cần chọn tùy chọn Ngang (bị lật) \- Landscape (flipped).  
* **Resolution (Độ phân giải):** Đây là nơi bạn có thể thay đổi cài đặt độ phân giải hoặc tỷ lệ khung hình cho màn hình của mình. Bạn có thể thử nghiệm các cài đặt khác nhau để tìm ra cài đặt mà bạn cảm thấy thoải mái nhất.  
* **Fractional Scaling (Chia tỷ lệ phân số):** Cài đặt này cho phép bạn chia tỷ lệ kích thước của các cửa sổ và văn bản trong màn hình nền. Bật tính năng này cho phép bạn đặt giá trị phân số, chẳng hạn như làm cho các đối tượng lớn hơn 125% hoặc 200% so với bình thường.

Nếu bạn có nhiều màn hình được kết nối với PC, đây là nơi bạn có thể kiểm soát cách chúng hoạt động. Khi GNOME 3 phát hiện nhiều màn hình, nó sẽ mở rộng cài đặt Displays để bao gồm các cài đặt cho nhiều màn hình (như Hình 4-13).

Điều đầu tiên bạn nên làm là chọn chế độ hiển thị. Có ba chế độ:

* **Join Displays (Nối Màn hình):** Theo mặc định, GNOME 3 sử dụng màn hình thứ hai để mở rộng màn hình nền và đặt màn hình thứ hai ở bên phải màn hình chính (nếu bạn di chuyển con trỏ chuột ra khỏi phía bên phải của màn hình, nó sẽ đi vào khu vực màn hình nền của màn hình thứ hai). Nếu màn hình thứ hai của bạn nằm ở vị trí thực tế khác, bạn có thể di chuyển biểu tượng màn hình thứ hai sang bất kỳ phía nào của biểu tượng màn hình chính để phản ánh vị trí thực tế của nó. Hình 4-13 cho thấy màn hình phụ của tôi được di chuyển sang phía bên trái của màn hình chính. Nếu cần, bạn thậm chí có thể chọn màn hình nào là màn hình chính.  
* **Mirror (Phản chiếu):** Thay vì mở rộng khu vực màn hình nền bằng màn hình thứ hai, bạn có thể chọn chỉ phản chiếu một màn hình nền duy nhất trên tất cả các màn hình được kết nối với PC. Bất cứ điều gì bạn làm trên màn hình chính đều được phản chiếu trên bất kỳ màn hình nền nào khác. Điều này rất tiện lợi khi thực hiện các bài thuyết trình.  
* **Single Display (Hiển thị Đơn):** Tùy chọn thứ ba khả dụng là coi mỗi màn hình như một màn hình hiển thị riêng biệt, không mở rộng màn hình chính.

Sau khi bạn đã thực hiện lựa chọn của mình từ nút thích hợp ở đầu cài đặt Displays, các tùy chọn bổ sung cho màn hình sẽ thay đổi tương ứng.

### **Chuột và bàn di chuột (Mouse and touchpad)**

Cài đặt chuột và bàn di chuột là một lĩnh vực khác mà các tập lệnh cài đặt cố gắng tự động phát hiện những gì cần thiết cho phần cứng cụ thể của bạn, nhưng không nhất thiết lúc nào cũng làm đúng. Nhấp vào tùy chọn **Mouse & Touchpad** ở phía bên trái của công cụ Settings để tùy chỉnh cài đặt chuột và/hoặc bàn di chuột của bạn (như Hình 4-14).

Cài đặt cho phép bạn chọn nút chuột nào là nút chính (nhấp chuột trái cho thiết lập dành cho người thuận tay phải, và nhấp chuột phải cho thiết lập dành cho người thuận tay trái). Bạn cũng có thể thiết lập tốc độ chuột khi di chuyển trên màn hình nền, cũng như bật tính năng cuộn tự nhiên (natural scrolling), tính năng này sẽ di chuyển nội dung của cửa sổ thay vì toàn bộ chế độ xem của cửa sổ.

## **Xem xét Kỹ hơn Các tính năng Trợ năng (Accessibility)**

Màn hình GNOME 3 bao gồm một số tính năng cho phép người khuyết tật vận hành các ứng dụng trên màn hình nền bằng các phương pháp thay thế. Các tính năng này bao gồm kính lúp màn hình (phóng to các khu vực của màn hình), trình đọc màn hình (đọc văn bản trên màn hình), và các tính năng trợ giúp bàn phím và chuột (chẳng hạn như phím cố định \- sticky keys và nhấp chuột chậm). Bạn có thể kích hoạt từng tính năng khi cần.

Bạn truy cập các tính năng trợ năng từ công cụ Settings. Hãy làm theo các bước sau để thực hiện điều đó:

1. Mở công cụ **Settings**.  
2. Chọn tùy chọn **Universal Access** (Truy cập Phổ quát) từ menu bên trái.  
3. Bật các tính năng bạn yêu cầu cho môi trường của mình.

Khi bạn chọn tùy chọn Universal Access trong công cụ Settings, bạn sẽ thấy rất nhiều tùy chọn để kích hoạt (như Hình 4-15).

Các tùy chọn được chia thành bốn danh mục:

* **Seeing (Nhìn):** Các tùy chọn để kích hoạt các tính năng cho người khiếm thị.  
* **Hearing (Nghe):** Các tùy chọn để kích hoạt các tính năng cho người điếc và khiếm thính.  
* **Typing (Gõ phím):** Các tùy chọn để kích hoạt các tính năng hỗ trợ gõ phím.  
* **Pointing & Clicking (Trỏ & Nhấp chuột):** Các tùy chọn để kích hoạt các tính năng hỗ trợ sử dụng chuột.

Danh mục **Seeing** bao gồm các tính năng sau:

* **High Contrast (Độ tương phản cao):** Làm cho các cửa sổ và biểu tượng trở nên sống động hơn để dễ nhìn hơn.  
* **Large Text (Văn bản lớn):** Sử dụng phông chữ lớn hơn cho văn bản trên máy tính để bàn.  
* **Cursor Size (Kích thước con trỏ):** Thay đổi kích thước con trỏ để dễ tìm hơn.  
* **Zoom (Thu phóng):** Phóng to các khu vực cụ thể của màn hình để dễ đọc hơn.  
* **Screen Reader (Trình đọc màn hình):** Sử dụng chương trình giọng nói Orca để đọc văn bản trên màn hình.  
* **Sound Keys (Âm thanh phím):** Tạo ra âm báo rõ ràng khi các phím được nhấn.

Danh mục **Hearing** chỉ bao gồm một tính năng \- khả năng kích hoạt cảnh báo trực quan (visual alerts) khi hệ thống phát ra tiếng bíp cảnh báo.

Danh mục **Typing** bao gồm các tính năng sau:

* **Screen Keyboard (Bàn phím màn hình):** Hiển thị bàn phím ảo trên màn hình khi có thể nhập văn bản.  
* **Repeat Keys (Phím lặp lại):** Mô phỏng việc nhấn phím nhiều lần khi một phím được giữ.  
* **Cursor Blinking (Nhấp nháy con trỏ):** Làm cho con trỏ chuột nhấp nháy để dễ tìm hơn.  
* **Typing Assist (Hỗ trợ Gõ phím):** Cho phép bạn bật ba tính năng gõ riêng biệt \- phím dính (sticky keys), phím chậm (slow keys) và phím nảy (bounce keys).

Danh mục **Pointing & Clicking** bao gồm các tính năng sau:

* **Mouse keys (Phím chuột):** Mô phỏng chuyển động và thao tác nhấp chuột bằng cách sử dụng các phím trên bàn phím.  
* **Locate Pointer (Định vị con trỏ):** Giúp bạn dễ dàng tìm thấy con trỏ trên màn hình hơn.  
* **Click Assist (Hỗ trợ Nhấp chuột):** Mô phỏng nhấp đúp bằng cách giữ nút chính hoặc di chuột qua một điểm.  
* **Double-Click Delay (Độ trễ nhấp đúp):** Đặt tốc độ mà nút chuột được nhấp đúp để gửi lệnh sự kiện nhấp đúp.

Nếu bạn cần bật và tắt các tính năng hỗ trợ cụ thể thường xuyên, cài đặt Universal Access cũng có một menu thả xuống mà bạn có thể kích hoạt trong menu hệ thống. Chỉ cần bật tính năng **Always Show Universal Access Menu** (Luôn hiển thị Menu Truy cập Phổ quát) trong phần cài đặt và một biểu tượng sẽ xuất hiện trong menu hệ thống (như Hình 4-16). Khi bạn nhấp vào menu, menu thả xuống sẽ xuất hiện, cho phép bạn dễ dàng bật và tắt các tính năng cụ thể.