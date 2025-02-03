#тервер 
## Подводка
[[Теорема Каратеодори. Борелевская алгебра|Борелевская алгебра]]
$(- \infty; a_i]$
$(a_i, b_i] = (\mathbb{R} \setminus (- \infty; a]) \setminus (- \infty, b_i] = (-\infty, b_i] \setminus (-\infty; a_i] = (a_i, b_i]$

## Функция распределения
Вводим функцию:
$P ((- \infty; x]) = F(x)$ - **функция распределения вероятностей**
$\implies P((a; b]) = F(b) - F(a)$

## Свойства функции распределения
1. $F(-\infty) = \lim\limits_{x \to -\infty} F(x) = 0$
2. $F(+\infty) = \lim\limits_{x \to +\infty} F(x) = 1$
3. $F(x)$ - [[Непрерывность функции в точке|непрерывная]] справа функция, то есть: 
	$\lim\limits_{x \to a + 0} F(x) = F(a)$
	$\lim\limits_{\varepsilon \to +0}F(x + \varepsilon) = F(x)$
	$(-\infty; x + \frac{1}{n}] \to_{n \to \infty} (-\infty; x]$
	$(-\infty; x - \frac{1}{n}] \to_{n \to \infty} (-\infty; x)$
4. $F(x)$ - [[Условия монотонности функции]] неубывающая

## Виды функций распределения
1. Дискретные функции распределения
	$x_1, \dots, x_n, \dots$
	$p_1, \dots, p_n, \dots, \ \sum\limits_i p_i = 1$
	![[Pasted image 20250203094427.png|300]]
2. Непрерывные функции распределения
	$F(x) \ \exists \ f(x)$ - **плотность вероятности**: $F(x) = \int\limits_{- \infty}^{x} f(t) dt$
	$\int\limits_{- \infty}^{+ \infty} f(t) dt = 1$
	$f(t) \geq 0$
	$f(t) = \begin{cases} 1, \ t \in [0; 1] \\ 0, \ иначе \end{cases}$
	$F(x) = \int\limits_{0}^{x} 1 dt = x$
	![[Pasted image 20250203195430.png|300]]
3. Сингулярная функция распределения
	$F(x)$ - Канторова лестница
	$F_K(x) \to F(x)$
	$\sum\limits_{k = 1}^{\infty} \frac{2^{k - 1}}{3^k} = \frac{1}{3} \sum\limits_{k = 1}^{\infty} (\frac{2}{3})^{k - 1} = 1$
	![[Pasted image 20250203195455.png|300]]