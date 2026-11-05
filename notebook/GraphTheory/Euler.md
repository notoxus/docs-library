Euler:
- Chu trình:
+ Điều kiện cần: Đồ thị liên thông
+ Là một chu trình đi qua mỗi cạnh của đồ thị đúng một lần và quay lại đỉnh xuất phát
+ Có chu trình Euler -> Gọi là đồ thị Euler
- Đường đi:
+ Là một đường đi đi qua mỗi cạnh của đồ thị đúng một lần
+ Có đường đi Euler -> Gọi là đồ thị nửa Euler
+ Nếu đồ thị có chu trình thì có thể có đường đi
- Các định lý (G vô hướng):
+ ĐL1: Một đồ thị vô hướng liên thông 𝐺 = (𝑉, 𝐸) với ∣𝑉∣> 1 có chu trình Euler (Eulerian Circuit) khi và chỉ khi mọi đỉnh của 𝐺 đều có bậc chẵn
+ ĐL2:  Một đồ thị vô hướng liên thông 𝐺 = (𝑉, 𝐸) có đường đi Euler nhưng không có chu trình Euler (Eulerian Path) khi và chỉ khi đồ thị có đúng hai đỉnh bậc lẻ.
- Các định lý (G có hướng)
+ ĐL3: Cho 𝐺 = (𝑉, 𝐸) là đồ thị có hướng với ∣𝑉∣> 1. 𝐺 có chu trình Euler (Eulerian Circuit) khi và chỉ khi:
1) Đồ thị liên thông yếu
2) Với mọi đỉnh 𝑣 ∈ 𝑉: 𝑑𝑒𝑔−(𝑣) = 𝑑𝑒𝑔+(v). Khi đó ta nói đồ thị cân bằng.
✓ Hệ quả: Nếu một đồ thị có hướng có chu trình Euler thì nó
liên thông mạnh.
+ ĐL4: Định lý Euler (đường đi Euler). Đồ thị có hướng 𝐺 = (𝑉, 𝐸), ∣𝑉∣>1 , không có đỉnh cô lập, có đường đi Euler nhưng không có chu trình Euler khi
và chỉ khi:
1) 𝐺 liên thông yếu
2) Có đúng hai đỉnh 𝑥, 𝑦 sao cho
		𝑑𝑒𝑔+(𝑥) = 𝑑𝑒𝑔−(𝑥) + 1
		𝑑𝑒𝑔−(𝑦) = 𝑑𝑒𝑔+(𝑦) + 1
Các đỉnh còn lại thỏa
		𝑑𝑒𝑔+(𝑣) = 𝑑𝑒𝑔−(v)
