### <u>1-1</u>

linear equation

systems of linear equations

- consistent : has at least one solution
- inconsistent : no solution

Gaussian elimination (row-reduction algo)

elementary row operations :

1. replacement
2. scale
3. swap

reduced row echelon form (rref) : does more elmination upwards

pivot 

- 在線代裡是指, 化成rref後, 在這種形式下, matrix左下部分都是0, 也就是每一列(row)除了第一列以外, 其他列從左邊看過來都是0, 此時出現第一個非0數字的那個位置, 看起來就像旗標一樣, 帶領著後面數字出現, 所以稱為 pivot
- 求pivot position : 把matrix化rref, 每一列第一個非0即為pivot position

### <u>1-2</u>

linear combination

matrix-vector product

span 

- why span?
  - we want to say " v is a linear combination of u1, u2, u3 " (v可以寫成 u1, u2, u3的線性組合), we can simply say  v is in Span{u1, u2, u3}

- properties :
  - Span{0} = {0}
  - Span{u} = the set of all multiples of  u (所有u的倍數)
  - If S contains a nonzero vector, then Span S has infinitely many vectors.

row euivalent : the solutions are identical



