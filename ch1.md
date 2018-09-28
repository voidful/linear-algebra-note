### <u>1-1</u>

linear equation

systems of linear equations

- consistent : has at least one solution (unique or infinitely many solutions)
- inconsistent : no solution

Gaussian elimination (row-reduction algo)

elementary row operations :

1. replacement
2. scale
3. swap

Reduced row echelon form (rref) 

- does more elmination upwards
- every matrix has one and only one rref (p63)

Pivot 

- 在線代裡是指, 化成 rref 後, 在這種形式下, matrix 左下部分都是 0, 也就是每一列(row)除了第一列以外, 其他列從左邊看過來都是 0, 此時出現第一個非 0 數字的那個位置, 看起來就像旗標一樣, 帶領著後面數字出現, 所以稱為 pivot
- 求 pivot position : 把 matrix 化 rref, 每一列第一個非 0 即為 pivot position

### <u>1-2</u>

linear combination

matrix-vector product

Span 

- why span?
  - we want to say " v is a linear combination of u1, u2, u3 " (v 可以寫成 u1, u2, u3 的線性組合), we can simply say  v is in Span{u1, u2, u3}

- properties :
  - Span{0} = {0}
  - Span{u} = the set of all multiples of  u (所有 u 的倍數)
  - If S contains a nonzero vector, then Span S has infinitely many vectors.

row euivalent : the solutions are identical (兩系統有相同的 solution set)

zero vector : 0 = (0, 0, 0, ...)  (和 0 不同, 可以任意方向)	

### <u>1-3</u>

linear algebra ?

- 向量空間 (vector space) 中的線性變換 (將向量空間中的子空間 map 到另一個子空間)

Linear Transform (important!)

- general : T(au + bv) = aT(u) + bT(v)
- matrix : 如果 T 是線性映射, 則存在唯一矩陣 A 使 T(x) = Ax

Homogeneous linear system : 齊次線性系統, Ax = 0

Trival solution

- 顯然解, Ax = 0, take x = 0 as a solution (因為顯然有 0 這個解)
- there are any other solutions -> nontrival solutions

Kernel

- ker(A) 的意思為讓 Ax = 0 的那些 x 集合, 也就是 {x : Ax = 0}

Rank

- 算到 rref 時, 非 0 列的個數, 其意義為此 linear system 的獨立方程式的個數
- is same as the number of pivot positions in the matrix! 



