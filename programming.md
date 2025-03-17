#aalto #programming

# Template for C

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "myprint.h"

int main(void)
{
	...
    return 0;
}
```

# Basic commands for the terminal
- скомпилировать сразу два файла и подключить математическую библиотеку:  
	`gcc main.c source.c -o main -lm`

- скомпилировать вместе с библиотекой:  
	`gcc -static -o main2 main.c`

- скопировать файл в папку:  
	`cp main.c /mnt/c/User/alexa/Documents/`

- посмотреть объем переменной или типа данных:  
	`printf("%zu\n", sizeof(int));`

- сделать ссылку на папку:  
	`ln -s /mnt/c/Users/alexa doc`

- загрузить папку:  
	`wget --no-check-certificate <download url>`  
	`unzip <module-name>.zip`

- конвертировать:  
	`pandoc 1.md -o 1.tex`

- выключить нумерцию строк в vim:  
	`:set nonumber`

- испривить проблему со вставкой:  
	`:set paste`  
	`:set nopaste`  

- открыть PDF:  
	`zathura`

- скопировать текст из vim:  
	`:w !xclip -selection clipboard`

- скомпелировать файл main.out:  
	`gcc -o main.out main.c`

- Valgrind:  
	`valgrind --leak-check=full --track-origins=yes --show-leak-kinds=all ./main.out`

- запускать Zathura с указанием конкретного конфигурационного файла:  
	`zathura -c ~/.config/zathura/zathurarc-light main.pdf`
---


# Команды vim

```
удалить все в скобках:
di(
di"
di{
w   - слово
p   - параграф
da(   - включая скобку
ci   - удалить и перейти в режим вставки
например ciw удалит слово и перейдет в режим вставки

ctrl + d   - вверх
ctrl + u   - вниз
```


# Скопировать в буфур обмена

```
w !xclip -selection clipboard
```


