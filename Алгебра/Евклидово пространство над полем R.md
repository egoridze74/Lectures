#линал 
# Основные определения
## Скалярное произведение
Функция $f(\vec{x}, \vec{y}), \vec{x}, \vec{y} \in V$ называется **скалярным произведением**, если:
	1. $f(\vec{x}, \vec{x}) \geq 0, \ f(\vec{x}, \vec{x}) = 0 \iff \vec{x} = \vec{0}$ - положительная определённость
	2. $f(\vec{x}, \vec{y}) = f(\vec{y}, \vec{x})$ - симметрия
	3. $f(\alpha_1 \vec{x_1} + \alpha_2 \vec{x_2}\vec{y}) = \alpha_1 f(\vec{x_1}, \vec{y}) + \alpha_2 f(\vec{x_2}, \vec{y})$ - линейность
## Евклидово пространство
Линейное пространство $V$ над полем $R$ со скалярным произведением называется **евклидовым пространством**.
## Длина вектора
Если $(\vec{x}, \vec{y})$ - скалярное произведение в $V$, то число: $$|\vec{x}| = \sqrt{(\vec{x}, \vec{x})}$$
## Угол между векторами
Углом между векторами $\vec{x}, \vec{y}$ называется угол $\phi$, для которого: $$\cos \phi = \frac{(\vec{x}, \vec{y})}{|\vec{x}| \cdot |\vec{y}|}, \ \vec{x} \neq 0, \ \vec{y} \neq 0$$
Проверим, что ([[Неравенство Коши-Буняковского]]): $$\frac{(\vec{x}, \vec{y})}{|\vec{x}| \cdot |\vec{y}|} \leq 1$$
## Примеры:
1. $V^3$ - трёхмерные вектора
	- $f(\vec{x}, \vec{y}) = |\vec{x}| \cdot |\vec{y}| \cos \widehat{|\vec{x}| \cdot |\vec{y}|}$
	- $\vec{i}, \vec{j}, \vec{k}$ - базис
	- $\vec{x} = x_1\vec{i} + x_2\vec{j} + x_3\vec{k} = \begin{pmatrix}x_1 \\x_2 \\x_3\end{pmatrix} \in \mathbb{R}^3$
	- $(\vec{x}, \vec{y}) = x_1y_1 + x_2y_2 + x_3y_3$
2. $\mathbb{R}^n = \begin{Bmatrix}x_1 &  \\ \vdots & x \in \mathbb{R} \\ x_n & \end{Bmatrix}$
	- Рассмотрим $f(\vec{x}, \vec{y}) = x_1y_1 + \dots + x_n y_n$. Это скалярное произведение
	- В линейном пространстве $V$ можно определить бесконечно много скалярных произведений
3. $\mathbb{C} = \begin{Bmatrix} \begin{pmatrix}z_1 \\\vdots \\z_n\end{pmatrix} \end{Bmatrix}$
	- $(\vec{z}, \vec{w}) = z_1 \vec{w_1} + \dots + z_n \vec{w_n}$
4. $P_3[x]$
	- $(p(x), q(x)) = \int\limits_{-1}^{1} p(x)q(x) dx$