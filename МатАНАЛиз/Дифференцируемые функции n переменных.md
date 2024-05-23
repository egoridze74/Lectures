#матан 
## Определение
Возьмём $\forall n$, пусть $u = f(x_1, \dots, x_n)$ определена в $O(x^0)$, $x^0 = (x^0_1, \dots, x^0_n)$

Тогда $\Delta x = (\Delta x_1, \dots, \Delta x_n)$ - **приращение аргумента**
$\Delta u = f(x^0 + \Delta x) - f(x^0)$ - **приращение функции**  

Функция $u = f(x_1, \dots, x_n)$ называется **дифференцируемой**, в $x^0$, если выполняются следующие (эквивалентные) условия:
1. $\Delta u = A_1 \Delta x_1 + \dots + A_n \Delta x_n + o(\rho), \rho = \sqrt{\sum^n_{k = 1}(\Delta x_k)^2}, \ \rho \to 0$
2. $\Delta u = \sum^n_{k = 1} A_k \Delta x_k + \sum^n_{k = 1} \alpha_k (\Delta x) \cdot \Delta x$, где $\alpha_k$ - бесконечно малая при $\Delta x \to 0$