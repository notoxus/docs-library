TỔNG QUAN VỀ CÁC NGUYÊN LÝ VÀ MẪU THIẾT KẾ HƯỚNG ĐỐI TƯỢNG

(Overview Object-Oriented Design Principles and Design Patterns)

1. Điều gì làm hỏng phần mềm? (What goes wrong with software?)

Bạn bắt đầu với một hình dung rất rõ ràng trong đầu về phần mềm sẽ như thế nào. Sự rõ ràng của thiết kế này giúp bạn đạt được phiên bản phát hành (release) đầu tiên.
• Thế nhưng sau đó, một điều gì đó đi sai hướng, phần mềm bắt đầu "mục nát" (rot):

Các thay đổi và bổ sung ngày càng khó thực hiện hơn.

Bạn buộc phải từ bỏ thiết kế ban đầu, dần dần ngay cả những thay đổi đơn giản nhất cũng khiến bạn khiếp sợ vì những hiệu ứng gợn sóng (rippling effects) không mong muốn, và kết quả là bạn phải thiết kế lại toàn bộ phần mềm.
Chuyện gì đã xảy ra?

You start with a clear picture in your mind what the software should be. The clarity of the design helps you to get to the first release.
• Then something goes wrong, the software starts to rot:

Changes and additions are harder and harder to make,

You are forced to let go of the original design, eventually even the simplest changes terrify you because of rippling unexpected effects, and you must redesign the whole software.
What went wrong?

2. Các dấu hiệu, triệu chứng của thiết kế mục nát (Bad signs, symptoms of rotting design)

• Rigidity (Sự cứng nhắc)

Code rất khó để thay đổi (không có tính liên tục).

Các thay đổi lan truyền (phát triển) thông qua các sự phụ thuộc (dependencies).

• Fragility (Sự dễ vỡ)

Ngay cả những thay đổi nhỏ cũng có thể gây ra hiệu ứng dây chuyền.

Code bị hỏng ở những vị trí không ngờ tới, nơi không có mối quan hệ về mặt khái niệm đối với khu vực vừa bị thay đổi (không có sự bảo vệ).

• Immobility (Sự bất động / Khó tái sử dụng)

Code quá rắc rối (chồng chéo) đến mức không thể tái sử dụng bất cứ thứ gì.

Không có khả năng kết hợp (không thể kết hợp các thành phần lại với nhau).

• Viscosity (Độ nhớt / Độ dễ hay khó khi thêm code mới):

Viscosity đề cập đến mức độ dễ dàng mà một lập trình viên có thể thêm các đoạn code mà vẫn giữ nguyên được thiết kế (design-preserving code) vào một hệ thống.

Nếu việc thêm code mới vào chương trình một cách dễ dàng trong khi vẫn duy trì được thiết kế, thì chương trình đó có độ viscosity thấp (dễ thêm code mới phù hợp với thiết kế).

Nếu việc thêm một đoạn code sửa tạm (hack) lại dễ dàng hơn là thêm một đoạn code phù hợp với thiết kế của chương trình, thì hệ thống đó có độ viscosity cao (lập trình viên dễ chọn cách sửa tạm thay vì viết code đúng theo thiết kế).

• Needless complexity (Độ phức tạp không cần thiết)

Thiết kế chứa các thành phần không hữu ích ở thời điểm hiện tại.

Là hậu quả của việc dự đoán quá mức về các nhu cầu trong tương lai.

• Opacity (Sự khó hiểu)

Xu hướng của một module trở nên ngày càng khó hiểu hơn.

Cần một nỗ lực liên tục để giữ cho code luôn ở trạng thái dễ đọc.

• Rigidity (Cứng nhắc)

Code difficult to change (no continuity)

Changes propagate (grow) via dependencies

• Fragility (Dễ vỡ)

Even small changes can cause cascading effects

Code breaks in unexpected places having no conceptual relationship with the area that was changed (no protection)

• Immobility (Khó tái sử dụng)

Code is so tangled that it's impossible to reuse anything

No composability (no combine together)

• Viscosity (Độ dễ hay khó khi thêm code mới vào thiết kế ban đầu):

viscosity refers to the ease at which a developer can add design-preserving code to a system.

If it is easy to add new code to the program while maintaining the design, then the program has low viscosity (dễ thêm code mới phù hợp với thiết kế).

If it is easier to add a hack than it is to add code that fits into the program's design, then the system has high viscosity (lập trình viên dễ chọn cách sửa tạm (hack) thay vì viết code đúng theo thiết kế).

• Needless complexity (Độ phức tạp không cần thiết)

Design contains elements that are not currently useful

Results from too much anticipating future needs

• Opacity (Khó hiểu)

The tendency of a module to become more difficult to understand

A constant effort is needed to keep code readable

3. Nguyên nhân làm thiết kế mục nát (Causes of rotting design)

• Sự thay đổi yêu cầu là điều không thể tránh khỏi

"Tất cả các hệ thống đều thay đổi trong suốt vòng đời của chúng. Điều này phải luôn được ghi nhớ khi phát triển các hệ thống được kỳ vọng sẽ tồn tại lâu hơn phiên bản đầu tiên." - Ivar Jacobson, OOSE 1992.

• Quản lý sự phụ thuộc (dependency) kém:

Các sự phụ thuộc thực chất là có thể kiểm soát được.

• Các công cụ để giải quyết:

Các nguyên lý thiết kế hướng đối tượng (OO-design principles), các mẫu thiết kế (design patterns).

Các hướng dẫn cốt lõi: coupling (sự liên kết), cohesion (sự gắn kết).

• Inevitably changing requirements

"All systems change during their life-cycles. This must be born in mind when developing systems expected to last longer than the first version." - Ivar Jacobson, OOSE 1992

• Poor dependency management:

Dependencies can be controlled

• Tools:

OO-design principles, design patterns

Guidelines: coupling, cohesion

4. Các Nguyên lý Thiết kế Hướng Đối Tượng (OO Design Principles)

• Mục tiêu: Nhằm tạo ra các hệ thống Hướng đối tượng có thể tái sử dụng, dễ mở rộng và dễ bảo trì.
• Các nguyên lý này làm nền tảng cho các patterns (mẫu thiết kế), giúp bạn đối phó với những sự thay đổi.

Danh sách các Nguyên lý Thiết kế:

Đóng gói những gì thay đổi (Encapsulate what varies)

Ưu tiên Composition (Thành phần) hơn Inheritance (Kế thừa)

Lập trình với Interface, không phải Implementation

Nguyên lý Đơn trách nhiệm (Single Responsibility Principle - SRP)

Nguyên lý Đóng/Mở (Open Closed Principle - OCP)

Nguyên lý Thay thế Liskov (Liskov Substitution Principle - LSP)

Nguyên lý Đảo ngược Phụ thuộc (Dependency Inversion Principle - DIP)

Nguyên lý Phân tách Interface (Interface Segregation Principle - ISP)

• To create reusable, extensible and maintainable OO systems
• Underlie the patterns, help you to cope changes.

Design Principles:

Encapsulate what varies

Favor Composition Over Inheritance

Program To An Interface, Not An Implementation

(SRP) The Single Responsibility Principle

(OCP) The Open Closed Principle

(LSP) The Liskov Substitution Principle

(DIP) The Dependency Inversion Principle

(ISP) The Interface Segregation Principle

5. Nguyên lý 1: Đóng gói những gì thay đổi (Encapsulate what varies)

Tách biệt những gì thay đổi khỏi những gì giữ nguyên
• Xác định các khía cạnh của ứng dụng có sự thay đổi và tách biệt chúng khỏi những phần luôn giữ nguyên.
• Nếu bạn có một vài khía cạnh trong code đang bị thay đổi (ví dụ: thay đổi ở mỗi yêu cầu mới), thì tức là bạn đang có một hành vi cần được kéo ra và tách khỏi tất cả những thứ không thay đổi.
Lấy những phần thay đổi đó và đóng gói chúng lại, để sau này bạn có thể thay đổi hoặc mở rộng mà không làm ảnh hưởng đến những phần luôn giữ nguyên.

Ví dụ về ứng dụng thương mại điện tử:
Giả sử chúng xuất có một ứng dụng thương mại điện tử cho phép khách hàng đặt hàng và thanh toán.
• Một trong những yêu cầu của ứng dụng là hỗ trợ nhiều cổng thanh toán (payment gateways), chẳng hạn như PayPal, CreditCard, và Bitcoin.
• Mỗi cổng thanh toán có một API khác nhau và yêu cầu một tập hợp các tham số khác nhau để xử lý thanh toán.

Code Logic thanh toán bị Hardcode (Thiết kế tồi):

class PaymentProcessor {
    public void processPayment(String method, double amount) {
        if (method.equals("PayPal")) {
            System.out.println("Đang xử lý thanh toán PayPal: $" + amount);
            // Gọi API PayPal
        } else if (method.equals("CreditCard")) {
            System.out.println("Đang xử lý thanh toán CreditCard: $" + amount);
            // Gọi API CreditCard
        } else if (method.equals("Bitcoin")) {
            System.out.println("Đang xử lý thanh toán Bitcoin: $" + amount);
            // Gọi API Bitcoin
        }
    }
}


Giải pháp sử dụng Interface để đóng gói sự thay đổi:

interface PaymentStrategy {
    void processPayment(double amount);
}

class PayPalPayment implements PaymentStrategy {
    @Override
    public void processPayment(double amount) {
        System.out.println("Đang xử lý thanh toán PayPal: $" + amount);
        // Gọi API PayPal
    }
}

class PaymentProcessor {
    // Ủy quyền cho Interface xử lý, tách biệt implementation bị thay đổi
    private PaymentStrategy paymentStrategy;

    public PaymentProcessor(PaymentStrategy paymentStrategy) {
        this.paymentStrategy = paymentStrategy;
    }

    public void processPayment(double amount) {
        paymentStrategy.processPayment(amount);
    }
}

public class Main {
    public static void main(String[] args) {
        PaymentStrategy method = new PayPalPayment();
        PaymentProcessor processor = new PaymentProcessor(method);
        processor.processPayment(100.0);
    }
}


Separate what changes from what stays the same
• Identify the aspects of application that vary and separate them from what stay the same
• If you've got some aspects of code that is changing, say with every new requirement, then you've got a behavior that needs to be pulled out and separated from all the stuff that doesn't change
Take the parts that vary and encapsulate them, so that later you can alter or extend without affecting those that don't vary.

Example an e-commerce application:
Let's say we have an e-commerce application that allows customers to place orders and make payments.
• One of the requirements of the application is to support multiple payment gateways, such as PayPal, CreditCard, and Bitcoin.
• Each payment gateway has a different API and requires a different set of parameters to process a payment.

Hardcoded Payment Logic:

class PaymentProcessor {
    public void processPayment(String method, double amount) {
        if (method.equals("PayPal")) {
            System.out.println("Processing PayPal: $" + amount);
            // PayPal API Call
        } else if (method.equals("CreditCard")) {
            System.out.println("Processing CreditCard: $" + amount);
            // CreditCard API Call
        } else if (method.equals("Bitcoin")) {
            System.out.println("Processing Bitcoin: $" + amount);
            // Bitcoin API Call
        }
    }
}


Solution:

interface PaymentStrategy {
    void processPayment(double amount);
}

class PayPalPayment implements PaymentStrategy {
    @Override
    public void processPayment(double amount) {
        System.out.println("Processing PayPal: $" + amount);
        // PayPal API Call
    }
}

class PaymentProcessor {
    private PaymentStrategy paymentStrategy;

    public PaymentProcessor(PaymentStrategy paymentStrategy) {
        this.paymentStrategy = paymentStrategy;
    }

    public void processPayment(double amount) {
        paymentStrategy.processPayment(amount);
    }
}

public class Main {
    public static void main(String[] args) {
        PaymentStrategy method = new PayPalPayment();
        PaymentProcessor processor = new PaymentProcessor(method);
        processor.processPayment(100.0);
    }
}


6. Ưu tiên Composition hơn Inheritance (Favor Composition Over Inheritance)

Hai phương pháp tái sử dụng thành phần
• Composition (Thành phần hóa): Mối quan hệ HAS-A (Có-một)

Là phương pháp tái sử dụng trong đó chức năng mới đạt được bằng cách tạo ra một đối tượng (object) bao gồm các đối tượng khác.

Chức năng mới có được bằng cách ủy quyền (delegating) chức năng cho một trong các đối tượng đang được chứa bên trong.

Composition có thể là: "By reference" (Tham chiếu) hoặc "By value" (Giá trị).

• Inheritance (Kế thừa): Mối quan hệ IS-A (Là-một)

Là phương pháp tái sử dụng trong đó chức năng mới đạt được bằng cách mở rộng quá trình thực thi (implementation) của một đối tượng có sẵn.

Lớp tổng quát hóa (lớp cha - superclass) nắm bắt rõ ràng các thuộc tính và phương thức chung.

Lớp chuyên biệt hóa (lớp con - subclass) mở rộng việc thực thi với các thuộc tính và phương thức bổ sung.

Ưu điểm/Nhược điểm của Composition
• Ưu điểm:

Các đối tượng bị chứa chỉ được lớp chứa truy cập hoàn toàn thông qua các interface của chúng.

Tái sử dụng theo kiểu "Hộp đen" (Black-box reuse), vì các chi tiết bên trong của đối tượng bị chứa không bị lộ ra ngoài.

Tính Đóng gói (Encapsulation) tốt.

Ít phụ thuộc vào việc thực thi (implementation dependencies) hơn.

Mỗi class chỉ tập trung vào đúng một nhiệm vụ.

Sự kết hợp (composition) có thể được xác định động tại thời điểm chạy (run-time) thông qua việc các đối tượng nhận tham chiếu đến các đối tượng khác cùng type.
• Nhược điểm:

Hệ thống tạo ra có xu hướng có nhiều object hơn.

Các Interface phải được thiết kế cẩn thận để có thể dùng nhiều đối tượng khác nhau làm các khối kết hợp.

Ưu điểm/Nhược điểm của Inheritance
• Ưu điểm:

Việc thực thi chức năng mới rất dễ dàng, do phần lớn mã đã được kế thừa.

Dễ dàng sửa đổi hoặc mở rộng phần implementation đang được tái sử dụng.
• Nhược điểm:

Phá vỡ tính Đóng gói, vì nó phơi bày cho lớp con các chi tiết implementation của lớp cha.

Tái sử dụng theo kiểu "Hộp trắng" (White-box reuse), vì chi tiết nội bộ của lớp cha thường bị nhìn thấy bởi các lớp con.

Các lớp con có thể buộc phải thay đổi nếu implementation của lớp cha thay đổi.

Các implementation kế thừa từ lớp cha không thể bị thay đổi tại thời điểm chạy (run-time).

Ví dụ So sánh Inheritance và Composition:
Trong ví dụ về Kế thừa, ta tạo một class InstrumentedHashSet kế thừa từ HashSet để đếm số lần thêm phần tử addCount. Ta ghi đè (override) cả hai phương thức add() và addAll().
Nghe có vẻ hợp lý đúng không? Nhưng khi test thử bằng cách dùng addAll() truyền vào mảng 3 phần tử, kết quả addCount lại bằng 6 thay vì 3.
Lý do là vì chi tiết cài đặt nội bộ của hàm addAll() trong lớp cha HashSet lại tự động gọi hàm add(). Do đó, đầu tiên ta cộng 3 vào addCount trong hàm addAll() của ta. Sau đó ta gọi super.addAll(). Với mỗi phần tử, addAll() của lớp cha lại gọi hàm add(), nhưng hàm add() này đã bị ta ghi đè (thêm 1 vào biến đếm). Hậu quả: mỗi phần tử bị đếm đến 2 lần.

Đây chính là vấn đề "Lớp cơ sở dễ vỡ" (Fragile base class): Chi tiết cài đặt của lớp cha đã ảnh hưởng tiêu cực đến hoạt động của lớp con.
Cách tốt nhất để sửa là sử dụng Composition. Lớp InstrumentedSet (còn gọi là wrapper class) sẽ chứa một object Set bên trong nó, sao chép lại interface của Set, và mọi hành động của Set thực chất sẽ được chuyển tiếp (forwarding) cho đối tượng Set bên trong. Đây là một ví dụ tuyệt vời về sự ủy quyền thông qua Composition!

public class InstrumentedSet implements Set {
    private final Set s;
    private int addCount = 0;
    
    public InstrumentedSet(Set s) { 
        this.s = s; 
    }
    
    public boolean add(Object o) {
        addCount++;
        return s.add(o);
    }
    
    public boolean addAll(Collection c) {
        addCount += c.size();
        return s.addAll(c);
    }
    
    public int getAddCount() { 
        return addCount; 
    }
    
    // Forwarding rest methods of the Set interface methods
    public void clear() { 
        s.clear(); 
    }
}


Two method of reuse components
• Composition: HAS-A relationship

Method of reuse in which new functionality is obtained by creating an object composed of other objects

The new functionality is obtained by delegating functionality to one of the objects being composed

Composition can be: "By reference" or "By value"

• Inheritance: IS-A relationship

Method of reuse in which new functionality is obtained by extending the implementation of an existing object

The generalization class (the superclass) explicitly captures the common attributes and methods

The specialization class (the subclass) extends the implementation with additional attributes and methods

Advantages/Disadvantages Of Composition
• Advantages:

Contained objects are accessed by the containing class solely through their interfaces

"Black-box" reuse, since internal details of contained objects are not visible

Good encapsulation

Fewer implementation dependencies

Each class is focused on just one task

The composition can be defined dynamically at run-time through objects acquiring references to other objects of the same type
• Disadvantages:

Resulting systems tend to have more objects

Interfaces must be carefully defined in order to use many different objects as composition blocks.

Advantages/Disadvantages of Inheritance
• Advantages:

New implementation is easy, since most of it is inherited

Easy to modify or extend the implementation being reused
• Disadvantages:

Breaks encapsulation, since it exposes a subclass to implementation details of its superclass

"White-box" reuse, since internal details of superclasses are often visible to subclasses

Subclasses may have to be changed if the implementation of the superclass changes

Implementations inherited from superclasses can not be changed at run-time

Inheritance vs Composition Example

public class InstrumentedHashSet extends HashSet {
    private int addCount = 0;
    
    public boolean add (Object o) {
        addCount++;
        return super.add(o);
    }
    
    public boolean addAll(Collection c) {
        addCount += c.size();
        return super.addAll(c);
    }
    
    public int getAddCount() { 
        return addCount; 
    }
}


Looks good, right. Let's test it! We get a result of 6, not the expected 3. Why?
It's because the internal implementation of addAll() in the HashSet superclass itself invokes the add() method. So first we add 3 to addCount in InstrumentedHashSet's addAll(). Then we invoke HashSet's addAll(). For each element, this addAll() invokes the add() method, which as overridden by InstrumentedHashSet adds one for each element. The result: each element is double counted.

This is "fragile base class" problem: Implementation details of our superclass affected the operation of our subclass.
The best way to fix this is to use composition. InstrumentedSet is known as a wrapper class, since it wraps an instance of a Set object. This is an example of delegation through composition!

public class InstrumentedSet implements Set {
    private final Set s;
    private int addCount = 0;
    
    public InstrumentedSet(Set s) { 
        this.s = s; 
    }
    
    public boolean add(Object o) {
        addCount++;
        return s.add(o);
    }
    
    public boolean addAll(Collection c) {
        addCount += c.size();
        return s.addAll(c);
    }
    
    public int getAddCount() { 
        return addCount; 
    }
    
    // Forwarding rest methods of the Set interface methods
    public void clear() { 
        s.clear(); 
    }
}


7. Nguyên lý 3: Lập trình với Interface (Program To An Interface)

• Interface là tập hợp các phương thức mà một đối tượng biết rằng nó có thể gọi trên một đối tượng khác.
• Một đối tượng có thể có nhiều interface. Một interface là một tập con của tất cả các phương thức mà đối tượng đó triển khai. "Type" (kiểu) là một interface cụ thể của đối tượng.
• Các đối tượng khác nhau có thể có cùng chung Type, và cùng một đối tượng có thể có nhiều Type khác nhau.
• Một đối tượng chỉ được các đối tượng khác biết đến thông qua interface của nó.
• Interface chính là chìa khóa cho khả năng lắp ghép (pluggability)!

Lập trình với Interface, không phải Implementation
• Đừng khai báo các biến là các bản thể (instances) của các concrete classes cụ thể. Thay vào đó, hãy chỉ gắn kết với một interface được định nghĩa bởi một abstract class (lớp trừu tượng).
Ưu điểm:

Client hoàn toàn không nhận biết (không cần biết) về class cụ thể của đối tượng mà chúng đang sử dụng.

Đối tượng này có thể dễ dàng bị thay thế bằng một đối tượng khác.

Các kết nối đối tượng không cần phải ghim cứng (hardwired) vào một đối tượng của một class cụ thể, qua đó tăng cường tính linh hoạt.

Nới lỏng sự liên kết (Loosens coupling).

Tăng cường khả năng tái sử dụng.

Cải thiện cơ hội áp dụng Composition vì đối tượng được chứa có thể thuộc về bất kỳ class nào miễn là nó triển khai một interface cụ thể.
Nhược điểm:

Làm tăng đôi chút độ phức tạp của thiết kế.

(Ví dụ: Điều khiển một phương tiện)

Lập trình dựa trên Implementation: Hàm chính gọi trực tiếp phương thức của lớp Car. Nếu muốn đổi sang Boat, phải sửa code gọi hàm.

Lập trình dựa trên Interface: Cả Car, Boat đều implements IManeuverable. Hàm travel() chỉ nhận tham số đầu vào là IManeuverable vehicle, do đó truyền Car hay Boat vào đều chạy tốt mà không cần sửa code hàm travel().

// Lập trình dựa trên Interface (Tốt)
interface IManeuverable {
    void left();
}

class Car implements IManeuverable { /* ... */ }
class Boat implements IManeuverable { /* ... */ }

public void travel(IManeuverable vehicle) {
    vehicle.left();
}


• An interface is the set of methods one object knows it can invoke on another object
• An object can have many interfaces. An interface is a subset of all the methods that an object implements. A type is a specific interface of an object.
• Different objects can have the same type and the same object can have many different types.
• An object is known by other objects only through its interface.
• Interfaces are the key to pluggability!

Program to an interface, not an implementation
• Don't declare variables to be instances of particular concrete classes. Instead, commit only to an interface defined by an abstract class.
Advantages:

Clients are unaware (not known) of the specific class of the object they use

One object can be easily replaced by another

Object connections need not be hardwired to an object of a specific class, thereby increasing flexibility

Loosens coupling

Increases likelihood of reuse

Improves opportunities for composition since contained objects can be of any class that implements a specific interface
Disadvantages:

Modest increase in design complexity

(Example: Controlling a vehicle)

// Program to implement (Bad)
class Car {
    void left() { 
        System.out.println("Car is turning left."); 
    }
}

public static void main(String[] args) {
    Car c = new Car();
    c.left(); 
}

// Program to interface (Good)
interface IManeuverable {
    void left();
}

class Car implements IManeuverable { /* ... */ }
class Boat implements IManeuverable { /* ... */ }

public void travel(IManeuverable vehicle) {
    vehicle.left();
}


8. Nguyên lý 4: Nguyên lý Đơn trách nhiệm (Single Responsibility Principle - SRP)

Một class chỉ nên có duy nhất một lý do để thay đổi.
• Nguyên lý này còn được biết đến là tính gắn kết (cohesion).
Lý do cốt lõi đằng sau nguyên lý:

Khi các yêu cầu thay đổi, sự thay đổi đó sẽ được biểu hiện thông qua sự thay đổi về mặt trách nhiệm giữa các class.

Một trách nhiệm "gắn kết" là một trục thay đổi duy nhất - các thay đổi về yêu cầu thường chỉ giới hạn ở một vài trách nhiệm có tính gắn kết với nhau.

Do đó, để tránh việc liên kết (coupling) các trách nhiệm vốn dĩ thay đổi vì những lý do hoàn toàn khác nhau, một class chỉ nên có một trách nhiệm, tức là một lý do duy nhất để thay đổi.

Sự vi phạm SRP gây ra các phụ thuộc bắc cầu giả tạo giữa các module rất khó để đoán trước, nói cách khác, nó gây ra sự "dễ vỡ" (fragility) cho hệ thống.

Trách nhiệm là gì?
• Trách nhiệm được coi là một tập hợp chức năng lớn hơn phục vụ cho đúng một mục đích.
• Việc nhìn ra được các trách nhiệm của một class đôi khi rất khó. Bạn thực sự không thể hiểu được các trách nhiệm của class đó nếu không hiểu rõ nhu cầu của các client đang sử dụng class đó.
• Trong bối cảnh của SRP, bạn nên nhìn nhận các trách nhiệm như là "các lý do để thay đổi", tức là làm thế nào những thay đổi khả thi trong nhu cầu của client được phản ánh lại vào một module hoặc một class duy nhất.
• Trách nhiệm là một trục thay đổi nếu sự thay đổi đó thực sự sẽ xảy ra. Đoán trước sự thay đổi là rất khó, do đó áp dụng SRP quá mức sẽ dẫn đến độ phức tạp không cần thiết (needless complexity). Đừng áp dụng SRP nếu hệ thống chưa xuất hiện triệu chứng bất ổn.

(Ví dụ minh họa)

// Vi phạm SRP: Lớp có nhiều trách nhiệm
class Employee {
    void calculateSalary() { /* Tính lương */ }
    void generateReport() { /* Xuất báo cáo */ }
    void sendEmail() { /* Gửi email */ }
}

// Tuân thủ SRP: Tách ra các lớp cohesive
class SalaryCalculator { 
    void calculateSalary(Employee e) { /* ... */ } 
}
class ReportGenerator { 
    void generateReport(Employee e) { /* ... */ } 
}
class EmailSender { 
    void sendEmail(String to, String msg) { /* ... */ } 
}


Ví dụ Hình chữ nhật (Rectangle) và Giao diện (GUI)
Nếu class Rectangle chứa hàm area() (Tính diện tích hình học) và draw() (Vẽ đồ họa), nó đang ôm đồm 2 trách nhiệm. Nếu ứng dụng hình học thay đổi cũng làm Rectangle thay đổi, và nếu ứng dụng đồ họa thay đổi thì Rectangle cũng đổi. Thiết kế tốt hơn là tách làm 2 class riêng biệt: GeometricRectangle (chỉ quản lý diện tích) và Rectangle (chỉ quản lý đồ họa).

Tách biệt trách nhiệm bằng Interface (Ví dụ Modem)
Nhiều lúc không thể dùng giải pháp tiêu chuẩn là xé nhỏ một class (ví dụ class phần cứng Modem). Lúc này, việc tách biệt trách nhiệm thành 2 interface (DataChannel - Kênh truyền dữ liệu, và Connection - Trạng thái kết nối) sẽ giúp tháo gỡ hai nhóm trách nhiệm này khỏi phần còn lại của ứng dụng. Điều này vẫn mang lại cho ta hầu hết các lợi ích của nguyên lý SRP.

A class should have only one reason to change.
• Also known as cohesion.
Rational behind the principle:

When the requirements change, that change will be manifest through a change in responsibility among the classes.

A "cohesive" responsibility is a single axis of change - requirement changes often are restricted to a few cohesive responsibilities

Thus, to avoid coupling responsibilities that change for different reasons, a class should have only one responsibility, one reason to change.

Violation of SRP causes spurious transitive dependencies between modules that are hard to anticipate, in other words fragility.

What is a 'responsibility'?
• A responsibility is thought of being a larger set of functionality that serves one purpose.
• Seeing the responsibilities of a class may be hard. You really can not understand the responsibilities of a class without understanding the needs of the clients of that class.
• In the context of SRP you should look at responsibilities as "reasons to change", i.e. how are possible changes in the needs of the clients reflected to a single module or class.
• A responsibility is an axis of change if that change will really occur. Anticipating change is hard, SRP applied too often leads to needless complexity. Do not apply SRP if there is no symptom.

(Examples)

// Bad: Violates SRP
class Employee {
    void calculateSalary() { /* ... */ }
    void generateReport() { /* ... */ }
    void sendEmail() { /* ... */ }
}

// Good: Complies with SRP
class SalaryCalculator { 
    void calculateSalary(Employee e) { /* ... */ } 
}
class ReportGenerator { 
    void generateReport(Employee e) { /* ... */ } 
}
class EmailSender { 
    void sendEmail(String to, String msg) { /* ... */ } 
}


Separating the responsibilities (Modem Example)
Often it is not possible to use the standard solution - splitting the class. Separating the responsibilities into two interfaces decouples the two responsibilities as far as rest of the application is concerned. This yields us most of the benefits of SRP.
<<interface>> DataChannel (send, recv) and <<interface>> Connection (dial, hangup). Both implemented by ModemImplementation.

9. Nguyên lý 5: Nguyên lý Đóng/Mở (The Open-Closed Principle - OCP)

Các Thực Thể Phần Mềm Nên Mở Để Mở Rộng, Nhưng Đóng Đối Với Sự Sửa Đổi.
• OCP khuyên rằng chúng ta nên cố gắng thiết kế ra các module mà không bao giờ cần phải thay đổi chúng.
• Để mở rộng hành vi của hệ thống, chúng ta thêm các đoạn code mới. Chúng ta không được sửa đổi code cũ.
Các module tuân thủ OCP sẽ đáp ứng 2 tiêu chí:

Mở để Mở rộng (Open For Extension): Hành vi của module có thể được mở rộng ra để đáp ứng các yêu cầu mới.

Đóng để Sửa đổi (Closed For Modification): Mã nguồn (source code) của module không được phép thay đổi.
Làm sao để làm được điều này? Thông qua Trừu tượng hóa (Abstraction), Đa hình (Polymorphism), Kế thừa (Inheritance) và Interfaces.
Việc mọi module trong hệ thống đều thỏa mãn OCP là điều không thể, nhưng ta nên cố gắng giảm thiểu số lượng module không tuân thủ nó. Nguyên lý Đóng-Mở thực sự là "trái tim" của thiết kế Hướng đối tượng (OO design).

Ví dụ về tính giá tiền:
Hàm totalPrice ban đầu dùng hàng loạt lệnh if (parts[i] instanceof Motherboard) để kiểm tra các loại phụ tùng và áp dụng mức giá tương ứng.
Thiết kế này có tuân thủ OCP không? Tuyệt đối không! Mỗi khi bộ phận Kế toán ban hành một chính sách giá mới, chúng ta lại phải chui vào sửa code của hàm totalPrice(). Nó không hề "Closed For Modification".

Giải pháp tốt hơn:
Tạo ra một class PricePolicy độc lập để quản lý các chính sách giá khác nhau (áp dụng hệ số factor). Bên trong class Part, chứa một object PricePolicy. Nhờ giải pháp này, ta có thể cài đặt linh động các chính sách giá mới ngay trong lúc chạy chương trình (run-time) chỉ bằng cách đổi object PricePolicy mà không cần sửa đổi bất kỳ code cốt lõi nào của lớp Part hay hàm tính tổng.

public class Part {
    private double price;
    private PricePolicy pricePolicy; // Sử dụng composition

    public void setPricePolicy(PricePolicy pricePolicy) {
        this.pricePolicy = pricePolicy;
    }
    
    public double getPrice() {
        return pricePolicy.getPrice(price);
    }
}

public class PricePolicy {
    private double factor;
    
    public PricePolicy(double factor) { 
        this.factor = factor; 
    }
    
    public double getPrice(double price) { 
        return price * factor; 
    }
}


Software Entities Should Be Open For Extension, Yet Closed For Modification.
• OCP says that we should attempt (try) to design modules that never need to be changed
• To extend the behavior of the system, we add new code. We do not modify old code.
Modules that conform to the OCP meet two criteria:

Open For Extension: The behavior of the module can be extended to meet new requirements.

Closed For Modification: the source code of the module is not allowed to change.
How can we do this? Abstraction, Polymorphism, Inheritance, Interfaces.
It is not possible to have all the modules of a software system satisfy the OCP, but we should attempt to minimize the number of modules that do not satisfy it. The Open-Closed Principle is really the heart of OO design.

Open-Closed Principle Example

// Bad: Violates OCP
public double totalPrice(Part[] parts) {
    double total = 0.0;
    for (int i=0; i<parts.length; i++) {
        if (parts[i] instanceof Motherboard) {
            total += (1.45 * parts[i].getPrice());
        } else if (parts[i] instanceof Memory) {
            total += (1.27 * parts[i].getPrice());
        } else {
            total += parts[i].getPrice();
        }
    }
    return total;
}


Does this conform to the OCP? No way! Every time the Accounting Department comes out with a new pricing policy, we have to modify the totalPrice() method!

Better Idea

public class Part {
    private double price;
    private PricePolicy pricePolicy; // Using composition

    public void setPricePolicy(PricePolicy pricePolicy) {
        this.pricePolicy = pricePolicy;
    }
    
    public double getPrice() {
        return pricePolicy.getPrice(price);
    }
}

public class PricePolicy {
    private double factor;
    
    public PricePolicy(double factor) { 
        this.factor = factor; 
    }
    
    public double getPrice(double price) { 
        return price * factor; 
    }
}


10. Nguyên lý 6: Nguyên lý Thay thế Liskov (The Liskov Substitution Principle - LSP)

Các Hàm (Functions) Sử Dụng Tham Chiếu (References) Đến Các Lớp Cơ Sở (Lớp cha) Phải Có Khả Năng Sử Dụng Các Đối Tượng Của Lớp Dẫn Xuất (Lớp con) Mà Không Cần Phải Nhận Biết Về Sự Khác Biệt Đó.
• Nguyên lý Thay thế Liskov (LSP) có vẻ rất hiển nhiên nếu xét trên mọi thứ chúng ta đã biết về tính Đa hình (polymorphism).
• Lấy ví dụ: Khi xây dựng một hàm drawShape(Shape s), hàm này phải hoạt động trơn tru với bất kỳ lớp con nào (ví dụ Circle, Rectangle) được kế thừa từ lớp cha Shape (hoặc nếu Shape là Interface, nó phải chạy được với mọi class triển khai Shape).
• Tuy nhiên, chúng ta phải cực kỳ cẩn thận trong quá trình xây dựng mã ở các lớp con để đảm bảo rằng chúng ta không vô tình phá vỡ nguyên lý LSP (như thay đổi hoàn toàn ý nghĩa cốt lõi của hành vi ở lớp cha).

public void drawShape(Shape s) {
    // Thực thi vẽ khối hình s mà không cần quan tâm nó là hình gì
}


Functions That Use References To Base (Super) Classes Must Be Able To Use Objects Of Derived (Sub) Classes Without Knowing It.
• The Liskov Substitution Principle (LSP) seems obvious given all we know about polymorphism.
• For example:

public void drawShape(Shape s) {
    // Code here.
}


• The drawShape method should work with any subclass of the Shape superclass (or, if Shape is a Java interface, it should work with any class that implements the Shape interface).
• But we must be careful when we implement subclasses to insure that we do not unintentionally violate the LSP.

11. Nguyên lý 7: Nguyên lý Đảo ngược Phụ thuộc (The Dependency Inversion Principle - DIP)

Các Module Cấp Cao Không Nên Phụ Thuộc Vào Các Module Cấp Thấp. Cả Hai Nên Phụ Thuộc Vào Các Abstractions (Trừu tượng).
Abstractions Không Nên Phụ Thuộc Vào Các Chi Tiết. Các Chi Tiết Phải Phụ Thuộc Vào Abstractions.

Tại sao lại gọi là "Sự đảo ngược" (Inversion)?
• Việc phát triển phần mềm theo kiểu truyền thống thường tạo ra các cấu trúc mà ở đó module cấp cao phụ thuộc vào module cấp thấp, các policy (hoặc logic nghiệp vụ) bị bắt ép phải phụ thuộc vào các chi tiết vụn vặt.

Những thay đổi ở module thực thi cấp thấp sẽ lan truyền ngược lên các module cấp cao, đây là điều không thể chấp nhận được.

Việc tái sử dụng các module cấp cao trở nên cực kỳ khó khăn.
• Cấu trúc phụ thuộc của một phần mềm Hướng đối tượng (OO) được thiết kế tốt phải là sự đảo ngược.

Không có sự lan truyền của sự thay đổi, dễ dàng tái sử dụng hơn.
• Các module cấp cao chứa đựng mô hình nghiệp vụ quan trọng của ứng dụng. Tầng cấp cao này phải hoàn toàn độc lập với các chi tiết.
• Các module cấp cao mang tính định hình chính sách (policy setting modules) nên là tâm điểm của việc tái sử dụng: những lợi ích lớn nhất có thể đạt được ở chính chỗ này.
• Tư duy này là trái tim của việc thiết kế các Framework.

Ai là chủ sở hữu của Interface?
• Cách làm thông thường là có một module thực thi một bộ dịch vụ và khai báo ra một interface công khai cho bất kỳ client nào cần đến dịch vụ đó (kiểu phân tầng ngây ngô - naive layering).
• DIP thường mang lại sự đảo ngược về quyền sở hữu (inversion of ownership) đối với các interface, bên cạnh sự đảo ngược về phụ thuộc.

Client là người sở hữu các interface trừu tượng, còn bộ phận thực thi (implementation) sẽ triển khai những gì client cần.

Chính sự đảo ngược về quyền sở hữu này đã bảo vệ tầng cấp cao khỏi các thay đổi xảy ra từ những tầng thấp hơn. Tính tái sử dụng của các tầng cấp cao nhờ đó được cải thiện.

Tìm kiếm sự trừu tượng cốt lõi (underlying abstraction)
• Bạn nên "trừu tượng hóa" phần chính sách cấp cao, nhưng tìm nó bằng cách nào?

Dựa vào nhiệm vụ chính yếu của hệ thống.

Dựa vào những thứ không bao giờ biến đổi khi các chi tiết thay đổi.
• Ví dụ: Đối tượng Button (Nút bấm) và Lamp (Bóng đèn). Một thiết kế ngây ngô sẽ vi phạm DIP: đó là logic cấp cao của Button bị phụ thuộc trực tiếp vào chi tiết nội bộ của Lamp.

Sự trừu tượng cốt lõi ở đây thực chất là nhận diện cử chỉ bật/tắt (on/off gesture) từ phía người dùng và truyền cử chỉ đó đến một đối tượng đích (target object) bất kỳ.

Bằng cách đổi tên interface thành SwitchableDevice (Thiết bị có thể bật tắt), ta thấy ngay là nó không còn bị phụ thuộc vào Button nữa. Vậy ai sở hữu interface SwitchableDevice? Không ai cả, hãy đặt nó vào một package riêng (trong Java) và việc này sẽ giúp tách rời (decouple) các class nhận biết môi trường với các class tạo ra ảnh hưởng lên môi trường bên ngoài.

(Vấn đề Vẽ và Hình Elip - Drawing/Eclipse)
Vấn đề gặp phải: Làm sao để cập nhật một đối tượng Eclipse (Hình Elip) mới từ cái cũ khi nó di chuyển sang vị trí khác? Phải xóa cái cũ ở điểm hiện tại -> Đổi sang điểm mới -> Vẽ cái mới.
Lỗi vi phạm: Class Drawing đang phụ thuộc trực tiếp vào class Eclipse cấp thấp. Hàm Move bị phụ thuộc trực tiếp vào 3 hàm Erase, ChangePoint, Draw của Elip.
Giải pháp cải tiến: Drawing phụ thuộc vào abstract class Shape. Hàm tổng MoveShape và các hàm chi tiết sẽ được triển khai bởi các lớp con như Eclipse, Circle. Đây là ứng dụng thực tế của mẫu thiết kế Template Method.

High-level modules should not depend on low level modules. Both should depend on abstractions.
Abstractions should not depend on details. Details should depend on abstractions.

Why call it "inversion"?
• Traditional software development tends to create structures where high-level modules depend on low-level modules, the policy (or business logic) gets to depend on details.

changes to low-level implementation modules propagate to high-level modules, which is unacceptable.

reuse of high-level modules becomes very difficult.
• The dependency structure of a well designed OO software is inverted.

no propagation of change, easier reuse.
• High-level modules contain the important business model of the application. This high-level should be independent (độc lập) of details.
• The high-level policy setting modules should be the focus of reuse: greatest benefits are achievable here.
• This thinking is in the heart of framework design.

Who owns the interface?
• The common way is to have a module implementing a set of services and declaring a public interface for any client needing these services (naive layering).
• DIP often brings about an inversion of interface ownership in addition to inversion of dependencies.

clients own the abstract interfaces, implementations implement what clients need.

it is this inversion of ownership that protects the high-level layer from changes from lower layers. Reusability of higher level layers is improved.

Finding the underlying abstraction
• You should "abstract out" the high-level policy, but how to find it?

the main task of the system

the things that do not vary when details change
• Example: button object and a lamp object. A naive design that violates the DIP - the high level logic of Button depends on details of lamp.

The underlying abstraction here is to detect an on/off gesture from the user and to rely that gesture to target object.

Change the name of the interface to "SwitchableDevice" to see that there is no dependency on Button. Who owns the interface SwitchableDevice? No-one, put it in an own package (Java) and it decouples the classes that sense the environment from classes that affect the external environment.

(Drawing/Eclipse Problem)
Problems: How to update a new Eclipse from old Eclipse when it moved to other position? Erase old Eclipse at the current point -> Change new point -> Draw new Eclipse.
Violation points: Drawing class depends on Eclipse class. MoveEclipse() depends on EraseEclipse(), ChangePoint(), DrawEclipse().
Improvement: Drawing depends on abstract class Shape. MoveShape abstract methods are implemented by child classes (Eclipse, Circle). (Template Method design pattern).

12. Tổng quan về Mẫu Thiết kế (Design Patterns)

Pattern (Mẫu thiết kế) là gì?
• Pattern mô tả một vấn đề xảy ra lặp đi lặp lại nhiều lần trong môi trường của chúng ta, và sau đó nó mô tả phần cốt lõi của giải pháp cho vấn đề đó, theo một cách mà bạn có thể tái sử dụng giải pháp này hàng triệu lần, mà không bao giờ phải làm theo một cách y hệt nhau hai lần. (Theo Alexander)

Học về Patterns (Lý thuyết Kiện tướng Cờ vua)
• Những giải pháp thành công trong nhiều lĩnh vực nỗ lực của con người đều có nguồn gốc sâu xa từ các pattern. Trên thực tế, một mục tiêu quan trọng của giáo dục là truyền đạt các pattern học tập từ thế hệ này sang thế hệ khác.
• Việc học cách phát triển một phần mềm tốt rất giống với việc học cách chơi cờ vua giỏi!
• Đầu tiên là học các quy tắc luật lệ (thuật toán, cấu trúc dữ liệu, ngôn ngữ lập trình). Sau đó học các nguyên lý (lập trình có cấu trúc, các nguyên lý Hướng đối tượng). Tuy nhiên, để trở thành một Bậc thầy (Master) về thiết kế phần mềm, người ta bắt buộc phải nghiên cứu thiết kế của những bậc thầy đi trước. Những thiết kế của họ chứa đựng các Patterns (Mẫu) cần được thấu hiểu, ghi nhớ và áp dụng lặp đi lặp lại trong thực tế.

Tổng quan về Patterns và Frameworks
• Patterns (Mẫu thiết kế) hỗ trợ việc tái sử dụng kiến trúc và thiết kế phần mềm. Pattern mô tả các cấu trúc tĩnh và động, cũng như sự phối hợp của các giải pháp thành công nhằm giải quyết các vấn đề phát sinh khi xây dựng ứng dụng trong một lĩnh vực cụ thể.
• Frameworks (Khung làm việc) hỗ trợ việc tái sử dụng các thiết kế chi tiết và mã nguồn (code). Framework là một tập hợp các thành phần được tích hợp để phối hợp làm việc nhằm cung cấp một kiến trúc có thể tái sử dụng cho một nhóm các ứng dụng có liên quan đến nhau.

Không gian Design Pattern (Phân loại)
• Creational Patterns (Mẫu Khởi tạo): Giải quyết các vấn đề liên quan đến việc khởi tạo và cấu hình các classes và objects.
• Structural Patterns (Mẫu Cấu trúc): Giải quyết các vấn đề về việc tháo gỡ liên kết (decoupling) giữa phần Interface và phần Implementation của các classes và objects.
• Behavioral Patterns (Mẫu Hành vi): Giải quyết các vấn đề xoay quanh sự tương tác giữa các classes và objects.

Phạm vi (Scope) áp dụng:
• Class Patterns (Phạm vi Lớp): Tập trung vào mối quan hệ giữa các lớp (classes) và lớp con (subclasses) của chúng. Liên quan chặt chẽ đến sự tái sử dụng bằng Kế thừa (Inheritance).
• Object Patterns (Phạm vi Đối tượng): Tập trung vào mối quan hệ giữa các đối tượng (objects). Liên quan chặt cụ đến sự tái sử dụng bằng Thành phần hóa (Composition).

What are Patterns?
• The pattern describes a problem which occurs over and over again in our environment, and then describes the core of the solution to that problem, in such a way that you can use this solution a million times over, without ever doing it the same way twice. (Alexander)

Learning Patterns
• Successful solutions to many areas of human endeavor are deeply rooted in patterns. In fact, an important goal of education is transmitting patterns of learning from generation to generation.
• Learning to develop good software is similar to learning to play good chess!
• First learn the rules (algorithms, data structures, languages). Then learn the principles (structured programming, OO principles). However, to become a master of software design, one must study the designs of other masters. These designs contain patterns that must be understood, memorized and applied repeatedly.

Overview of Patterns and Frameworks
• Patterns support reuse of software architecture and design. Patterns capture the static and dynamic structures and collaborations of successful solutions to problems that arise when building applications in a particular domain.
• Frameworks support reuse of detailed design and code. A framework is an integrated set of components that collaborate to provide a reusable architecture for a family of related applications.

Design Pattern Space
• Creational Patterns: Deal with initializing and configuring classes and objects.
• Structural Patterns: Deal with decoupling interface and implementation of classes and objects.
• Behavioral Patterns: Deal with interactions among classes and objects.

Scope:
• Class Patterns: Focus on the relationships between classes and their subclasses (Involve inheritance reuse).
• Object Patterns: Focus on relationships between objects (Involve composition reuse).