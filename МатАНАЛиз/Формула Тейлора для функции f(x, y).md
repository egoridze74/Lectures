#матан 
## Вывод формулы
1. $z = f(x, y)$
2. $\Delta z = \frac{1}{1!} dz + \frac{1}{2!} d^2 z + R_2$
3. $dz = f'_x \cdot dx + f'_y \cdot dy$
4. $d^2 z = f''_{xx} dx^2 + 2f''_{xy} dx dy + f''_{yy} dy^2$
5. $dx = x - x_0, \ dy = y - y_0$
6. $\Delta z = f'_x(x_0, y_0)(x - x_0) + f'_y(x_0, y_0)(y - y_0) + \frac{1}{2!}[f''_{xx} (x - x_0)^2 + 2f''_{xy} (x - x_0) (y - y_0) + f''_{yy} (y - y_0)^2] + R_2$
## Пример
$z = x^y$ в точке $(e, 0)$
- $z_0 = z(e, 0) = e^0 = 1$
- $z'_x(e, 0) = y \cdot x^{y - 1} = 0$
- $z'_{y}(e, 0) = x^y \cdot \ln x = e^0 \cdot \ln e = 1$
- $z''_{xx}(e, 0) = y \cdot (y - 1) \cdot x^{y - 2} = 0$
- $z''_{xy}(e, 0) = x^{y - 1} + y \cdot (x^{y - 1})\ln x = e^{-1} = \frac{1}{e}$
- $z''_{yy}(e, 0) = \ln x \cdot x^y \ln x = 1$

$\Delta x = (x - e); \ \Delta y = y$
$z = 1 + 0 \cdot \Delta x + 1 \cdot \Delta y + \frac{1}{2}(0 \cdot \delta x^2)$