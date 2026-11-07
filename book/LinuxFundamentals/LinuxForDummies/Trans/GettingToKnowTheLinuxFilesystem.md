# **Phần 2: Bắt nhịp với Linux**

**TRONG PHẦN NÀY..**

* Khám phá nơi lưu trữ các thành phần khác nhau trong hệ thống tệp Linux của bạn.  
* Điều hướng hệ thống tệp Linux như một chuyên gia.  
* Kết nối máy tính Linux của bạn với Internet.

# **Chương 7: Làm quen với Hệ thống tệp Linux**

**TRONG CHƯƠNG NÀY**

* Khám phá cách tìm đường trong hệ thống tệp  
* Tìm kiếm các thiết bị lưu trữ di động (removable media) của bạn  
* Hiểu về quyền hạn trên hệ thống tệp (filesystem permissions)

Một trong những điều bực bội nhất khi thành thạo một hệ điều hành mới có thể là việc tìm ra nơi nó lưu trữ tệp tin. Thay vì giữ tất cả các tệp hệ thống quan trọng trong một thư mục duy nhất, chẳng hạn như thư mục C:\\Windows trong Microsoft Windows, Linux học theo những người anh em UNIX của mình và dàn trải mọi thứ ra một chút. Mặc dù cấu trúc của Linux và Windows liên quan đến các phương pháp khác nhau, nhưng cả hai đều có tính logic, mặc dù bạn có thể không cảm thấy như vậy cho đến khi bạn hiểu rõ mình cần tìm ở đâu.

Sau khi đưa bạn đi tham quan để biết nơi tìm kiếm mọi thứ, chương này sẽ chỉ cho bạn cách làm việc trong hệ thống tệp của mình trên giao diện dòng lệnh (command line). Việc đọc phần này không phải là bắt buộc nếu việc gõ các lệnh khiến bạn "tim đập chân run", nhưng nó có thể hữu ích nếu sau này bạn cần sửa chữa một cái gì đó, và đôi khi một số người lại thích biết cách làm những việc này theo cách thủ công.

## **Các Mảnh ghép Cơ bản**

Sẽ rất hữu ích nếu bạn hiểu các thuật ngữ chuyên môn trước khi bắt đầu. Rất nhiều trong số này sẽ quen thuộc với bạn từ các hệ điều hành khác như Microsoft Windows, nhưng cũng có một số điểm khác biệt mà bạn sẽ sớm nhận ra.

### **Hệ thống tệp (Filesystem) là gì?**

Linux sử dụng thuật ngữ *hệ thống tệp* (filesystem) để chỉ toàn bộ cách thức các tệp của bạn được tổ chức và quản lý trên ổ đĩa. Nó bao gồm các quy tắc về cách đặt tên, lưu trữ, và truy xuất dữ liệu.

### **Thư mục gốc (Root) của Linux: Không chỉ là chuyện nhuộm tóc**

Trong Windows, mỗi phân vùng (partition) hoặc ổ đĩa cứng (hard drive) được gán một ký tự ổ đĩa (ví dụ: C:\\ hoặc D:\\). Mỗi ổ đĩa có một hệ thống phân cấp thư mục riêng biệt bắt đầu từ gốc của ổ đĩa đó.

Trong Linux, mọi thứ đều bắt đầu từ một thư mục gốc (root directory) duy nhất, được biểu diễn bằng một dấu gạch chéo tiến (forward slash: /). Bất kể bạn có bao nhiêu ổ cứng, ổ đĩa DVD, hoặc ổ USB, tất cả chúng đều được gắn (mount) vào một vị trí nào đó bên trong hệ thống phân cấp duy nhất này.

### **Gắn kết (Mounting) trong Linux: Không chỉ dành cho thợ nhồi bông thú**

Khi bạn muốn truy cập nội dung của một ổ đĩa cứng mới, đĩa DVD, hoặc thẻ nhớ USB trong Linux, thiết bị đó phải được *gắn kết* (mounted) vào hệ thống tệp. Quá trình gắn kết là cách Linux liên kết phần cứng vật lý (như ổ USB) với một thư mục cụ thể (gọi là *mount point* \- điểm gắn kết) trong cây hệ thống tệp.

Ví dụ, nếu bạn cắm một thẻ USB vào, Linux có thể gắn nó vào thư mục /media/usb. Khi đó, bạn chỉ cần điều hướng đến thư mục /media/usb để xem nội dung của thẻ USB đó.

## **Sắp xếp Hệ thống tệp (Sorting Through the Filesystem)**

Bây giờ bạn đã biết mọi thứ đều bắt đầu từ thư mục gốc /, bạn có thể tự hỏi điều gì nằm bên dưới đó. Mặc dù các bản phân phối Linux khác nhau có thể có những biến thể nhỏ, nhưng hầu hết đều tuân theo một tiêu chuẩn gọi là *Filesystem Hierarchy Standard* (FHS \- Tiêu chuẩn Phân cấp Hệ thống tệp).

Bảng 7-1 giải thích một số thư mục cấp cao nhất phổ biến mà bạn sẽ thấy trong hầu hết các hệ thống Linux.

**Bảng 7-1: Các Thư mục Cơ bản của Linux**

| Thư mục | Nội dung bên trong |
| :---- | :---- |
| /bin | Các tệp nhị phân (binaries) của lệnh người dùng thiết yếu (ví dụ: ls, cp). |
| /boot | Các tệp tĩnh của bộ tải khởi động (boot loader), bao gồm cả nhân Linux (kernel). |
| /dev | Các tệp thiết bị (device files) đại diện cho phần cứng vật lý. |
| /etc | Các tệp cấu hình hệ thống dành riêng cho máy chủ (thường là tệp văn bản thuần túy). |
| /home | Thư mục cá nhân của người dùng (user home directories), nơi bạn lưu trữ các tệp và cài đặt cá nhân của mình. |
| /lib | Các thư viện dùng chung thiết yếu và các mô-đun nhân (kernel modules) cần thiết để khởi động hệ thống. |
| /media | Điểm gắn kết (mount point) cho các phương tiện có thể tháo rời (như đĩa CD-ROM, USB). |
| /mnt | Điểm gắn kết cho việc gắn các hệ thống tệp tạm thời. |
| /opt | Các gói phần mềm ứng dụng tùy chọn từ bên thứ ba (thường là phần mềm không đi kèm với hệ điều hành). |
| /root | Thư mục cá nhân dành riêng cho người dùng root (quản trị viên hệ thống). |
| /sbin | Các tệp nhị phân hệ thống thiết yếu, chủ yếu được sử dụng bởi người dùng root để quản trị hệ thống. |
| /srv | Dữ liệu cho các dịch vụ do hệ thống cung cấp (chẳng hạn như dữ liệu trang web cho máy chủ web). |
| /tmp | Thư mục chứa các tệp tạm thời (thường bị xóa khi khởi động lại máy). |
| /usr | Hệ thống phân cấp thứ cấp chứa dữ liệu chỉ đọc của người dùng, bao gồm phần lớn các chương trình (user utilities) và ứng dụng của người dùng. |
| /var | Dữ liệu biến đổi (variable data), chẳng hạn như các tệp nhật ký (log files), cơ sở dữ liệu và tệp spool của máy in. |

## **Trò chơi Dòng lệnh (Playing the Shell Game)**

Mặc dù các máy tính để bàn đồ họa (như GNOME và KDE Plasma) cung cấp các trình quản lý tệp tuyệt vời, đôi khi việc sử dụng dòng lệnh (command line) lại nhanh chóng và hiệu quả hơn. Các chương sau (như Chương 16\) sẽ đi sâu hơn vào dòng lệnh, nhưng đây là một vài lệnh cơ bản để giúp bạn điều hướng hệ thống tệp.

### **Tôi đang ở đâu? (pwd)**

Lệnh pwd (viết tắt của *print working directory* \- in thư mục làm việc) là người bạn tốt nhất của bạn khi bạn bị lạc. Nó sẽ cho bạn biết chính xác vị trí hiện tại của bạn trong hệ thống tệp.

$ pwd  
/home/rich

### **Dạo quanh (cd)**

Lệnh cd (viết tắt của *change directory* \- thay đổi thư mục) cho phép bạn di chuyển từ thư mục này sang thư mục khác. Bạn có thể sử dụng đường dẫn tuyệt đối (bắt đầu bằng /) hoặc đường dẫn tương đối (từ vị trí hiện tại của bạn).

$ cd /etc  
$ pwd  
/etc

Có một lối tắt hữu ích: Ký hiệu dấu ngã (\~) đại diện cho thư mục home của bạn. Vì vậy, lệnh cd \~ sẽ đưa bạn thẳng về thư mục cá nhân của mình, bất kể bạn đang ở đâu. (Chỉ cần gõ cd và nhấn Enter cũng thường có tác dụng tương tự).

### **Nhìn xung quanh (ls)**

Khi bạn đã ở trong một thư mục, bạn có thể sử dụng lệnh ls (viết tắt của *list* \- liệt kê) để xem có gì bên trong đó.

$ ls  
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos

Thêm tùy chọn \-l (long) vào lệnh ls sẽ hiển thị cho bạn rất nhiều thông tin bổ sung, bao gồm kích thước tệp, quyền sở hữu và thời gian sửa đổi:

$ ls \-l  
total 32  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Desktop  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Documents  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Downloads  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Music  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Pictures  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Public  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Templates  
drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Videos

## **Đĩa DVD của tôi ở cái quái nào rồi? (Where the Heck Is My DVD?)**

Trong Windows, bạn quen với việc thấy đĩa DVD xuất hiện dưới dạng ổ D: hoặc E:. Trong Linux, như đã đề cập trước đó, phương tiện có thể tháo rời phải được gắn kết (mounted) vào hệ thống tệp ảo.

Ngày nay, hầu hết các môi trường máy tính để bàn Linux hiện đại sẽ tự động thực hiện việc này cho bạn. Khi bạn đưa đĩa DVD vào hoặc cắm thẻ USB, chúng thường sẽ được tự động gắn kết và một biểu tượng sẽ xuất hiện trên màn hình nền hoặc trong trình quản lý tệp của bạn.

Dưới nền (under the hood), các thiết bị này thường được gắn vào thư mục /media hoặc /run/media, tiếp theo là tên đăng nhập của bạn và nhãn của ổ đĩa. Ví dụ: /media/rich/MY\_USB\_DRIVE.

## **Hiểu về Quyền hạn trên Hệ thống tệp (Understanding Filesystem Permissions)**

Một trong những khía cạnh quan trọng nhất (và đôi khi gây nhầm lẫn nhất) của hệ thống tệp Linux là các quyền (permissions). Hệ thống quyền của Linux được thiết kế từ thời UNIX để cho phép nhiều người dùng chia sẻ cùng một máy tính một cách an toàn.

Hãy quay lại đầu ra của lệnh ls \-l mà chúng ta đã thấy trước đó:

drwxr-xr-x 2 rich rich 4096 Jul 27 06:50 Desktop

Hãy nhìn vào chuỗi ký tự đầu tiên: drwxr-xr-x. Chuỗi này thực sự cho bạn biết rất nhiều điều về tệp hoặc thư mục:

1. **Ký tự đầu tiên:** Chỉ định loại tệp. Chữ d có nghĩa đây là một thư mục (directory). Một dấu gạch ngang (-) có nghĩa nó là một tệp thông thường.  
2. **Ba ký tự tiếp theo (rwx):** Đây là các quyền dành cho **Chủ sở hữu** (Owner) của tệp. r (read) là quyền đọc, w (write) là quyền ghi/sửa đổi, và x (execute) là quyền thực thi.  
3. **Ba ký tự tiếp theo (r-x):** Đây là các quyền dành cho **Nhóm** (Group) được liên kết với tệp. Ở đây, nhóm có thể đọc và thực thi, nhưng không thể ghi (dấu gạch ngang biểu thị việc thiếu quyền).  
4. **Ba ký tự cuối cùng (r-x):** Đây là các quyền dành cho **Tất cả mọi người khác** (Others). Tương tự, họ có thể đọc và thực thi, nhưng không thể ghi.

### **Thay đổi quyền (chmod)**

Nếu bạn là chủ sở hữu của một tệp, bạn có thể thay đổi quyền của nó bằng cách sử dụng lệnh chmod (viết tắt của *change mode*).

Có nhiều cách để sử dụng lệnh chmod, nhưng một cách phổ biến là sử dụng các chữ cái: u (user/owner), g (group), o (others), và a (all). Bạn sử dụng dấu \+ để thêm quyền và dấu \- để xóa quyền.

Ví dụ, nếu bạn muốn cấp cho "nhóm" (group) quyền ghi (w) vào một tệp có tên myfile.txt:

$ chmod g+w myfile.txt

Nếu bạn muốn tước quyền đọc (r) của "những người khác" (others):

$ chmod o-r myfile.txt

### **Thay đổi chủ sở hữu (chown)**

Lệnh chown (viết tắt của *change owner*) cho phép bạn chuyển quyền sở hữu của một tệp cho người khác. Thông thường, bạn cần quyền của siêu người dùng (root/sudo) để thực hiện việc này.

Ví dụ, để thay đổi chủ sở hữu của myfile.txt thành người dùng có tên là sarah:

$ sudo chown sarah myfile.txt

*(Bạn sẽ được yêu cầu nhập mật khẩu của mình khi sử dụng lệnh sudo).*

Nếu bạn vừa muốn thay đổi chủ sở hữu và nhóm cùng một lúc, bạn sử dụng cú pháp chủ\_sở\_hữu:nhóm:

$ sudo chown rich:users myfile.txt

### **Tụ tập theo nhóm (Hanging out in groups)**

Làm việc với các nhóm thường thú vị hơn làm việc với các chủ sở hữu. Bạn sử dụng nhóm để cho phép người dùng root (quản trị viên) gán khả năng chia sẻ một số khu vực hệ thống tệp nhất định cho nhiều người dùng.

Ví dụ, trong nhiều phiên bản Linux, tất cả người dùng được thêm vào một nhóm có tên là users (chẳng hạn như openSUSE làm điều này). Khi đó, thay vì một danh sách tệp dài như đã trình bày ở phần trước của chương này, bạn có thể thấy như sau:

total 20  
drwx------ 2 rich users 4096 Jul 29 07:48 Desktop  
drwxr-xr-x 5 root root 4096 Jul 27 11:57 Public  
\-rw-r--r-- 1 rich users   24 Jul 27 06:50 .bash\_logout  
\-rw-r--r-- 1 rich users  230 Jul 27 06:50 .bash\_profile  
\-rw-r--r-- 1 rich users  124 Jul 27 06:50 .bashrc  
\-rw-rw-r-- 1 rich users    0 Jul 29 07:48 lsfile

Trong ví dụ này với tệp lsfile, mọi người trong nhóm users đều có quyền đọc (r) và ghi (w) đối với tệp đó (-rw-rw-r--).

Trong các bản phân phối khác (chẳng hạn như Ubuntu), một nhóm duy nhất (unique group) được tạo cho mỗi người dùng (tên nhóm giống hệt tên người dùng), do đó theo mặc định một người dùng không thể truy cập vào các tệp do người dùng khác tạo ra. Đây là lý do tại sao danh sách ở trên cho thấy các mục chủ sở hữu và nhóm giống hệt nhau (ví dụ: rich rich).