# **Chương 3: Cài đặt Linux**

**TRONG CHƯƠNG NÀY**

* Xem xét một số vấn đề phút chót trước khi cài đặt  
* Cài đặt Ubuntu từ LiveDVD hoặc thẻ USB  
* Cài đặt openSUSE làm máy tính để bàn cá nhân  
* Khởi động lần đầu tiên

Trong những ngày đầu của Linux, bạn gần như cần phải có bằng Khoa học Máy tính mới có thể tìm ra cách làm cho Linux hoạt động trên PC. May mắn cho chúng ta, ngày nay quá trình cài đặt đồ họa đã trở nên khá dễ dàng thực hiện và sẽ quen thuộc với những người dùng đến từ hệ điều hành đồ họa khác, chẳng hạn như Microsoft Windows. Chương này cung cấp các chi tiết bạn cần biết để thiết lập và chạy một bản phân phối Linux trên PC của mình.

Mặc dù các bản phân phối Linux khác nhau sử dụng các tập lệnh trình cài đặt khác nhau, nhưng tất cả chúng thực sự khá thông minh. Bạn có thể thấy rằng mình không thấy chính xác các màn hình giống như tôi hiển thị trong chương này, nhưng các khái niệm chung thì đều giống nhau. Nếu bạn thấy điều gì đó không quen thuộc hoặc không thấy điều mà tôi đề cập ở đây, đừng hoảng sợ. Trình cài đặt chỉ đang điều chỉnh những gì nó cung cấp dựa trên phần cứng trong hệ thống của bạn và phần mềm bạn đã chọn để cài đặt.

## **Những điều cần Cân nhắc Trước khi Bạn Bắt đầu Cài đặt**

Sau khi tải xuống hình ảnh ISO cho bản phân phối Linux cụ thể của mình, về cơ bản có ba cách để bạn có thể cài đặt Linux từ nó:

* Ghi hình ảnh ISO lên một đĩa DVD trắng, sau đó khởi động máy trạm của bạn từ đĩa DVD. (Chi tiết về cách thực hiện việc này được trình bày ở Chương 2).  
* Tạo thẻ USB có khả năng khởi động bằng tệp hình ảnh ISO và khởi động máy trạm của bạn từ thẻ USB. (Chi tiết về cách thực hiện việc này cũng được trình bày ở Chương 2).  
* Gắn tệp hình ảnh ISO như một ổ đĩa DVD ảo trong một máy ảo được tạo bằng phần mềm như VMware hoặc VirtualBox.

Phương pháp cuối cùng tôi sẽ đề cập chi tiết trong Chương 20, tập trung vào việc chạy Linux trong môi trường ảo. Chương này tập trung vào việc cài đặt Linux bằng cách khởi động máy trạm của bạn bằng đĩa DVD hoặc thẻ USB.

Để giúp bạn có cái nhìn khái quát về một số phương pháp cài đặt khác nhau, trong chương này tôi tập trung vào hai quá trình cài đặt bản phân phối Linux khác nhau \- Ubuntu từ bản phân phối Live và openSUSE từ đĩa DVD cài đặt đầy đủ. Tôi chọn hai phương pháp này vì hai lý do:

* Quá trình cài đặt Ubuntu Live và phương pháp cài đặt đầy đủ openSUSE đại diện cho hai kiểu cài đặt chính mà bạn sẽ cần thực hiện đối với hầu hết các hệ thống Linux.  
* Việc bao gồm chi tiết cài đặt của mọi bản phân phối Linux đang tồn tại sẽ biến cuốn sách này thành một bộ bách khoa toàn thư mất.

Sau khi nắm được cách cài đặt Linux bằng hai phương pháp này, bạn có thể tự tin ra ngoài và giải quyết gần như mọi bản cài đặt Linux nào.

Ngoài ra, tôi giả định rằng bạn muốn cài đặt phiên bản máy tính để bàn (desktop) của Linux chứ không phải phiên bản máy chủ (server). Có rất nhiều cuốn sách ngoài kia tập trung vào máy chủ, vì vậy mục tiêu của tôi là *Linux For Dummies* sẽ tập trung hoàn toàn vào những người muốn sử dụng Linux làm máy tính để bàn thực sự của họ. Việc bao hàm đủ sâu cả chức năng máy tính để bàn và máy chủ trong một cuốn sách có kích cỡ thế này là điều không thể.

**GHI NHỚ:** Nếu bạn đang cài đặt một phiên bản Ubuntu hoặc openSUSE khác, hoặc một bản phân phối Linux hoàn toàn khác, màn hình của bạn sẽ trông khác với những gì được hiển thị trong cuốn sách này. Quy trình cài đặt của mỗi bản phân phối Linux đều bao gồm các tác vụ cơ bản giống nhau, nhưng các hành động cụ thể có thể được trình bày theo một thứ tự khác hoặc được tùy chỉnh để trông khác trên màn hình. Ví dụ, một bản phân phối có thể đưa phần tạo tài khoản lên trước phần phân vùng đĩa, và một bản phân phối khác có thể đảo ngược hai chủ đề đó. Tuy nhiên, hầu hết các bản phân phối đều trải qua các lựa chọn cơ bản giống nhau, vì vậy việc đọc chương này vẫn sẽ hữu ích cho một thứ gì đó khác ngoài Ubuntu hoặc openSUSE.

## **Cài đặt từ Ubuntu Live**

Quá trình cài đặt Ubuntu là một trong những quá trình đơn giản nhất trong thế giới Linux. Ubuntu hướng dẫn bạn qua tất cả các bước cần thiết để thiết lập hệ thống, sau đó cài đặt toàn bộ hệ thống Ubuntu mà không cần hỏi bạn quá nhiều thông tin.

Bạn có thể bắt đầu quá trình cài đặt từ hai vị trí sau khi khởi động từ đĩa Live DVD hoặc thẻ USB:

* Trực tiếp từ menu khởi động mà không cần khởi động Ubuntu  
* Từ biểu tượng Install (Cài đặt) trên máy tính để bàn sau khi bạn khởi động hệ thống Ubuntu Live

Cả hai vị trí đều bắt đầu cùng một quá trình cài đặt, hướng dẫn bạn qua một vài bước tùy chọn.

**CẢNH BÁO:** Để bắt đầu cài đặt từ đĩa DVD hoặc thẻ USB, trước tiên bạn có thể cần thay đổi hệ thống của mình để bắt đầu, hoặc khởi động, từ ổ đĩa DVD hoặc thẻ USB — nhiều hệ thống ngày nay đã được cấu hình sẵn để làm việc này, vì vậy bạn có thể không cần phải thực hiện bất kỳ thay đổi nào. Bạn cần xem cài đặt BIOS của mình để xác định xem hệ thống của bạn có thể khởi động từ ổ DVD hay thẻ USB hay không.

Sau khi đã có đĩa Live DVD hoặc thẻ USB trong tay, bạn có thể bắt đầu quá trình cài đặt. Chỉ cần làm theo các bước sau.

1. **Đặt đĩa Ubuntu Live DVD vào khay đĩa DVD của PC (hoặc cắm thẻ USB vào cổng USB), và khởi động lại PC của bạn.**

PC của bạn sau đó sẽ khởi động từ đĩa Ubuntu Live DVD hoặc thẻ USB, và bạn sẽ thấy menu Ubuntu Live chính (như Hình 3-1).

2. **Từ menu, chọn ngôn ngữ của bạn, sau đó chọn cài đặt trực tiếp Ubuntu (Install Ubuntu), hoặc dùng thử Ubuntu trước bằng cách chạy nó từ đĩa DVD hoặc thẻ USB (Try Ubuntu).**

Tính năng tuyệt vời về các phiên bản Live là bạn có thể lái thử Ubuntu mà không cần phải can thiệp vào ổ cứng của mình. Điều này cung cấp cho bạn ý tưởng về những gì sẽ hoạt động và những gì không. Sau khi hoàn thành quá trình lái thử, nếu quyết định cài đặt Ubuntu, bạn chỉ cần nhấp vào biểu tượng **Install Ubuntu** trên máy tính để bàn (như Hình 3-2). Nếu bạn quyết định chạy quá trình cài đặt từ menu chính, hãy bỏ qua và chuyển sang Bước 4\.

3. **Chọn ngôn ngữ để sử dụng cho quá trình cài đặt, sau đó nhấp vào Continue (Tiếp tục).**

Nếu bạn cài đặt Ubuntu từ biểu tượng cài đặt trên máy tính để bàn, nó sẽ hỏi lại bạn về ngôn ngữ mặc định (như Hình 3-3). Ubuntu sử dụng ngôn ngữ này để hiển thị các tin nhắn văn bản trong quá trình cài đặt, cộng với việc đặt ngôn ngữ mặc định được sử dụng khi hệ điều hành chạy. Tuy nhiên, điều này không nhất thiết có nghĩa là tất cả các ứng dụng chạy trên hệ thống sẽ sử dụng ngôn ngữ đó. Mỗi ứng dụng riêng lẻ có thể phát hiện hoặc không phát hiện ra ngôn ngữ mặc định được cấu hình trong Ubuntu.

4. **Chọn Bàn phím (Keyboard), sau đó nhấp vào Continue (Tiếp tục).**

Bước tiếp theo trong quá trình cài đặt là xác định bàn phím bạn sẽ sử dụng với hệ thống Ubuntu. Mặc dù điều này nghe có vẻ như một tùy chọn đơn giản, nó có thể trở nên phức tạp nếu bạn có một bàn phím bao gồm các phím đặc biệt. Ubuntu nhận ra hàng trăm loại bàn phím khác nhau, và liệt kê tất cả chúng trong cửa sổ Bố cục Bàn phím (Keyboard Layout) (như Hình 3-4).

Cửa sổ Bố cục Bàn phím liệt kê các loại bàn phím khác nhau thường được sử dụng dựa trên quốc gia của bạn. Danh sách bên trái liệt kê các quốc gia và danh sách bên phải liệt kê các loại bàn phím đã biết khác nhau được sử dụng ở quốc gia đã chọn. Trước tiên, hãy chọn quốc gia của bạn từ danh sách bên trái, sau đó chọn loại bàn phím của bạn từ danh sách bên phải.

Đối với hầu hết các bàn phím tiêu chuẩn, tập lệnh cài đặt Ubuntu tự động phát hiện đúng bàn phím và bạn sẽ không phải làm gì cả. Ngoài ra còn có một nút để buộc trình cài đặt thử phát hiện lại bàn phím của bạn nếu có điều gì đó không ổn trong lần đầu tiên. Nếu bạn có một bàn phím đặc biệt, bên dưới hai danh sách là khu vực nơi bạn có thể kiểm tra lựa chọn bàn phím. Chỉ cần nhập bất kỳ ký tự đặc biệt hoặc độc đáo nào có trên bàn phím của bạn để xem liệu cài đặt bạn chọn có tạo ra các ký tự phù hợp hay không.

5. **Chọn phần mềm bạn muốn cài đặt theo mặc định trên màn hình Ubuntu của mình, sau đó nhấp vào Continue.**

Trình cài đặt Ubuntu cung cấp cho bạn một số lựa chọn về chính xác những phần mềm nào cần cài đặt (như Hình 3-5). Trình cài đặt Ubuntu cung cấp cho bạn hai tùy chọn cho các gói phần mềm cần cài đặt:

* **Cài đặt Bình thường (Normal Installation):** Bao gồm phần mềm để duyệt web, tự động hóa văn phòng (chẳng hạn như xử lý văn bản và làm việc với bảng tính), trò chơi và trình phát âm thanh/video.  
* **Cài đặt Tối thiểu (Minimal Installation):** Cung cấp một gói phần mềm máy tính để bàn tối thiểu, chỉ bao gồm phần mềm để duyệt web và các tiện ích máy tính để bàn tiêu chuẩn để kiểm soát môi trường làm việc của bạn.

Đối với hầu hết các bản cài đặt máy tính để bàn Ubuntu, hãy chọn Cài đặt Bình thường. Nếu bạn đang sử dụng một máy trạm cũ có ổ cứng nhỏ, bạn có thể phải chọn cài đặt máy tính để bàn tối thiểu và sau đó cài đặt thủ công bất kỳ gói phần mềm nào khác mà bạn cần.

**MẸO:** Nếu PC của bạn được kết nối với mạng, trình cài đặt cung cấp cho bạn tùy chọn cài đặt ngay mọi bản cập nhật có sẵn từ kho phần mềm Ubuntu nếu bạn muốn (Download updates while installing Ubuntu). Việc chọn tùy chọn này làm tăng thời gian cài đặt, nhưng nó cũng đảm bảo phần mềm máy tính để bàn Ubuntu của bạn được cập nhật khi bạn đăng nhập lần đầu tiên.

Tùy chọn cuối cùng là cài đặt phần mềm của bên thứ ba. Chủ đề này hơi gây tranh cãi trong thế giới Linux. Một số công ty phần cứng sử dụng trình điều khiển độc quyền để Linux có thể tương tác với phần cứng của họ. Các trình điều khiển này không phải là mã nguồn mở, do đó nhiều người theo chủ nghĩa thuần túy Linux không thích sử dụng chúng. Cũng có những định dạng âm thanh và video nhất định mang tính độc quyền, và như bạn có thể nghi ngờ, điều này cũng gây ra sự lo lắng cho những người theo chủ nghĩa thuần túy Linux. Tôi sẽ để lại quyết định có chọn tùy chọn này hay không cho bạn, nhưng hãy lưu ý nếu bạn chọn không cài đặt gói này, máy tính để bàn của bạn có thể không hoạt động với một số thiết bị phần cứng của bạn, hoặc không thể phát một số định dạng âm thanh và video phổ biến hơn.

6. **Chọn cách cài đặt Ubuntu trên ổ cứng của bạn, sau đó nhấp vào Install Now (Cài đặt Ngay).**

Bước này trong quá trình cài đặt rất có thể là bước quan trọng nhất và cũng phức tạp nhất. Đây là nơi bạn cần cho trình cài đặt Ubuntu biết chính xác vị trí đặt hệ điều hành Ubuntu trên hệ thống của bạn. Một động thái sai lầm ở đây có thể thực sự phá hỏng ngày của bạn.

Các tùy chọn bạn nhận được trong cửa sổ này trong quá trình cài đặt phụ thuộc vào cấu hình ổ cứng của bạn và liệu bạn có bất kỳ phần mềm hiện có nào trên ổ cứng hay không. Nếu bạn đã trải qua các bước trong Chương 2, bạn hẳn đã sẵn sàng cho bài kiểm tra này\! (Hình 3-6 hiển thị ví dụ về cửa sổ *Installation type* trông như thế nào).

Trình cài đặt Ubuntu cố gắng phát hiện chính xác thiết lập hệ thống của bạn và cung cấp một số tùy chọn đơn giản:

* Nếu toàn bộ ổ cứng của bạn hiện đang được sử dụng cho Windows, trình cài đặt Ubuntu đề nghị thu nhỏ phân vùng đó lại để nhường chỗ cho phân vùng Ubuntu và tạo một môi trường khởi động kép.  
* Nếu bạn đã tự thu nhỏ phân vùng Windows hiện có của mình theo cách thủ công (như đã thảo luận trong Chương 2), trình cài đặt Ubuntu đề nghị cài đặt Ubuntu trên phân vùng trống khả dụng và tạo môi trường khởi động kép.  
* Nếu bạn đã cài đặt một phiên bản Ubuntu trước đó, trình cài đặt Ubuntu đề nghị chỉ nâng cấp HĐH và giữ nguyên dữ liệu của bạn nếu có thể.  
* Nếu bạn có một ổ cứng thứ hai trong máy trạm của mình, trình cài đặt Ubuntu đề nghị sử dụng nó cho Ubuntu, để nguyên ổ cứng hiện có của bạn và tạo môi trường khởi động kép.  
* Nếu bạn có một ổ cứng duy nhất đã chứa một phân vùng Windows hoặc Linux hiện có, trình cài đặt Ubuntu cung cấp tùy chọn xóa toàn bộ phân vùng (Erase disk and install Ubuntu) và chỉ cài đặt Ubuntu.  
* Tùy chọn **Something else** (Thứ gì đó khác) cho phép bạn phân vùng thủ công ổ cứng của mình để tạo các phân vùng của riêng bạn.

Việc bạn chọn tùy chọn nào phụ thuộc vào việc bạn muốn thử kiểu thiết lập nào. Nếu bạn muốn chạy một máy trạm chỉ có Ubuntu, tùy chọn xóa hệ điều hành hiện tại là cách nhanh nhất và dễ dàng nhất.

**CẢNH BÁO:** Ngay cả khi bạn chọn một trong các tùy chọn để giữ lại hệ điều hành hiện tại, bạn vẫn rất nên sao lưu bất kỳ tệp quan trọng nào có trong hệ điều hành đó. Những sai sót có thể (và thường xuyên) xảy ra khi thao tác với ổ cứng.

Nếu bạn chọn tùy chọn giữ lại hệ điều hành hiện có trên ổ cứng, trình cài đặt Ubuntu cho phép bạn chọn dung lượng ổ đĩa sẽ phân bổ cho phân vùng Ubuntu mới. Bạn có thể kéo thanh phân cách phân vùng để phân phối lại không gian đĩa giữa hệ điều hành ban đầu và phân vùng Ubuntu mới. Hy vọng rằng bạn vẫn nhớ các yêu cầu về không gian đĩa mà mình đã xác định trước đó trong Chương 2 để sử dụng ở đây\!

Nếu bạn chọn quy trình phân vùng thủ công, Ubuntu sẽ trao quyền kiểm soát quy trình phân vùng cho bạn. Nó cung cấp một tiện ích phân vùng tuyệt vời (như Hình 3-7) để bạn sử dụng nhằm tạo, chỉnh sửa hoặc xóa các phân vùng ổ cứng. Tiện ích phân vùng thủ công hiển thị các ổ cứng hiện tại, cùng với bất kỳ phân vùng hiện có nào được định cấu hình trong đó. Một khi bạn trở thành người dùng Linux có kinh nghiệm, bạn có thể xóa, sửa đổi hoặc tạo từng phân vùng riêng lẻ trên bất kỳ ổ cứng nào được cài đặt trên hệ thống để tùy chỉnh thiết lập Linux của mình.

7. **Nếu bạn đang thực hiện phân vùng thủ công, hãy chọn một hệ thống tệp cho phân vùng Ubuntu của bạn.**

Một phần của quy trình phân vùng thủ công là chỉ định một hệ thống tệp cho mỗi phân vùng. Hệ thống tệp (filesystem) là phương pháp được sử dụng để lưu trữ và truy cập các tệp trên phân vùng. Không giống như một số hệ điều hành khác, Ubuntu hỗ trợ một số hệ thống tệp khác nhau. Bạn có thể chọn bất kỳ hệ thống tệp nào có sẵn cho bất kỳ phân vùng nào mà Ubuntu sẽ sử dụng. Bảng 3-1 hiển thị các loại hệ thống tệp có sẵn cho bạn khi tạo phân vùng đĩa trong Ubuntu.

**Bảng 3-1: Các loại Hệ thống Tệp Phân vùng của Ubuntu**

| Loại phân vùng | Mô tả |
| :---- | :---- |
| **ext4** | Một hệ thống tệp nhật ký (journaling) phổ biến của Linux, là phần mở rộng hiện tại của hệ thống tệp ext2 gốc của Linux. |
| **ext3** | Hệ thống tệp nhật ký cũ của Linux, là phần mở rộng của hệ thống tệp ext2 gốc của Linux. |
| **ext2** | Hệ thống tệp Linux không có tính năng ghi nhật ký ban đầu. |
| **btrfs** | Một hệ thống tệp mới hơn, hiệu suất cao hỗ trợ kích thước tệp lớn. |
| **JFS** | Hệ thống tệp có ghi nhật ký (Journaled Filesystem), do IBM tạo ra và được sử dụng trong các hệ thống AIX Unix. |
| **XFS** | Một hệ thống tệp nhật ký hiệu suất cao do Silicon Graphics tạo ra cho hệ điều hành IRIX. |
| **FAT16** | Hệ thống tệp Microsoft DOS cũ hơn. |
| **FAT32** | Hệ thống tệp Microsoft DOS mới hơn tương thích với Microsoft Windows. |
| **swap area** | Khu vực bộ nhớ ảo (vùng hoán đổi). |
| **encrypted volume** | Linux cho phép bạn mã hóa toàn bộ phân vùng \- chỉ cần đừng quên khóa mật khẩu. |
| **Do not use** | Bỏ qua phân vùng này. |

Loại phân vùng phổ biến nhất (và là mặc định được các phương pháp hướng dẫn của Ubuntu sử dụng) là định dạng **ext4**. Định dạng hệ thống tệp này cung cấp một hệ thống tệp có tính năng ghi nhật ký (journaling) cho Ubuntu. Một hệ thống tệp nhật ký sẽ ghi chép lại mọi thay đổi tệp vào một tệp nhật ký trước khi cố gắng cam kết (commit) chúng vào đĩa. Nếu hệ thống gặp sự cố trước khi có thể cam kết dữ liệu một cách thích hợp, tệp nhật ký sẽ được sử dụng để hoàn thành các cam kết tệp đang chờ xử lý và đưa đĩa trở lại trạng thái bình thường. Các hệ thống tệp nhật ký làm giảm đáng kể tình trạng hỏng tệp trong Linux.

8. **Nếu bạn đang thực hiện phân vùng thủ công, hãy chọn các điểm gắn kết (mount points) cho các phân vùng.**

Sau khi chọn hệ thống tệp cho phân vùng, mục tiếp theo mà Ubuntu muốn đối với phân vùng là nơi gắn phân vùng đó vào hệ thống tệp ảo (xem Chương 7). Hệ thống tệp ảo của Ubuntu xử lý các ổ cứng bằng cách "cắm" chúng vào các vị trí cụ thể trong hệ thống tệp ảo. Bảng 3-2 liệt kê các vị trí khả thi nơi bạn có thể gắn một phân vùng.

Nếu bạn chỉ tạo một phân vùng duy nhất cho Ubuntu, bạn phải gắn nó ở điểm gắn kết gốc (/). Nếu bạn có các phân vùng bổ sung, bạn có thể gắn chúng ở các vị trí khác trong hệ thống tệp ảo.

**Bảng 3-2: Vị trí Điểm Gắn kết (Mount Point)**

| Vị trí | Mô tả |
| :---- | :---- |
| **/** | Thư mục gốc của hệ thống tệp ảo Linux |
| **/boot** | Vị trí của nhân Linux (kernel) được sử dụng để khởi động hệ thống |
| **/home** | Các thư mục người dùng để lưu trữ các tệp cá nhân và tệp cài đặt ứng dụng cá nhân |
| **/tmp** | Các tệp tạm thời được sử dụng bởi các ứng dụng và hệ thống Linux |
| **/usr** | Vị trí chung cho các tệp ứng dụng đa người dùng |
| **/var** | Thư mục biến thiên, thường được sử dụng cho các tệp nhật ký và tệp spool |
| **/srv** | Vị trí chung cho các tệp được sử dụng bởi các dịch vụ chạy trên hệ thống |
| **/opt** | Thư mục cài đặt gói tùy chọn cho các ứng dụng của bên thứ ba |
| **/usr/local** | Một vị trí thay thế chung cho các bản cài đặt gói đa người dùng tùy chọn |

**MẸO:** Nếu bạn đang sử dụng phương pháp phân vùng thủ công, đừng quên phân bổ một phân vùng cho vùng hoán đổi (swap area), ngay cả khi bạn đã cài đặt rất nhiều bộ nhớ vật lý trên hệ thống của mình. Nhân Linux sử dụng vùng hoán đổi làm nơi lưu giữ tạm thời để di chuyển các ứng dụng đang "ngủ" ra khỏi bộ nhớ vật lý nhằm nhường chỗ cho các ứng dụng đang chạy. Quy tắc tiêu chuẩn cho việc này là tạo một vùng hoán đổi có kích thước lớn bằng với bộ nhớ vật lý mà bạn có. Do đó, nếu bạn có 8GB bộ nhớ vật lý, hãy tạo một phân vùng 8GB và gán nó làm swap area.

9. **Nếu bạn đang xóa một phân vùng hiện có hoặc tạo một phân vùng mới, hãy chọn bất kỳ tính năng đĩa nâng cao nào để sử dụng, sau đó nhấp vào OK.**

Ubuntu cung cấp tùy chọn để bạn sử dụng tính năng Trình quản lý Dung lượng Hợp lý (Logical Volume Manager \- LVM) trong Linux với các phân vùng ổ cứng của bạn. LVM cung cấp một cách để bạn dễ dàng thêm dung lượng vào một thư mục hiện có bất kỳ lúc nào nếu cần, ngay cả khi đã có dữ liệu trong thư mục đó. Bạn cũng có thể chọn mã hóa logical volume nếu cần. Tùy chọn khác là sử dụng hệ thống tệp ZFS, đây là một hệ thống tệp thương mại mới được phát hành cho thế giới mã nguồn mở.

10. **Nhấp vào Install Now (Cài đặt Ngay) để chấp nhận các thay đổi phân vùng ổ cứng được đề xuất và tiếp tục quá trình cài đặt.**

Cho đến thời điểm này, bạn vẫn có thể thay đổi ý định về các thay đổi trên ổ cứng. Tuy nhiên, sau khi bạn nhấp vào **Install Now** ở đây, bạn đã cam kết thực hiện những thay đổi đó và không thể quay lại được nữa\!

11. **Chọn vị trí của bạn, sau đó nhấp vào Continue.**

Bởi vì Ubuntu được sử dụng trên toàn thế giới, bạn sẽ cần chọn thủ công chính xác nơi bạn sống trên thế giới để Ubuntu có thể chỉ định cài đặt múi giờ và ngôn ngữ địa phương (locale) chính xác.

12. **Tạo ID Đăng nhập (Login ID), sau đó nhấp vào Continue.**

Bước tiếp theo trong quá trình cài đặt là cửa sổ Login ID (như Hình 3-8).

**GHI NHỚ:** ID đăng nhập bạn tạo trong quá trình này hơi quan trọng một chút. Không giống như các bản phân phối Linux khác, bản phân phối Ubuntu không sử dụng tài khoản đăng nhập quản trị viên (thường được gọi là root trong thế giới Unix/Linux). Thay vào đó, Ubuntu cung cấp khả năng cho các tài khoản người dùng bình thường thuộc về một nhóm quản trị viên. Các thành viên trong nhóm quản trị viên có khả năng trở thành quản trị viên tạm thời trên hệ thống (xem Chương 17). Việc có một tài khoản có đặc quyền quản trị là rất quan trọng, vì quản trị viên là tài khoản duy nhất được phép thực hiện hầu hết các chức năng của hệ thống, chẳng hạn như thay đổi các tính năng hệ thống, thêm thiết bị mới và cài đặt phần mềm mới. Nếu không có tài khoản quản trị, bạn sẽ không thể làm được nhiều điều mới mẻ trên hệ thống.

Ngoài việc xác định danh tính bản thân, bạn cũng cần gán tên cho chính máy tính đó. Ubuntu sử dụng tên này khi quảng bá sự hiện diện của nó trên mạng, cũng như khi tham chiếu hệ thống trong các tệp nhật ký. Bạn nên chọn một tên máy tính duy nhất trên mạng của mình, dài dưới 63 ký tự và không chứa bất kỳ ký tự đặc biệt nào (mặc dù dấu gạch nối được cho phép).

Một cài đặt cuối cùng \- bạn phải xác định xem bạn muốn hệ thống tự động đăng nhập bạn vào máy tính để bàn (Log in automatically) hay yêu cầu mật khẩu đăng nhập (Require my password to log in). Tôi không khuyên bạn nên sử dụng tính năng tự động đăng nhập trên máy tính xách tay mà bạn có thể vô tình để quên ở đâu đó. Nếu bạn là người duy nhất sử dụng PC để bàn (và không có ai tọc mạch xung quanh), bạn có thể sử dụng tính năng đăng nhập tự động để tiết kiệm chút thời gian. Nếu không, hãy đặt nó ở chế độ nhắc bạn nhập mật khẩu mỗi khi bạn đăng nhập vào hệ thống của mình.

13. **Hãy ngồi lại và thưởng thức chương trình\!**

Khi quá trình cài đặt diễn ra, trình cài đặt sẽ trình bày một loạt các slide thông tin. Hãy xem lướt qua các trang trình bày này để tìm hiểu về các tính năng có sẵn trong hệ thống Ubuntu mới của bạn. Tôi sẽ đề cập sâu hơn về từng tính năng này trong các chương sắp tới.

Sau khi hệ thống Ubuntu được cài đặt trên ổ cứng, chương trình cài đặt sẽ nhắc bạn khởi động lại. Lần tiếp theo hệ thống của bạn khởi động, bạn sẽ ở trong vùng đất Ubuntu\!

### **Lần Khởi động Ubuntu Đầu tiên của Bạn**

Sau khi khởi động lại Ubuntu, nó sẽ tự động đăng nhập và đưa bạn thẳng đến màn hình của mình, hoặc bạn sẽ được chào đón bằng cửa sổ đăng nhập, tùy thuộc vào cài đặt bạn đã chọn trong quá trình cài đặt. Nếu bạn được chào đón bởi cửa sổ đăng nhập, hãy nhấp vào tài khoản người dùng của bạn, sau đó nhập mật khẩu của bạn vào hộp văn bản mật khẩu (bạn vẫn nhớ những gì mình đã đặt chứ, phải không?).

Lần đầu tiên bạn truy cập vào màn hình người dùng của mình, Ubuntu sẽ hỏi một số câu hỏi về dọn dẹp nội vụ. Làm theo các bước sau để tiến tới màn hình nền của bạn:

1. **Nếu bạn có tài khoản mạng từ Ubuntu, Google, Nextcloud hoặc Microsoft, hãy chọn biểu tượng thích hợp từ menu.** Nếu bạn không có tài khoản mạng hoặc chọn không sử dụng tài khoản đó, hãy nhấp vào **Skip** (Bỏ qua).

Ubuntu có thể đồng bộ hóa nhiều tính năng tài khoản mạng của bạn, chẳng hạn như lịch trên máy tính để bàn, cùng với bất kỳ tệp nào bạn đã lưu trữ trong các tài khoản đám mây chung từ bất kỳ nhà cung cấp nào được liệt kê. Chỉ cần chọn loại tài khoản bạn có từ menu hiển thị trong Hình 3-9, sau đó nhập thông tin đăng nhập của bạn và chọn các mục bạn muốn đồng bộ hóa.

2. **Chọn xem bạn có muốn sử dụng tính năng Ubuntu Livepatch hay không.** Để sử dụng nó, nhấp vào **Setup Livepatch**. Nếu bạn chọn không sử dụng nó, hãy nhấp vào **Next** (Tiếp theo).

Tính năng Ubuntu Livepatch cho phép bạn liên kết nhiều máy tính với mạng đám mây Canonical. Canonical là tập đoàn tài trợ cho Ubuntu và cung cấp một số tính năng nâng cao, một số tính năng miễn phí và một số tính năng dưới dạng dịch vụ đăng ký. Bạn có thể liên kết tối đa ba máy trạm miễn phí hoặc trả tiền để trở thành thành viên Advantage để liên kết nhiều máy hơn. Nếu bạn tham gia vào tính năng Livepatch, Ubuntu sẽ tự động cài đặt tất cả các bản cập nhật trên hệ thống của bạn mà bạn không cần phải làm gì cả\!

3. **Chọn có gửi cho Ubuntu báo cáo về trải nghiệm cài đặt của bạn hay không.** Sau khi bạn đã đưa ra lựa chọn của mình, hãy nhấp vào **Next**.

Các nhà phát triển Ubuntu sử dụng thông tin này để xác định phần cứng nào được hoặc không được phát hiện chính xác trên hệ thống của bạn trong quá trình cài đặt, cũng như những phần mềm bổ sung nào bạn đã cài đặt sau khi cài đặt. Thông tin này giúp các nhà phát triển xác định những gì cần đưa vào hoặc loại bỏ trong các phiên bản tương lai.

4. **Chọn có bật dịch vụ định vị (location services) hay không, sau đó nhấp vào Next.**

Dịch vụ định vị cho phép các ứng dụng tự động xác định vị trí của bạn mà không cần phải nhắc bạn.

5. **Lướt nhanh qua các phần mềm bổ sung có sẵn để cài đặt trong cửa sổ Ready to Go, sau đó nhấp vào Done (Hoàn tất).**

Đây chỉ là một phần nhỏ trong số các phần mềm có sẵn để bạn cài đặt. Các kho phần mềm Ubuntu chứa hàng trăm ứng dụng mã nguồn mở sẵn sàng để bạn cài đặt và sử dụng\! Tôi sẽ trình bày quy trình cài đặt phần mềm trong Chương 15\.

Chúc mừng \- bạn đã vượt qua tất cả các lời nhắc cài đặt và sau cài đặt\! Lúc này đầu bạn có lẽ hơi quay cuồng, vì vậy hãy dành chút thời gian để xốc lại tinh thần, sau đó tiếp tục đọc cuốn sách để tìm hiểu thêm về hệ thống Linux của bạn.

## **Cài đặt openSUSE**

Khi bạn cài đặt từ một bản phân phối Linux cốt lõi (core distribution) đầy đủ, bạn sẽ phải đối mặt với khá nhiều điều bất ngờ. Nếu bạn để ý từ quá trình cài đặt Ubuntu Live, một điều còn thiếu là *sự lựa chọn*. Ngoài việc cấu hình các phân vùng ổ đĩa cứng của bạn, Ubuntu Live không cung cấp cho bạn nhiều quyền kiểm soát đối với những gì được cài đặt trên hệ thống của mình.

Cuộc sống sẽ hơi khác một chút khi làm việc với một bản phân phối Linux cốt lõi, chẳng hạn như openSUSE. Bạn có nhiều lựa chọn hơn để kiểm soát chính xác phần mềm nào mà quá trình cài đặt sẽ cài đặt, cũng như cách tập lệnh cài đặt cấu hình mọi thứ.

Phần này hướng dẫn quá trình cài đặt từ đĩa DVD cài đặt đầy đủ openSUSE. Bản phân phối openSUSE cũng hỗ trợ phiên bản cài đặt Live, nhưng nếu bạn muốn có các lựa chọn, thì bản cài đặt đầy đủ mới là cách tối ưu\! Chỉ cần làm theo các bước sau để mọi thứ được cài đặt:

1. **Tải xuống tệp hình ảnh ISO cài đặt đầy đủ openSUSE Leap từ www.opensuse.org.**

Tại thời điểm viết bài này, bản phân phối openSUSE hiện hỗ trợ hai phiên bản phân phối:

* **Tumbleweed:** Là bản phát hành cuốn chiếu (rolling release) chứa các phiên bản phần mềm mới nhất. Nó chủ yếu dành cho người dùng thành thạo (power user) và nhà phát triển phần mềm.  
* **Leap:** Là phiên bản phát hành thông thường ổn định được thiết kế cho người dùng Linux bình thường như chúng ta.  
2. **Ghi tệp hình ảnh ISO openSUSE Leap lên một đĩa DVD trắng, hoặc sử dụng một chương trình như Rufus để tạo thẻ USB có khả năng khởi động.**  
   (Các quy trình này được mô tả chi tiết trong Chương 2).  
3. **Khởi động máy trạm của bạn bằng đĩa DVD hoặc thẻ USB có thể khởi động. Nhấp vào Installation để bắt đầu quá trình cài đặt.**

Khi openSUSE khởi động, bạn được chào đón bằng một menu (như Hình 3-10). Menu khởi động cung cấp rất nhiều tùy chọn, bao gồm việc cho phép bạn khởi động từ ổ cứng trong máy trạm của mình trong trường hợp khẩn cấp, hoặc chỉ để nâng cấp bản cài đặt openSUSE hiện có. Bạn muốn thực hiện cài đặt mới, vì vậy hãy chọn tùy chọn menu **Installation**.

4. **Chọn ngôn ngữ và bàn phím của bạn, sau đó nhấp vào Next để đồng ý với giấy phép (license).**

Như một phần của bước đầu tiên này, quá trình cài đặt openSUSE sẽ tự động phát hiện cài đặt mạng của bạn. Nếu có vấn đề, nó có thể hỏi bạn các cài đặt mạng cụ thể cho môi trường của bạn. Nếu nó có thể tự động phát hiện mạng của bạn, nó sẽ hiển thị một cửa sổ để bạn chọn ngôn ngữ và bàn phím mặc định (như Hình 3-11). Giống như Ubuntu, tập lệnh cài đặt openSUSE sẽ cố gắng phát hiện bàn phím của bạn, nhưng nếu bạn đang sử dụng một bàn phím lạ (chẳng hạn như bố cục Dvorak), bạn có thể cần phải chọn thủ công từ danh sách.

5. **Chọn xem có sử dụng các kho phần mềm trực tuyến (online repositories) của openSUSE hay không. Nhấp vào Yes nếu PC của bạn có kết nối Internet để bạn có thể theo kịp các thay đổi phần mềm và cài đặt phần mềm mới.**

Hầu hết các bản phân phối Linux duy trì phần mềm trong các kho lưu trữ trực tuyến để giúp bạn nâng cấp các gói phần mềm và cài đặt phần mềm mới dễ dàng hơn (xem Chương 15). Cài đặt openSUSE cho phép bạn chọn có sử dụng các kho phần mềm trực tuyến hay không. Khi bạn chọn **Yes**, một cửa sổ khác xuất hiện hiển thị các tùy chọn kho lưu trữ khác nhau (như Hình 3-12).

6. **Chọn Next trong cửa sổ List of Online Repositories.**

Theo mặc định, trình cài đặt chọn các kho phần mềm tiêu chuẩn để tìm các bản cập nhật, bản vá bảo mật và cả các gói phần mềm nguồn mở và không phải nguồn mở. Nếu cần, bạn có thể chọn thêm các kho lưu trữ để gỡ lỗi phần mềm và tải xuống mã nguồn cho các ứng dụng. Những thứ này không cần thiết đối với người dùng Linux bình thường, nhưng có sẵn cho các nhà phát triển phần mềm.

7. **Chọn Desktop with KDE Plasma từ cửa sổ System Role (Vai trò Hệ thống) để cài đặt môi trường máy tính để bàn openSUSE mặc định, sau đó nhấp vào Next.**

Đây là trải nghiệm đầu tiên của bạn về cài đặt đầy đủ là như thế nào. Lưu ý từ danh sách hiển thị trong Hình 3-13 rằng cài đặt openSUSE cung cấp cho bạn tùy chọn không chỉ cài đặt môi trường máy tính để bàn hoặc máy chủ, mà còn tùy chỉnh loại hình. Tôi sẽ xem xét sự khác biệt giữa màn hình nền GNOME và KDE Plasma trong Chương 4 và 5\. Hiện tại, hãy chọn tùy chọn **KDE Plasma**. Nếu sau khi đọc Chương 4 bạn nghĩ mình sẽ thích màn hình nền GNOME hơn, bạn có thể thêm nó vào sau.

8. **Chọn tùy chọn phân vùng bạn muốn trong cửa sổ Suggested Partitioning (Phân vùng được Đề xuất).**

Tương tự như trình cài đặt Ubuntu, trình cài đặt openSUSE cố gắng phát hiện thiết lập phân vùng cụ thể của bạn (như Hình 3-14). Nếu bạn không thích lược đồ phân vùng do trình cài đặt openSUSE đề xuất, có hai phương pháp thủ công có sẵn:

* Tùy chọn **Guided Setup** (Thiết lập có Hướng dẫn) bắt đầu với bố cục phân vùng do trình cài đặt đề xuất và cho phép bạn thực hiện các tinh chỉnh.  
* Tùy chọn **Expert Partitioner** (Trình Phân vùng dành cho Chuyên gia) cho phép bạn kiểm soát hoàn toàn cách các ổ đĩa cứng trên hệ thống của bạn được Linux phân vùng và sử dụng.  
9. **Nếu bạn muốn kiểm soát hoàn toàn để tùy chỉnh bố cục phân vùng của mình, hãy nhấp vào Expert Partitioner.**

Cửa sổ Expert Partitioner (như Hình 3-15) cung cấp giao diện đồ họa để bạn thêm, thay đổi và tạo các phân vùng đĩa. Tương tự như công cụ Ubuntu, bạn phải chọn loại hệ thống tệp, cùng với vị trí gắn kết cho từng phân vùng bạn tạo.

Một công cụ bổ sung mà Expert Partitioner cung cấp là biểu diễn đồ họa về chính xác cách các phân vùng được định dạng và gắn kết. Chỉ cần nhấp vào **Device Graphs** trong khung System View để xem bố cục (như Hình 3-16). Công cụ này cung cấp cho bạn một cái nhìn bao quát về chính xác cách các phân vùng đĩa được sử dụng trong lược đồ phân vùng được đề xuất. Đây là một công cụ tuyệt vời để giúp bạn tổ chức bố cục ổ đĩa\!

10. **Nhấp vào Accept để chấp nhận lược đồ phân vùng cuối cùng.**  
11. **Chọn cài đặt đồng hồ phần cứng và múi giờ của bạn, sau đó nhấp vào Next.**

Cửa sổ Clock and Time Zone (Đồng hồ và Múi giờ) (như Hình 3-17) cho phép bạn không chỉ chọn múi giờ của mình mà còn cả các tính năng đồng hồ nâng cao, chẳng hạn như liệu máy trạm của bạn có thiết lập thời gian BIOS bằng giờ UTC thay vì giờ địa phương hay không. Nếu mạng của bạn sử dụng máy chủ thời gian mạng riêng, hãy nhấp vào **Other Settings** và bạn có thể định cấu hình openSUSE để sử dụng nó thay vì mặc định.

12. **Tạo một ID đăng nhập (Login ID), sau đó nhấp vào Next.**

Bước tiếp theo trong quá trình cài đặt là cửa sổ Login ID (như Hình 3-18). ID Đăng nhập bạn tạo trong quy trình này nhận dạng bạn trên hệ thống. Bản phân phối openSUSE sử dụng một tài khoản người dùng riêng biệt có tên là root cho mục đích quản trị. Bên cạnh việc tạo tài khoản người dùng của bạn, còn có một hộp kiểm để đặt mật khẩu tài khoản quản trị viên giống với tài khoản người dùng của bạn (Use this password for system administrator). Nếu bạn bỏ dấu kiểm, bạn sẽ được nhắc đặt một mật khẩu quản trị viên riêng biệt. Điều đó có thể hữu ích nếu bạn đang dùng chung hệ thống với những người khác cũng có thể cần quyền truy cập root để cài đặt các gói phần mềm.

**MẸO:** Một cài đặt cuối cùng \- bạn phải xác định xem bạn muốn hệ thống tự động đăng nhập vào màn hình của mình (Automatic Login) hay nhắc nhập mật khẩu đăng nhập. Nếu tình cờ bạn đang nâng cấp từ phiên bản openSUSE trước đó, bạn có thể chọn nhập (import) cài đặt người dùng của mình từ bản cài đặt trước đó. Mặc dù điều này không hoàn hảo 100%, nhưng nó có thể giúp ích phần nào trong việc di chuyển tài khoản của bạn.

13. **Chọn Install để bắt đầu quá trình cài đặt.**

Cửa sổ Installation Settings (Cài đặt Cài đặt) (như Hình 3-19) tóm tắt tất cả các lựa chọn của bạn. Đây là một điểm nữa mà việc sử dụng bản cài đặt đầy đủ tỏa sáng. Bạn có thể nhấp vào bất kỳ danh mục nào và thực hiện mọi thay đổi cần thiết trước khi bắt đầu cài đặt thực tế.

Ví dụ: nếu bạn nhấp vào tiêu đề **Software**, bạn sẽ thấy cửa sổ *Software Selection and System Tasks* (Lựa chọn Phần mềm và Các Tác vụ Hệ thống). Trong cửa sổ này, bạn có thể đặt chính xác gói phần mềm nào được cài đặt (hoặc không được cài đặt) trên thiết lập máy trạm của bạn. Bạn cũng có thể thực hiện các thay đổi đối với bộ tải khởi động (boot loader), cài đặt mạng và thậm chí cả việc hệ thống bắt đầu ở chế độ đồ họa (graphical) hay chế độ văn bản (text mode). Đó chính là sức mạnh\!

Sau khi trình cài đặt hoàn thành công việc của nó, bạn đã sẵn sàng \- bạn sẽ có một máy trạm openSUSE đầy đủ chức năng\! Giờ đây, bạn đã sẵn sàng chuyển sang tập hợp các chương tiếp theo, đi sâu vào việc thảo luận về các tính năng máy tính để bàn khác nhau trong Linux để bạn có thể bắt đầu làm việc theo cách của mình xung quanh môi trường desktop.