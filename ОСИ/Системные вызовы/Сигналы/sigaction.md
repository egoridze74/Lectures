#оси #системные_вызовы 
В начале программы должен присутствовать sigaction, чтобы прописать, какой будет реакция на различные сигналы.
```
sigaction(sig, SIG_IGN/SIG_DFL, Имя_функции)
```
Как устроен sigaction:
```
struct sigaction {
	void sa_handler();
	sigset_t sa_mask();
	int sa_flags;
}
```

Замечание: Функция с "Имя_функции" должна быть описана раньше, чем sigaction. 
Пример:
```
void func() {
	system("date")
}
int main() {
	int i; char a[500];
	struct sigaction new, old;
	new.sa_handler = func;
	sigprocmask(0, 0, &new.sa_mask);
	new.sa_flags = 0;
	sigaction(SIGINT, &new, 0);
}
```
- sa_handler() - сигнал, который хотим заменить
- sa_mask() - сигнальные макси процесса при обработке
- sa_flags - набор флагов, влияющих на обработку сигнала