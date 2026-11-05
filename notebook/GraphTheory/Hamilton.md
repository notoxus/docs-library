# CHU TRÌNH HAMILTON
## Định nghĩa
- Chu trình Hamilton là chu trình đi qua tất cả các đỉnh của đồ thị,  mỗi đỉnh
 đúng một lần, ngoại trừ đỉnh đầu trùng với đỉnh cuối.
- Đường đi Hamilton là đường đi đi qua tất cả các đỉnh của đồ thị, mỗi đỉnh
 đúng một lần.
- Đồ thị Hamilton là đồ thị có chứa ít nhất một chu trình Hamilton.
- Đồ thị nửa Hamilton là đồ thị có đường đi Hamilton nhưng không có chu trình
 Hamilton.

Cho đồ thị vô hướng 𝐺 = (𝑉, 𝐸) với 𝑛 = ∣𝑉∣. 
Mục tiêu: tìm chu trình Hamilton 𝐻 hoặc chứng minh 𝐺 không phải 
đồ thị Hamilton.

✓ QT0: Nếu tồn tại đỉnh bậc ≤ 1 → đồ thị không Hamilton.

✓ QT1: Đỉnh bậc 2 → hai cạnh của nó bắt buộc thuộc chu trình Hamilton.

✓ QT2: Không tạo chu trình con có độ dài < n.

✓ QT3: Khi một đỉnh đã có 2 cạnh thuộc chu trình, xoá các cạnh còn lại của nó.

✓ QT4: Sau mỗi bước phải giữ đồ thị liên thông và bậc mỗi đỉnh ≥ 2.

## Điều kiện đủ
### Nhận biết
◼ Chưa có điều kiện cần và đủ tổng quát để nhận biết đồ thị Hamilton.

◼ Việc kiểm tra Hamilton nói chung là bài toán khó.

◼ Các kết quả thường ở dạng điều kiện đủ.

◼ Đồ thị càng nhiều cạnh thì khả năng Hamilton càng cao.

### Các định lý:
- Mọi đồ thị đầy đủ kn (với n>=3) đều có chu trình Hamilton
- Cho đơn đồ thị G, giả sử tồn tại k đỉnh sao cho khi xoá k đỉnh này
cùng với các cạnh kề với chúng, thì đồ thị còn lại có nhiều hơn k thành phần
liên thông, khi đó: 
					*G không phải là đồ thị Hamilton.*
## Điều kiện đủ
Định lý Dirac: Cho đơn đồ thị vô hướng G có n đỉnh (n≥3). Nếu mọi đỉnh v 
của G đều có bậc: deg(v)≥n/2 thì G có chu trình Hamilton
Định lý: Mọi đơn đồ thị có hướng, có n đỉnh, liên thông mạnh. Nếu với mọi 
đỉnh v của G thỏa:
					*deg-(v)≥n/2 và deg+(v)≥n/2*
thì G có chu trình hamilton
Bao đóng của đồ thị: Cho đơn đồ thị G có n đỉnh, bao đóng của đồ thị G, 
ký hiệu c(G) được tạo ra từ G bằng cách:

✓ Xét mỗi cặp đỉnh không kề nhau u và v

✓ Nếu deg(v) + deg(u) ≥ n thì thêm cạnh uv vào đồ thị

Quá trình này tiếp tục lặp lại cho đến khi không còn cặp đỉnh không kề nhau
nào thỏa điều kiện trên. Đồ thị thu được gọi là bao đóng của 𝐺.

Định lý của Václav Chvátal và Paul Erdős: Đồ thị 𝐺 là Hamilton khi và chỉ khi
bao đóng 𝑐(𝐺) của nó là Hamilton.

Đồ thị đấu loại:
	Là đồ thị có hướng thỏa:
	✓ với mọi cặp đỉnh phân biệt 𝑢, 𝑣
	✓ chỉ có đúng một cung giữa chúng:
	𝑢 → 𝑣 hoặc 𝑣 → 𝑢
	nhưng không tồn tại cả hai cung đồng thời.
	
Định lý:

▪ Mọi đồ thị đấu loại đều có đường đi Hamilton

▪ Mọi đồ thị đấu loại liên thông mạnh đề có chu trình Hamilton

Định lý (Ore, 1960): Một đơn đồ thị vô hướng G gồm n đỉnh với n≥3. Nếu với
mọi cặp đỉnh u, v không kề nhau của G ta có:
						*deg(u)+deg(v)≥n*
thì G là đồ thị Hamilton
