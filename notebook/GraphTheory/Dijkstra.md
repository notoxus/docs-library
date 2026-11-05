# Thuật toán Dijkstra
Các bước của thuật toán Dijkstra
• Bước 1: L(a) = 0, S = Ø, ∀v∈V, v ≠ a: L(v) = ∞
• Bước 2: Nếu z ∈ S thì kết thúc.
• Bước 3: Chọn v ∉ S sao cho L(v) là nhỏ nhất. Đưa v vào S.
• Bước 4: Với mỗi đỉnh x liền kề v và x ∉ S thì đặt:
	◼ L(x) = min{L(x), L(v) + c(v,x)}
	◼ Quay lại bước 2
Một số kí hiệu sử dụng trong mã giả
✓ Gán nhãn cho đỉnh v (L(v), P(v)): Đường đi từ s đến v có độ dài là L(v), đỉnh trước kề với v trên đường đi là P(v).
✓ S = Tập các đỉnh đã xét,
✓ R = V-S: tập đỉnh chưa xét
*Procedure Dijsktra (G: Có trọng số và liên thông, s: Đỉnh nguồn)*
Begin R:=V;
	For each v in R do
	Begin L[v]: = ∞;
		  P[v]: = - ;
	end
	L[s]=0;
	While (R≠∅)
		Begin v = Đỉnh trong R có L[v] nhỏ nhất;
			  R=R-{v}
			  For each i in (R  Tập đỉnh kề với v) do
				If (L[i]> L[v]+w[v][i]) then
					L[i]:=L[v]+w[v][i];
					P[i]=v; 
		end
End