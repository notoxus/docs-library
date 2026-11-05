#TREE

## Định nghĩa và tính chất

### Cây tự do (Free Tree)
- Là một đồ thị vô hướng liên thông, không có chu trình và có ít nhất 2 đỉnh.
### Cây có gốc (Rooted tree)
- Là một cây có hướng, trên đó đã chọn một đỉnh là gốc (root) của cây và các cạnh định 
hướng sao cho với mọi đỉnh luôn có một đường đi từ gốc đến đỉnh đó.
- Một cây tự do có thể chọn một đỉnh bất kỳ làm gốc để trở thành cây có gốc
- Xét cây có gốc T
+ Mức của đỉnh: Khoảng cách từ gốc đến nút đó
+ Chiều cao của cây: Mức lớn nhất của một đỉnh bất kỳ
+ Nếu (xy) là cạnh của T: ta gọi x đỉnh cha (parent) của y, y là
đỉnh con (child) của x
+ Lá (leaves): Những đỉnh không có cây con.
+ Đỉnh trong (internal vertices): là những đỉnh có ít nhất 1 cây con, nút gốc cũng được 
xem như nút trong
### Rừng (Forest)
- Là tập hợp các cây đôi một không có đỉnh chung
- Là một đồ thị vô hướng không chứa chu trình và có ít nhất hai đỉnh
- Trong một rừng, mỗi thành phần liên thông là một cây
### Cây m-phân
Cho cây có gốc T:
o Mỗi đỉnh trong T có tối đa m cây con. Nếu có ít nhất một đỉnh trong cây T có đúng m cây con, 
thì T gọi là cây m-phân (m-arytree).
o Nếu mọi đỉnh trong của T đều có đúng m cây con thì T gọi là cây m-phân đủ (complete m-arytree)
o Cây m-phân với m=2 gọi là cây nhị phân
### Các định lý:
- Định lý 1: Giữa 2 đỉnh bất kỳ trong cây T luôn có một và chỉ một đường đi trong T nối chúng.
- Định lý 2: Nếu một cây có n đỉnh thì sẽ có *m = n-1 cạnh*
- Định lý 3 (Định lý Daisy Chain): T là một đồ thị có n đỉnh (n>=2), các mệnh đề sau là tương đương
	1. T là cây
	2. T liên thông và có n-1 cạnh
	3. T không chứa chu trình và có n-1 cạnh
	4. T liên thông và mỗi cạnh là cầu
	5. Giữa 2 đỉnh phân biệt bất kỳ của T luôn tồn tại duy
	nhất một đường đi đơn.
	6. T không chứa chu trình nhưng khi thêm một cạnh
	mới thì có được một chu trình duy nhất.
- Định lý 4: Một cây m-phân đầy đủ, có i đỉnh trong thì tổng số đỉnh của cây là: [n = m*i+1]
Trong đó: n số đỉnh của cây ,
		  m số cây con của mỗi đỉnh trong,
		  i là số đỉnh trong của cây
## Cây bao trùm:

Cho đồ thị vô hướng G. Cây T gọi là một cây bao trùm của G nếu T≤G (T là cây khung của G) và 
T chứa mọi đỉnh ccây bao trùm <-> G liên thôngủa G.
- Định lý: Đồ thị G có
- Tính chất:
◼ Có cây bao trùm khi và chỉ khi G liên thông
◼ Số cây bao trùm của đồ thị đầy đủ G n đỉnh là n
n-2
◼ G liên thông có ít nhất 1 cây bao trùm
◼ Mọi cây bao trùm có cùng số lượng đỉnh và cạnh
◼ G có n đỉnh thì cây bao trùm G có n – 1 cạnh

### Các giải thuật tìm cây bao trùm:

#### DFS:
*proceduce*
DFS (G: Liên thông với các đỉnh v1, v2,…,vn){
	T := Cây chỉ gồm 1 đỉnh v1
	visit(v1)
}
visit(v: đỉnh của G){
	For (mỗi đỉnh w kề với v nhưng chưa có trong T)
		Thêm đỉnh w và cạnh (v,w) vào T visit(w);
}
*pseudos code:*
FUNCTION SpanningTreeDFS(r) {
	visited[r] = true
	FOR u kề r DO {
		IF (visited[u]==false) {
		T = T ∪ (r, u)
		SpanningTreeDFS(u)
		}
	}
}
#### BFS
*proceduce*
BFS (G: liên thông với tập đỉnh v1,v2,...,vn) {
	T:= Cây chỉ gồm 1 đỉnh v1;
	Q={v}//Queue: các đỉnh chưa xử lý
	while (Q≠∅){
	v = Q.Remove();
	for (mỗi đỉnh w kề với v)
		if w∉Q and w∉T{
			Q.Add(w)
			Thêm cạnh (v,w) vào T
		}
	}
}
*pseudos code:*
FUNCTION SpanningTreeBFS(r){
	InitQueue(Q)
	EnQueue(Q, r)
	visited[r] = true
	WHILE Q ≠ ∅ DO{
		u = DeQueue(Q)
		FOR v kề u DO{
			IF (visited[v]==false){
				EnQueue(Q, v)
				visited[v] = true
				T = T ∪ (r, u)
			}
		}
	}
}
### Cây bao trùm nhỏ nhất:
- Đồ thị có trọng số: Là đồ thị trong đó mỗi cạnh (cung) được gán thêm một số thực gọi là trọng số 
(weight) của cạnh (cung)
- Kí hiệu:
	c(e): Trọng số của cạnh e
	c(G): Trọng số của đồ thị G
- Ma trận kề của đồ thị có trọng số: Cho G = <V, E> có trọng
số, ma trận kề trọng số của G là ma trận A có kích cỡ
|V|x|V| trong đó mỗi phần tử aij có giá trị như sau:

aij =	Trọng số của cạnh/cung i(vj ,v ) nếui (jv ,v )E
		Nếu (vi,vj)∉E
- Định lý: Cho T là một cây bao trùm của đồ thị có trọng số G (liên thông). T là một cây bao trùm 
tối thiểu nếu và chỉ nếu mỗi cạnh e ∉ T đều có trọng số lớn nhất trên chu trình tạo bởi e và các 
cạnh của T.

#### Thuật toán Kruskal:
- Các bước:
	1. Liệt kê tất cả cạnh với trọng số của cạnh đó:
		Dựa vào đồ thị ta liệt kê ra các cạnh gồm đỉnh đầu, đỉnh cuối và trọng số.
	2. Sắp xếp các cạnh theo trọng số tăng dần.
	3. Tìm cây khung bằng thuật toán Kruskal dựa trên kết quả bước 2.
	4. Tính tổng trọng số từ các cạnh tìm được.
*pseudos code:*
Đầu vào: G = (VG, EG) gồm n đỉnh và m cạnh
Kết quả: Tập cạnh ET cây bao trùm nhỏ nhất của G
𝐸T = ∅
WHILE (|ET|<n-1) and (EG ≠ ∅) DO{
	Chọn e là cạnh có trọng số nhỏ nhất trong EG
	IF(ET ∪ {e} không chứa chu trình) 
		then ET = ET ∪ {e}
		Loại cạnh e khỏi tập EG
	}
}
IF (|ET|<n-1) THEN
	{Không tìm được cây bao trùm nhỏ nhất}
#### Thuật toán Prim:
*pseudos code:*
Đầu vào: G = (VG, EG) gồm n đỉnh và m cạnh
Kết quả: Tập đỉnh VT và tập cạnh ET cây bao trùm nhỏ nhất
của G
VT = {x}, x là một đỉnh bất kì (đỉnh bắt đầu) trong V, ET = {}
Lặp lại cho tới khi VT = V:
	Chọn cạnh (u, v) có trọng số nhỏ nhất (𝒖 ∈ 𝑽𝑻, 𝑣 ∈ V\𝑉𝑇)
	Thêm v vào VT, và thêm cạnh (u, v) vào ET.

