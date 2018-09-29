# Ch1 Systems of Linear Equations
Reference

- [Mr. Opengate](http://mropengate.blogspot.com/search/label/Computer%20Science-Linear%20Algebra "link")

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

- linear combination can be written as matrix-vector product

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

Rank 秩

- 算到 rref 時, 非 0 列的個數, 其意義為此 linear system 的獨立方程式的個數

- 可以理解成規範度, 也就是 matrix 被限制的程度,

  當 matrix 的 rank = n 時(滿秩), 此時這個 matrix 被約束到只有一個點, 

  當 rank 降低時, 方程組的 solution set 也就變大; 反之, rank 越大, 其 solution set 也就被規範的越有序

- is same as the number of pivot positions in the matrix! 

Rank-nullity Thm

- rank A + nullity A = n

Linear Dependence (L.D.)

- Concept 

  - 用最少的向量來做到 span

  - 是否某個向量為其他向量的線性組合 (若有向量為其他向量的線性組合, 那麼代表這個 span 不是由最少的向量所得到)

  - 與其去尋找每個向量(u1, u2,...)是否為其他的向量的 span, 可以反過來思考, 是否能找出一組不全為0(因為都為0組合出來當然為0)的係數 c1, c2, ... 使得向量 u1, u2, ... 組合成0

    ​	c1 * u1 + c2 * u2 + ..... = 0 

    這時候可以發現有人可以寫成別人的線性組合!  -> 線性相依

- Property

  - 若集合中有一向量為零向量, 那麼就一定是L.D. , 因為 1 * 0 + 0 * u1 + 0 * u2 + ... = 0
  - <u>Ax = 0 有一組 nonzero solution</u>, 代表它有無限多組解或有 free variable

Linear Independence (L.I.)

- Concept

  - 和 L.D. 相反
  - 不存在不全為0的係數使得向量可以組合成0
  - 亦即只有一組係數可以讓向量組合成0, 就是所有係數 c 必須都是0
  - 此時 span 由最少的向量所組成, 因為每個向量都不是其他向量的線性組合, 不能隨便移除

- Question

  - Can Ax = b have infintely many solutions?  -> No!

    Suppose A * x1 = b, A * x2 = b, then A * (x1- x2) = b - b = 0, 

    此時若 x1 不等於 x2, 代表有 nonzero solution, 就是 L.D. , 而非 L.I.

  - Does Ax = b always have a solution? -> Not necessarily

    Ax = b should always have no more than one solution (最多只能有一組解, 超過就是L.D.)

  - What is rank A?  What is nullity A?

    此時 rank A = n, 因為若 rank A < n, 代表有 pivot column 對應到 free variable 了, 就是 L.D.

    又根據 Rank-nullity Thm, nullity = n - n = 0