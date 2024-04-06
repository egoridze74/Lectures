#графика
## Определения
- Display - подключение к x-серверу
- Screen - экран (монитор, проектор и т.д.)
- Window - окно
# Код
```cpp
int main()
{
  Dispay *d;
  Window w;
  int s;
  d = XOpenDispay(0);
  if (d == 0)
    exit(1);
  s = DefaultScreen(d); //Дефолтный экран - установленный нулевым в списке xScreen (обычно это монитор, то есть, первый подключённый разъём)
  w = XCreateSimpleWindow(d, RootWindow(d, s), 10, 10, 200, 100, 1, BlackPixel(d, s), WhitePixel(d, s)); // Задаем цвет нашей ОС
  XMapWindow(d, w); // Показываем наше окно
  XFlush(d); // Заставляет применять все отправленные команды
  while(1)
  {
    XEvent event;

	xNextEvent(d, &event);

	switch(event.type)
	{
		case ButtonPress:
			xClearWindow(d, w);
			break;
		case ButtonRelease:
			xClearWindow(d, w);
			break;
	}
  }
}
```