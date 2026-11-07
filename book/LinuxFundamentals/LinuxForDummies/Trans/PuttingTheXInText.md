# **Chương 11: Làm việc với Văn bản (Putting the X in Text)**

**TRONG CHƯƠNG NÀY**

* Xem nội dung của các tệp văn bản  
* Thao tác với các tệp văn bản trong nano  
* Làm việc với các tệp văn bản trong gedit  
* Khám phá trình soạn thảo Kate

Từ các trình soạn thảo văn bản (text editors) đến các trình xử lý văn bản (word processors), Linux cung cấp rất nhiều lựa chọn để làm việc với câu chữ. Ngày nay, với việc các gói phần mềm cố gắng tích hợp nhiều tính năng, thật khó để phân biệt sự khác nhau giữa một trình soạn thảo văn bản và một trình xử lý văn bản. Khi nói đến *trình soạn thảo văn bản*, tôi đang đề cập đến một công cụ chủ yếu được các lập trình viên sử dụng để tạo ra các tệp văn bản thuần túy (plain text) không có định dạng. Mặc dù các trình xử lý văn bản cũng có thể làm được điều đó, nhưng trọng tâm chính của chúng là tạo ra các tài liệu đẹp mắt, định dạng văn bản bằng các phông chữ và kiểu dáng khác nhau.

Trong chương này, tôi sẽ xem xét các cách khác nhau để làm việc với các tệp văn bản thuần túy, sử dụng một số trình soạn thảo văn bản đơn giản trong cả môi trường không có giao diện đồ họa (dòng lệnh) và môi trường đồ họa (GUI). Trong Chương 12, tôi sẽ xem xét các bộ ứng dụng văn phòng (office suites) dành cho những ai thích làm công việc xử lý văn bản chuyên nghiệp hơn.

## **Xem Nội dung của một Tệp Văn bản**

Hầu như tất cả các tệp cấu hình trong Linux đều là tệp văn bản. Ngoài ra, nhiều chương trình giả (được gọi là các kịch bản shell \- shell scripts), tất cả các tài liệu HTML và nhiều mục khác trong hệ thống của bạn đều là tệp văn bản. May mắn thay, nếu bạn chỉ muốn xem những gì có bên trong một tệp văn bản và không muốn chỉnh sửa nội dung của nó, bạn không cần phải mở một trình soạn thảo hay trình xử lý văn bản.

Bạn có thể sử dụng ba lệnh trên dòng lệnh để xem các tệp văn bản: cat, less, và more. Tôi cá là bạn sẽ dần yêu thích chúng cho xem.

Vâng, lệnh đầu tiên thực sự được gọi là cat. Nó là viết tắt của từ *concatenate* (nối), nhưng bạn thường sử dụng nó để hiển thị toàn bộ tệp văn bản ra màn hình. Lệnh cat rất tuyệt vời cho các tệp ngắn, nhưng với các tệp dài, văn bản sẽ trôi tuột qua màn hình nhanh hơn mức bạn có thể đọc.

Cú pháp rất đơn giản:

$ cat ten\_tep.txt

Nếu tệp quá dài, bạn sẽ muốn sử dụng một trình phân trang (pager). Trình phân trang sẽ tạm dừng văn bản khi màn hình đã đầy. Lệnh more là trình phân trang nguyên bản của UNIX. Khi màn hình đầy, lệnh more sẽ dừng lại và hiển thị chữ \--More-- ở dưới cùng. Nhấn phím Space (Dấu cách) để xem trang tiếp theo, hoặc nhấn phím q để thoát.

$ more ten\_tep.txt

Lệnh less là một phiên bản cải tiến của more (đúng vậy, trong thế giới Linux, *less* is *more* \- ít hơn tức là nhiều hơn\!). Lệnh less không chỉ cho phép bạn cuộn xuống bằng phím Space mà còn cho phép bạn sử dụng các phím mũi tên Lên/Xuống và phím Page Up/Page Down để cuộn ngược lại hoặc tiến tới trong tài liệu. Để thoát khỏi less, bạn cũng chỉ cần nhấn phím q.

$ less ten\_tep.txt

## **Thao tác với Tệp Văn bản trong nano**

Nếu bạn đang làm việc trên giao diện dòng lệnh (Terminal) và cần thực hiện một thay đổi nhỏ đối với tệp văn bản (chẳng hạn như tệp cấu hình hệ thống), việc mở một trình soạn thảo đồ họa cồng kềnh có thể hơi mất thời gian. Đây là lúc nano tỏa sáng.

Trình soạn thảo nano là một trình soạn thảo văn bản dựa trên dòng lệnh (CLI), cực kỳ nhẹ và dễ sử dụng đối với người mới bắt đầu. Không giống như các trình soạn thảo dòng lệnh "khét tiếng" khác (như vi hay vim), nano không yêu cầu bạn phải ghi nhớ các chế độ lệnh phức tạp.

Để bắt đầu chỉnh sửa một tệp bằng nano, hãy nhập lệnh sau tại dấu nhắc lệnh:

$ nano ten\_tep.txt

Nếu tệp đã tồn tại, nano sẽ mở nó. Nếu tệp chưa tồn tại, nano sẽ tạo một tệp trống mới với tên đó.

### **Giao diện của nano**

Khi nano mở ra, bạn sẽ thấy giao diện được chia làm ba phần:

* **Thanh tiêu đề ở trên cùng:** Hiển thị phiên bản của nano và tên tệp bạn đang chỉnh sửa.  
* **Khu vực soạn thảo ở giữa:** Nơi bạn thực sự gõ và chỉnh sửa văn bản của mình.  
* **Menu phím tắt ở dưới cùng:** Hiển thị các lệnh phổ biến nhất.

**MẸO NHỚ:** Ký hiệu dấu mũ (^) trong menu dưới cùng đại diện cho phím **Ctrl** trên bàn phím của bạn. Ví dụ: ^O có nghĩa là bạn cần nhấn và giữ phím Ctrl rồi gõ chữ O.

### **Các lệnh nano cơ bản**

Dưới đây là một số phím tắt cơ bản bạn sẽ sử dụng nhiều nhất trong nano:

* **Ctrl+O (Write Out):** Lưu tệp. nano sẽ hỏi bạn xác nhận tên tệp, chỉ cần nhấn Enter để lưu.  
* **Ctrl+X (Exit):** Thoát khỏi nano. Nếu bạn có những thay đổi chưa lưu, nano sẽ hỏi bạn có muốn lưu chúng trước khi thoát hay không (Nhấn Y cho Có, N cho Không).  
* **Ctrl+K (Cut Text):** Cắt (xóa) toàn bộ dòng văn bản hiện tại và lưu nó vào bộ nhớ tạm.  
* **Ctrl+U (Uncut Text):** Dán dòng văn bản bạn vừa cắt vào vị trí hiện tại của con trỏ.  
* **Ctrl+W (Where Is):** Tìm kiếm một từ hoặc cụm từ trong tài liệu.

Thật đơn giản phải không? nano là vị cứu tinh của bạn khi hệ thống đồ họa gặp sự cố và bạn chỉ có thể làm việc qua dòng lệnh đen trắng\!

## **Làm việc với Tệp Văn bản trong gedit**

Nếu bạn đang sử dụng môi trường máy tính để bàn đồ họa GNOME (như trên Ubuntu), trình soạn thảo văn bản mặc định của bạn là gedit. Nó cung cấp một giao diện đồ họa thân thiện, tương tự như Notepad trên Windows nhưng mạnh mẽ hơn rất nhiều.

Bạn có thể khởi chạy gedit bằng cách tìm kiếm "Text Editor" (Trình soạn thảo Văn bản) trong menu Activities, hoặc bằng cách gõ gedit vào cửa sổ Terminal.

### **Các tính năng của gedit**

Mặc dù trông có vẻ đơn giản, gedit chứa đựng rất nhiều tính năng mà các lập trình viên yêu thích:

* **Duyệt theo tab:** Bạn có thể mở nhiều tệp văn bản cùng lúc trong các tab khác nhau trên cùng một cửa sổ.  
* **Đánh dấu cú pháp (Syntax highlighting):** Nếu bạn đang mở một tệp mã nguồn (như kịch bản shell, mã HTML, hoặc Python), gedit sẽ tự động nhận diện ngôn ngữ và tô màu các từ khóa, giúp mã dễ đọc hơn rất nhiều.  
* **Đánh số dòng (Line numbering):** Bạn có thể bật tính năng này trong phần Preferences (Tùy chọn) để dễ dàng theo dõi các dòng mã dài.

### **Tùy chỉnh gedit**

Bạn có thể điều chỉnh gedit để phù hợp với quy trình làm việc của mình bằng cách đi tới menu **Preferences** (Tùy chọn).

Hộp thoại Preferences cung cấp một vài tab:

* **View (Xem):** Bật hiển thị số dòng, ngắt dòng (text wrapping) hoặc làm nổi bật dòng hiện tại.  
* **Editor (Trình soạn thảo):** Thiết lập kích thước tab (tab width) và tự động lưu.  
* **Fonts & Colors (Phông chữ & Màu sắc):** Thay đổi phông chữ và chọn các chủ đề màu sắc khác nhau (chủ đề tối hoặc sáng).  
* **Plugins (Tiện ích mở rộng):** Bật các tính năng bổ sung như kiểm tra chính tả (spell checker) hoặc bảng điều khiển thống kê tài liệu.

## **Khám phá trình soạn thảo Kate**

Đối với những người dùng môi trường máy tính để bàn KDE Plasma (như Kubuntu hoặc openSUSE), **Kate** (KDE Advanced Text Editor) là trình soạn thảo văn bản mặc định. Kate là một con quái vật thực sự khi nói đến các tính năng chỉnh sửa văn bản.

Giống như gedit, Kate hỗ trợ mở nhiều tệp cùng lúc, nhưng thay vì chỉ dùng tab, nó cung cấp một thanh bên (sidebar) mạnh mẽ để bạn quản lý tất cả các tài liệu, thư mục và các phiên làm việc (sessions) đang mở.

### **Cấu hình Kate**

Kate có khả năng tùy biến cực cao. Hộp thoại **Configure Kate** (Cấu hình Kate) cho phép bạn thay đổi mọi thứ, từ hành vi của các phiên làm việc, danh sách tài liệu, cho đến giao diện của trình soạn thảo. Kate cũng hỗ trợ các ứng dụng tiện ích bổ sung (plugins) bên ngoài, có thể được kích hoạt tại đây.

### **Tích hợp Terminal (Built-in Terminal)**

Một trong những plugin tuyệt vời nhất (và là mục yêu thích của tôi) đối với trình soạn thảo Kate là cửa sổ dòng lệnh (terminal) tích hợp.

Nút Terminal ở dưới cùng của cửa sổ soạn thảo văn bản sẽ khởi động trình giả lập dòng lệnh được tích hợp ngay bên trong Kate (sử dụng trình giả lập dòng lệnh Konsole của KDE). Tính năng này sẽ chia đôi cửa sổ chỉnh sửa hiện tại theo chiều ngang, tạo ra một không gian mới với Konsole đang chạy trong đó.

Giờ đây, bạn có thể nhập các lệnh trên dòng lệnh, bắt đầu các chương trình, hoặc kiểm tra các cài đặt hệ thống mà không cần phải rời khỏi trình soạn thảo\! Khi bạn muốn đóng cửa sổ terminal này, chỉ cần gõ lệnh exit tại dấu nhắc lệnh và nhấn Enter.