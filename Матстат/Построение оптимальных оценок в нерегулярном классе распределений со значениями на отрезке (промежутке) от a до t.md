#матстат 
[[Достаточные статистики|Полная достаточная статистика]]
$f(x, \theta) = Q(\theta) \cdot M(x)$
$\int\limits_{a}^{\theta} f(x, \theta)dx = 1$
$\int\limits_{a}^{\theta} Q(\theta) M(x) dx = 1$
$\int\limits_{a}^{\theta} M(x) dx = \frac{1}{Q(\theta)}$
$\int\limits_{a}^{t} M(x) dx = \frac{1}{Q(t)}$
$L(\vec{x}, \theta) = g(T(\vec{x}), \theta) \cdot h(\vec{x})$
$$L(\vec{x}, \theta) = \prod\limits_{i = 1}^{n} f(x_i, \theta) = \prod\limits_{i = 1}^{n} M(x_i) \cdot Q(\theta) \cdot I(a \leq x_i \leq \theta) = Q^n(\theta) \cdot \prod\limits_{i = 1}^{n} M(x_i) \cdot I(x_{(1)} \geq a) \cdot I(x_{(n)} \leq \theta)$$
Из этого получаем, что $x_{(n)}$ - **достаточная статистика**

Для проверки полноты необходимо установить распределение
$P(x_{(n)} \leq t) = P(x_1 \leq t, \dots, x_n \leq t) = F^n(t)$
$F(t) = \int\limits_{a}^{t} M(x) \cdot Q(\theta) dx = \frac{Q(\theta)}{Q(t)}$
$F_{x_{(n)}} = (\frac{Q(\theta)}{Q(t)})^n$
$f_{x_{(n)}}(t) = Q^n(\theta) \cdot \frac{-n Q'(t)}{Q^{n + 1}(t)}$

Найдём функцию H:
$E H(x_{(n)}) = 0$
$\int\limits_{a}^{\theta} H(t) \cdot Q^n(\theta) \cdot \frac{-nQ'(t)}{Q^{n + 1}(t)}dt = 0$
$\int\limits_{a}^{\theta} H(t) \cdot \frac{Q'(t)}{Q^{n + 1}(t)}dt = 0$ - вынесли не зависящее от t за скобку и обнулили
$H(\theta) \cdot \frac{Q'(\theta)}{Q^{n + 1}(\theta)} = 0$ - взяли производную по t
$H(\theta) = 0$
Так как H не зависит от $\theta$, то $H \equiv 0 \implies x_{(n)}$ - полная достаточная статистика

Тогда, если:
$E H(x_{(n)}) = \tau(\theta)$
То:
$\int\limits_{a}^{\theta} H(t) Q^n(\theta) \cdot \frac{-n Q'(t)}{Q^{n + 1}(t)} dt = \tau(\theta)$
$\int\limits_{a}^{\theta} H(t) \frac{Q'(t)}{Q^{n + 1}(t)} dt = \frac{\tau(\theta)}{- n Q^n(\theta)}$
$H(\theta) \frac{Q'(\theta)}{Q^{n + 1}(\theta)} = \frac{\tau'(\theta)}{-n Q^n(\theta)} + \frac{\tau(\theta)}{-n} \cdot (-n Q^{-n-1}(\theta) \cdot Q'(\theta))$
$H(\theta) = \tau(\theta) \frac{Q'(\theta)}{Q^{n + 1}(\theta)} \cdot \frac{Q^{n + 1}(\theta)}{Q'(\theta)} - \frac{\tau'(\theta)}{n Q^n(\theta)} \cdot \frac{Q^{n + 1}(\theta)}{Q'(\theta)} = \tau(\theta) - \frac{\tau'(\theta)}{n} \cdot \frac{Q(\theta)}{Q'(\theta)}$

$\int\limits_{a}^{t} M(x) dx = \frac{1}{Q(t)}$
$M(t) = - \frac{Q'(t)}{Q^2(t)}$

Тогда:
$H(\theta) = \tau(\theta) + \frac{\tau'(\theta)}{n Q(\theta)} \cdot \frac{1}{M(\theta)}$
$H(\theta) = \tau(\theta) + \frac{\tau'(\theta)}{n f(\theta, \theta)}$

Тогда оптимальной оценкой для $\tau(\theta)$ будет функция $$H(x_{(n)}) = \tau(x_{(n)}) + \frac{\tau(x_{(n)})}{n f(x_{(n)}, x_{(n)})}$$

## Пример
$R[0, \theta], \ f(x, \theta) = \frac{1}{\theta}$
$x_{(n)}$ - достаточная статистика
Попробуем найти оптимальную оценку $H$
$\tau(\theta) = 0$
$H(x_{(n)}) = x_{(n)} + \frac{1}{n(\frac{1}{x_{(n)}})} = x_{(n)}(1 + \frac{1}{n})$


## Лемма
Пусть $T(\vec{x})$ - оптимальная оценка для $\tau(\theta)$
$ET^* = 0$, тогда
$cov(T, T^*) = 0$
Словами: оптимальная оценка является некорреллированной с несмещённой оценкой нуля

### Доказательство
$T' = T + \lambda T*$
$ET' = \tau(\theta)$
$DT' = DT + \lambda^2 DT^* + 2\lambda cov(T, T^*)$
Если дисперсия ненулевая, то оценка не оптимальная

Значит, если $T$ - оптимальная, то $DT' = 0$

## Теорема
Пусть $T_1(\vec{x})$ - оптимальная для $\tau(\theta)$
Пусть $T_2(\vec{x})$ - оптимальная для $\gamma(\theta)$
Тогда $T^* = \lambda_1 T_1 + \lambda_2 T_2$ будет оптимальной для $\lambda_1 \tau + \lambda_2 \gamma$

### Доказательство
$f(\theta) = \lambda_1 \tau(\theta) + \lambda_2 \gamma(\theta)$
$T^*$ - несмещённая для f, $T'$ - ещё одна для $\delta$
$T^* - T'$ - несмещённая оценка нуля
$0 = \lambda \cdot cov(T_1, T^* - T') + \lambda_2 cov(T_2, T^* -  T') = cov(T^*, T^* - T') = DT^* - cov(T^*, T')$
Тогда:
$$DT^* = cov(T^*, T') \leq \sqrt{DT^* \cdot DT'}$$
$$DT^* \leq DT'$$
, где $T'$ - любая несмещённая оценка

Значит, наша оценка $T^*$ - оптимальна янесмещённая