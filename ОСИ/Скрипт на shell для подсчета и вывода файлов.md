#оси 
Написать shell-скрипт, который подсчитывает количество файлов в текущем каталоге, содержащих текстовую информацию, или содержащих в имени "text". Список этих файлов сохранить в a.txt

- Чтобы найти файлы с "text": `file * | grep text`
- `if test -f a.txt then unlink a.txt fi` - создание файла

### Код скрипта (методом Истратова)
``` shell
if test -f a.txt
then unlink a.txt
fi

a = `ls -a`
n = 0 # счетчик файлоа

for i in $a
do
	t = `file $i`
	echo $t | grep text >/dev/null
	if [ $? -eq 0 ]
		then echo $i >> a.txt
		n = `expr $n + 1`
	fi
done
echo кол-во текстовых файлов $n
```

### Код скрипта (методом Хаджика)
``` shell
fin . -exec `file {} \; | grep text | cut -d : -f 1 | tee a.txt | wc -l
```