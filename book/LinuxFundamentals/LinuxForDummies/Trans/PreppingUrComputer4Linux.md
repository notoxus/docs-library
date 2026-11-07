# **Chương 2: Chuẩn bị Máy tính của bạn cho Linux**

**TRONG CHƯƠNG NÀY**

* Thực hiện các bước cơ bản trước khi cài đặt  
* Sử dụng chung Linux và Windows trên cùng một máy tính  
* Tùy chỉnh các phân vùng ổ đĩa trước khi cài đặt  
* Biết (và tìm kiếm) thông tin phần cứng của bạn  
* Chuẩn bị phương tiện để cài đặt

Có rất nhiều cách khác nhau để thiết lập và chạy một máy trạm Linux. Với sự phổ biến ngày càng tăng của Linux, một số công ty bán laptop đã cài đặt sẵn Linux trên đó. Nếu bạn đã mua một trong những chiếc máy như vậy, bạn có thể bỏ qua và chuyển thẳng đến Chương 4 để hòa mình vào thế giới Linux. Nếu bạn có một chiếc máy tính dự phòng chỉ định dùng để chạy Linux và không có gì khác, bạn thật may mắn\! Bạn có thể bỏ qua phần "Chuẩn bị sử dụng chung Linux và Microsoft Windows". Thực tế, nếu cảm thấy dũng cảm, bạn có thể muốn bỏ qua và tiến thẳng đến Chương 3 để bắt đầu cài đặt. Ngoài ra cũng có thông tin khắc phục sự cố ở Chương 22\.

Tất nhiên, nhiều người không có sự xa xỉ để sở hữu nhiều hơn một máy tính chỉ dành riêng cho Linux. Để cài đặt Linux vĩnh viễn trên một PC hiện có, bạn cần phải thiết lập một không gian ổ cứng cho nó. Có ba giải pháp phổ biến cho việc này:

* Thay thế hoàn toàn hệ điều hành hiện tại trên ổ cứng  
* Cài đặt Linux trên một ổ cứng thứ hai  
* Phân vùng lại một ổ cứng hiện có để chứa thêm Linux

**SAO LƯU WINDOWS**

Thuật ngữ sao lưu (back up) có ý nghĩa khác nhau đối với từng người. Một bản *sao lưu toàn bộ* sẽ sao chép tất cả hệ điều hành, chương trình và tệp dữ liệu trên hệ thống. Việc này thường đòi hỏi phần mềm chuyên dụng có thể sao chép tất cả các tệp ngay khi PC của bạn đang chạy. Một bản *sao lưu dữ liệu* chỉ sao chép các tệp cá nhân riêng lẻ mà bạn đã tạo. Bạn thường có thể tự làm điều đó bằng cách chỉ sao chép các tệp thường nằm trong thư mục Documents, Music, Pictures và Videos sang một thiết bị bên ngoài như đĩa DVD hoặc ổ USB. Rất có khả năng đối với quá trình chuyển đổi sang Linux, bạn chỉ cần thực hiện sao lưu dữ liệu. Ngày nay, hầu hết các PC hiện đại đều bao gồm một phân vùng riêng chứa các tệp hệ điều hành Windows để bạn có thể dễ dàng tự khôi phục lại hệ điều hành. Tất cả những gì bạn cần quan tâm là đảm bảo các tệp cá nhân của mình được an toàn.

**CẢNH BÁO:** Giải pháp đầu tiên là cách dễ nhất để cài đặt Linux lên PC. Hầu hết các bản cài đặt Linux thậm chí còn bao gồm một quy trình tự động hướng dẫn bạn chuyển đổi toàn bộ PC sang Linux. Tuy nhiên, đây là cách tiếp cận "được ăn cả ngã về không" — bạn sẽ thay thế hoàn toàn hệ điều hành hiện tại của mình bằng Linux\!

Nếu bạn thực sự thay thế hệ điều hành hiện tại, hãy lưu ý rằng khi hoàn tất, bạn sẽ không còn các tệp dữ liệu gốc của mình nữa\! Nếu bạn muốn giữ lại bất kỳ tệp nào từ PC Windows, bạn cần phải tự sao lưu chúng sang một phương tiện lưu trữ mà bạn có thể đọc được từ Linux. Xem phần chú ý "Sao lưu Windows" để biết thêm chi tiết về quá trình đó.

Hai phương pháp còn lại yêu cầu kịch bản khởi động kép (dual boot). Trong kịch bản khởi động kép, cả Linux và Microsoft Windows đều nằm trên các ổ cứng trong cùng một máy tính. Khi bạn khởi động máy tính, một menu sẽ xuất hiện, hỏi bạn muốn sử dụng hệ điều hành nào. Điều này cho phép bạn giữ lại các ứng dụng và tệp Windows ban đầu của mình, đồng thời sử dụng thêm Linux — tất cả trên cùng một máy tính\!

Nếu đang sử dụng máy tính để bàn, bạn có thể lắp thêm một ổ cứng thứ hai mới tinh để cài đặt Linux lên đó. Cho đến nay, đây là giải pháp dễ dàng nhất cho hệ thống khởi động kép và nên được sử dụng nếu có thể. Thật không may, hầu hết các laptop không có khả năng lắp thêm ổ cứng thứ hai, vì vậy bạn sẽ phải dùng đến cách phân vùng lại ổ cứng hiện tại như được giải thích trong phần tiếp theo.

Nếu bạn lắp thêm ổ cứng thứ hai, chỉ cần ghi chú lại xem máy tính nhận diện ổ đĩa nào là ổ đĩa nào: Bạn muốn đảm bảo rằng mình không đụng chạm gì đến bản cài đặt Microsoft Windows. Tất cả những gì bạn cần biết là ổ đĩa nào (Windows hay Linux) là ổ thứ nhất và ổ thứ hai theo cách máy tính hiểu. Khi bạn đã chắc chắn mình biết ổ đĩa nào là ổ đĩa nào, hãy chuyển sang phần "Kiểm tra lại khả năng tương thích của phần cứng" ở phần sau của chương này.

**CẢNH BÁO:** Việc biết ổ cứng nào chứa bản cài đặt Windows gốc của bạn là cực kỳ quan trọng. Khi đến lúc tải Linux, bạn không muốn vô tình cài đặt đè nó lên ổ đĩa Windows ban đầu\! Đây là một lý do khác giải thích tại sao việc sao lưu bất kỳ tệp quan trọng nào trước khi bắt đầu quá trình này lại quan trọng đến vậy. Tai nạn có thể (và thường xuyên) xảy ra\!

Những người không thể dành trọn một ổ cứng cho Linux và đã cài đặt sẵn Microsoft Windows sẽ phải thu nhỏ bản cài đặt Windows hiện tại của họ lại và tạo một phân vùng thứ hai trên ổ cứng. Phân vùng cho phép một ổ cứng duy nhất có các phần logic riêng biệt mà máy tính coi như các ổ cứng độc lập. Nếu đây là tình huống của bạn, rất có thể bạn sẽ cần phải đọc hết toàn bộ chương này.

**MẸO:** Một số bản phân phối Linux (chẳng hạn như Ubuntu) có khả năng sửa đổi các phân vùng Windows hiện có và thêm một phân vùng Linux một cách tự động như một phần của quá trình cài đặt. Hy vọng tính năng này sẽ trở nên phổ biến hơn ở các bản phân phối khác. Hãy kiểm tra tài liệu cài đặt của bản phân phối Linux cụ thể của bạn trước khi tiến hành.

Nếu bạn hoàn toàn không muốn khởi động kép bằng ổ cứng của mình, bạn có ba lựa chọn khác — tôi biết tôi đã nói rằng có tổng cộng ba cách tiếp cận và việc thêm ba cách nữa ở đây sẽ nâng tổng số lên sáu, nhưng hãy cho tôi một phút để giải thích.

Bạn có thể sử dụng phần mềm ảo hóa, chẳng hạn như VMware hoặc VirtualBox của Oracle (xem Chương 20\) để cài đặt một máy Linux "ảo" nằm gọn trong một cửa sổ bên trong bản cài đặt Windows hiện tại của bạn. Bạn giữ nguyên đĩa Windows của mình mà không có bất kỳ sửa đổi nào. Bạn chỉ cài đặt Linux trong khu vực ảo do phần mềm VMware hoặc VirtualBox tạo ra.

Bạn cũng có thể làm ngược lại: chỉ cài đặt Linux trên máy tính và sau đó sử dụng VMware hoặc VirtualBox để cài đặt một máy Windows ảo nằm trong một cửa sổ bên trong bản cài đặt Linux của bạn. Nếu làm điều này, hãy nhớ sao lưu các tệp Windows gốc trước khi cài đặt Linux, và sau đó khôi phục chúng trong khu vực Windows mới.

Cuối cùng, nếu ý nghĩ thay đổi bất cứ thứ gì trên máy tính khiến bạn nổi da gà, bạn chỉ cần sử dụng một bản phân phối Live (xem Chương 1\) để khởi động máy tính của bạn vào Linux mà không cần cài đặt bất cứ thứ gì. Bằng cách chạy Linux từ ổ đĩa DVD hoặc USB, nó sẽ chậm hơn (thậm chí là chậm một cách đau đớn trên các PC cũ), nhưng dẫu sao thì nó vẫn sẽ hoạt động, và cho bạn ý niệm về Linux thực sự là gì.

Vì vậy, hãy suy nghĩ xem bạn thích tùy chọn nào được trình bày chi tiết ở đây, và sau đó đọc tiếp.

**MẸO:** Windows 10 đã giới thiệu một tính năng mới gọi là Hệ thống con Windows dành cho Linux (WSL). Nó cung cấp một giao diện Linux cơ bản (ý tôi là cực kỳ cơ bản) để bạn có thể chạy một số ứng dụng Linux trong Windows. Tại thời điểm viết bài này, WSL vẫn đang ở giai đoạn sơ khai và không phù hợp để chạy một hệ thống Linux quy mô đầy đủ bên trong Windows. Tuy nhiên vẫn có hy vọng, vì phiên bản tiếp theo của WSL dự kiến sẽ hỗ trợ một nhân Linux và các thư viện đầy đủ. Có lẽ một ngày nào đó...

## **Chuẩn bị sử dụng chung Linux và Microsoft Windows**

Nếu bạn dự định chạy Linux và Microsoft Windows trong môi trường khởi động kép trên cùng một máy, nhiều khả năng là bạn đã cài đặt sẵn Windows và đang sử dụng nó một thời gian. Vì tôi rất ghét phải nghe tiếng la hét đau khổ từ những người dùng Linux mới, hãy dành một chút thời gian để đánh giá những gì bạn đang có và những gì bạn cần làm.

Trong trường hợp hy hữu là bạn thực sự chưa cài đặt Windows mà vẫn muốn có khả năng khởi động kép, bạn nên cài đặt Windows trước khi cài đặt Linux. Nếu không, trong quá trình cài đặt, Windows sẽ ghi đè lên phần ổ cứng mà Linux dùng để lưu trữ menu khởi động của nó. (Yếu tố này có thể tạo ra một mớ hỗn độn sau này khi bạn muốn khởi động lại vào Linux\!) Sau khi bạn đã cài đặt xong Windows, hãy quay lại đây.

Tuy nhiên, phần lớn các bạn muốn khởi động kép vì bạn có một máy và nó đã chạy một bản cài đặt Windows mà bạn thực sự không muốn phải làm lại. Các phần sau đây sẽ hướng dẫn các quy trình cần thiết để chuẩn bị cho máy tính của bạn sẵn sàng cho môi trường khởi động kép.

### **Cài đặt ổ cứng thứ hai**

Đứng sau việc thay thế hệ điều hành hiện tại, cách dễ thứ hai để đưa Linux lên PC là cài đặt một ổ cứng thứ hai. Nhiều máy tính để bàn hỗ trợ nhiều ổ cứng bằng cách nối hai ổ cứng với nhau trên cùng một cáp đĩa, hoặc cung cấp nhiều cáp để xử lý các ổ cứng.

Bạn phải mở nắp thùng máy PC và nhìn vào bên trong để xem bạn đang đối mặt với cái gì. Các thẻ điều khiển đĩa tiêu chuẩn trong hầu hết các PC cho phép tối đa hai thiết bị trên mỗi bộ điều khiển và PC thường sẽ có nhiều hơn một bộ điều khiển được cài đặt trên bo mạch chủ. Nếu bạn thấy hai cáp có các đầu nối nhiều chân dài trên đó, bạn thật may mắn. Nếu bạn chỉ thấy một cáp có đầu nối trống trên đó, bạn cũng sẽ ổn.

**MẸO:** Thông thường, bạn có thể xác định cấu hình bộ điều khiển đĩa bằng cách nhìn vào màn hình thiết lập BIOS cho PC của bạn. Để vào màn hình thiết lập BIOS, bạn thường cần nhấn một phím Chức năng (thường là F2 hoặc F12) khi PC của bạn vừa bắt đầu khởi động. Hãy tham khảo ý kiến nhà sản xuất PC cụ thể của bạn để tìm xem nên dùng phím nào. Bên cạnh ổ cứng, bộ điều khiển cũng hỗ trợ kết nối ổ đĩa CD/DVD, vì vậy bạn sẽ cần phải cẩn thận khi đánh giá tình trạng bộ điều khiển đĩa của mình.

Nếu bo mạch chủ của bạn chỉ chứa một bộ điều khiển đĩa, và sử dụng nó cho ổ cứng cùng với một thiết bị DVD, bạn sẽ không thể thêm ổ cứng thứ hai vào bộ điều khiển đó. Thông thường, bạn có thể tìm mua các thẻ điều khiển đĩa cắm thêm để bổ sung bộ điều khiển thứ hai cho PC. Bạn sẽ cần phải làm chính xác điều đó nếu muốn thêm một ổ cứng nữa.

Sau khi cài đặt xong ổ cứng thứ hai, bạn đã sẵn sàng bắt đầu với Linux. Như đã đề cập trước đó, sẽ rất hữu ích nếu biết ổ cứng nào là của Windows và ổ cứng nào sẽ được sử dụng cho Linux. Nếu bạn không biết, bạn có thể sử dụng một trong các công cụ quản lý đĩa được thảo luận trong phần tiếp theo. Một khi bạn đã biết ổ cứng nào là ổ cứng nào, bạn có thể chuyển đến phần "Kiểm tra lại khả năng tương thích của phần cứng" để kiểm tra phần cứng còn lại của máy tính.

### **Phân vùng một ổ đĩa hiện có**

Nếu bạn chỉ có một ổ cứng duy nhất khả dụng trong PC, bạn cần tạo các khu vực riêng biệt (gọi là phân vùng) trên ổ cứng cho Windows và Linux. Phần này hướng dẫn quy trình thực hiện điều đó, nhưng trước tiên, bạn cần hiểu cách thức hoạt động của các phân vùng.

Có ba loại phân vùng: chính (primary), mở rộng (extended) và logic (logical). Một ổ cứng có thể có ba phân vùng chính và một phân vùng mở rộng. Mỗi phân vùng chính hoạt động như một ổ cứng riêng biệt đối với hệ điều hành. Bên trong phân vùng mở rộng, bạn có thể có tới 12 phân vùng logic — hãy coi phân vùng mở rộng chỉ như một hộp các tông chứa các phân vùng logic. Các phân vùng logic hoạt động tương tự như các phân vùng chính và chứa dữ liệu; phân vùng mở rộng chỉ chứa các phân vùng logic. Vì tôi không thể dự đoán được phần mềm nào bạn muốn cài đặt, tôi khuyên bạn nên có ít nhất 10GB dung lượng trống trong một phân vùng dành cho bản cài đặt Linux của bạn. Càng nhiều càng tốt vì nó cung cấp cho bạn nhiều không gian hơn để tải xuống và cài đặt thêm nhiều chương trình.

Hãy ghi lại phân vùng nào bạn dành riêng cho Windows và phân vùng nào bạn dành riêng cho Linux. Bạn cần thông tin này khi cài đặt Linux.

Những ai không bắt đầu lại từ đầu cho việc khởi động kép nhiều khả năng sẽ cần phải thực hiện những thay đổi đối với bản cài đặt hiện tại của họ. Tiến hành sang phần tiếp theo để tìm hiểu cách thực hiện.

### **Phân vùng bằng các công cụ của Windows**

Nếu bạn đã cài đặt sẵn Windows trên toàn bộ ổ cứng, bạn sẽ cần phải thu nhỏ phân vùng đó lại để có chỗ cho Linux. Bước đầu tiên là kiểm tra ổ cứng hiện tại xem có bao nhiêu dung lượng trống có thể dành cho Linux. Bạn có thể làm điều đó bằng cách sử dụng công cụ File Explorer trong Windows theo các bước sau:

1. Mở File Explorer bằng cách nhấp vào biểu tượng thư mục trên thanh tác vụ, hoặc nhập **file explorer** vào ô tìm kiếm trên thanh tác vụ và chọn **File Explorer** từ kết quả tìm kiếm.  
2. Khi File Explorer mở ra, hãy nhấp vào **This PC** ở phía bên trái của cửa sổ.

Thao tác này hiển thị trạng thái của các thiết bị lưu trữ khác nhau mà bạn đã kết nối với PC của mình. (Hình 2-1 hiển thị một ví dụ về những gì bạn có thể thấy trong File Explorer).

Ví dụ được hiển thị trong Hình 2-1 cho thấy một ổ cứng duy nhất được kết nối với PC (được gán làm ký tự ổ đĩa C). File Explorer cho thấy ổ đĩa có kích thước 899GB và có 483GB trống để sử dụng làm phân vùng thứ hai.

**MẸO:** Thường không phải là một ý hay nếu phân bổ toàn bộ dung lượng trống trên ổ cứng của bạn cho Linux; bạn sẽ muốn chừa lại một chút không gian trong phân vùng Windows để có thể tiếp tục làm nhiều việc khi đang chạy Windows, chẳng hạn như tải xuống và cài đặt các bản vá lỗi hoặc lưu tệp mới.

Sau khi xác định được lượng dung lượng muốn dành cho Linux, bạn đã sẵn sàng phân vùng ổ cứng.

Tiện ích Windows mà bạn muốn sử dụng là chương trình Disk Management (Quản lý Đĩa). Làm theo các bước sau để sử dụng nó:

1. Nhấp chuột phải vào biểu tượng **Start** trên thanh tác vụ.  
2. Từ menu xuất hiện, chọn **Disk Management**.

Hộp thoại Disk Management xuất hiện (như Hình 2-2). Hộp thoại hiển thị tất cả các ổ cứng được cài đặt trên PC, cùng với các phân vùng cho mỗi ổ.

3. Nhấp chuột phải vào phân vùng cho biết nó được chỉ định là phân vùng Windows và được gán một ký tự ổ đĩa (thường là ổ C).

Bạn có thể nhấp vào mục phân vùng trong danh sách văn bản, hoặc hình ảnh đồ họa của phân vùng.

**CẢNH BÁO:** Nhiều PC hiện đại tạo ra một hoặc nhiều phân vùng ẩn không được gán ký tự ổ đĩa trong Windows. Các phân vùng này không xuất hiện trong File Explorer, nhưng được PC sử dụng để chứa dữ liệu khôi phục nhằm cài đặt lại Windows trong trường hợp khẩn cấp. Đừng đụng chạm gì đến những phân vùng đó\!

4. Chọn **Shrink Volume** (Thu nhỏ dung lượng) từ menu bật lên.

Hộp thoại Shrink Volume xuất hiện (như Hình 2-3).

5. Nhập lượng dung lượng bạn muốn gán cho phân vùng Linux vào hộp văn bản.

Lưu ý rằng mục nhập được tính bằng MB (megabyte) thay vì GB (gigabyte). Một gigabyte bằng 1024 megabyte, vì vậy bạn chỉ cần nhân giá trị không gian GB khả dụng với 1024 để có được giá trị MB cần nhập vào đây.

6. Nhấp vào **Shrink**.

**CẢNH BÁO:** Trong quá trình thu nhỏ, Windows cố gắng di chuyển bất kỳ dữ liệu nào được lưu trữ ở gần cuối phân vùng về phía trước để nhường chỗ cho phân vùng mới. Tuy nhiên, một số tệp hệ thống không thể di chuyển được, điều này có thể gây ra sự cố và tạo ra thông báo lỗi. Nếu điều này xảy ra, có những cách để di chuyển những tệp đó, nhưng nó sẽ phức tạp hơn nhiều so với những gì tôi có thể đề cập ở đây. May mắn thay, bạn không phải là người đầu tiên cần làm việc này, vì vậy có rất nhiều sự trợ giúp có sẵn. Một nơi để tham khảo là diễn đàn Windows của Microsoft tại answers.microsoft.com và bạn sẽ thấy rất nhiều bài đăng về cách xử lý tình huống này.

Khi quá trình thu nhỏ hoàn tất, một phân vùng mới xuất hiện trong danh sách Disk Manager. Phân vùng mới này xuất hiện dưới dạng Unassigned (Chưa được gán) và không có ký tự ổ đĩa nào được Windows gán cho nó.

**GHI NHỚ:** Nếu có nhiều dung lượng trống trên phân vùng Windows hiện tại, bạn có thể sẽ muốn nhiều hơn 10GB dung lượng. 10GB là mức tối thiểu được khuyến nghị cho hầu hết các bản phân phối Linux để vừa vặn hệ điều hành. Tuy nhiên, nếu bạn tải xuống nhiều nội dung đa phương tiện, bạn sẽ nhanh chóng ngốn sạch bất cứ thứ gì còn sót lại sau khi cài đặt phần mềm của mình\! Hãy cấp cho Linux bao nhiêu dung lượng tùy thích mà bạn nghĩ có thể nhường bớt từ môi trường Windows của mình.

### **Phân vùng bằng các công cụ của Linux**

Nếu bạn đang trong tình huống chưa cài đặt Windows trên ổ cứng nhưng muốn phân vùng ổ cứng trước, bạn có thể sử dụng các công cụ Linux để thực hiện công việc đó thay mình. Giải pháp dễ dàng là khởi động PC của bạn bằng một bản phân phối Live và sử dụng các công cụ quản lý đĩa có sẵn. Có rất nhiều bản phân phối Live bao gồm các công cụ quản lý đĩa theo mặc định, nhưng phổ biến nhất cho đến nay là bản phân phối KNOPPIX Linux.

Bản phân phối KNOPPIX Linux là bản đầu tiên tạo ra phiên bản Linux trực tiếp, thậm chí từ trước khi có đĩa DVD (nó được gọi là LiveCD\!). Điều giữ cho KNOPPIX luôn đứng đầu danh sách các bản phân phối Linux phổ biến là vô số các tiện ích mà nó tích hợp sẵn theo mặc định. Nó tự quảng cáo bản thân như một đĩa cứu hộ — một cách để khởi động PC của bạn nếu mọi thứ diễn ra tồi tệ với hệ điều hành hiện tại, và có thể khắc phục sự cố cũng như sửa lỗi.

Làm theo các bước sau để phân vùng ổ cứng của bạn bằng KNOPPIX:

1. Tải xuống hình ảnh ISO CD hoặc DVD KNOPPIX mới nhất từ trang web KNOPPIX tại www.knopper.net.  
2. Ghi hình ảnh ISO lên một đĩa CD, DVD hoặc USB có khả năng khởi động bằng cách sử dụng công cụ ghi hình ảnh ISO tiêu chuẩn. (Hãy chuyển đến phần "Tạo đĩa khởi động" để xem hướng dẫn nhanh về cách thực hiện việc này, sau đó quay lại đây).  
3. Khởi động PC của bạn bằng KNOPPIX LiveDVD. Tại dấu nhắc khởi động, nhấn phím Enter để bắt đầu KNOPPIX.  
4. Chọn **Graphical Programs \> startlxde** từ menu chính. Môi trường máy tính để bàn đồ họa KNOPPIX hiện lên. Nó là một máy tính để bàn đồ họa khá cơ bản để có thể chạy trên gần như mọi PC, nhưng nó hoàn thành tốt công việc.  
5. Từ máy tính để bàn đồ họa KNOPPIX, nhấp vào biểu tượng **Terminal** trên thanh tác vụ ở cuối màn hình. Một phiên Terminal bắt đầu cung cấp quyền truy cập vào dấu nhắc lệnh (tôi nói thêm về điều đó trong Chương 16).  
6. Tại dấu nhắc lệnh trong Terminal, nhập lệnh: sudo gparted. Ứng dụng GParted là một công cụ quản lý đĩa phổ biến cho Linux. Nó cung cấp một giao diện tương tự như công cụ quản lý đĩa của Windows (như Hình 2-4).  
7. Nhấp chuột phải vào bên trong phân vùng bạn cần thu nhỏ.  
8. Chọn **Resize/Move** từ menu bật lên. Hộp thoại Resize/Move mở ra (như Hình 2-5).  
9. Trong hộp thoại Resize/Move, hãy kéo phần cuối cùng bên phải của hộp đồ họa phân vùng để thay đổi kích thước phân vùng, hoặc nhập một giá trị mới vào hộp văn bản New Size. Phần có màu của hộp biểu thị nơi lưu trữ dữ liệu hiện có trong phân vùng. Bạn sẽ có thể di chuyển phần cuối của phân vùng xuống gần khu vực đó.  
10. Nhấp vào nút **Resize/Move** để bắt đầu quá trình thay đổi kích thước.

Sau khi ổ cứng được phân vùng, bạn có thể thoát công cụ và tắt KNOPPIX. Và đó là tất cả những gì cần làm\! Sau khi thay đổi kích thước các phân vùng, bạn đã sẵn sàng chuyển sang bước tiếp theo trong việc chuẩn bị PC cho Linux — kiểm tra phần cứng của bạn, như được mô tả trong phần tiếp theo.

## **Kiểm tra lại khả năng tương thích của phần cứng**

Nếu bạn đang cài đặt Linux trên phần cứng mà bạn đã sở hữu, cứ thử nghiệm đi và xem có gì không hoạt động. Các phần trong mục này giải quyết việc khắc phục sự cố phần cứng theo nghĩa chung. Trong các chương khác, các mục cụ thể hơn như card âm thanh (Chương 13), card không dây (Chương 9), v.v., sẽ được giải quyết. Vì vậy, nếu gặp rắc rối, hãy bắt đầu ở các phần cụ thể dành riêng cho các tác vụ nhất định, và sau đó đến đây để được trợ giúp chung nếu bạn vẫn chưa giải quyết được sự cố.

Khu vực có vấn đề không tương thích phần cứng lớn nhất là card mạng không dây và các phần cứng đa phương tiện hào nhoáng mới nhất như card video và card âm thanh. Bạn có thể kiểm tra danh sách khả năng tương thích phần cứng trước khi cài đặt hoặc mua phần cứng mới, nhưng chúng có tiện ích hạn chế vì thế giới phần cứng thay đổi quá nhanh.

Nếu bạn quan tâm đến việc tìm kiếm, trước tiên hãy thử trang web hỗ trợ cho bản phân phối Linux cụ thể của bạn, chẳng hạn như danh sách của Red Hat Enterprise Linux tại https://www.google.com/search?q=access.redhat.com/ecosystem/search/%23/category/ đối với các bản phân phối CentOS hoặc Fedora, hoặc danh sách của Ubuntu tại certification.ubuntu.com/ đối với bất kỳ bản phân phối Ubuntu nào.

**MẸO:** Hãy nhớ rằng danh sách khả năng tương thích phần cứng thường tập trung vào thiết bị doanh nghiệp thay vì đồ dùng gia đình, vì vậy chỉ vì bạn không thấy một thứ gì đó được liệt kê ở đó không có nghĩa là nó sẽ không hoạt động. Đừng lo lắng về việc các mặt hàng có được "Chứng nhận" (đã được kiểm tra kỹ lưỡng để đảm bảo chúng hoạt động bình thường) hay không. "Được hỗ trợ" (Supported) và "Tương thích" (Compatible) là ổn trong hầu hết thời gian đối với người dùng gia đình. Cuối cùng, cách tốt nhất để biết một phần cứng có được hỗ trợ hay không là tìm kiếm trên web. Nhiều người truy cập Google và thực hiện tìm kiếm trên web về nhà sản xuất và kiểu dáng của phần cứng, cộng với từ "Linux". Nếu cần các trình điều khiển cụ thể để hỗ trợ phần cứng, bạn thường có thể tìm thêm thông tin cài đặt bằng cách thêm tên bản phân phối Linux của mình vào tìm kiếm. Một tìm kiếm như vậy có khả năng cho bạn thấy những vấn đề và thành công mà mọi người đã gặp phải với phần cứng cụ thể đó.

Nếu ngay cả việc nghĩ đến phần cứng máy tính cũng khiến bạn chóng mặt, đừng lo lắng, bạn có thể tìm thấy rất nhiều thông tin trên Internet. Một nơi tuyệt vời để bắt đầu là www.tomshardware.com. Những nơi khác để tìm kiếm thông tin về cách các thiết bị khác nhau hoạt động trong Linux bao gồm:

* **Các trang web định hướng Linux khác:** Khá nhiều trang web dành riêng cho việc giúp người dùng Linux hỗ trợ phần cứng. Tiêu chuẩn cũ là danh sách phần cứng Linux chung tại www.tldp.org/HOWTO/Hardware-HOWTO/. Có sẵn các trang web cập nhật hơn, chẳng hạn như linux-hardware.org.  
* **Trang web của nhà cung cấp:** Nhiều nhà cung cấp phần cứng có hỗ trợ Linux, nhưng họ không làm cho việc tìm kiếm thông tin về nó trở nên dễ dàng. Nói chung, hãy tìm kiếm trong diễn đàn của nhà cung cấp (nếu họ có) cho phần cứng đó, mục Câu hỏi thường gặp (FAQ) cho phần cứng, hoặc làm theo các liên kết Hỗ trợ (Support) để tìm kiếm các bản tải xuống cho Linux. Đừng tải xuống những gì bạn tìm thấy (nếu có các bản tải xuống). Vấn đề là hãy nhìn và xem liệu chúng có tồn tại hay không. Trình điều khiển (phần mềm cho hệ điều hành biết cách sử dụng phần cứng) có sẵn để tải xuống có thể thực sự đã được bao gồm trong bản cài đặt Linux của bạn. Chỉ tải xuống trình điều khiển từ nhà cung cấp nếu đây là cách duy nhất bạn có thể lấy được nó.

Nếu trường hợp tồi tệ nhất xảy ra, có thể bạn sẽ không tìm thấy bất kỳ thông tin nào về phần cứng đang được đề cập liên quan đến Linux. Tuy nhiên, một lần nữa, điều này không có nghĩa là phần cứng sẽ không hoạt động. Dù sao hãy cứ thử nếu bạn đã có món đồ đó. Bạn có thể thấy rằng nó hoạt động tốt. Hoặc, bạn có thể không sử dụng được các tính năng mới nhất, trong khi phần còn lại vẫn hoạt động tốt. (Ví dụ: với một card video thế hệ mới nhất, các tính năng lạ mắt mới nhất có thể không hoạt động, nhưng ít nhất bạn vẫn có thể sử dụng nó như một chuẩn SVGA chung).

* **Những cuốn sách hướng dẫn đáng sợ:** Khi có thể, hãy giữ sổ tay máy tính của bạn (đặc biệt là những cuốn dành cho card video và màn hình) ở nơi thuận tiện, phòng trường hợp bạn cần chúng để trả lời một câu hỏi do trình cài đặt đặt ra — hầu hết mọi người không phải đối phó với điều này chút nào, nhưng một số thì có.

**NHỮNG ĐIỀU CẦN LƯU Ý VỚI LAPTOP**

Các bản phân phối hiện tại của Linux hoạt động rất tốt trên các laptop tương đối mới. (Truy cập www.linux-laptop.net để xem một trang web nghiên cứu xuất sắc về mức độ hòa hợp của Linux với các hãng và mẫu máy khác nhau.) Nếu laptop của bạn là một thương hiệu phổ biến, bạn sẽ không gặp bất kỳ vấn đề nào khi cài đặt Linux. Tuy nhiên, một số laptop phải sử dụng phần cứng kỳ lạ để nhồi nhét tất cả các tính năng tiện dụng đó vào những chiếc hộp nhỏ xíu như vậy. Đôi khi Linux sẽ không hoạt động với các tính năng quá lạ trên những chiếc laptop đó, chẳng hạn như màn hình cảm ứng, bàn di chuột có thể nhấp và đèn bàn phím.

Nếu bạn định mua một chiếc laptop cho Linux, hãy kiểm tra thông số kỹ thuật phần cứng của nó (chẳng hạn như card mạng) để đảm bảo chúng không dành riêng cho Windows. Nếu phần cứng tích hợp hoặc phần cứng mặc định cho laptop được dán nhãn "Win" (hoặc bạn phát hiện ra trong quá trình nghiên cứu chiếc máy đó rằng nó chứa một sản phẩm Win, ngay cả khi nó không được dán nhãn đúng cách), bạn có thể chuyển đổi phần cứng gặp vấn đề đó bằng một thiết bị ngoại vi cắm vào laptop qua cổng USB. Hầu hết các laptop hiện tại đều chứa ít nhất một khe cắm USB để bạn có chỗ kết nối card mạng hoặc card âm thanh bên ngoài. Miễn là bạn sử dụng một thương hiệu thiết bị ngoại vi USB phổ biến, nó sẽ hoạt động tốt với Linux.

Nếu cần tìm hiểu chính xác phần cứng nào có trong máy của mình, bạn có các tùy chọn sau:

* **Sử dụng hệ điều hành hiện có để ghi lại phần cứng của bạn:** Nếu máy tính của bạn đã chạy Windows, bạn có thể thu thập rất nhiều thông tin từ môi trường Windows. Trong Windows 10, nhấp chuột phải vào biểu tượng menu **Start** trên thanh tác vụ, sau đó chọn **Device Manager**. Hộp thoại Device Manager xuất hiện (như Hình 2-6).  
* **Tải xuống một công cụ phát hiện phần cứng PC:** Một số công cụ phát hiện phần cứng cũng có sẵn trên Internet, chẳng hạn như Dr. Hardware. Công cụ Dr. Hardware chứa rất nhiều thông tin về những gì bên trong máy của bạn. Công cụ này là phần mềm dùng thử (shareware) và thông tin về việc sử dụng cũng như phí có trên trang web của Gebhard Software (www.dr-hardware.com/).  
* **Truy cập Hệ thống Đầu vào/Đầu ra Cơ bản (BIOS)**, hoặc đối với các PC mới hơn là thông tin **Giao diện Phần mềm cơ sở Mở rộng Hợp nhất (UEFI)**. Được lưu trữ trong một khu vực bộ nhớ nhỏ và được duy trì bằng pin, khu vực này đôi khi được gọi là CMOS (Complementary Metal-Oxide Semiconductor), cho biết loại chip máy tính có thể lưu trữ và giữ lại thông tin. Lượng thông tin được lưu trữ trong BIOS hoặc UEFI có thể dao động từ rất ít đến khá nhiều. Một số hệ thống mới hơn có thể hiển thị một vài màn hình thông tin về phần cứng của máy tính.

**MẸO:** Nếu bạn chọn truy cập BIOS, hãy đảm bảo bạn làm vậy trước khi bất kỳ hệ điều hành nào tải lên. Hầu hết các nhà sản xuất đều chỉ định phím trên bàn phím (hoặc tổ hợp phím) giúp bạn vào màn hình BIOS (hoặc Setup \- Thiết lập) khi hệ thống đang khởi động — ví dụ: "Press Del to enter Setup" (Nhấn Del để vào Thiết lập). Nếu bạn không thể tìm thấy tổ hợp phím, hãy kiểm tra trang web của nhà sản xuất. Sau khi đã vào BIOS, bạn thường điều hướng bằng các phím mũi tên, phím Tab hoặc phím Enter. Một số môi trường BIOS cũng sử dụng các phím chức năng; hãy tìm danh sách các tùy chọn phím chức năng ở trên cùng hoặc dưới cùng của màn hình. Hãy đặc biệt cảnh giác với các nhãn dán trên hộp phần cứng và các trang web có bao gồm thuật ngữ "Win" (như trong Windows). Những linh kiện này phụ thuộc vào Microsoft Windows để có thể hoạt động — tệ hơn nữa, bao bì có thể không hiển thị bất cứ thứ gì cho thấy hạn chế này. Chỉ có một cơ hội rất mong manh để bạn có thể tìm thấy trình điều khiển Linux cho phần cứng Win. Nếu bạn tìm thấy một trình điều khiển, hãy sao chép nó vào ổ USB trước khi cài đặt Linux.

## **Cuối cùng, cuối cùng, trước khi bạn bắt đầu**

Trước khi có thể cài đặt Linux, bạn cần đảm bảo bạn và PC của bạn đã sẵn sàng để khởi động một bản phân phối Linux. Bạn cần kiểm tra hai điều cuối cùng trước khi chuyển sang chương tiếp theo và cài đặt Linux:

* Đảm bảo PC của bạn có thể khởi động một hệ điều hành thay thế.  
* Tạo phương tiện có thể khởi động cho bản phân phối Linux của bạn.

Hai phần sau đây thảo luận chi tiết về cả hai yêu cầu này.

### **Vô hiệu hóa tính năng khởi động an toàn (Secure boot)**

Nhờ tất cả các cuộc tấn công khác nhau nhắm vào PC ngày nay, hầu hết các PC hiện đại đều bao gồm lớp bảo mật bổ sung để ngăn chặn việc khởi động bằng một "hệ điều hành không được ủy quyền". Thật không may, theo mặc định, hệ điều hành được ủy quyền duy nhất cho hầu hết các PC là Microsoft Windows (hãy thử nghĩ xem). Bạn cần phải vô hiệu hóa tính năng này để khởi động hầu hết các bản phân phối Linux.

Các hệ thống sử dụng phương pháp khởi động UEFI bị khóa để bản ghi khởi động không thể bị thay đổi nhằm khởi động từ Linux, hoặc khởi động kép giữa Linux và Windows. Bạn cần vô hiệu hóa tính năng này để có thể cài đặt Linux trên PC của mình.

Tính năng này là một phần của trang cài đặt UEFI mà bạn chỉ có thể truy cập khi khởi động PC của mình. Bạn có thể truy cập các cài đặt này bằng cách nhấn một phím đặc biệt khi hệ thống vừa khởi động. Bạn cần nhấn phím nào phụ thuộc vào thương hiệu PC cụ thể của bạn. Hãy tham khảo sổ tay hướng dẫn của bạn để tìm xem đó là phím nào.

**MẸO:** Hầu hết các PC dùng UEFI cũng sử dụng một tính năng gọi là khởi động nhanh (fast boot), tính năng này bỏ qua nhiều quy trình kiểm tra trước khi khởi động trước đây do BIOS thực hiện và chuyển thẳng vào khởi động Windows. Bạn phải bấm phím thật nhanh để đến được trang cài đặt UEFI\!

Sau khi truy cập vào các trang cài đặt UEFI, bạn cần phải tìm kiếm một chút. Các hệ thống khác nhau kết hợp các tính năng bảo mật khác nhau. Hãy tìm kiếm các cài đặt liên quan đến **Secure Boot** (Khởi động An toàn) và đảm bảo bạn đặt chúng thành giá trị **Disabled** (Đã vô hiệu hóa). Khi hoàn tất, hãy lưu các thay đổi và thoát khỏi trang UEFI.

**MẸO:** Một số bản phân phối Linux đã đàm phán với Microsoft để bao gồm các khóa chứng nhận cần thiết trong hệ điều hành của họ nhằm có thể khởi động từ UEFI với tính năng khởi động an toàn được bật. Hãy kiểm tra với bản phân phối Linux cụ thể của bạn để xem nó có hỗ trợ tính năng này hay không.

### **Tạo đĩa khởi động**

Đĩa DVD hoặc ổ USB có khả năng khởi động là thứ cuối cùng bạn cần trước khi tiến hành cài đặt Linux. Nếu bạn còn nhớ ở Chương 1, các bản phân phối Linux xuất hiện dưới dạng các tệp hình ảnh ISO. Đối với hầu hết các tình huống, bạn cần ghi tệp ISO sang đĩa DVD, hoặc sử dụng một tiện ích để tạo ổ USB khởi động. Phần này hướng dẫn bạn qua cả hai quy trình đó.

#### **Tạo đĩa DVD khởi động**

Nếu hiện tại bạn có sẵn một PC chạy Windows, bạn có thể sử dụng các tính năng tích hợp sẵn của Windows 10 để ghi hình ảnh ISO Linux ra đĩa DVD. Chỉ cần làm theo các bước sau:

1. Mở **File Explorer** và điều hướng đến vị trí của tệp hình ảnh ISO đã tải xuống.  
2. Nhấp chuột phải vào tệp hình ảnh và chọn **Burn Disc Image**. Công cụ Microsoft Disc Image Burner khởi động (như Hình 2-7).  
3. Đưa một đĩa DVD trắng vào khay đĩa DVD, sau đó nhấp vào **Burn** để bắt đầu quá trình.  
4. Khi quá trình ghi hoàn tất, hãy lấy đĩa DVD ra và dán nhãn cho nó với hệ điều hành và phiên bản.

Mặc dù có vẻ buồn cười khi đưa việc dán nhãn DVD vào bước cuối cùng, nhưng sau khi bắt đầu thử nghiệm với Linux, bạn sẽ ngạc nhiên về số lượng đĩa DVD khác nhau mà bạn bắt đầu tích lũy được\! Tôi không thể nói cho bạn biết tôi có bao nhiêu chiếc DVD không dán nhãn nằm vương vãi quanh văn phòng chứa các bản phân phối Linux khác nhau trên đó\!

#### **Tạo USB khởi động**

Một xu hướng ở các máy tính để bàn và laptop hiện đại ngày nay là từ bỏ ổ đĩa DVD. Với sự dễ dàng của việc tải phần mềm từ Internet, việc có ổ đĩa DVD chỉ chiếm không gian có thể được sử dụng cho những việc khác (hoặc trong trường hợp của laptop, chỉ để làm cho chúng nhỏ hơn). Nếu PC của bạn không có ổ DVD, đừng bực mình — có một cách khác để khởi động Linux.

Các PC hiện đại bao gồm tùy chọn khởi động từ thẻ USB. Tuy nhiên, có một chút thủ thuật trong việc tạo ra một thẻ USB mà PC có thể khởi động từ đó. Bạn không thể chỉ sử dụng tiện ích ghi DVD để ghi tệp hình ảnh ISO vào ổ USB như cách bạn làm với đĩa DVD.

May mắn thay, nhiều bản phân phối Linux hiện đã bao gồm các tiện ích để tạo ổ USB khởi động với các bản phân phối của họ. Hãy kiểm tra tài liệu của bản phân phối Linux của bạn để xem nó có hỗ trợ tiện ích như vậy hay không.

Nếu bản phân phối Linux cụ thể của bạn không có tiện ích riêng để tạo ổ USB khởi động, bạn có thể sử dụng tiện ích của bên thứ ba. Một trong những công cụ phổ biến hơn cho việc này là Rufus, tìm thấy tại rufus.ie. Sau khi tải xuống tệp ISO bản phân phối Linux cụ thể và Rufus, hãy làm theo các bước sau để tạo thẻ USB khởi động từ tệp ISO:

1. Cắm một thẻ USB trắng vào cổng USB trên PC của bạn. Đảm bảo thẻ USB bạn chọn đủ lớn để chứa tệp hình ảnh ISO. Các tệp hình ảnh ISO cho một số bản phân phối Linux có kích thước lên tới 4GB\!  
2. Khởi động chương trình **Rufus**. Hộp thoại chương trình Rufus mở ra (như Hình 2-8).  
3. Chọn ổ USB trong hộp thả xuống **Device**. Hãy thật cẩn thận nếu bạn cắm nhiều ổ USB vào PC. Sẽ rất hữu ích nếu bạn chỉ cắm ổ đĩa bạn muốn định dạng để không vô tình xóa sạch những điểm số bowling quan trọng mà bạn đang theo dõi\!  
4. Trong hộp thả xuống **Boot Selection**, chọn **Disk or ISO image**, sau đó nhấp vào nút **Select** và điều hướng đến tệp hình ảnh ISO bạn muốn sử dụng.  
5. Nhấp vào **Start** để bắt đầu tạo thẻ USB khởi động. Rufus hiển thị hộp thoại cảnh báo cho biết mọi thứ trên thẻ USB sẽ bị xóa. Hãy đảm bảo bạn không có bất kỳ tệp quan trọng nào trên thẻ USB trước khi tiếp tục\!  
6. Khi quá trình hoàn tất, hãy tháo thẻ USB ra và dán nhãn cho nó với hệ điều hành và phiên bản.

Giờ đây, bạn có thể khởi động PC của mình từ thẻ USB có thể khởi động. Hầu hết các PC đều yêu cầu bạn chọn tùy chọn khởi động từ thiết bị USB lúc khởi động (startup). Bạn có thể cần phải ngắt quá trình khởi động bình thường để thấy menu lựa chọn đó.

Nếu bạn đã làm được đến bước này, bạn đã hoàn toàn sẵn sàng để bắt đầu cài đặt Linux\!