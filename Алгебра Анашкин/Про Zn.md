#алгебра 
Из [[МатАНАЛиз/Семинар 04.03.25|семинара]]: $[a]_n \in \mathbb{Z}_n^* \iff (a, n) = 1$

## Утверждение про поле по простому числу
$\mathbb{Z}_n$ - [[Алгебра Анашкин/Поле|поле]] $\iff$ n - простое число

### Доказательство
В одну сторону $\Leftarrow$: очевидно
В другую сторону $\Rightarrow$:
$a \neq 0 \implies [a]_n \in \mathbb{Z}_n^* \implies$
$\exists \ b: \ [a \cdot b]_n = [1]_n \iff a \cdot b - 1 = n \cdot q$
$a \cdot b + n(-q) = 1 \implies (a, n) = 1$

От противного: пусть n - не простое
Тогда $^{d}|_{n}, \ d \neq 1, \ d \neq n$
$n = d \cdot k, \ 1 < k < n$
$[d]_n \cdot [k]_n = [0]_n$ - противоречие, так как тогда эти числа - делители нуля, а в поле их нет

## Утверждение про поле из [[Фактор-кольцо|фактор-кольца]]
Пусть R - коммутативное кольцо с единицей, $I \vartriangleleft R$, тогда:
$\overline{R} = R/I$ - поле $\iff$ I - [[Главный идеал. Кольцо главных идеалов. Максимальный идеал|максимальный]] в R

### Доказательство
#### В одну сторону $\Rightarrow$:
$\overline{R}$ - [[Алгебра Анашкин/Поле|поле]]
$[a]_I \in \overline{R}^*, \ [a]_I \neq 0 (\ni \overline{R}) \implies a \notin I \ (a + I = I = [0]_I), \ a \in R, a \notin I$
$R \supset J = \{ a \cdot r + i| r \in R, i \in I \}$

Покажем, что $J \vartriangleleft R$
$\varnothing \neq J \ni a \ (r = e, i = 0)$
$(ar + i) - (ar' + i') = a(r - r') + (i - i') \in J$

$(J, +)$ - абелева группа
$(ar + i)(ar' + i') = a(rar') + ari' + iar' + i \cdot i' \in J \implies$ [[Подкольцо]]

$(ar + i) \cdot r' = ar \cdot r' + i r' \in J$
$J \vartriangleleft R$, но $I \subsetneq J$

$[a]_I \cdot [b]_I = [e]_I$
$a \cdot b - e \in I$
$a \cdot b - e = i \in I$
$a \cdot b + (-i) = e \implies e \in J \implies J = R$

Получается, что даже если есть идеал $J \vartriangleright I$, то он обязательно равен самому кольцу $R$.

#### В обратную сторону $\Leftarrow$:
$I$ - максимальный $\implies I \vartriangleleft K \vartriangleleft R, \ K = I \ или \ K = R$
$[a]_I \in \overline{R} \setminus [0]_I$
$J = \{ a \cdot r + i | r \in R, i \in I\} \vartriangleleft R$
$J \ni a, \ I \supsetneq J \implies J = R$

$\exists \ r \in R \ и \ i \in I$
$ar + i = e$
$ar - e = -i$
$[ar - e]_I = [-i]_I = [0]_I \implies [a]_I[r]_I = [e]_I \implies [a]_I \in \overline{R}^*$

$G > H$
$gH = H \iff g \in H$
$g_1H = g_2H \iff g_2^{-1}g_1 \in H$
$g_1 - g_2 \in H$

## Утверждение про евклидово кольцо и [[Главный идеал. Кольцо главных идеалов. Максимальный идеал|КГИ]]
$R$ - [[Евклидово кольцо. Алгоритм Евклида. Анашкин|Евклидово кольцо]] $\implies$ R - КГИ
$I \vartriangleleft R \implies \exists \ a \in R: \ I = aR$
- $a = 0 \implies I = 0$
- $a \in R^* \implies I = R$
- $a \in R \setminus (\{ 0 \} \cup R^*) \implies$
	a - неразложимый или $a = a_1 \cdot a_2 \cdot \dots a_n$, где $a_i$ - неразложимые

$I \vartriangleleft J \vartriangleleft R$
Приравниваем это к $bR \vartriangleleft cR \vartriangleleft eR (\vartriangleleft R)$
Значит, $^{c}|_{b}, \ ^{e}|_{c} \implies b = c \cdot d$

В итоге получаем, что:
$\mathbb{Z}_n = \mathbb{Z} / n \mathbb{Z} \implies$ поле $\iff n \mathbb{Z}$:
- n - неразложимое
- n - простое