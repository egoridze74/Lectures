#алгебра 
$\mathbb{Z}_n$
$n = p_1^{\alpha_1} \cdot \dots p_r^{\alpha_r}$
$a_1 = p_1^{\alpha_1}, \ a_2 = p_2^{\alpha_2}, \dots, a_r = p_r^{\alpha_r}$
$b_1 = \frac{n}{a_1} = \frac{n}{p_1^{\alpha_1}}, \ b_2 = \frac{n}{p_2^{\alpha_2}}, \dots, b_r = \frac{n}{p_r^{\alpha_r}}$

Эти числа в совокупности взаимно-простые.

$\exists u_1, u_2, \dots, u_r \in \mathbb{Z}$
$u_1 b_1 + u_2 b_2 + \dots + u_r b_r = 1$

Рассмотрим $R_i = b_i \mathbb{Z}_n$:
$\mathbb{Z}_n = b_1 \mathbb{Z}_n \dot{+} b_2 \mathbb{Z}_n \dot{+} \dots \dot{+} b_n \mathbb{Z}_n$

$|R_i| = |b_i \mathbb{Z}_n| = p_i^{\alpha_i}$, тогда $R_i = b_i \mathbb{Z}_n \cong \mathbb{Z}_{p_i^{\alpha_i}}$
$ord(g_i) = \frac{n}{(n, \frac{n}{p_i^{\alpha_i}}) = p_{i}^{\alpha_i}}$

Тогда любой элемент может быть записан как сумма элементов из этих колец:
$b_1 (u_1 s) + b_2 (u_2 s) + \dots + b_r (u_r s) = s, \ s \in \mathbb{Z}_n$

## КТО
$\mathbb{Z}_n = b_1 \mathbb{Z}_n \dot{+} b_2 \mathbb{Z}_n \dot{+} \dots \dot{+} b_n \mathbb{Z}_n$

$a_i \mathbb{Z}_n \cong \mathbb{Z}_{p_i^{\alpha_i}}$
$\mathbb{Z}_n \cong \mathbb{Z}_{p_1^{\alpha_1}} \oplus \mathbb{Z}_{p_2^{\alpha_2}} \oplus \dots \oplus \mathbb{Z}_{p_k^{\alpha_k}}$
$\mathbb{Z}_n^* \cong \mathbb{Z}_{p_1^{\alpha_1}}^* \oplus \mathbb{Z}_{p_2^{\alpha_2}}^* \oplus \dots \oplus \mathbb{Z}_{p_k^{\alpha_k}}^*$
$p_1 < p_2 < \dots < p_k$
- $p_1 \neq 2, \ \mathbb{Z}_n^*$ - циклическая $\iff$ $k = 1$
- $p_1 = 2, \ \mathbb{Z}_n^*$ - циклическая $\iff$ $k \leq 2 (\begin{cases} k = 1 \ \alpha_1 = 1, 2 \\ k = 2 \ \alpha_1 = 1 \end{cases})$