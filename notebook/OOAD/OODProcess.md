**Quá trình Thiết kế Hướng Đối Tượng**

(The Object-Oriented Design Process)

**Các Chủ đề**

* Từ Bài toán đến Mã nguồn (From Problem to Code)  
* Nhận diện các Lớp (Identifying Classes)  
* Nhận diện các Trách nhiệm (Identifying Responsibilities)  
* Mối quan hệ giữa các Lớp (Relationships Between Classes)  
* Các Use Case  
* Các thẻ CRC  
* Biểu đồ Lớp UML (UML Class Diagrams)  
* Biểu đồ Tuần tự (Sequence Diagrams)  
* Biểu đồ Trạng thái (State Diagrams)  
* Nghiên cứu tình huống (Case Study): Hệ thống Thư thoại (A Voice Mail System)

**Từ Bài toán đến Mã nguồn**

* Ba Giai đoạn (Phases):  
  * Phân tích (Analysis)  
  * Thiết kế (Design)  
  * Triển khai (Implementation)

**Giai đoạn Phân tích (Analysis Phase)**

* Thiết lập các chức năng, dịch vụ và các ràng buộc của phần mềm sẽ được phát triển.  
  * Các nhà phát triển và người dùng phần mềm làm việc cùng nhau để tạo ra một bản đặc tả yêu cầu (requirements specification), đây sẽ là đầu vào cho giai đoạn thiết kế.  
* Đặc tả Chức năng (Functional Specification) là một phần của đặc tả yêu cầu. Nó có các đặc điểm sau:  
  * Xác định hoàn toàn các nhiệm vụ cần giải quyết  
  * Không có sự mâu thuẫn nội bộ  
  * Dễ đọc đối với cả chuyên gia lĩnh vực (domain experts) và các nhà phát triển phần mềm  
  * Có thể được đánh giá/xem xét (reviewable) bởi các bên liên quan khác nhau  
  * Có thể kiểm thử (testable) so với thực tế

**Giai đoạn Thiết kế (Design Phase)**

* Mục tiêu (Goals)  
  * Nhận diện các lớp (Identify classes)  
  * Nhận diện hành vi của các lớp (Identify behavior of classes)  
  * Nhận diện các mối quan hệ giữa các lớp (Identify relationships among classes)  
* Tạo tác (Artifacts)  
  * Mô tả bằng văn bản về các lớp và các phương thức chính  
  * Các biểu đồ về mối quan hệ giữa các lớp  
  * Các biểu đồ về các kịch bản sử dụng quan trọng (Biểu đồ Use Case hoặc Biểu đồ Tuần tự)  
  * Biểu đồ trạng thái cho các đối tượng có trạng thái phong phú

**Giai đoạn Triển khai (Implementation Phase)**

* Triển khai là việc hiện thực hóa thiết kế phần mềm bằng một ngôn ngữ lập trình cụ thể.  
* Mỗi đơn vị (một lớp đơn lẻ) được triển khai riêng biệt.  
* Kiểm thử đơn vị (Unit testing) được thực hiện để đảm bảo rằng mỗi đơn vị hoạt động đúng theo đặc tả của nó trước khi các đơn vị được tích hợp.  
* Các đơn vị riêng lẻ được tích hợp và kiểm thử tổng thể để đảm bảo rằng toàn bộ hệ thống phần mềm hoạt động đúng và tuân thủ theo đặc tả của nó.

**Nghiên cứu tình huống: Hệ thống Thư thoại**

* Chương trình mô phỏng một hệ thống thư thoại điện thoại (telephone voice mail system)  
* Hệ thống có một tập hợp các hộp thư (mailboxes), mỗi hộp thư có thể được truy cập bằng một số máy nhánh (extension number)  
* Sử dụng văn bản (text) thay cho giọng nói, phím điện thoại, cúp máy  
  * 1 2 ... 0 \# trên một dòng duy nhất có nghĩa là phím (key)  
  * H trên một dòng duy nhất có nghĩa là "cúp máy" (hang up)  
  * Tất cả các đầu vào khác có nghĩa là giọng nói (voice)  
  * Trong chương trình GUI, sẽ sử dụng các nút bấm (buttons) cho các phím

**Giai đoạn Phân tích**

* Tạo tác  
  * Đặc tả Yêu cầu Phần mềm (Software Requirements Specification \- SRS)  
  * Đặc tả Chức năng: Mô hình Use case (Use case Model)  
* Các Use Case  
  * Kỹ thuật phân tích (Use Case, Biểu đồ Hoạt động \- Activity Diagram, Biểu đồ Trạng thái \- State Diagram)  
  * Mỗi use case tập trung vào một kịch bản (scenario) cụ thể  
  * Use case \= chuỗi các hành động  
  * Hành động (Action) \= sự tương tác giữa tác nhân (actor) và hệ thống máy tính  
  * Mỗi hành động mang lại một kết quả (result)  
  * Mỗi kết quả có một giá trị đối với một trong những tác nhân  
  * Sử dụng các biến thể (variations) cho các tình huống ngoại lệ

**Mô hình Use-Case**

**![][image1]Biểu đồ Use Case Hệ thống Thư thoại**

**![][image2]**Caller (Người gọi) \-\>

![][image3]Leave a Message (Để lại tin nhắn)

![][image2]Owner (Chủ sở hữu) \-\>

![][image4]:

* Login (Đăng nhập)  
* Retrieve Messages (Lấy tin nhắn)  
* Change the Greeting (Thay đổi lời chào)  
* Change the Passcode (Thay đổi mật mã)  
1. Mô tả bài toán (Problem Description)  
   Xây dựng một chương trình mô phỏng hệ thống thư thoại điện thoại.  
   Hệ thống có các đặc điểm:  
* Có nhiều mailbox (hộp thư thoại).  
* Mỗi mailbox được truy cập bằng extension number.  
  Người dùng có thể:  
* nghe tin nhắn  
* đăng nhập vào mailbox  
* gửi tin nhắn cho mailbox khác  
* xóa tin nhắn  
* ghi lời chào (greeting)  
  Trong chương trình mô phỏng:  
* phím điện thoại → nhập số (0–9, \#)  
* H → gác máy  
* text → nội dung tin nhắn thoại.

**Đặc tả Use Case mẫu**

Để lại tin nhắn (Leave a Message)

1. Người gọi bấm số chính của hệ thống thư thoại  
2. Hệ thống phát lời nhắc  
   Nhập số hộp thư kèm theo phím \#  
3. Người dùng nhập số máy nhánh  
4. Hệ thống phát lời nói  
   Bạn đã kết nối tới hộp thư xxxx. Vui lòng để lại tin nhắn bây giờ.  
5. Người gọi nói tin nhắn  
6. Người gọi cúp máy  
7. Hệ thống đặt tin nhắn vào hộp thư

**Đặc tả Use Case mẫu \-- Các biến thể (Variations)**

* Biến thể \#1  
  1.1. Ở bước 3, người dùng nhập số máy nhánh không hợp lệ  
  1.2. Hệ thống thư thoại phát lời nói  
  Bạn đã nhập số hộp thư không hợp lệ.  
  1.3. Tiếp tục với bước 2\.  
* Biến thể \#2  
  2.1. Sau bước 4, người gọi cúp máy thay vì nói tin nhắn  
  2.3. Hệ thống thư thoại hủy bỏ tin nhắn trống

**Giai đoạn Thiết kế**

* Nhận diện các lớp  
* Nhận diện hành vi của các lớp  
* Nhận diện các mối quan hệ giữa các lớp

**Nhận diện các Lớp**

* Quy tắc theo kinh nghiệm (Rule of thumb): Tìm các danh từ (nouns) trong phần mô tả bài toán  
  * Mailbox (Hộp thư)  
  * Message (Tin nhắn)  
  * User (Người dùng)  
  * Passcode (Mật mã)  
  * Extension Number (Số máy nhánh)  
  * Menu (Trình đơn)  
* Tập trung vào các khái niệm, không phải việc triển khai  
  * MessageQueue (Hàng đợi tin nhắn) lưu trữ các tin nhắn  
  * Đừng bận tâm vội về cách hàng đợi được triển khai như thế nào

**Các Danh mục của Lớp**

* Những thứ hữu hình (Tangible Things)  
* Tác nhân xử lý (Agents)  
* Sự kiện và Giao dịch (Events and Transactions)  
* Người dùng và Vai trò (Users and Roles)  
* Các hệ thống (Systems)  
* Các giao diện hệ thống và thiết bị (System interfaces and devices)  
* Các Lớp nền tảng (Foundational Classes)

**Nhận diện các Trách nhiệm**

* Quy tắc theo kinh nghiệm (Rule of thumb): Tìm các động từ (verbs) trong phần mô tả bài toán  
* Một ví dụ: Hành vi của MessageQueue:  
  * Thêm tin nhắn vào cuối (tail)  
  * Xóa tin nhắn từ đầu (head)  
  * Kiểm tra xem hàng đợi có trống không  
* Nguyên lý OO: Mỗi thao tác (operation) là trách nhiệm của một lớp duy nhất  
  * Ví dụ: Thêm tin nhắn vào hộp thư  
  * Ai chịu trách nhiệm: Message (Tin nhắn) hay Mailbox (Hộp thư)?  
* Một công cụ thiết kế: Thẻ CRC, Biểu đồ Tuần tự (Sequence Diagram)

**Nhận diện Mối quan hệ giữa các Lớp**

* Các mối quan hệ sau có thể tồn tại giữa các lớp:  
  * Phụ thuộc (Dependency \- "sử dụng" / "uses")  
  * Kết hợp (Association, bao gồm cả tập hợp \- aggregation và cấu thành \- composition)  
  * Tổng quát hóa (Generalization, bao gồm kế thừa \- inheritance và hiện thực hóa \- implementation)  
* Trong số đó, kế thừa ("là một" / "is-a"), tập hợp ("có" / "has"), và phụ thuộc ("sử dụng" / "use") là những mối quan hệ cơ bản nhất.

**Mối quan hệ Phụ thuộc (Dependency Relationship)**

Lớp A phụ thuộc vào lớp B:

Một phương thức của A thao tác trên các đối tượng của B thông qua các tham số, biến cục bộ, hoặc kiểu trả về.

Giảm thiểu sự phụ thuộc: giảm sự liên kết (reduce coupling)

Ví dụ: Loại bỏ sự phụ thuộc vào System.out.println và Message

public class Message {  
    void print() {  
        System.out.println(text);  
    }  
}  
// Thay thế bằng (Replace with)  
public class Message {  
    String getText() {  
        // có thể in ở bất cứ đâu  
        return text;  
    }  
}

* Ký hiệu UML cho sự phụ thuộc![][image5]

**Kết hợp (Association)**

* Kết hợp đại diện cho các mối quan hệ nhị phân chung giữa các lớp  
* Kết hợp có thể có các vai trò (roles)  
* Được triển khai thông qua các trường thể hiện (instance fields)  
* Một ví dụ và ký hiệu UML cho mối quan hệ kết hợp

class Mailbox {  
    private MessageQueue messageQueue;  
}

![][image6]**Tập hợp (Aggregation)**

* Một hình thức đặc biệt của kết hợp  
* Đại diện cho mối quan hệ "có một" (has-a) hoặc "toàn thể-bộ phận" (part-whole).  
* Đơn giản chỉ là một mối quan hệ cấu trúc (quan hệ cấu trúc giữa các lớp)  
* Được triển khai thông qua các trường thể hiện  
  * ví dụ: MessageQueue tập hợp các Messages (Tin nhắn)  
  * ví dụ: Mailbox tập hợp MessageQueue  
* Một ví dụ và ký hiệu UML cho tập hợp![][image7]  
  (Hình thoi rỗng ở phía MessageQueue)

**Cấu thành / Hợp thành (Composition)**

* Một hình thức mạnh hơn của tập hợp  
* Lớp tổng thể (aggregate class) sở hữu độc quyền lớp thành phần (component class).  
* Các đối tượng được chứa không tồn tại bên ngoài vật chứa (container)  
* Một ví dụ và ký hiệu UML cho cấu thành:  
  * Các hàng đợi tin nhắn được chứa vĩnh viễn trong hộp thư![][image8]  
    (Hình thoi đặc ở phía MailBox)

**Hướng Kết hợp (Association Direction)**

* Một số kết hợp là hai chiều (bidirectional)  
  * Có thể điều hướng từ lớp này sang lớp kia.  
  * ví dụ: Khóa học có một tập hợp sinh viên, sinh viên có một tập hợp các khóa học  
* Một số kết hợp có hướng (directed)  
  * Điều hướng là một chiều (unidirectional)  
  * ví dụ: Message (Tin nhắn) không biết về hàng đợi tin nhắn chứa nó![][image9]  
    (Hình thoi rỗng ở MessageQueue, mũi tên hướng về Message)

**Bản số (Multiplicities)**

* Số lượng thể hiện mà một lớp liên kết với một thể hiện của lớp khác.  
  * số lượng bất kỳ (0 hoặc nhiều hơn): 0..\*  
  * một hoặc nhiều hơn: 1..\*  
  * không hoặc một: 0..1  
  * chính xác là một: 1  
* Ví dụ:  
  * Đối với mỗi thể hiện của Professor (Giáo sư), có thể giảng dạy nhiều Course Offerings (Lớp học được mở) (\*).  
  * Đối với mỗi thể hiện của Course Offering, có thể có một hoặc không có Professor nào làm giảng viên (0..1).![][image10]

**Bản số (Multiplicities)**

Triển khai:

* Mối quan hệ 1, 0..1:

public class Mailbox {  
    ...  
    private MessageQueue queue;  
}

* ![][image11]Mối quan hệ *, 1..*:

public class MessageQueue {  
    private List\<Message\> messages;  
    ...  
}

![][image12]**Tổng quát hóa \- Quan hệ kế thừa (Generalization \- Inheritance relationship)**

* Mối quan hệ kế thừa được hình thành khi một lớp (hoặc một giao diện) mở rộng (extends) một lớp (hoặc giao diện) khác.  
* Ký hiệu UML cho tổng quát hóa:  
  * SuperClass \<|--- SubClass (Mũi tên tam giác rỗng chỉ về SuperClass)  
  * \<\<interface\>\> SuperInterface \<|--- \<\<interface\>\> SubInterface

**Tổng quát hóa \- Quan hệ hiện thực hóa (Generalization \- implementation relation)**

* Mối quan hệ hiện thực hóa giữa một lớp và một giao diện  
* Kiểu giao diện (Interface type) mô tả một tập hợp các phương thức.  
  * Không có triển khai, không có trạng thái  
* Lớp hiện thực hóa giao diện (Class implements interface)  
  * nếu nó triển khai các phương thức của giao diện đó  
* Ký hiệu UML cho quan hệ hiện thực hóa:  
  * \<\<interface\>\> Comparable \<| \- \- \- Message (Mũi tên đứt nét với tam giác rỗng chỉ về Interface)

**Phần mềm vẽ biểu đồ UML (UML Diagram Softwares)**

* StarUML  
* UML designer tool  
* Visual Paradigm

**Biểu đồ Lớp UML cho Hệ thống Thư thoại**

\[Biểu đồ hiển thị các lớp và quan hệ:

* Telephone (Điện thoại) \<--- (Đứt nét) Connection (Kết nối)  
* Connection \<\>---\> MailSystem (Hệ thống thư)  
* Connection \<\>---\> (\*) MailBox (Hộp thư)  
* Connection \---\> (Đứt nét) Message  
* MailSystem \<\>---\> (\*) MailBox  
* MailBox \<\>---\> (2) MessageQueue  
* MessageQueue \<\>---\> (\*) Message\]

**Một công cụ thiết kế: Thẻ CRC (A design tool: CRC Cards)**

* CRC \= Classes (Các lớp), Responsibilities (Các trách nhiệm), Collaborators (Các cộng tác viên)  
* Một công cụ thiết kế rất hiệu quả trong việc nhận diện các lớp, trách nhiệm của chúng, và mối quan hệ với các lớp khác  
* Được phát triển bởi Beck và Cunningham  
* Sử dụng một thẻ chỉ mục (index card) cho mỗi lớp  
  * Tên lớp ở trên cùng của thẻ  
  * Trách nhiệm ở bên trái  
  * Các cộng tác viên ở bên phải

**Thẻ CRC (CRC Cards)**

* Lớp: Mailbox  
* Responsibilities (Trách nhiệm):  
  * quản lý mật mã (manage passcode)  
  * quản lý lời chào (manage greeting)  
  * quản lý tin nhắn mới và đã lưu (manage new and saved messages)  
* Collaborators (Cộng tác viên):  
  * MessageQueue

**Thẻ CRC**

* Các trách nhiệm nên ở mức độ cao (high level) mà không quan tâm đến các chi tiết triển khai  
* Lý tưởng là từ 1 \- 3 trách nhiệm trên mỗi thẻ  
* Các cộng tác viên là dành cho cả lớp, không phải cho từng trách nhiệm  
* Ví dụ: Order có trách nhiệm:  
  * Quản lý thông tin đơn hàng  
  * Tính tổng giá trị đơn hàng  
  * Cập nhật trạng thái đơn hàng  
    → Lớp Order có trách nhiệm xử lý đơn hàng và cộng tác với Customer, OrderItem và Payment để hoàn thành nhiệm vụ.

**Làm thế nào để tạo mô hình CRC?**

Một mô hình CRC được tạo lặp đi lặp lại bằng cách thực hiện các bước sau:

* Tìm các lớp  
* Một thẻ cho mỗi lớp  
* Lướt qua kịch bản của các use case, để tìm các trách nhiệm, xác định các cộng tác viên để điền vào thẻ

**Lướt qua kịch bản (Walkthroughs)**

* Use case: "Để lại một tin nhắn" (Leave a message)  
  * Người gọi kết nối với hệ thống thư thoại  
  * Người gọi bấm số máy nhánh  
* "Ai đó" phải xác định vị trí của hộp thư  
* Cả Mailbox và Message đều không thể làm được việc này  
* Giải pháp: Lớp mới: MailSystem  
* Trách nhiệm: quản lý các hộp thư (manage mailboxes)  
* Cộng tác viên: lớp Mailbox

**Walkthroughs**

* Lớp: MailSystem  
* Responsibilities: manage mailboxes  
* Collaborators: Mailbox

**Các Biểu đồ UML khác (Other UML Diagrams)**

Nhiều loại biểu đồ UML

Chúng ta sẽ sử dụng ba loại:

* Biểu đồ Lớp (Class Diagrams)  
* Biểu đồ Tuần tự (Sequence Diagrams)  
* Biểu đồ Trạng thái (State Diagrams)

**Biểu đồ Tuần tự (Sequence Diagrams) (tuần 3\_NT)**

* Mỗi biểu đồ hiển thị động lực học (dynamics) của kịch bản  
* Biểu đồ đối tượng: tên lớp được gạch chân![][image13]  
1. Mailbox nhận một Message mới  
2. Mailbox gọi phương thức add() của MessageQueue  
3. MessageQueue lưu tin nhắn vào hàng đợi newMessages

**Biểu đồ Tuần tự (Sequence Diagrams)**

* Tự gọi (Self call)![][image14]  
* Khởi tạo Đối tượng (Object Construction)![][image15]  
* MailSystem quản lý các mailbox.  
* Khi có người dùng mới hoặc extension mới:  
* MailSystem tạo Mailbox mới.

**Biểu đồ Tuần tự cho Use Case: Để lại tin nhắn**

(Sequence Diagram for Use Case: Leave a message)

* ![][image16]Người dùng nhập máy nhánh (user enter extension):  
  1: dial \-\> Connection  
  1.1: findMailBox \-\> MailSystem  
  1.2: getGreeting \-\> MailBox  
  1.3: speak \-\> Telephone  
* Người dùng nói tin nhắn (user speak message):  
  2: record \-\> Connection  
* Người dùng cúp máy (user hang up):  
  3: hangup \-\> Connection  
  3.1: create \-\> Message  
  3.2: addMessage \-\> MailBox  
  (Leave a Message  
1. Người gọi bấm số hệ thống...  
2. Hệ thống phát lời nhắc...  
3. Người dùng nhập số...  
4. Hệ thống phát lời nói...  
5. Người gọi nói tin nhắn  
6. Người gọi cúp máy  
7. Hệ thống lưu tin nhắn)

**Diễn giải Biểu đồ Tuần tự**

* Mỗi lần nhấn phím sẽ dẫn đến một lệnh gọi riêng biệt tới dial, nhưng chỉ hiển thị một lệnh gọi  
* Connection muốn nhận lời chào (greeting) để phát  
* Mỗi mailbox tự biết lời chào của nó  
* Connection phải tìm đối tượng mailbox:  
  * Gọi findMailbox trên đối tượng MailSystem  
* Các tham số không được hiển thị (ví dụ: số hộp thư)  
* Các giá trị trả về không được hiển thị (ví dụ: hộp thư được tìm thấy)  
* Lưu ý rằng Connection sẽ giữ kết nối với mailbox đó qua nhiều lần gọi

**Biểu đồ Trạng thái (State Diagram)**

Sử dụng cho các lớp mà đối tượng của nó có các trạng thái đáng chú ý.

\[Biểu đồ các trạng thái:

* connected (đã kết nối) \--- extension dialed (đã quay số nhánh) \---\> recording (đang ghi âm)  
* recording \--- passcode entered (đã nhập mật mã) \---\> mailbox menu (trình đơn hộp thư)\]

**Tài liệu hóa Thiết kế (Design Documentation)**

* Khuyến nghị: Sử dụng các comment Javadoc  
* Để trống các phương thức

/\*\*  
Adds a message to the end of the new messages.  
@param aMessage a message  
\*/  
public void addMessage(Message aMessage)  
{  
}

* Không cần biên dịch tệp, chỉ cần chạy Javadoc  
* Tạo thành một điểm khởi đầu tốt cho việc viết code sau này

**Hệ thống Thương mại điện tử**

Mô tả hệ thống: Một công ty muốn xây dựng một hệ thống thương mại điện tử (E-Commerce) để mở rộng hoạt động kinh doanh trên Internet.

Khách hàng truy cập website để:

* xem danh sách sản phẩm  
* xem các chương trình khuyến mãi  
* đặt mua sản phẩm.  
  Để đặt hàng, khách hàng cần đăng nhập vào hệ thống.  
  Sau khi đặt hàng, khách hàng có thể lựa chọn:  
* Thanh toán trực tuyến qua hệ thống  
* Thanh toán tại cửa hàng  
  Sau khi thanh toán, khách hàng có thể chọn:  
* Nhận hàng tại cửa hàng  
* Giao hàng tận nơi (có tính phí).  
  Hệ thống cho phép người bán (quản trị hệ thống) quản lý các đơn hàng, bao gồm:  
* xác nhận đơn hàng  
* theo dõi thanh toán  
* quản lý việc giao hàng.

Yêu cầu

*   
  1. Xây dựng Use Case Diagram cho hệ thống

**Nghiên cứu tình huống: Hệ thống Thư thoại**

(Case Study: Voice Mail System)

**Hệ thống Thư thoại**

* Chương trình mô phỏng một hệ thống thư thoại điện thoại  
* Hệ thống có một tập hợp các hộp thư, mỗi hộp thư có thể được truy cập bằng một số máy nhánh  
* Sử dụng văn bản (text) thay cho giọng nói, phím điện thoại, cúp máy  
* 1 2 ... 0 \# trên một dòng duy nhất có nghĩa là phím  
* H trên một dòng duy nhất có nghĩa là "cúp máy"  
* Tất cả các đầu vào khác có nghĩa là giọng nói  
* Trong chương trình GUI, sẽ sử dụng các nút bấm cho các phím

**Biểu đồ Use Case**

* Caller (Người gọi) \-\> Leave Message (Để lại tin nhắn)  
* Owner (Chủ sở hữu) \-\>  
  * Login (Đăng nhập)  
  * Retrieve Messages (Lấy tin nhắn)  
  * Change the Greeting (Thay đổi lời chào)  
  * Change the Passcode (Thay đổi mật mã)

**Use Case: Kết nối tới Máy nhánh (Reach an Extension)**

1. Người dùng bấm số chính của hệ thống  
2. Hệ thống phát lời nhắc  
   Nhập số hộp thư kèm theo phím \#  
3. Người dùng nhập số máy nhánh  
4. Hệ thống phát lời nói  
   Bạn đã kết nối tới hộp thư xxxx. Vui lòng để lại tin nhắn bây giờ.

**Use Case: Để lại Tin nhắn (Leave a Message)**

1. Người gọi thực hiện việc Kết nối tới Máy nhánh (Reach an Extension)  
2. Người gọi nói tin nhắn  
3. Người gọi cúp máy  
4. Hệ thống đặt tin nhắn vào hộp thư

**Use Case: Lấy Tin nhắn (Retrieve Messages)**

1. Chủ hộp thư thực hiện Đăng nhập (Log in)  
2. Chủ hộp thư chọn tùy chọn menu "lấy tin nhắn" (retrieve messages)  
3. Hệ thống phát menu tin nhắn:  
   Bấm 1 để nghe tin nhắn hiện tại  
   Bấm 2 để xóa tin nhắn hiện tại  
   Bấm 3 để lưu tin nhắn hiện tại  
   Bấm 4 để quay lại menu hộp thư  
4. Chủ hộp thư chọn "nghe tin nhắn hiện tại"  
5. Hệ thống phát tin nhắn mới hiện tại, hoặc, nếu không còn tin mới nào, Hệ thống phát menu tin nhắn  
6. Người dùng chọn "xóa tin nhắn hiện tại". Tin nhắn bị xóa.  
7. Tiếp tục với bước 3\.

**Use Case: Lấy Tin nhắn (Retrieve Messages)**

Biến thể \#1

1.1. Bắt đầu ở Bước 6

1.2. Người dùng chọn "lưu tin nhắn hiện tại".

\* Tin nhắn bị xóa khỏi hàng đợi tin mới và được thêm vào cuối hàng đợi tin cũ (old queue)

1.3. Tiếp tục với bước 3\.

**Use Case: Thay đổi Lời chào (Change the Greeting)**

1. Chủ hộp thư thực hiện Đăng nhập  
2. Chủ hộp thư chọn tùy chọn menu "thay đổi lời chào"  
3. Chủ hộp thư nói lời chào mới  
4. Chủ hộp thư bấm \#  
5. Hệ thống thiết lập lời chào mới

Biến thể \#1: Cúp máy trước khi xác nhận

1.1. Bắt đầu ở bước 3\.

1.2. Chủ hộp thư cúp máy.

1.3. Hệ thống giữ lại lời chào cũ.

**Use Case: Thay đổi Mật mã (Change the Passcode)**

1. Chủ hộp thư thực hiện Đăng nhập  
2. Chủ hộp thư chọn tùy chọn menu "thay đổi mật mã"  
3. Chủ hộp thư bấm mật mã mới  
4. Chủ hộp thư bấm \#  
5. Hệ thống thiết lập mật mã mới

Biến thể \#1: Cúp máy trước khi xác nhận

1.1. Bắt đầu ở bước 3\.

1.2. Chủ hộp thư cúp máy.

1.3. Hệ thống giữ lại mật mã cũ.

**Thẻ CRC cho Hệ thống Thư thoại**

Một số lớp hiển nhiên:

* Mailbox (Hộp thư)  
* Message (Tin nhắn)  
* MailSystem (Hệ thống Thư)  
* MessageQueue (Hàng đợi Tin nhắn)

**Thẻ CRC ban đầu**

* Mailbox: giữ tin nhắn mới và đã lưu (Collaborators: MessageQueue)  
* MessageQueue: thêm và xóa tin nhắn theo thứ tự FIFO  
* MailSystem: quản lý các hộp thư (Collaborators: Mailbox)

**Điện thoại (Telephone)**

* Ai tương tác với người dùng?  
* Telephone nhận thao tác bấm nút, đầu vào giọng nói  
* Telephone phát đầu ra cho người dùng

Thẻ CRC:

* Lớp: Telephone  
* Responsibilities: nhận đầu vào của người dùng từ bàn phím, micro, cúp máy; phát đầu ra

**Kết nối (Connection)**

* Telephone giao tiếp với ai? Với MailSystem?  
* Điều gì xảy ra nếu có nhiều điện thoại?  
* Mỗi kết nối cần theo dõi trạng thái hiện tại (đang quay số, đang ghi âm, đang lấy tin nhắn,...)  
* Có nên để hệ thống thư theo dõi tất cả các trạng thái kết nối không?  
* Tốt hơn là giao trách nhiệm này cho một lớp mới (Connection)

Thẻ CRC:

* Lớp: Connection  
* Responsibilities: lấy đầu vào từ điện thoại, thực hiện các lệnh của người dùng, theo dõi trạng thái  
* Collaborators: Telephone, MailSystem

**Phân tích Use Case: Để lại một tin nhắn**

1. Người dùng bấm số máy nhánh. Telephone gửi số đến Connection  
   Thêm collaborator Connection vào Telephone  
2. Connection yêu cầu MailSystem tìm Mailbox tương ứng  
3. Connection yêu cầu Mailbox cung cấp lời chào  
   Thêm trách nhiệm "manage greeting" (quản lý lời chào) vào Mailbox, thêm collaborator Mailbox vào Connection  
4. Connection yêu cầu Telephone phát lời chào  
5. Người dùng nói tin nhắn. Telephone yêu cầu Connection ghi lại nó  
   Thêm trách nhiệm "record voice input" (ghi âm giọng nói) vào Connection  
6. Người dùng cúp máy. Telephone thông báo cho Connection.  
7. Connection khởi tạo Message  
   Thêm thẻ cho lớp Message, thêm collaborator Message vào Connection  
8. Connection thêm Message vào Mailbox

**Kết quả Phân tích Use Case**

* Thẻ Telephone:  
  * Nhận đầu vào... (Collaborators: Connection)  
  * Phát đầu ra  
* Thẻ Connection:  
  * Lấy đầu vào... (Collaborators: Telephone, MailSystem, Mailbox, Message)  
  * Thực hiện lệnh...  
  * Theo dõi trạng thái...  
  * Ghi âm giọng nói...

**Kết quả Phân tích Use Case**

* Thẻ Mailbox:  
  * Giữ tin nhắn mới và đã lưu (Collaborators: MessageQueue)  
  * Quản lý lời chào  
* Thẻ Message:  
  * Quản lý nội dung tin nhắn

**Phân tích Use Case: Lấy tin nhắn (Retrieve messages)**

1. Người dùng nhập mật mã.  
   Telephone thông báo cho Connection  
2. Connection yêu cầu Mailbox kiểm tra mật mã.  
   Thêm trách nhiệm "manage passcode" (quản lý mật mã) cho Mailbox  
3. Connection thiết lập hộp thư hiện tại và yêu cầu Telephone phát menu  
4. Người dùng chọn "lấy tin nhắn".  
   Telephone chuyển phím bấm tới Connection  
5. Connection yêu cầu Telephone phát menu  
6. Người dùng chọn "nghe tin nhắn hiện tại".  
   Telephone chuyển phím bấm tới Connection

**Phân tích Use Case: Lấy tin nhắn (Retrieve messages)**

7\. Connection lấy tin nhắn đầu tiên từ hộp thư hiện tại.

\* Thêm "retrieve messages" (lấy tin nhắn) vào trách nhiệm của Mailbox.

\* Connection yêu cầu Telephone phát tin nhắn

8\. Connection yêu cầu Telephone phát menu

9\. Người dùng chọn "lưu tin nhắn hiện tại".

Telephone chuyển phím bấm tới Connection

10\. Connection bảo Mailbox lưu tin nhắn

Sửa đổi trách nhiệm của Mailbox thành "retrieve, save, delete messages" (lấy, lưu, xóa tin nhắn)

11\. Connection yêu cầu Telephone phát menu

**Kết quả Phân tích Use Case**

* Thẻ Mailbox:  
  * giữ tin nhắn mới và đã lưu (Collaborators: MessageQueue)  
  * quản lý lời chào  
  * quản lý mật mã  
  * lấy, lưu, xóa tin nhắn

**Tóm tắt CRC**

* Một thẻ cho mỗi lớp  
* Trách nhiệm ở mức cao  
* Sử dụng các bước lướt qua kịch bản để điền vào thẻ  
* Thông thường, thiết kế đầu tiên không bao giờ hoàn hảo.

**Biểu đồ Lớp UML cho Hệ thống Thư**

* Các collaborator trong CRC tạo ra sự phụ thuộc (dependencies)  
  * Mailbox phụ thuộc vào MessageQueue  
  * Message không phụ thuộc vào Mailbox  
  * Connection phụ thuộc vào Telephone, MailSystem, Message, Mailbox  
  * Telephone phụ thuộc vào Connection

**Mối quan hệ Phụ thuộc (Dependency Relationships)**

\[Biểu đồ UML thể hiện mũi tên đứt nét (Dependency):

* Telephone \---\> Connection và Connection \---\> Telephone  
* Connection \---\> MailSystem  
* Connection \---\> MailBox  
* Connection \---\> Message  
* MailBox \---\> MessageQueue\]

**Mối quan hệ Tập hợp (Aggregation Relationships)**

* Một hệ thống thư có các hộp thư (mailboxes)  
* Một hộp thư có hai hàng đợi tin nhắn (message queues)  
* Một hàng đợi tin nhắn có một số lượng tin nhắn nhất định  
* Một kết nối (connection) có một hộp thư hiện tại.  
* Một kết nối có các tham chiếu (references) đến một hệ thống thư và một điện thoại

**Biểu đồ Lớp UML cho Hệ thống Thư thoại**

\[Biểu đồ đầy đủ:

* MailSystem \<\>--- (\*) MailBox  
* Connection \<\>--- MailSystem  
* Connection \<\>--- MailBox  
* Connection \<\>--- Telephone  
* Connection \---\> Message  
* MailBox \<\>--- (2) MessageQueue  
* MessageQueue \<\>--- (\*) Message\]

**Biểu đồ Tuần tự cho Use Case: Để lại một tin nhắn**

* **![][image17]**1: dial \-\> Connection \-\> 1.1 findMailbox \-\> 1.2 getGreeting \-\> 1.3 speak  
* 2: record \-\> Connection  
* 3: hangup \-\> Connection \-\> 3.1 create(Message) \-\> 3.2 addMessage(Mailbox)

**Biểu đồ Tuần tự: Lấy tin nhắn (Retrieve messages)**

* **![][image18]**Người dùng nhập mật mã (user enter passcode): 1: dial \-\> 1.1 checkPassword \-\> 1.2 speak  
* Người dùng nhập 1 (lấy tin nhắn): 2: dial \-\> 2.1 speak  
* Người dùng nhập 1 (nghe tin nhắn): 3: dial \-\> 3.1 getCurrentMessage \-\> 3.2 getText \-\> 3.3 speak  
* Người dùng nhập 2 (lưu tin nhắn): 4: dial \-\> 4.1 saveCurrentMessage

**Biểu đồ Trạng thái của Connection**

\[Sơ đồ luồng trạng thái của Connection:

* connected \-\> (extension dialed) \-\> recording  
* recording \-\> (hang up) \-\> connected  
* connected \-\> (passcode entered) \-\> mailbox menu  
* mailbox menu \-\> (hang up) \-\> connected  
* mailbox menu \-\> (1\#) \-\> message menu  
* message menu \-\> (4\#) \-\> mailbox menu  
* mailbox menu \-\> (2\#) \-\> change passcode \-\> (passcode entered) \-\> mailbox menu  
* message menu \-\> (3\#) \-\> change greeting \-\> (greeting entered) \-\> message menu  
* message menu tự lặp: (1\#, 2\#, 3\#)\]

**Biểu đồ Lớp cuối cùng cho Hệ thống Thư thoại**

\[Sơ đồ Lớp chi tiết bao gồm thuộc tính và phương thức:

* **Connection**: \-currentRecording, \-accumulatedKeys, \-state | \+dial(), \+record(), \+hangup()  
* **Telephone**: \-scanner | \+speak(), \+run()  
* **MailSystem**: \+MailSystem(mailboxCount), \+findMailbox(ext)  
* **Mailbox**: \-greeting, \-passcode | \+Mailbox(), \+checkPasscode(), \+setPasscode(), \+addMessage(), \+getCurrentMessage(), \+removeCurrentMessage(), \+saveCurrentMessage(), \+setGreeting(), \+getGreeting()  
* **MessageQueue**: \+add(), \+remove(), \+peek(), \+size()  
* **Message**: \-text | \+Message(), \+getText()\]

**Xây dựng sơ đồ Use case cho một hệ thống thương mại điện tử (ECommerce)**

* Để mở rộng hoạt động kinh doanh của mình, công ty mong muốn xây dựng một hệ thống thương mại điện tử nhằm mở rộng phạm vi kinh doanh trên mạng Internet.  
* Hệ thống mới phải đảm bảo cho khách hàng viếng thăm Website dễ dàng lựa chọn các sản phẩm, xem các khuyến mãi cũng như mua hàng  
* Khách hàng đăng nhập vào hệ thống để đặt hàng và có thể thực hiện việc thanh toán qua mạng hoặc thanh toán trực tiếp tại cửa hàng.

**Xây dựng sơ đồ Use case cho một hệ thống thương mại điện tử (ECommerce)**

* Khách hàng có thể nhận hàng tại cửa hàng hoặc sử dụng dịch vụ chuyển hàng có phí của công ty.  
* Người bán hàng (Hệ thống) có thể quản lý đơn hàng như thu tiền, theo dõi chuyển hàng.  
* Yêu cầu:  
  * Xây dựng mô hình Use Case cho hệ thống trên (xác định actor, usecase, ....)  
  * Xây dựng mô hình hoá hiện thực cho một chức năng cụ thể trong hệ thống với một chức năng tuỳ ý.

**Bài tập Quản lý Học viên**

* Một trung tâm tin học muốn quản lý các giáo viên, học viên của mình. Thông tin của mỗi giáo viên bao gồm: tên giáo viên, ngày tháng năm sinh, học vị (cử nhân, thạc sĩ, tiến sĩ). Thông tin của mỗi học viên bao gồm: tên học viên, ngày tháng năm sinh, giáo viên chủ nghiệm. Mỗi học viên sẽ đăng ký học một số môn học và phải thi cuối khóa. Thông tin của một môn học bao gồm: tên môn học, số tín chỉ, giáo viên giảng dạy. Sau khi kết thúc khóa học nhà trường sẽ đánh giá loại tốt nghiệp của học viên dựa trên điểm trung bình các điểm thi các môn học của học viên.

**Bài tập Quản lý Học viên**

Yêu cầu 1: Cho Use case: In bảng điểm cho sinh viên

1. Hệ thống hiển thị thông báo:  
   Nhap ten hoc vien:  
2. Người dùng nhập mã học viên muốn in bảng điểm  
3. Hệ thống tính điểm trung bình cho học viên dựa vào kết quả điểm số các môn học của học viên như sau:  
   Điểm ![][image19] (Điểm môn i \* Số tín chỉ môn i) / Tổng số tín chỉ các môn học  
4. Hệ thống xếp loại tốt nghiệp cho học viên dựa vào điểm trung bình như sau:  
* Điểm ![][image20] xếp loại xuất sắc.  
* ![][image21] Điểm ![][image22] xếp loại là giỏi.  
* ![][image23] Điểm ![][image24] xếp loại là khá.  
* ![][image25] Điểm ![][image26] xếp loại là trung bình khá.  
* 6 \> Điểm ![][image27] xếp loại là trung bình.  
* Điểm ![][image28] không được tốt nghiệp.

**Bài tập Quản lý Học viên**

5\. Hệ thống in bảng điểm cho học viên theo mẫu sau:

Họ tên:

* Ngày sinh:  
  STT Môn Điểm  
* Điểm TB:  
* Xếp loại:

Yêu cầu: Hãy hiện thực use case trên:

* Nhận diện, thiết kế và cài đặt các lớp cho use case  
* Thiết kế các ứng xử trong use case và gán cho các lớp  
  a. Tính điểm trung bình cho học viên.  
  b. Xếp loại tốt nghiệp cho học viên  
  c. In bảng điểm cho học viên.

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAlsAAABICAYAAADBGDBtAAAFPElEQVR4Xu3cTYhWVRgA4Bk0KIp+oMFyfu73jUMgBRHTD4TtlJKohRIEumtRi1YFBe0iXEQ7ESoQqkUEIUGLaJGLaBW5aZEUgqASuQiJAgONtPf95tzxzJlRG2vGoOeBw/3Oe9977v12L+ece8fGAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAgOttbm7u1sFg8EQbXwsTExO3DIfDLlt7biXz8/M3tDEAgHXRdd3FVbTj7fXFeJ/Tnvi3xT2+iPZn3mtmZma+Pd/KQqs82y/tOQCANRUFyNa2CIkCZrYUJ4fq+GAweDPaB3WsF7k/RTsfP8fbc2shnvHVUthd8X5TU1M3Zd7s7Oxt09PTD5VnBABYH1lQDYfDTU1sX5k12lbHo/9UtjqWIvdAtCNtfC3F/U5EO9vGW1FgPRiHDX0/isW7svCqUgAA1k47q1Vip1eaNSpF2N117HopxeB7bRwA4L8k91ltbYNZyET7fYX4o20sRdGzN9qpwWDwSHuutmnTpptjjEPRjkf+9j4e/d3RfsgN9tnfsmXLdPS/jXY4lwEvjbAgZ+JKsTVfZttORXtn7PJLihvi2d6Na75eaby8b94/n6OENsR47+dzXu0/AQCsSrVf68P2XKvfDxUFyePZj99vlGuXbaKP2PdZFI0tFERZ5J2M654tBdMr0d9Trv08+jvymiziMlauqcd6qeSen5ycnMpYjPVV9M/VeSnGeCZz+yIrfp8t1+7sc7qF2b2NJf5cjPVpxvuN9ev1hiUA8D8QxcX+LDByM3l7rlUKkY/bWLR9dSwKnmNdVQjNlM3tWWzF8WgdGw6HD1d582W8JUuX0T+e8fpzDtF/LWNN3gMZi0Jrro/lTFjG4nhH6W/Plp+SKPc6fGmExf+44ksBAACrFsXFmVK0XG5JbqRb2BQ/esuvj/WzYnmsYjtKbHHZMEUBc3se49yT5Xgi2m91Tl+AjS2f2cqiaMmbktE/0jVLn9G/0DWzXXldGXOkLBOOR3H5dMZzqbM/1xdgea6PAQD8I6WQWbZfq1XyLjSx0VuMTSyLqKt+e6uMd7CJ5Ub9M3Vs8+bNd5YCaMnMW7n+QN/vC79o+5u8P7oV3pyM2Jftc3ZlaTMKshvrOADANekWvrmVBcpV92uVvM+aWBZHp5tY5l3xEw1TU1OTmTccDu/vY1nglELn+To3+xkfq2a7+uXG+hMW/XJht/QFgH5f1p4qNlLi7RJizvItKfYAAK5Zt8r9WrnM18a6sl8rjifKMWeSTtZ5xXi/ub1aLlwU/RdLbLy8fTiaoYrj0W75cmHGRrNscdwTz39fHHfm9bkU2OfFfbZlLPdr5e9+ebDar7W4ab7f/N/ndD6GCgD8U1FQnCsFzsb2XCvyfuyqfVPx++dSyMxHgfJY/wZfHF8oYy4qn1q40G9w7xY2vC+ZQeoWlvVGsRjzWJV7sWtm3upYd2nf12gWq98/lnvLSt7oWeK5vhkrs2NdKczq5cJ+tqzMsO2O/t7+HADA39aVN/su0z5q8yv5+YZfS975LIaiIHm79L+rE2cWPu2wOG4UMK/X50v85ToWBdlElT/IWPlOVxZQ99a5EdvV59ZvKEaBdU91309K7vnS31Vdf7Bb+eOuowIy2lvtOQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABgXfwFr9N/NhWx4z8AAAAASUVORK5CYII=>

[image3]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAlsAAABICAYAAADBGDBtAAAE0ElEQVR4Xu3cTYiVVRgH8BENiqIPSiadufPeGSbCiiAmgqJ2EUW5qY0UQdDCZVBQ4C7ERbQpiwILokUEoYsWUoSLqE3kQjeRiwSJUFqEm1qoaD2PnjMejzP50RBT/H5wuPc8z3k/ZvfnvO/ciQkAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADgf2jNeDzeOgzDoRgHp6en52sj5jubdQAAq1cEl8Mxfo/xZxlHM9zU/szMzPMxP932IwTd3J5jJUWoui6ucTKvFdd5Y2Fh4Zqsx/ydGPti7IrxQ38cAMCqFYFqrgSpvX2vyn5fW2lxH4+W+9jT91LUPywhbGvfAwBYtSLAbMsQk2Gn76XJycnro3+sr6+k2dnZB0rQ2tX3qlgzmWs2btx4W98DAFi1IsD8Unau1vW9VHactvX1lZKPCkvQOt33WuvXr7+h3CcAwH9HCTqn+noVvb3T09NTfb0VgeylGD+Px+O3Y7qm74e10Xs91+TathHn/y7vYTQaPdLWeyVsLfm+VtQfGs69TP9s32tNTU3dOpx79+tQ3MdC309xn+Oy5mCMDX0fAOCyZYgqYWt336uid6avtaJ/enZ29t78Xh71/dr19+SafByZ88gyL0TQ+ai015XrX+2O1Zo49mQGuZzE9R9b7nxReybG4Wa+P9bfWefl5fw89r1mzYkMeXUOAHBFIvS8lgEjPh/ueylCzLXRP9LXq/LzDH/UeX6P8Vszzx2iDD6Lu12j0eieoYS7+HyiBJwld6wuJY47HuNoV8vz7W9rtV53s/KzrNuU8/ooM/6ez7pjfoy1t7Q1AIDLFmHiSIaMib95XysDWV+vIpx8XELLgVh3d9urL7TXXawMNCWcLYavobycP1zFb2fFuR4vxz7YlOtO2XNN7axSz/t5tf6kRBW1L7NXd7Hi+4bh3N/0frsOAOCKlACy7GPC4RLva83Nzd1UQ0wdEyVI1V2zGJ/kY76Yb14i5NSdtWUDXZGPCy/Y/Yr5sXK9RblDV8530W7UUHbZ6og1bzW9rJ2JsSvudUv8zXe0xwIAXJUSMr7t61UGkL62jLWx9oMSYjZnoe56TSyza5Zmzj/O29H3WtHf3v6KfKnlcYuPLEttd7nmsqK/qRy7uK7ML3r0CADwj5SQ8XVfT/n+Uv7+VV+v+sDS1M6+BxWfL/f9Kh8B1u/lmBNtvxX3MMT6r/r6Uvce81NDCU31nPH5Yq6tIbDUnh4ufLfsonOlfKm/340DALhs+Sgtg8ZE93MNEW4+j/orba2Xx+V//zXzJ2Mcr/P60vkSO1I/jUaj++s8v5ews69dl+L+nop7+aavp1j/6dD82Gp8/yLPk48ky088vFvqO/Ka5488F8TaIBnz7Vlr18R1x1E72dYAAK5YBIo3S9hZHBFWpvt1vVh3X3tM7oT1a6J2e7fm+yiv7dfNz8/f2K6rI4LTXf3aVp6vOXdeK3escn5BSIr5gfa8S/19Ud/ZronzbenXAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAD/mr8AjtlRSJPE760AAAAASUVORK5CYII=>

[image4]: <data:image/png;base64,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>

[image5]: <data:image/png;base64,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>

[image6]: <data:image/png;base64,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>

[image7]: <data:image/png;base64,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>

[image8]: <data:image/png;base64,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>

[image9]: <data:image/png;base64,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>

[image10]: <data:image/png;base64,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>

[image11]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAlsAAABVCAYAAAB+UCEoAAAXrElEQVR4Xu2df6wtVXXHzws0oekPiy0+y+PNmvvuSwnSn3lWA7TBWFCJtWkEIyoaEtq0oSZNNGgx/oEh/FHbGkJsTa1GSEM1lVobRE1L2ltNKip/vCa+QhRSaGhNMWJqgAAGXtd3z1pz1qzZc855754L716/n2TnzKy9Z8+e/WPttX/MnNmMEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYSQU4MjR478SNM0v5vlhBBCCCFkDbRte4OIHFd3efYjhBBCCCFrQA2t98PgOnTo0IuyHyGEEELInkMNn6P6c5r+Ppf9doqDBw/+qt7v2SwnhBBCCNmTYJapaZr3ZDkhhBBCCFkDIvKnWUYIIWRvo4Psi84555wfzXJCyMlzWhYANbTuxB6qgwcP/nr2O1natr3aNsI/kf0ieDsxy05V9FmeVveIKqf/codn1Gd9ZQ671znrrLN+fGNjQ1RJ/0L2I2Qvo+3+Km3398Np239d9t9N6DNcru6jWU7IqYLaJS/XOnq39bfvVtG+HGbtHDp06Ofshs+aIfN47vit87+4cu2LzP/hKN/c3HwJ4tNrboN/9NsuGt8jssDYUr/v4J779+//sST/J3WP+vOoewzP5/7IB5U9Hv2zwaOyC2OeqPtB9M9o2PeGsDCo/jWHASo/08L8T/bbSfR+9+KeIY1vy2Ei6v+ch0U+qGH0SznMKni9gWHlMo3vs2L5r8eXxPBaDmdYvnv5PFuro+qui9eR55dURijHM3MYB4Z1KLeic1R8eg6319G6/TXLq5eZaJ/L9PelMexu4MCBA+do2p/OcrJ+NJ+/JaFP0zr0azlMJLS3oj9RVjnMXkef+z3Wtq52mR7/keXfO0LQnUNvtoUbzioKT6yThYJMXvtUfn/FsPkPP7ZN6zdG/xNFM+ENoaJE97MxnJ5/T93rMX0N/8qbiafbdd9N8h7pjKLJTgJomAfVfQVxZT/H0vAxhNH4PpH9I5pHv4VwWui/l/12GpSd3vuY3f+27O/oM9ysYT6JcJV6cEJ4vuTGrrK3WTrOiHKnMeNVfw9lP5XfZ35Hsh95/tAyuCzU+8myMMPs+wiX/X4YsHZ3XN1fZz+g8m9Y3uz8iHuNaJqfUH3281lOdgYdsO5Xffkla2/vzf6OdCtN/7Ib69S6kM4++F6WA83D30feaL99OPutHWv41ZkaMUNskfJ8vrC0jGa2sHSYMmofjLRw7oYfnvOWKI9YZVyIdMbn+xB2yjCQrvNHx7M03zTM3Qh39tln/0z222k0bZfAyLN8OZb9AYxWDXO97HDnqHF/HXmb5Y50Rm71/sEQm1Q4ZOfRMrhL29kmymJq8KDyN6trrc5tZf+9DnSV5c/Xsp+j/ufttvoMI2uqfZKdAW0MOtza0l3ZH6Ctoc1ZmFHf+cOAdIbWwrpp+fNQlq8VLYgz7EZ3ZD8gNrM1q8x61Thw4MBPa/gHcM2yWZ1l2Nfhv2rp+yuZMLZWQa+73dI0mhkBMHbU/8tZHrEwd4kZUpJm14DGf6m688WMqNmSkYTFs7Ai7BR4FnsmGFLVfMUsBH4tnVvJe21Y/FWFAcz/21kOxGa21G1kP/L8IWYsoyza+kwpZsPvxBI0wmBWNwfY6+hzP4Fnny3QC2GZdbBF41RGOt1c7UPIzqD5fSz039W6Av3tM6nb7Y93I3hme/bzs1/E8nBn+2G3jJvKmq/KP2qJeL3LbM8N9ng9rO7uGF7jeHsTPvcgyaIM196fr5Wuw+xl2NNj1xalZAYM0lI1CswwuxWVS90fZn9cF9OSwShhmfL3kYTtTUBaLktBsOfiSzhYlFYnLCd8Pfutglj5VJZMV0LmneOXa3mDERGGRSt2jqdp0L/UcPdMvYmkfp/T/PtUlje2bw15m/2AGYTIp5uyn3QbcuFXffvV8vgO1Av9fWv2P3z48E8izag7JsL34e5R9+cxHFmMKf0yO2rl8WAlDNoGDK6y1LhkSRr16QNT7RmgbJtuv9+DU3VH5S9T/6NWpqPBEdAwV+E+7fIXU05DPUF8U3UcaJg3WZpunQWjSuO/0vLmw/PQY4Kx1esPq8fQm9fGsEDGeqiAMkGbtLrf63CgsrcjPtT/KLf2UM0n6WbckI/35OuQ3qkyWAOoMzeF9OL8dvfU4+ukUiZ4jpxOZ6qMbObxKOrePHTHyeTzBFh5+Y0sPFFkrr+xl7mmv6+3PnelVZapPAkUHW/PeU32BKu0SfW7ULq6PNLHGZQD4pKJOglkol6GfeXV5cOIhRvkoUz3V7CVavmDevlu5E/2KEg3U3N8c3PzIB4IDpkknVH0aKUCP2W/ZSkteJU9UeG8JAqy1pYUxJYqpWs4+cEGSw84V3dBCvNtqRgw0s0iQV7ejtTjG2X4gVNkAuKrzowA9Tu2RPmXMGhYwUh6X/K/U3/2rTqSkPkM2cLN6VPodd+166tKYBF4DjwPjsU6v9mwApVZiOg/lT/WSLHmXeqKmGEb0yVd2SNO+A1GwLJkvxbqhcV3gVgdtWULbBBFPa02RJXfZxXfDfZPSWh40hlqH8Jx2021Iy74I50YTIyMO1IHOiO0c8yUPpn8z1d3afAfdQ6O+v0dysL3g2q8V+e2tLGx8QovK7vm0xruVTGMdIOR2Ck/FeuY7+9U2WvNH3rjuFQMRen+pQI6BToG9aO8VLQRXhTx/Zcq+0Wcq+I/S4K+ku7t46WDI8Rp6SizFfbNwm/iGHJT9gWp6FKAem9133XiHT5Yki5f8MJPWX6P11n8g7zWfHox5JpP15uo6FP82rnvh622w+0gXZs/7p2o2ABerG3q793YQtJ2L2QNtsLYswyWYheVkRlaRT/YPXq9jGPIZkMduTCfpxDbEqHuXdlvVXyVBccyX0XpQd3WdN2c/GsGwsI8cdxwCTr+d9T9WQyzQptEvXmmNUNWw7/G8mFUf1X2arvfi3GO+m9h+zxbVi/F9hmr/5V+zRQ5HdLVJQy8B/2VpuOQpeuAy4DKPgQ5VvaifIB0y4Q/EOvE3LX2Vky0FHEjr7zSKY77QjxuONTc1qJrXbn4viUv/FmqHIhHUiWQSkXzkWFjlrX+HrF0THaeOY4aEvYUWXz9TFzb8WbzK3mB53L/Gp72Zsmm/EUsLNwFIG/aeef4RkvvfvdvbRbC/Cc7R5X/CvzinrnGXmrw50JlFzOcTT5Q5rJ8v9YxXCepjkq3tIz4/G2uHmucgzej7BrEc96s6yC+5X5eR6ye+ksZ7wyXkwWILUnb8WimVIa6Ank7mNl2ILdr+7ZvhnU20J9DOdlxKVdv76C15RUfIED34BzyEAfO/9bPXSZJT4jNnkYjSc//wNJZtld4mLx3VMwA8PTYNQvB/S1s2V+qv/foz+lQ8CZH/fWwGIA+0l/cyWCQ5Lr/TumMB9R7xAfZloR2h/aK+LG/1WVhdmDwohPuMZs/e8n/qcHYyeIrCAfDJ4R87y3aqaXtk5Dr70MSXn6CP8LFF3FkSRkhLsSZ+w/zg44aDCCQBzKdz5OI6VvZhnEK3e3pE5v4iC+rybi9fd/PI7IkTxzpJhpuC+eIc7D/WZa0Senya/DWvcUzWNnZsFUtCZMtvicQ5YrzFevl1Mt9A7yuiNWf3F9JeE6pDG7EVpgWfnYqKIDqWrvYSGyW9muFZZ0+MywRo1mnjDfoVAg+s+Lnd8TzIN+K9/ACQMWL4cI0fMmkZr5uu2i/1laWR+JIAlj8vZJrwtShVDqMGhbH6DkBykbj/GKWrws8i3eObuy6km3CLISFRTq3/DwiXYXOCmdQfnp8of2WUWp+GcDi7/M2Y/7VWUnppo/LzKzLNO9eB1msYxa2KADUF4yK4uhE5bfENC9D4/gpi2+pW9UgztctcrPldWt0zZSbLYlrFWQ4EBnMlGo53Owj4lDXRqN/GPvwQ3vFOZQXyirG5UBm7ia0lehn/ng2+ONV96tm4+s/DP9oQLnSzXrC4skGDTrfvkOyMHEWC0sl/SdOgkIfzZplxPSutxPUZ5OXkXoKizj7GXav+56/pgtRt7+Dc3TIwSjGtf2SplRmb8T2Q7pM86uRbtYX3ycq+LP5eUYqdW7KzcK3G6WysVlCO8VzmIHhM2v94EjqnSLCTJaR57P+3mDXxnzAtf0s6bJ83mnEVlnsuAzu3bCE7oYOx/GyVZZleRLkZbVC47l1Sp9ZXHCjNun5JcPVKi+3gXEq9XIflKesUC8t7sl66ch8BswnHwb9FfRSCDsY3ECv2X22TIStBm9y/x50RgjYVPZrAURg/oO1Xk9clDWVKekaUm8EmDnplZCYsZILzNITKwYU3igcnsfknnlr26/l59IVbIlTf29Mo97jMZ01gkF4LPsBNPis9NeJhM4xjOR85nE041PLn9CB5BEOZkpH+9CkayCDfDn33HN/wu49MIycRfu1gNc7TzuQrkGMylusM6ndS7ol2UGHuoiWxlYP2p+EetzMZwbLs7fzaf5+4FMbbXpZqru97fZrvWFqtCjz/aTuypJ3CuNLTsU14wHEYDZVKrrJZ1Jclzh2fRmkSpePOL9X3V/ofa5A/Yjhwz7PrSjP2HYOhPtG9ov3BN7+op5A/BYO+XNt2y3jjMoXbcCu7WfVJRmQJkNcTyM+PBc6tegP/Nmy3JFKnZtyMzO2kC6792AQJl07HQy8UDYIOwuTAggTw1n8iG+yjBzpBpC9/vK0NMPl25XyeadAGsNxeTa0Fz3d19q+YeCrRE1lv5ZfJ6vlie+NdTcyKmVBm5SKTkZ+QhbroPcHMi73XJ4Is7BeWpjJeulMhZNuRaXWHvq+CHlusr9X90HNv9+GPozXFMT2a1U9Z8UfneZoj4FFXqZv9WZftV9fqht9V0vjv8GPpTNSBo0F1zXWWervZ73xtOlryjI2tqpGlNhzhfVlpGswBRyRsM48hYSRhJ2Xe5ih0j9zMFw+4bIa3gjwrNlP8bXnHQHPgeeJMssjbCT/SOzg8Bz+nDG8+XlF65c1ZhOjFZfn5xWbUp+qg14X0j16xAxuGc6y4nw0bS62HDmrlLVdM9iDR1ajCUvSAGWF/IQybdJmUZlos6Cdfwh5MJO+CL2m1WuemYoTQI9Y+T7sMjtfqNAB9BLCxtEtOgd/Pjv3JejqoBWEfZ7VwZUj9mHmWaqjvoSIe7lMKsahhEHgIsSMhSRD+vJy7UiWEeu0azriZAl5mmenkZ68zPuQjLeXDMKtUkbA9XccXMp8xi8acyvl806QV1lMn5fn1eN/nA1n5LycRzpv1TyJ2PLdA7huqrxrbdLSN/jGpVRWsDxNkvYhm6wvTztfVi8RZmEZNd03JJEHo7cVTd73401lcNPMB/uLtwJZYqp7ZWRuyQ72VmzYMgCUj23C65e6ZP4l+n9Gh40wevzMbFj4UGi90sN6PK7B6AjLgqa0i7EB5waTXTv41pLFlWeQ/Nr+LyNk8acN8CbS0j/MlpRPnsnqHo/yRSOJiFgjyEtqs25THirqwjeWABoW4sgfCF1GkzpHYM+C8uunYU0+2TmKTV/HRoeGa89/Jo5daUm3l6EoLP3daM0Al25/j79VswV/j8tkk9/X2piv7Q/eNpFukNDXMeDfN/KyRh7YteehrMwvzhCUfTJ9BGQSCUvSIMzaPpbqprfNrSDrUfm74J/lAAaT/b7KyqqfybTZpzjSxygT98FMicvw6Ze+g8pxuExMoYt9c6exAcVsqMNKXUYnh3PTc9U23wxn0/rlEeu0nlT3cZm/iFJmBtrK1+M9HbGtSaf/Sgfm6ZXKHlanCXsbpWvXfRtBe7VnuMTKz2ftkJ7bPJxjaSx5gnxAOAn5vV28n4lxon1aGmvLvFt+7uHUnWdG6k2rlpHrgnhfCXtK7T7QYSvlcw1bevpglq8KdDfKKcoszU/lFQiTV/u+VfLEPuWEOLbcz2ef/HzFNjmIw2T9CojYVhQxwz3qDdgFdn3cq7i0XoptFUDdtvOnpGtjsEl8Qz/iuXoeQ0eYNOm/1ylhcINntXo26gNHhA1mg9HdrFOInzG/0SZWX9axBgZDI1rMMBTc4CouGwJN9z9gZTOfxvFaPf43i++XJXSayLQYT9O9brpl5++3uC7F+SykwcINpuA9XF7OabrP938hymq03Uc9BxW2MaMibSxE2PJiwWyYLz3Sza6UV3X9udy5zOSLLeVZiavEg8qe/aYwo+MJveYtUS6d4i4V3nEDRaa/P1Zmq1DpcBLqVKmQyIvZvOKj7MqsQdO9WeVyjBCL0sfz4DfgnfPoq/+t/c2CVKazW/sicBAhHnQufVlbekoj8TLzPLdGyP93WwHNJ1i8/VtDQY56Odh87gMrdW+McsfrW25TKntAr325HWOW4dFZaF84V3d5OEfn2C9heLxpqR9tpx8Zi80oaR04gnS281n1Ugeh8HHSdjrruIyXF7CkkTfr/onG9xE/D+0DCr+f4dLjuzTef4Bf3OQcEcvnsM+ydBQy7/wxOEBHfhjytPxaBnDp+bHXMW4o/6bFh7fRMZDcgBxlKGlTs3Wkg3aHa5vK8vx2sDjLrEvQRSMDR7qyjPlZjFrrMD/mzy0nVkalY9+YD+gGOmrVfK6BuHAt8jn7LcNmSLEP8aIol85wGZRTMJT6vWYZWZIn0O24X6o7n5PhZMYqbRJbj+Iy4BeQNuSBpTPuHYQNUfbfheX3QbmfQL0sb5i33T7dskcX9VS6z4VAR10cw0fMv0xK5Pon85UT1w/j/4HemI8YJp0m5otTjR4g45v0hfYToe02f2Od1QsQm8quwG8Mtwoa11ti2tuJb+Vo/L+Zn1Pdq3O4SDtffuidK12rIJ/3sGJv7CX3v/PYXngk7WGRNBvghvGGjXiyaytG3aHufyU9zGcgE5tCltCpxkYTDfAo9/oQllwWuaNxU3ymsf/BMvesPtO50T/eF4001g9cG8OSOiF/Pd/iLHcZPdpxmbHKDnrAwzhtGmS1ncE+0Asq/3wM04xnEtDp/V8I82ScITegJD3MM1Cm6GDsfDBYs5mI/1aH/3x9pYXJSxgxPrgn8+AOWFw+IIVR+BiOocc8zJTu1TB/HOK/ru0GqOU8dvoqvziEg/t4jMdAer2dFiNPbOCr7tMxoMwH3+5GelM64y3nybZIdeErUtmvBWJHKFaWYktdMvz+3kplpPJrQ5hbajoKrJjPI7zcKnVyIelecP3khB7/u8+uTPXxWQcaS/Ok7b511ccT66ojy9sk4imDWovjpTJ/K7PXFQbShPJGPO+QyvI+kBXqJZD5R6/R//2nHf9NDFNrc7F9Ie2xnsHPw1X6qwdiPIQQQk6QprJZertofHe3YX+qnt8b/XcDYm9uZfk6sY6s+qIM2busu9w1rsviwNAG19wyQgghLwRhCekCl4l9+HQWlky2i8y3R/gs19KPMJ6KaNqf9pn/dSPzly527A1t8sLiM0dteKHOtx5sbm6+JATdFs38xS6f2S1L8IQQQl4AxL4X5sveevxW6wz6JYR10MxftoExUb4Uvxsx43Sw73MN4K9trkC+WN5fifvkQGT3I7bZ3Df5YynS2kXZv7Uu/M1ed7M1DpwIIYScBKqMr5HujVi4a7L/usALAOrOzvLdhnRvsa/t5RJ74/0KNbBeo+4VOM4vY5C9A8pZ689RLWf8V+kHZjtkCOl99qM+ZTkhhBCyK9CO8qIT3fxNCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCCCGEEEIIIYQQQgghhBBCyLb5f1Y8+Uo8OgPOAAAAAElFTkSuQmCC>

[image12]: <data:image/png;base64,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>

[image13]: <data:image/png;base64,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>

[image14]: <data:image/png;base64,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>

[image15]: <data:image/png;base64,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>

[image16]: <data:image/png;base64,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>

[image17]: <data:image/png;base64,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>

[image18]: <data:image/png;base64,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>

[image19]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEMAAAAYCAYAAAChg0BHAAACQElEQVR4Xu2WPUsDQRCGT1BQRFQUYj7IJgFJLQFt7BTFVgsLwVbwZ2hlbxVsxFZsxM5CsLSw0Ua0UIJtsEjhR6LvxNlzbsxdEtGz2QeGS+ad3Z2d20zW8xwOh6NLjDGHsPdOjcdsZbPZB+F/pO/sq1h/IpEY1Ov9NVh3SeRVsXmJ/KxGdqEHv+dyuQntI5O+dDo9pn0c9yp9RCaTGWCtobU4wKZveP0rrVmgHcBqvgODCnDsihjyjfJEwap5zQnu7Wd66xx3KGMsrAWKFyM9dn286FUtWgL50UboLQqdfGs80bL0U5Ew8b74Pk9xeM7KOEKcjGetxQXWnrIFKRQKw1onoN35X7C5RaE1QcAFTVAsFoekn04CNpkWcScUh4+9Isxq1agk4gI5lLkgda0R2P8IHj3a72Orqf0axDRgb7CksE0ef6Tj/wvkUuOcylqLJJVKjfPAc61JUNF+jjsWhUji5Ezi+QK79aIqzqApZyjJbszrYF5JqVTqMxGnIxRscoMHBvqFJqpfgF6e46tT/yO2GPTUWiQYdE0Ddb/QmIh+QXAx2v7UYoD+VephvQvamfb5dLoJ89kvwu4Q9mS0neeHP5OWL6AViK/m8/lp7beYsD102i/E/eJEawT8p6yvaC1O+OIVmgNawoxpcWFsAmGbN7GmNQktQHHUN6Sfm+oTa+tSixvzeYqOTPCfrmk4KQt4XvJe/UskDZL3+G8m5qfYPa0rq6MgO16X3f63wYuYa5FbmJ3p8Q6Hw+FwOH6FD1F8BToy3GnWAAAAAElFTkSuQmCC>

[image20]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAYCAYAAACiNE5vAAACp0lEQVR4Xu1XO2gUURSdQAr/Irpu3F337U+2s0mRJqQIgqSwMSBCwCKNYGNnLVqJrTZBkPRLmhAEsQikCaRKEdKkUdQ2WGRBYz7nztxZ7xxmZmcTP6hz4DI755w77955897Mel6OHDn+eTjnOoiDrKE5T6rV6gfDf5Zz5T6GfLFYPM3jMUql0inmfgZQyx1T3yaooYhBhFqtNsKchOXK5fJF5tS3azlBpVI5qdo+awx4ZtU7ydpRgWu9QWyb8+lI7bgrDRAvekTAXdBC1iwvAPc+/C2zqb6O9YRQLXKj0iCNix/jP2RtECB/VMeesrxwmODH4UlHZocMM5p42/JyQ5A4b85vaKHj1icwM/6VtX6o1+vXNfc5a1mAvCWta5T4HUTXP0EjN60ogLgmie12+6zlZYbRUNn4/AHwc9jYQm1btEajcZ61rEB+XW/AAmtpgH85pfHkJ1AHSzYo4NlHfEdcMfHgKMWmodVqncP1upiktx5vUDFwulnHNC71HhQKhTOW94Ed9pIWvsKaBYo4ob5FbdgPPBHXcPyG2PIyFJkVGG9Mx5tljYEaWuJF47cMPaz58Y1jgPtqiKxvRtr69n4MssPCoEA9d+VacmQtDciZc9Fd/R1iV67lxU0IhA0ReX0zXMr6FmjjfZdLEmRn14bHWMsKbJITuMYe4pNutslrPGvBLlgvSe/o3mPFQj8g56Xkoeg2a8eF1rTKfOb1bd7fS6wJXPBYiT7NWhLgXUB05SOJtUFh9p/1kMONLArXbDavWq8PCE81YYY1C2lIfLLOLa8DflHtntXSAP8Gf0scB2ZiFkPOBa/XuZ4JJ1Nqio2eMfC+Yp1iD80/8+I2j98M3PjXUlNV/0/g+Ig9Of4UsO4uu+hHUGLEvoP/Vvy3jefIkeOX4RD0zgr9Sp1W+AAAAABJRU5ErkJggg==>

[image21]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAXCAYAAAAcP/9qAAABWUlEQVR4Xu2Uu07DQBBFHSUUCIkUIFn4tbZlCUFrAQ1VREFDE2q+IWW+hIaOH6Cjo6CmoaIHKQ009CAe92IbjYbEjxDR4CON7Lkz3rveXduyWv4Nrut6xpg3xAevSZKs6p6FA6MhDdM0XWIex3GfOSazpnsXSS9/yyspIr9DTKQ2jTAMD7VWiyAIDmiMAc6lzpw6bjtS13CV0PeAuEXa1fWZwPiozBixJfUSujRHPNm2vaKLP4Dx/jRjaJfUOTGp1wHPXZjsoG7omqSTv9m1FJG/zmtcgOdPOUYURZu69gUKu2zwPG+ZOe6PEffUfN/f0f1NweRHHAuruqdrFr9bFB+5RGjcLvbYcZx13duUUmONyT4nnuq5qVxqFN+1CXPMdCy1upjscL1U/oBowiUW+RniWfbU4PtzKs5KJWge5OYTXrEXN7qnBBo2/4H8FmzHiVXxd2tp+VM+ARVMYc2Eztu2AAAAAElFTkSuQmCC>

[image22]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAYCAYAAACiNE5vAAACn0lEQVR4Xu2XO2gUURSGNxDB+CToZnV32bsv2c5mIWmsgiC2sVECEdIINulSSKqkEhsRgyBpxHZJI2nEQrBMm3Q2itgGCwM+kvifzLnrmd+dRyYRUeeDw86c/5x7z537mNlCIScn55/HOdeD7aU1zVms1Wrvjf+j3Kvvg/eXSqWT3B9TLpdPsO8oqNfrt0x9W9VqdSQUIAKCLrBPzPoqlco59mncN+sTpBPVdlljEDOrsZOsZQUT8AQ25+9lAqSPZrN51gc04Xjczwh8o1rIuvUL8L3z174xWM/GeFQLPag4ZOASbwvOyqB+4bsHW/M3PV4C8E1r0VPWLw8EK+OZub+qhV6xcYKZ8S+sJdFoNC5r7gPW0lAsFk9JfrvdLlq/DjyYJAzkmhUFiOuS2Ol0Tlu/zDAGVDFxaxKHy2ET5rUt0fpLKwPIb+gDWGUtCc2TSZlX11BiPT6J/QxidmHfYReN3c1abBSYuTNobxuT9BK3Q6wPAqtm3I/DG59jIXDCntfAN6xZ0MhxjXvhzMCxIi7h9yvsbSFlkWlAfxPa3yxrUSDntuZ4W+aYPgi+o0Gh/c3E7W8wrG18ZuGgoJ6b0pb8shYHcjZgK3Ity90M/inH7gNhUwJ4fzMuZn8LviP2p0VOdh3wBGtJIG/K0UPvdrvH4NuJrCltwS7Y31HvaD/jie0wyFmWPOzRDmtpQf5r2CP2y8EmbcupHxLS7m/z/g7eiQT8r1S/wVoUiF2FbctHEmsHxQVfooNq2z/Z2SkJS1rwNGsWGZDEyT63fj3wPqk2Y7U4EL/J3xKHwc8sVo2zfvieo66H/ua6DnagUeIK62Q7GPz9whGe5llBHXVfk/v532GB43L+BK1Wa8yFP4Ii7ZeD6W/mvx14Tk7Ob+MHzRMH5DW0ntAAAAAASUVORK5CYII=>

[image23]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAXCAYAAAAcP/9qAAABUUlEQVR4XmNgGAUjBkhLS8vIy8v/h2E5OTktdDVUB0CLDIH4NJrYeyAORhajOgBa8FZdXZ0XWQwaAv+QxbABBQUFD3QxogEoaIEGJCCLQS3+jSyGDRgbG7MC1T0E4vNALjO6PF4A1HQdavkpmBgwjm+RGNTMIMuB+JW4uDg3uiRWAHX1fyT8F+iICHR1xAKg/nUgM4BYEl0OA2BJ1Y/Q1ZAKgOZMBZmlqKioji4HBkDJYiB+D2KDshGSA8BilAKgmfkg84ChaA4XFBUV5QEJApksCKVgx4DiC2S5JrI4OQCrxUBBX6DgWyR1cABSDJJHFycWyOMLaqDBNvI48itQ/BtQXgldnBCQhySuX8B0I4wuhwJAFgMtKEMWA/JdgOKvkcUIAHh2kpGR4USXxAVAmn5Bg/YRND4uoSvCAUB6yStAKAFAh8YCKUZ08VEwCgYMAABsAV0rJmH19wAAAABJRU5ErkJggg==>

[image24]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAYCAYAAACiNE5vAAACfklEQVR4Xu2WvUscURTFJ6CQ+BVCXDfu1+yXLCFisxAbKwmIbUwREFLYBNLkf4hVSJs0ISD2YhNsgqRJp7WdjRJiKRYR1Ghy7nqf3Dm7szO7bghJ5geX3bnnvPfue2/ezHheQkLCP4/v+2uIn3FD27wqFAr7Jv9NrjX31eXT6fQgj8dkMpkBzl0XHf8z4j1qemIDufkrU7FYvNeiYWOSjmw2e5dz6juzOSGXy91S7YI1Bp4l9c6y1i2u/pBY9rACZfx5axshd0cN2zYvILfn/stuqm/NehxuIM6HAe+s+DH+S9Y6AXfQqNSeSqWGbL5cLt9G/rBxIUXL7lgDcota9GOblwXBnbFqrh9poTPWJ5gdP2EtilKpNKVt37AWB6lHauM8+juv1+v9jQtMZI50MWzLwLVabdjmZYcxoazxbYgPf/uMzWmHoskqsxYXtC/pAqyz1ilYiBUs6EPOB9DBIm9ReC4QPxDjJl70qlhHtVodQX/H2KRPuLzBehSY9AO03eJ8AD0fUvgX1izo6Kb6PtqJ446YwO8pYtfrosgwMN60jrfEWhRoc4K4z/kAGOC5DhA430y78w36tI/vLHQK6nkqfckva3HI5/OT0p7zTcC0I0Y+34zf5nwLOvHoAUOQJ7tOeJq1TvAvn1dNr9sm4hbsX57vsHe02/HIfhi0eSft8CCqsdYNWscB5wPEPd/m/b3BmoD8puoLrIUB7zriWD6SWOsWeY9rHVffHi2BYVmNi6xZZELi43elPvCOVHtmtXbAv8PfEr0Ai5gLnTiS8yq2DPJ+YJ3iHJN/7fXwaX4dzB28yVrCn6RSqYz5wY+g0ODv77+a/3biCQkJv41f8PD0PSWkECkAAAAASUVORK5CYII=>

[image25]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAXCAYAAAAcP/9qAAABCUlEQVR4XmNgGAUjAsjLyx8A4qdAPAuIo+Xk5EKQMbp6qgGgZZ+A+D8O/AxdPdUAyAJlZWUxLOJ/gRQLujgyUFBQ8EAXIxawAC3Yii4INHCXoqKiGbo4OjA2NmYF6n8IxOeBXGZ0eZIA0FJzoEGz0MUJAGaQ5UD8SlxcnBtdkhjACAp6dEFSAFD/OlA0AbEkuhxOAPTtKqCGSeji5ACgOVNBngBGmTq6HDoA+xaYhZTQJSgBQPPyQeaCohBdDgyAktHQYMabkkkFxFh8l9L4RQZEBzVIETUslockrl/S0tLC6HJYAYUWw7OTjIwMJ7okXkCmxSALqVOAkAKACScWSDGii4+CUTBgAABbdUhTgmZkZQAAAABJRU5ErkJggg==>

[image26]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAYCAYAAACiNE5vAAACp0lEQVR4Xu2Wv2sUQRTHT0jhbxE9T++Om/slh42NYBorESRttBADFmkEG/8HxULSaieIhd0ZEEkTLAQbIUWqdGkUuVYsEtBo4vfdvtl7+83t3nh3Fup+YNid7/e9nTc7O7tbKOTk5PzzOOe6aHuhTXMe1Gq1T0bvSV+1z14vlUpHeDymXC4fZm1aoIZFU+M6m3v1ev0sa9KsVqlUTrGmcTtWE6rV6iH1dtlj3KC4q+xNgi7CK9/H+Sa0595sQngSR0faSS1kzeoCtI/+XFZT47o2xqNe4kZlIROXeIx/n73fRSbozE3H+QWt570XurI6cUakLWjQvNXlhuDJeGH617TQKzZOMCv+jb1RNBqNi5q7xF4gM5r/yIryxMYdTOS68fogYU0SO53OMavLCmNCFRO3InE4nTFh3vsiXrPZPMFeKMhv6ASW2cvC6cLJgmB+B3G8iWOd4/ahg418RBGzi/YD7Zxp98YpNot2u30c19tG7avoHmCfcYOX9RLabdGQ+xrnWxwbgzfsaU2K9kIKcic17o0zE8cTcR7H72ibhYAiQ8F4szreInsMYt5p7AfS+/VaLQYD3NWAxP5msvZ3YbDH0u9wIKjnllxLjuylYSY+R/qW6FaLgbEhJu9vxmXsb0EHHj5IAPJm1wnPsjcK5L2UXFzjEun9iReLxaNW92ZQwS7a32nfaL/iI6/DIOep5OHN3mEvFOTPZ018309V6P423+8V9gTob9W/wV4aiF1G2058csbEvH8S2xX9HTdssSA+1IQF9iwyIYmTfW51HfCreneslwXiN/hfYlJQyyqu2/N9+axKXXiSLvcFdOZ0skNbfKUo9hn71H5iwMeFKb7NJwH1rGtdPT1O9Zc4Z1xardYZl/wJSm1D38h/K//txHNycv4YvwCD9Ao9YyQIOgAAAABJRU5ErkJggg==>

[image27]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAYCAYAAACiNE5vAAACnklEQVR4Xu2WO0wUURSGl4RCFDE+loV9zb7IdlREGwtDSAitNCQQChoTGxML7bEytpoYso09oTE0hEQTS2pCQ7NGaYmFJCoC/1nOXc/+mdmZWTAamC852b3nP/fec+Y+ZlKphISEC4/neauw46imfZaLxeJn49+Ttvq+OH8mk7nG8zHZbPYq+84K5m4il7e5XC6fTqcHy+XyXfi+wkZt0HGpVBox/Vo+MevDILfZp3G/rE/I5/MDqh2xxiBmSWMnWesVjNV0NTjDg1hsB6BRgfO16SO+mxq8Zf2CDOj+y2pq3KqNcbgJ2R8EYic1wSesxUXyxDgL+F3Boj5gvbXNZXXIN69JP7R+eSAY5J1pT2mi922cYFb8B2thYFuOa99XrEVFCpctzv42KGSafei0JRPX6/Xr1i8rjIJyJm5d4vC334Q5bV+0SqVyg7WooH9ZH8Aaa2GEFu6HTha6RRFzBDuEjRp73GuyQdRqtSGMd4BF2kCzj3U/pHDYB9hH7MhnklPHGWdww97RxD+xZkESVzTuvWcKx44Yw+9P2G4qYpJRwHz3dL4l1vxAXBN9Sqbd2j0yjgn7A4RHOkHH+Wa6nW/Qr2N8ZyEuyGdOE55jLS6a0z77W0DYlgA+34zX5XwLOknocQlCbnYt2H+FQpCLmH1dc+oqGrzT8x30jnYrHjoOgz5vpB9u9jprUUHRz3X+hvUH5hT1fJv39zprAvybqs+yFgRi12AH8pHEWlwwzlOZv1AoTBh3n+a0Y3ynwPlCxXnWLFKQxMk5t3698L6pFnyDEojf5m+JMyI7ruN+cTd7+/WKxowW62u2M9oN1sl+o/iXqXO8zXsFeYxoTnsuPzzcWxyX8C+oVqvDXudHUKDF/hr7n7m0hSckJPw1TgB7lwBdgAAPtAAAAABJRU5ErkJggg==>

[image28]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAYCAYAAACiNE5vAAACgklEQVR4Xu1Wv08UURBeIiYYFQN6Obhf7+5y5v6AI9pYaGJCqEykhFjYmFhaaEMFFb0FMVjYExtDQ0ggoaSwMjY2GKElFJCo/Pq+Y945N9nb3eMIibpfMrl73zdv3sy+N/s2CFKkSPHPwzm3BDtJajJntlQqfVf8DsfC/fB8Npu9bte7DGDtLeSykM/nC5lM5kalUrkHbhs2qp1OyuXyiJrX5GiaQ5DblhO/35ojCoXCNdGOrXYZYOG+Bm94EM9aDhhUQb5Vc8gNifOm5gkG9P+5m+K3pH08/IKW7wF9iPfIkmFgnqhjGr/vsKkPrd485twdw01J0k81zweCIB/U+DH98PtA+xFqx39arVs0Go2rLAT2FcMrVg8D/XnELd8CChm3HCZtMul6vX5T89xhFJRXfsv0w99+5ea1XWrVavWW1ZJCWusAOa5g2Gf1KMQWHgbZqdgjCp9j2CFsVNlLmf/R+icF5lYkxnurJYU7OyFrsHWcyNeM19bjFrlc7o4sumE1DezCgPh9cqpwnIi7+P0F+xZ0uUuIeV9izlitWyDGFuKV1bj5MLmGcvsDCC9k8bb+tojqb6BfYuxbIQxY84nE6rwjFwDJadfyTUD4Qgfb3xYuor8JWSS2XQhfOOy51c4LvogtF5lTpKjgzvq70x3tdzw2jsZFHXUU/UbiLGq+Y05J+1vd38tWI8Cvij5ptSRwPb7cMO8V5xeLxTFF8xuAMXkltgPknIhTVtNgQfRjn2teXnh7ovXcr7VabdCd7zrjiWt7v/g3e+t6xWBCig01PRnjRasbO0KS80F3ScZCfcB8DhJ+wCCPEclpx+eHG2fY+v0tSPzJmiJFihQp/iecAqqB9YrUO6mVAAAAAElFTkSuQmCC>