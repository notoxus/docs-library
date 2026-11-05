**Cơ bản về OO**

**Giới thiệu các chủ đề về Hướng Đối Tượng**

* Tổng quan  
* Các nguyên lý cơ bản của Hướng Đối Tượng  
* Các khái niệm cơ bản của Hướng Đối Tượng  
* Điểm mạnh của Hướng Đối Tượng

**Tổng quan**

* Các phương thức hướng đối tượng (OO) là gì?  
  * Các phương thức OO cung cấp một tập hợp các kỹ thuật để phân tích, phân rã và mô-đun hóa kiến trúc hệ thống phần mềm.  
* Lợi ích của OO là gì?  
  * OO tăng cường các yếu tố chất lượng phần mềm chính của một hệ thống và các thành phần cấu thành của nó.

**Các định nghĩa cơ bản OOA, OOD và OOP**

* Các phương thức hướng đối tượng có thể được áp dụng cho các giai đoạn khác nhau trong vòng đời phần mềm.  
  * ví dụ: phân tích, thiết kế, triển khai, v.v.  
* Phân tích hướng đối tượng (OOA) là một quá trình khám phá.  
  * mô hình hóa và hiểu các yêu cầu của hệ thống.  
* Thiết kế hướng đối tượng (OOD) là một quá trình sáng chế và thích ứng.  
  * tạo ra các sự trừu tượng hóa và cơ chế cần thiết để đáp ứng các yêu cầu về hành vi của hệ thống đã được xác định trong quá trình phân tích.

**Các định nghĩa cơ bản OOA, OOD và OOP**

* Lập trình Hướng Đối Tượng (OOP)  
  * xây dựng các hệ thống phần mềm sử dụng các khái niệm hướng đối tượng như kế thừa, đa hình, đóng gói, liên kết động.  
* Phân biệt giữa OOD và OOP  
  * OOD tương đối độc lập với ngôn ngữ lập trình được sử dụng.  
  * OOP chủ yếu quan tâm đến các vấn đề về ngôn ngữ lập trình và triển khai phần mềm.

**Cách tiếp cận Hướng Đối Tượng**

* Mô hình hóa các đối tượng là một phần của bài toán.  
* Để các đối tượng thể hiện hành vi bình thường của chúng.  
* Thêm các đối tượng không có sự tương đồng trong không gian bài toán.  
* Cho các đối tượng làm việc cùng nhau để tạo ra một giải pháp.  
* Các mẫu thiết kế (Design patterns) giúp bạn xác định các sự trừu tượng hóa ít rõ ràng hơn và các đối tượng có thể nắm bắt chúng -GOF-  
* Ví dụ: BÀI TOÁN: Hệ thống thanh toán đơn hàng (E-commerce)  
  * Yêu cầu: Khách hàng đặt hàng. Có nhiều phương thức thanh toán:  
    * Credit Card  
    * PayPal  
    * Bank Transfer  
  * Sau này có thể thêm ví điện tử

**Năm đặc điểm cơ bản của OO**

* Hướng đối tượng "thuần túy" theo Alan Kay (Smalltalk):  
* Mọi thứ đều là một đối tượng.  
* Một chương trình là một tập hợp các đối tượng nói cho nhau biết phải làm gì bằng cách gửi các thông điệp.  
* Mỗi đối tượng có bộ nhớ riêng của nó (được tạo thành từ các đối tượng khác).  
* Mỗi đối tượng có một kiểu.  
* Tất cả các đối tượng của một kiểu cụ thể có thể nhận cùng một thông điệp.

**Các nguyên lý cơ bản của Hướng Đối Tượng**

Hướng Đối Tượng

* Trừu tượng hóa (Abstraction)  
* Đóng gói (Encapsulation)  
* Đa hình (Polymorphism)  
* Phân cấp (Hierarchy)

**Trừu tượng hóa là gì?**

* Đây là một nguyên lý rất đơn giản. Trừu tượng hóa có nghĩa là xác định các đặc điểm chính, quan trọng nhất của một thứ gì đó, đồng thời loại bỏ bất cứ điều gì nhỏ nhặt và không quan trọng.

**Đóng gói là gì?**

* Che giấu việc triển khai với các đối tượng gọi (clients).  
  * Clients phụ thuộc vào giao diện (interface).  
* Ở đây, biến "name" được giữ ở mức riêng tư (private) hoặc được "đóng gói".

//save as Student.java  
package com.javatpoint;  
public class Student {  
    private String name;  
    public String getName() {  
        return name;  
    }  
    public void setName (String name) {  
        this.name \= name;  
    }  
}

//save as Test.java  
package com.javatpoint;  
class Test {  
    public static void main(String\[\] args) {  
        Student s \= new Student();  
        s.setName("vijay");  
        System.out.println(s.getName());  
    }  
}  
// Compile By: javac \-d . Test.java  
// Run By: java com.javatpoint.Test  
// Output: vijay  
**Đóng gói (Encapsulation)**

* "Đóng gói là một cơ chế được sử dụng để che giấu dữ liệu, cấu trúc bên trong và chi tiết triển khai của một đối tượng. Mọi tương tác với đối tượng đều thông qua một giao diện công khai gồm các phương thức." (Craig Larman)  
* Có một ranh giới tồn tại xung quanh mỗi đối tượng; ranh giới này đóng gói các đặc điểm (các phần tử dữ liệu) và hành vi (chức năng) của đối tượng.  
* Lý do để che giấu các tính năng là để:  
  (1) giữ cho người dùng không chạm vào những phần của đối tượng mà họ không nên chạm vào;  
  (2) cho phép người tạo ra đối tượng thay đổi cách hoạt động bên trong của đối tượng mà không ảnh hưởng đến người sử dụng đối tượng.

**Đa hình là gì?**

* Khả năng che giấu nhiều cách triển khai khác nhau đằng sau một giao diện duy nhất.  
  * Nguyên lý OO: Đóng gói (Ví dụ: Các Nhà sản xuất A, B, C và Điều khiển từ xa).

**Đa hình**

* Xảy ra cùng với tính kế thừa.  
* Các lớp con (subclasses) khác nhau có thể có các cách triển khai khác nhau cho cùng một phương thức hoạt động.  
* Cho phép bạn đối xử với một đối tượng như là lớp cơ sở (base class), thay vì như một kiểu kế thừa cụ thể.

**Đa hình**

public class Animal {  
    public void speak() {  
        System.out.println("Hello\!");  
    }  
}  
public class Dog extends Animal {  
    @Override  
    public void speak() {  
        System.out.println("Woof-woof\!");  
    }  
}  
public class Cat extends Animal {  
    @Override  
    public void speak() {  
        System.out.println("Meow\!");  
    }  
}  
public class Main {  
    public static void main(String\[\] args) {  
        Animal dog \= new Dog();  
        dog.speak();  
    }  
}

**Phân cấp là gì?**

* Các mức độ trừu tượng hóa  
  * Mức độ trừu tượng tăng dần (Ví dụ: Tài sản \-\> Tài khoản ngân hàng, Chứng khoán, Bất động sản)  
  * Mức độ trừu tượng giảm dần (Ví dụ: Tiết kiệm, Thanh toán, Cổ phiếu, Trái phiếu)  
* Các phần tử ở cùng một cấp độ của hệ thống phân cấp nên ở cùng một mức độ trừu tượng.

**Các khái niệm cơ bản của Hướng Đối Tượng**

* Đối tượng (Object)  
* Lớp (Class)  
* Thuộc tính (Attribute)  
* Phương thức (Operation)  
* Giao diện (Interface)  
* Gói (Package)  
* Mối quan hệ (Relationships)

**Đối tượng là gì?**

* Về mặt phi chính thức, một đối tượng đại diện cho một thực thể, có thể là vật lý, khái niệm, hoặc phần mềm  
  * Thực thể vật lý: Xe tải  
  * Thực thể khái niệm: Quy trình hóa học  
  * Thực thể phần mềm: Danh sách liên kết

**Một định nghĩa chính thức hơn**

* Một đối tượng là một khái niệm, sự trừu tượng hóa, hoặc một sự vật có ranh giới rõ ràng và có ý nghĩa đối với một ứng dụng  
* Một đối tượng là thứ có:  
  * Trạng thái (State)  
  * Hành vi (Behavior)  
  * Danh tính (Identity)

**Lớp là gì?**

* Một lớp là một bản mô tả về một nhóm các đối tượng có chung các thuộc tính (attributes), hành vi (operations), mối quan hệ và ngữ nghĩa  
* Một đối tượng là một thể hiện (instance) của một lớp  
* Một lớp là một sự trừu tượng hóa ở chỗ nó:  
  * Nhấn mạnh các đặc điểm có liên quan  
  * Triệt tiêu các đặc điểm khác  
  * Nguyên lý OO: Trừu tượng hóa

**Lớp Mẫu**

* Lớp: Khóa học (Course)  
* Thuộc tính: Tên, Địa điểm, Ngày cung cấp, Số tín chỉ, Thời gian bắt đầu, Thời gian kết thúc  
* Hành vi: Thêm một sinh viên, Xóa một sinh viên, Lấy danh sách lớp, Xác định xem lớp đã đầy chưa

**Biểu diễn Lớp trong UML (Ngôn ngữ Mô hình hóa Thống nhất)**

* Một lớp được biểu diễn bằng một hình chữ nhật với ba ngăn:  
  * Tên lớp (Ví dụ: Professor)  
  * Cấu trúc \- các thuộc tính (Ví dụ: name, employeeID, hireDate, status, discipline, maxLoad)  
  * Hành vi \- các phương thức (Ví dụ: submitFinalGrade(), acceptCourseOffering(), setMaxLoad(), takeSabbatical(), teachClass())

**Các Lớp của Đối tượng**

* Bạn nhìn thấy bao nhiêu lớp?

**Mối quan hệ giữa Lớp và Đối tượng**

* Một lớp là một định nghĩa trừu tượng của một đối tượng  
  * Nó định nghĩa cấu trúc và hành vi của mỗi đối tượng trong lớp đó  
  * Nó đóng vai trò là một khuôn mẫu để tạo ra các đối tượng  
* Các đối tượng được nhóm thành các lớp  
  * Đối tượng: Professor Smith, Professor Jones, Professor Mellon  
  * Lớp: Professor

**Thuộc tính là gì?**

* Thuộc tính là một đặc tính có tên của một lớp mô tả phạm vi các giá trị mà các thể hiện của đặc tính đó có thể nắm giữ.  
  * Một lớp có thể có bất kỳ số lượng thuộc tính nào hoặc không có thuộc tính nào cả.  
  * Ví dụ các thuộc tính của Lớp Student: name, address, studentID, dateOfBirth

**Phương thức là gì?**

* Một dịch vụ có thể được yêu cầu từ một đối tượng để thực hiện hành vi.  
* Một phương thức có một chữ ký (signature), có thể hạn chế các tham số thực tế có thể có.  
* Một lớp có thể có bất kỳ số lượng phương thức nào hoặc không có phương thức nào cả.  
  * Ví dụ các phương thức của Lớp Student: get tuition(), add schedule(), get schedule(), delete schedule(), has prerequisites()

**Giao diện là gì?**

* Giao diện hình thức hóa tính đa hình  
  * Giao diện Shape: Draw, Move, Scale, Rotate  
  * Các lớp Tube, Pyramid, Cube có Mối quan hệ hiện thực hóa (Realization relationship) với giao diện Shape.  
  * (hãy chờ xem về các mối quan hệ hiện thực hóa)

**Giao diện**

* Làm thế nào để bạn khiến một đối tượng làm công việc hữu ích cho bạn?  
  * Các đối tượng chỉ được biết đến thông qua các giao diện của chúng  
* Mọi đối tượng đều trình bày một giao diện với thế giới.  
* Giao diện xác định những gì bạn có thể yêu cầu một đối tượng làm.  
* Đại diện cho một "bản hợp đồng" với các đối tượng khác.  
* Giao tiếp với các đối tượng bằng cách gửi thông điệp cho chúng; giao diện của một đối tượng là tập hợp các thông điệp mà một đối tượng sẽ phản hồi.

**Gói là gì?**

* Một gói là một cơ chế đa mục đích để tổ chức các phần tử thành các nhóm  
* Một phần tử mô hình có thể chứa các phần tử mô hình khác  
  * Tên Gói (Package Name)  
* Công dụng  
  * Tổ chức mô hình đang được phát triển  
  * Một đơn vị của quản lý cấu hình

**Các mối quan hệ**

* Kết hợp (Association)  
* Tập hợp (Aggregation)  
* Phụ thuộc (Dependency)  
* Kế thừa (Inheritance) \- Tổng quát hóa (generalization)  
* Hiện thực hóa (Realization)

**Các mối quan hệ: Kết hợp**

* Mô hình hóa một kết nối ngữ nghĩa giữa các lớp  
  * Lớp Professor (Giáo sư) có Tên kết hợp là "Works for" (Làm việc cho) Lớp University (Đại học).

**Các mối quan hệ: Kết hợp Tập hợp**

* Để mô hình hóa một mối quan hệ "toàn thể/bộ phận", sử dụng tập hợp (aggregation).  
* Tập hợp đại diện cho một mối quan hệ "có một" ("has-a") hoặc "là một phần của", có nghĩa là một đối tượng của cái toàn thể chứa các đối tượng của bộ phận.  
  * Ví dụ: Company (1) có nhiều Department (\*).

**Kết hợp: Bản số và Điều hướng**

* Bản số (Multiplicity) xác định có bao nhiêu đối tượng tham gia vào một mối quan hệ  
  * Được chỉ định cho mỗi đầu của mối kết hợp  
* Các mối kết hợp mặc định là hai chiều, nhưng thường mong muốn hạn chế điều hướng (Navigation) theo một chiều  
  * Ví dụ: Customer (1) hướng đến Account (0..\*)

**Các mối quan hệ: Phụ thuộc**

* Một mối quan hệ giữa hai phần tử mô hình trong đó sự thay đổi ở một phần tử có thể gây ra sự thay đổi ở phần tử kia  
  * Ví dụ: Lớp A phụ thuộc vào lớp B: phương thức của A thao tác trên các đối tượng của B trong các tham số, biến cục bộ hoặc kiểu trả về  
  * Minh họa: Lớp Client có Mối quan hệ phụ thuộc vào Supplier; Gói ClientPackage phụ thuộc vào SupplierPackage.

**Các mối quan hệ: Hiện thực hóa**

* Mối quan hệ hiện thực hóa (Realization relationship) giữa giao diện Shape (với các phương thức Draw, Move, Scale, Rotate) và các lớp Tube, Pyramid, Cube.  
  * (hãy chờ xem về các mối quan hệ hiện thực hóa)

**Kế thừa**

* Lớp Shape (với thuộc tính origin và các phương thức draw(), erase(), move(), setColor(), getColor()) là lớp cha.  
* Lớp Circle và Square kế thừa từ lớp Shape.

**Đa hình**

* FlockManager sử dụng phương thức reLocate() tác động lên lớp Bird thông qua phương thức move().  
* Lớp Goose và Penguin kế thừa lớp Bird và có phương thức move() riêng.

**Cái gì được Kế thừa?**

* Một lớp con kế thừa các thuộc tính, phương thức và mối quan hệ của lớp cha nó  
* Một lớp con có thể:  
  * Thêm các thuộc tính, phương thức, mối quan hệ bổ sung  
  * Định nghĩa lại các phương thức được kế thừa (sử dụng cẩn thận\!)  
* Các thuộc tính, phương thức và/hoặc mối quan hệ chung được hiển thị ở cấp độ áp dụng cao nhất trong hệ thống phân cấp  
* Kế thừa tận dụng những điểm tương đồng giữa các lớp

**Ví dụ: Cái gì được Kế thừa**

* Lớp cha (Superclass): GroundVehicle có thuộc tính weight, licenseNumber và phương thức register(). Lớp này có kết hợp với lớp Person (owner).  
* Lớp con (Subclass): Lớp Car (với thuộc tính size) và Truck (với thuộc tính tonnage và phương thức getTax()) có quan hệ tổng quát hóa lên lớp GroundVehicle. Lớp Truck có quan hệ tập hợp với lớp Trailer.

**Bài tập 1 – Xác định Class từ bài toán**

Bài toán: Hệ thống quản lý bán hàng online:

* Khách hàng đặt sản phẩm  
* Đơn hàng gồm nhiều sản phẩm  
* Mỗi sản phẩm có giá  
* Khách hàng thanh toán đơn hàng  
  Yêu cầu  
1. Xác định các class  
2. Xác định attributes  
3. Xác định operations  
4. Xác định quan hệ giữa các lớp

**Bài tập 2 – Nhận diện Class từ tình huống thực tế**

Bài toán: Hệ thống đặt vé máy bay:

* Hành khách đặt vé  
* Vé thuộc một chuyến bay  
* Chuyến bay có ngày giờ bay  
* Hành khách thanh toán vé  
  Yêu cầu  
1. Liệt kê các class  
2. Xác định attributes  
3. Xác định relationships

**Bài tập 3 – Phân tích Object-Oriented**

Bài toán: xây dựng hệ thống ATM với chức năng:

* Rút tiền  
* Nạp tiền  
* Kiểm tra số dư  
* In biên lai  
  Yêu cầu  
1. Xác định actors  
2. Xác định use cases  
3. Xác định classes  
4. Xác định attributes và operations