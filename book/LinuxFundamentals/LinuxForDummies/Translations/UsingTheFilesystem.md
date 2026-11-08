# **Chương 8: Sử dụng Hệ thống tệp**

**TRONG CHƯƠNG NÀY**

* Quản lý hệ thống tệp của bạn với ứng dụng Files  
* Khám phá trình quản lý tệp Dolphin  
* Xem qua trình quản lý tệp Thunar

Các chương 4, 5 và 6 đã trình bày chi tiết về một số máy tính để bàn đồ họa phổ biến hiện có trong Linux và cách sử dụng chúng, nhưng tôi đã cố tình bỏ qua một kỹ năng: xử lý các tệp tin. Chương 7 giải quyết cách làm việc với các tệp và thư mục bằng cách sử dụng giao diện dòng lệnh (command line), điều này có thể hơi cồng kềnh, đặc biệt nếu bạn mới làm quen với Linux. Nếu bạn đã quen thuộc với thế giới Microsoft Windows hoặc Mac OS, bạn đã quen với việc sử dụng các công cụ đồ họa để thao tác với tệp và thư mục (và trong thế giới đồ họa, các thư mục thường được gọi là *folder* vì biểu tượng kẹp tài liệu được sử dụng để đại diện cho chúng). Đừng lo lắng — Linux sẽ không làm bạn thất vọng đâu. Chương này tập trung vào việc chỉ cần nhấp chuột là bạn có thể dạo quanh các thư mục và thao tác tệp một cách dễ dàng.

## **Nhấp chuột để Dạo quanh Hệ thống tệp (Clicking Your Way Through the Filesystem)**

Chìa khóa để quản lý tệp và thư mục từ màn hình đồ họa của bạn là chương trình quản lý tệp (file manager). Chương trình quản lý tệp cung cấp một giao diện đồ họa đẹp mắt cho mớ bòng bong các tệp và thư mục có trên hệ thống của bạn. Thay vì phải đào bới thông qua các lệnh trên dòng lệnh, bạn chỉ cần trỏ và nhấp chuột để tiến tới một hệ thống tệp được quản lý gọn gàng\!

Tuy nhiên, giống như hầu hết mọi thứ khác trong thế giới Linux, bạn có thể chọn từ một số chương trình quản lý tệp khác nhau. Trình quản lý tệp mặc định có sẵn trong hệ thống của bạn phụ thuộc vào môi trường máy tính để bàn bạn đang sử dụng.

### **Quản lý hệ thống tệp của bạn với ứng dụng Files**

Nếu bạn đang sử dụng máy tính để bàn GNOME 3 (chẳng hạn như trong Ubuntu), trình quản lý tệp mặc định đơn giản được gọi là **Files** (trước đây nó được gọi là Nautilus). Bạn có thể khởi chạy ứng dụng Files bằng cách nhấp vào biểu tượng của nó trên thanh dash hoặc tìm kiếm nó trong phần tổng quan hoạt động (Activities overview).

Khi mở Files, bạn sẽ thấy giao diện được chia làm hai phần chính:

* **Khung bên trái (Sidebar):** Cung cấp các lối tắt truy cập nhanh đến các thư mục phổ biến (như Home, Documents, Downloads, Music, Pictures, Videos), thùng rác (Trash) và bất kỳ ổ đĩa mạng hoặc thiết bị USB nào đang được kết nối.  
* **Khung chính (Main view):** Hiển thị nội dung của thư mục hiện đang được chọn.

Bạn có thể điều hướng bằng cách nhấp đúp vào các thư mục trong khung chính hoặc nhấp chuột một lần vào các lối tắt ở khung bên trái. Các biểu tượng lớn và rõ ràng giúp việc tìm kiếm tệp trở nên cực kỳ trực quan.

### **Khám phá trình quản lý tệp Dolphin**

Đối với những người dùng sử dụng máy tính để bàn KDE Plasma (như trong openSUSE hoặc Kubuntu), trình quản lý tệp tiêu chuẩn là **Dolphin**. Dolphin nổi tiếng với việc cung cấp nhiều tính năng nâng cao và khả năng tùy biến cao.

Giao diện của Dolphin cũng bao gồm một khung Places (Vị trí) ở bên trái và một khu vực xem tệp ở bên phải. Tuy nhiên, Dolphin cho phép bạn:

* **Chia đôi màn hình (Split view):** Bạn có thể xem hai thư mục cùng lúc cạnh nhau, làm cho việc kéo và thả (drag-and-drop) tệp giữa các thư mục trở nên dễ dàng hơn bao giờ hết. Nhấn phím F3 để kích hoạt tính năng này.  
* **Tích hợp Terminal:** Bạn có thể mở một bảng điều khiển dòng lệnh ngay bên dưới cửa sổ quản lý tệp bằng cách nhấn F4, rất tiện lợi nếu bạn muốn gõ lệnh nhanh trong thư mục hiện tại.

### **Xem qua trình quản lý tệp Thunar**

Nếu bạn thích sự gọn nhẹ và đang chạy môi trường máy tính để bàn Xfce (chẳng hạn như trong MX Linux), **Thunar** sẽ là trình quản lý tệp mặc định của bạn.

Thunar được thiết kế để khởi động nhanh và hoạt động mượt mà ngay cả trên phần cứng cũ. Mặc dù nó không có quá nhiều tính năng đồ sộ như Dolphin, nó cung cấp một giao diện cực kỳ sạch sẽ, tốc độ phản hồi nhanh, và hoàn thành xuất sắc các tác vụ quản lý tệp cơ bản.

## **Làm việc với Tệp và Thư mục**

Bất kể bạn đang sử dụng Files, Dolphin hay Thunar, các thao tác cơ bản với tệp đều hoạt động gần như giống hệt cách bạn làm trên Windows hoặc Mac.

* **Tạo thư mục mới (Create a new folder):** Nhấp chuột phải vào vùng trống trong cửa sổ trình quản lý tệp và chọn *New Folder* (Thư mục mới) hoặc *Create New \-\> Folder*.  
* **Sao chép và Di chuyển (Copy and Move):** Bạn có thể kéo và thả tệp từ cửa sổ này sang cửa sổ khác. Bạn cũng có thể nhấp chuột phải vào tệp, chọn *Copy* (Sao chép) hoặc *Cut* (Cắt), sau đó đi đến thư mục đích, nhấp chuột phải và chọn *Paste* (Dán).  
* **Đổi tên (Rename):** Nhấp chuột phải vào tệp và chọn *Rename*, hoặc chọn tệp và nhấn phím F2.  
* **Xóa tệp (Delete):** Nhấp chuột phải và chọn *Move to Trash* (Chuyển vào thùng rác), hoặc chọn tệp và nhấn phím Delete. Hãy nhớ rằng tệp trong Thùng rác vẫn chiếm dung lượng ổ cứng cho đến khi bạn nhấp chuột phải vào biểu tượng Trash và chọn *Empty Trash* (Dọn sạch thùng rác).

### **Sửa đổi Quyền hạn (Permissions) bằng Đồ họa**

Trong Chương 7, bạn đã học cách sử dụng lệnh chmod và chown để thay đổi quyền truy cập tệp. Nếu bạn không thích gõ lệnh, các trình quản lý tệp cung cấp một cách dễ dàng để thực hiện điều này thông qua giao diện đồ họa.

Chỉ cần nhấp chuột phải vào tệp hoặc thư mục, chọn **Properties** (Thuộc tính). Trong hộp thoại xuất hiện, chuyển sang tab **Permissions** (Quyền hạn). Tại đây, bạn có thể sử dụng các menu thả xuống hoặc các hộp kiểm để thiết lập xem ai (Chủ sở hữu, Nhóm, hoặc Những người khác) có quyền Đọc (Read), Ghi (Write) và Thực thi (Execute) đối với tệp đó.

**MẸO:** Để thay đổi quyền cho một tệp hệ thống, bạn vẫn có thể phải cần quyền root, do đó bạn có thể cần mở trình quản lý tệp của mình dưới quyền quản trị viên.

## **Trên Mạng (On the Network)**

Các trình quản lý tệp Linux ngày nay cực kỳ giỏi trong việc giao tiếp với các máy tính khác trên mạng của bạn. Khung bên trái (sidebar) của hầu hết các trình quản lý tệp đều có mục **Network** (Mạng).

Khi bạn nhấp vào Network, Linux sẽ quét mạng cục bộ của bạn để tìm kiếm các thiết bị đang chia sẻ tệp. Điều tuyệt vời là Linux hỗ trợ hoàn hảo giao thức SMB (Server Message Block), có nghĩa là nó có thể nhìn thấy và tương tác với các thư mục chia sẻ trên mạng Windows (Windows network shares). Các thư mục chia sẻ Windows của bạn sẽ xuất hiện dưới thư mục *Shares* hoặc trực tiếp trong mục Network. Bạn chỉ cần nhấp đúp vào chúng, nhập tên người dùng và mật khẩu mạng (nếu được yêu cầu), và bạn có thể làm việc với các tệp đó như thể chúng đang nằm ngay trên ổ cứng máy tính của bạn.

## **Tìm kiếm Mọi thứ (Finding Things)**

Hệ thống tệp có thể trở nên rất lớn và việc quên mất mình đã lưu tài liệu ở đâu là chuyện bình thường. Cả máy tính để bàn GNOME 3 và KDE Plasma đều cung cấp những cách dễ dàng để bạn tìm kiếm các tệp và thư mục trong hệ thống tệp.

Đối với máy tính để bàn KDE Plasma, tiện ích **KFind** là công cụ phù hợp.

Mở menu KDE và ở trên cùng, bạn sẽ thấy hộp văn bản tìm kiếm KFind. Nhập tên tệp bạn cần tìm và khi bạn gõ, KFind hiển thị các tệp phù hợp, như được hiển thị trong Hình 8-12. Chọn tệp phù hợp bạn cần để mở nó, bằng cách sử dụng ứng dụng mặc định.

Đúng như mong đợi, máy tính để bàn GNOME 3 cũng có tiện ích tìm kiếm tệp riêng, được gọi đơn giản là **File Searcher**. Thực ra bạn không cần phải tự khởi động File Searcher; nó sẽ tự động xuất hiện dưới dạng hộp văn bản Search trong khu vực tổng quan ứng dụng (application overview) hoặc tổng quan hoạt động (activities overview), như được hiển thị trong Hình 8-13.

Khi bạn nhập tên tệp cần tìm, File Searcher sẽ hiển thị một danh sách tất cả các tệp phù hợp ngay khi bạn gõ.

Sử dụng tính năng Tìm kiếm thường có thể cứu bạn khỏi việc phải "đào bới" từng thư mục một cách mệt mỏi\!