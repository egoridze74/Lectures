#матлог 
## Булевая функция
Функция $f = f(x_1, \dots, x_d)$ от переменных $x_1, \dots, x_d$ называется **булевой**, если $x_1, \dots, x_d$ и сама функция могут принимать только значения 0 и 1.

### Переформулировка
Обозначим $\mathbb{Z}_{2}$ множество из двух элементов 0 и 1 (то есть, $\mathbb{Z}_2$ - поле из двух элементов)

Тогда **булевая функция f** от n переменные - это любое отображение: $$f: \ (\mathbb{Z}_2)^n \to \mathbb{Z}_2$$, где прообраз - совокупность всех строк вида $(a_1, \dots, a_n)$, где $a_i \in \mathbb{Z}_2 \ \forall i$

## Базисные функции
![[Pasted image 20250405160233.png]]

## Добавление фиктивных переменных
$f(x_1, \dots, x_n)$ - булевая функция
$\tilde{f}(x_1, \dots, x_n, x_{n + 1}, \dots, x_{n + d})$ по определению:
	$\tilde{f}(a_1, \dots, a_n, a_{n + 1}, \dots, a_{n + d}) = f(a_1, \dots, a_n), \ a_i \in \mathbb{Z}_2$

## Другое определение
Булевая функция $f(x_1, \dots, x_n)$ - это любое отображение $f: \ \mathbb{Z}_2^n \to \mathbb{Z}_2 \ (\varepsilon_1, \dots, \varepsilon_n), \ \varepsilon_i \in \mathbb{Z}_2$

## Теорема о количестве булевых функций
Всего булевых функций от n переменных $2^{2^n}$

Пример: $n = 1, \ 2^{2^1} = 4$
$(0) \to (0)$
$(0) \to (1)$
$(1) \to (0)$
$(1) \to (1)$

### Доказательство
У таких булевых функций число аргументов = числу элементов $\mathbb{Z}_2^n$, то есть числу строк $(\varepsilon_1, \dots, \varepsilon_n), \ \varepsilon_i = 0 \ или \ \varepsilon_i = 1 \ \forall i$

Их всего $2^n$ (на каждый элемент можно поставить 2 значения - 0 и 1).

Каждую из строк можно отправить либо в 0, либо в 1 $\implies 2^{2^n}$ вариантов

## Способы задания булевых функций от n переменных
1) Табличный
	$\begin{vmatrix}x_1 & \dots & x_n & f(x_1, \dots, x_n) \\\vdots &  & \vdots & \vdots \\\varepsilon_1 & \dots & \varepsilon_n & f(\varepsilon_1, \dots, \varepsilon_n)\end{vmatrix}$
	Пример:
	$\begin{vmatrix}x_1 & x_2 & f(x_1, x_2) &  \\0 & 0 & 1 & f(0, 0) = 1 \\0 & 1 & 1 & f(0, 1) = 1 \\1 & 0 & 0 & f(1, 0) = 0 \\1 & 1 & 1 & f(1, 1) = 1\end{vmatrix}$
2) Векторный
	Занумеруем все строки $(\varepsilon_0, \dots, \varepsilon_{n - 1}) \in \mathbb{Z}_2^n$ следующим способом: строке $(\varepsilon_0, \dots, \varepsilon_{n - 1})$ присвоим номер $\varepsilon_0 + \varepsilon_1 \cdot 2^1 + \varepsilon_2 \cdot 2^2 + \dots + \varepsilon_{n - 1}2^{n - 1}$
	И рассмотрим строку (вектор) длины $2^n$, элементы которой равны 0 и 1. $(u_0, \dots, u_{2^n - 1}), \ u_i = f(\varepsilon_0, \dots, \varepsilon_{n - 1})$ - набор, имеющий номер i в этой нумерации.
	Пример: $n = 2$
	$\begin{vmatrix}(x_1, x_2) & i \\ (0, 0) & 0 + 0 \cdot 2^1 = 0 \\(1, 0) & 1 + 0 \cdot 2^1 = 1 \\(0, 1) & 0 + 1 \cdot 2^1 = 2 \\(1, 1) & 1 + 1 \cdot 2^1 = 3\end{vmatrix}$
	Поэтому булевую функцию из предыдущего примера можно задать вектором $(1, 0, 1, 1)$
3) Геометрический
	$\mathbb{R}^n$ - пространство всех строк $(\alpha_1, \dots, \alpha_n), \ \alpha_i \in \mathbb{R}$
	
	Определение:
	Единичным n-мерным кубом в $\mathbb{R}^n$ называется подмножество $E_n \ \{ (\alpha_1, \dots, \alpha_n) \in \mathbb{R}^n \ | \ 0 \leq \alpha_i \leq 1 \ \forall i \}$
	![[Pasted image 20250413174806.png]]
	Рассмотрим $E_n$. Зафиксируем какие-либо целые числа $1 \leq i_1 < i_2 < i_3 < \dots < i_k \leq n$, а также зафиксируем какие-либо k элементов из $\mathbb{Z}_2$. $\varepsilon_1, \dots, \varepsilon_k \in \mathbb{Z}_2$
4) Задание булевой функции [[Формулы для задания булевых функций|формулами]]
	Булевых функций имеется конечное число (= $2^{2^n}$). Имеются разные формулы, задающие одну и ту же булевую функцию. 
	
	Функции $F_1$ и $F_2$, задающие одну и ту же функцию (то есть, дающие одни и те же значения при совпадающих наборах значений переменных) называются **эквивалентными** (обозначаются $F_1 = F_2$)
## Грань
Обозначим: $F^n \begin{pmatrix}\varepsilon_1 & \varepsilon_2 & \dots & \varepsilon_k \\i_1 & i_2 & \dots & i_k\end{pmatrix}$ - это совокупность всех элементов из $E_n$, имеющих вид, где $i_j$ - позиция.

На фиксированных позициях фиксируем значения $\begin{pmatrix} \dots & \varepsilon_1 & \dots & \varepsilon_2 & \dots & \varepsilon_k & \dots \\ \dots & i_1 & \dots & i_2 & \dots & i_k & \dots \end{pmatrix}$, где вместо троеточий стоит что угодно

Такое $F^n \begin{pmatrix}\varepsilon_1 & \varepsilon_2 & \dots & \varepsilon_k \\i_1 & i_2 & \dots & i_k\end{pmatrix}$ называется (n-k)-мерной гранью куба $E_n$.

Пример: n = 3
![[Pasted image 20250413182841.png]]

При k = n получим вершину $(\varepsilon_1, \dots, \varepsilon_k)$

## n-мерный куб (сами вершины)
Обозначим $B_n = E_n \cap (\mathbb{Z}_2)^n = \mathbb{Z}_2^n$ (из вершин)

Тогда $B_n$ называется **n-мерным кубом**

Грань куба $B_n$ - $F^n \begin{pmatrix}\varepsilon_1 & \varepsilon_2 & \dots & \varepsilon_k \\i_1 & i_2 & \dots & i_k\end{pmatrix} \cap \mathbb{Z}_2^n = F^n \begin{pmatrix}\varepsilon_1 & \varepsilon_2 & \dots & \varepsilon_k \\i_1 & i_2 & \dots & i_k\end{pmatrix} f(x_1, \dots, x_n)$ - булевая функция

## Носитель булевой функции
Носителем булевой функции f называется совокупность всех вершин куба $B_n$, на которых f принимает значение 1.

Обозначается: $supp(f) - support$

Пример: $n = 3, \ f(x_1, x_2, x_3)$
$f(\varepsilon_1, \varepsilon_2, \varepsilon_3) = 0$ только при $(\varepsilon_1, \varepsilon_2, \varepsilon_3) = (0, 0, 0)$
Совокупность вершин, кроме нулевой - **носитель**
![[Pasted image 20250413184823.png]]