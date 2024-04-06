#линал 
Если $\alpha \in \mathbb{C}$ - корень $p(x) \in \mathbb{R}[x]$, то $\bar{\alpha}$ - корень этого же многочлена.
## Доказательство:
1. $p(\alpha) = a_n\alpha^{n} + \dots + a_1\alpha  +a_0 = 0 \implies p(\bar{\alpha}) = a_n(\bar{\alpha})^n + \dots + a_1\bar{\alpha} + a_0 = 0$
2. Комплексное сопряжённое обладает свойствами:
	1. $\overline{z_1 + z_2} = \bar{z_1} + \bar{z_2}$
	2. $\overline{z_1 \cdot z_2} = \bar{z_1} \cdot \bar{z_2}$
3. $a_n\alpha^n  +\dots + a_1\alpha + a_0 = 0 \implies p(\bar{\alpha}) = \overline{a_n\alpha^n} + \dots + \overline{a_1\alpha} + \bar{\alpha_0} = 0$
4. $a_n(\bar{\alpha})^n + \dots + a_1\bar{\alpha} + a_0 = 0$
5. Тогда $(x - \alpha)(x - \bar{\alpha}) = x^2 - (\alpha + \bar{\alpha})x + \alpha \bar{\alpha}$ - вещественный многочлен 2-ой степени, [[Неприводимый многочлен|неприводимый]] многочлен
	1. $\alpha + \bar{\alpha} = 2Re(\alpha)$
	2. $\alpha \bar{\alpha} = |\alpha|^2$