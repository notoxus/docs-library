# ĐỒ THỊ PHẲNG

## Khái niệm và định nghĩa

Khái niệm: Là *đồ thị* mà ta có thể *vẽ nó trên một mặt phẳng sao cho không có hai cạnh nào cắt nhau*.

Đặc điểm:
- Các cạnh đồ thị phẳng chia mặt phẳng thành các *miền* (Region).
- Phần giới hạn bởi chu trình đơn, không chứa trong chu trình đơn khác gọi là *miền hữu hạn*.
- Mọi đồ thị phẳng luôn có duy nhất 1 miền vô hạn.
- *Biên* là chu trình giới hạn miền.

ứng dụng: Xây dựng mạng giao thông giữa các thành phố.
Đỉnh: Thành phố.
Cạnh: Đường đi giữa các thành phố.
Biểu diễn được bằng đồ thị phẳng -> Không cần cầu vượt, hầm chui.

## Công thức Euler

1. Cho G là đơn đồ thị phẳng liên thông với
• e cạnh,
• v đỉnh,
• r miền (trên biểu diễn phẳng của G)
• Khi đó công thức
					[r - e + v = 2]
- Khi bỏ 1 cạnh, số miền giảm 1
2. G là một đồ thị phẳng với v đỉnh, e cạnh, r miền, và p là số thành phần liên thông. Thì ta có 
công thức Euler mở rộng:
					[v - e + r = p + 1]

### Các hệ quả:

1. Giả sử G là đơn đồ thị phẳng liên thông với v đỉnh, trong đó *v ≥ 3*, có e cạnh. Khi đó
					[e ≤ 3v – 6]
2. Giả sử G là đơn đồ thị phẳng liên thông với v đỉnh, trong đó *có 1 đỉnh có bậc không quá 5*. khi đó
					[𝒓 ≤ 𝟐e/3]
3. *K5* không phải đồ thị phẳng (Có thể suy ra từ HQ1&2).
4. Giả sử G là đơn đồ thị phẳng liên thông với v đỉnh, v ≥ 3 và không chu trình với độ dài là 3
(không chứa tam giác). Khi đó:
					[e ≤ 2v – 4]
5. K3,3 không phải đồ thị phẳng (Có thể chứng minh bằng hệ quả 4).

### Một số đồ thị không phẳng:

• Các đồ thị K1, K2, K3, K4 là các đồ thị phẳng. Đồ thị K5 không là đồ thị phẳng.
• Đồ thị Km,n (m,n≥3) là đồ thị không phẳng vì chứa đồ thị con 𝐾3,3.
- Định lý: Cho H là đồ thị con của đồ thị G:
o Nếu G phẳng → H phẳng.
o Nếu H không phẳng → G không phẳng.

## Đai của đồ thị:
Định nghĩa: Cho một đồ thị G
▪ Đai (girth) là chu trình đơn giản ngắn nhất trong G, kí hiệu: g.
▪ Số g = số chu trình đơn giản ngắn nhất trong G.
▪ Trường hợp nếu G không có chu trình thì g = ∞.

## Bất đẳng thức EV:

Cho G là đồ thị liên thông có n đỉnh, m cạnh và đai là g≥3. Nếu G phẳng thì ta có bất đẳng thức:
				[m <= g(n-2)/g-2]

## Định lý KURATOWSKI

Phép phân chia sơ cấp:
• Cho đồ thị 𝐺 = (𝑉, 𝐸) . Chọn một cạnh (𝑢, 𝑣) ∈ 𝐸.
• Thực hiện:
✓ Bỏ cạnh (𝑢, 𝑣)
✓ Thêm một đỉnh mới 𝑤(không thuộc 𝑉)
✓ Thêm hai cạnh: (𝑢, 𝑤), (𝑤, 𝑣)
• Khi đó ta thu được một đồ thị mới 𝐺'.
→ Phép biến đổi này gọi là phép phân chia sơ cấp của cạnh (𝑢, 𝑣).

Các đồ thị đồng phôi: Hai đồ thị 𝐺 và 𝐺′ được gọi là đồng phôi (homeomorphic) nếu có thể biến đổi 
từ đồ thị này sang đồ thị kia bằng một dãy hữu hạn các phép:
	• phân chia sơ cấp (subdivision), và/hoặc
	• phép ngược lại, tức là loại bỏ một đỉnh bậc 2 (suppressing a degree-2 vertex)

Định lý Kuratowski: Một đồ thị 𝐺 là phẳng khi và chỉ khi
• 𝐺 không chứa một đồ thị con là phép chia (subdivision) của:
✓ đồ thị đầy đủ K5 hoặc
✓ đồ thị hai phía đầy đủ K3,3

## Tô màu đồ thị

Đồ thị đối ngẫu cảu bản đồ là đồ thị phẳng mỗi miền tương ứng với 1 đỉnh của đồ thị, và 2 đỉnh có cạnh nối là 
2 miền chung biên.

### Định nghĩa: 
- Tô màu (đỉnh) của một đơn đồ thị là việc gán màu cho mỗi đỉnh sao cho không có hai đỉnh kề nhau
cùng màu.
- Số sắc (Chromatic number), Ký hiệu: 𝜒 𝐺 là số màu ít nhất cần để tô màu hợp lệ đồ thị G
- Định lý 4 màu: Mọi đồ thị phẳng đều có thể tô màu các đỉnh bằng không quá 4 màu sao cho hai đỉnh kề nhau có
màu khác nhau (hoặc χ(G)≤4 với mọi đồ thị phẳng G).
- Nhận xét: 
+ Số màu của đồ thị lưỡng phân là 2 màu.
+ Số màu của đồ thị đầy đủ Kn là n màu.

Giải thuật tô màu:

Input: G(V, E)
Output: Gán màu cho các đỉnh
1. Xác định bậc các đỉnh trong đồ thị, sắp xếp các đỉnh theo
thứ tự bậc giảm dần
2. Khởi tạo: color = 1;
3. Trong khi còn đỉnh chưa được tô màu
a) Duyệt danh sách đỉnh theo thứ tự đã sắp
• Với mỗi đỉnh chưa tô:
• Nếu không kề với đỉnh nào đã tô màu 𝑐𝑜𝑙𝑜𝑟 → gán màu color
b) Tăng:
color = color + 1

