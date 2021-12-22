# **Работа с редактором Bash**


### В этой инструкции приведены основы работы c редактором Bash в Git.


### **Основные команды****  
  

| **Команда**            | **Действие**                                                                                                      |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **break**              | Выход из цикла for, while или until                                                                               |
| **continue**           | Выполнение следующей итерации цикла for, while или until                                                          |
| **echo**               | Вывод аргументов, разделённых пробелами, на стандартное устройство вывода                                         |
| **exit**               | Выход из оболочки                                                                                                 |
| **export**             | Отмечает аргументы как переменные для передачи в дочерние процессы в среде                                        |
| **hash**               | Запоминает полные имена путей команд, указанных в качестве аргументов, чтобы не искать их при следующем обращении |
| **kill**               | Посылает сигнал завершения процессу                                                                               |
| **let**                | Производит арифметические операции над числами и переменными                                                      |
| **pwd**                | Выводит текущий рабочий каталог                                                                                   |
| **read**               | Читает строку из ввода оболочки и использует её для присвоения значений указанным переменным                      |
| **return**             | Заставляет функцию оболочки выйти с указанным значением                                                           |
| **shift**              | Перемещает позиционные параметры налево                                                                           |
| **test**               | Вычисляет условное выражение                                                                                      |
| **times**              | Выводит имя пользователя и системное время, использованное оболочкой и её потомками                               |
| **trap**               | Указывает команды, которые должны выполняться при получении оболочкой сигнала                                     |
| **unset**              | Вызывает уничтожение переменных оболочки                                                                          |
| **wait**               | Ждёт выхода из дочернего процесса и сообщает выходное состояние                                                   |
| **alias**              | Создаёт псевдоним                                                                                                 |
| **export PATH=$PATH:** | Добавляет каталог пути:...                                                                                        |
| **which nano**         | Отображает расположение исполняемого файла nano                                                                   |
| **whereis nano**       | Отображает расположение исполняемого файла, справочных страниц, исходного кода и т. д.                            |


### **Зарезервированные переменные**

| **Команда**   | **Действие**                                                                                                                                                              |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **$DIRSTACK** | Содержимое вершины стека каталогов                                                                                                                                        |
| **$EDITOR**   | Текстовый редактор по умолчанию                                                                                                                                           |
| **$EUID**     | Эффективный UID: если вы использовали программу**su** для выполнения команд от другого пользователя, то эта переменная содержит UID этого пользователя, в то время как... |
| **$UID**      | Содержит реальный идентификатор, который устанавливается только при логине                                                                                                |
| **$FUNCNAME** | Имя текущей функции в скрипте                                                                                                                                             |
| **$GROUPS**   | Массив групп, к которым принадлежит текущий пользователь                                                                                                                  |
| **$HOME**     | Домашний каталог пользователя                                                                                                                                             |
| **$HOSTNAME** | Ваш hostname                                                                                                                                                              |
| **$HOSTTYPE** | Архитектура машины                                                                                                                                                        |
| **$LC_CTYPE** | Внутренняя переменная, которая определяет кодировку символов                                                                                                              |
| **$OLDPWD**   | Прежний рабочий каталог                                                                                                                                                   |
| **$OSTYPE**   | Тип ОС                                                                                                                                                                    |
| **$PATH**     | Путь поиска программ                                                                                                                                                      |
| **$PPID**     | Идентификатор родительского процесса                                                                                                                                      |
| **$SECONDS**  | Время работы скрипта (в сек.)                                                                                                                                             |
| **$#**        | Общее количество параметров, переданных скрипту                                                                                                                           |
| **$\***       | Все аргументы, переданные скрипту (выводятся в строку)                                                                                                                    |
| **$@**        | Все аргументы, переданные скрипту (параметры выводятся в столбик)                                                                                                         |
| **$!**        | PID последнего запущенного в фоне процесса                                                                                                                                |
| **$$**        | PID самого скрипта                                                                                                                                                        |


### **Команды, возвращающие код возврата**

| **Команда** | **Действие**                                                                                                                                |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **test**    | Используется для логического сравнения; после выражения необходима закрывающая скобка ]                                                     |
| **\[**      | Синоним команды test                                                                                                                        |
| **\[\[**    | Расширенная версия \[ (начиная с версии 2.02), внутри которой могут быть использованы \|\| (или), & (и). Должна иметь закрывающую скобку ]] |
| **(( ))**   | Математическое сравнение                                                                                                                    |


### **Логические операции**

| **Символ**        | **Значение**                    |
| ----------------- | ------------------------------- |
| **-z #**          | Строка пуста                    |
| **-n #**          | Строка не пуста                 |
| **=, (==) #**     | Строки равны                    |
| **!= #**          | Строки не равны                 |
| **-eq #**         | Равно                           |
| **-ne #**         | Не равно                        |
| **-lt,(&lt; ) #** | Меньше                          |
| **-le,(&lt;=) #** | Меньше или равно                |
| **-gt,(>) #**     | Больше                          |
| **-ge,(>=) #**    | Больше или равно                |
| **! #**           | Отрицание логического выражения |
| **-a,(&&) #**     | Логическое «И»                  |
| **-o,(\|\|) #**   | Логическое «ИЛИ»                |


### **Математические операции**

| **Символ** | **Значение**                                   |
| ---------- | ---------------------------------------------- |
| **+**      | Сложение                                       |
| **—**      | Вычитание                                      |
| **\***     | Умножение                                      |
| **/**      | Деление                                        |
| **\*\***   | Возведение в степень                           |
| **%**      | Модуль (деление по модулю), остаток от деления |


### **Условные операторы**


#### В Bash условия пишутся следующим образом (на примере):

| \#!/bin/bash\#в переменную source вносим первый параметр скриптаsource=$1\#в переменную dest вносим второй параметр скриптаdest=$2\# в кавычках указываем имена переменных для сравнения. -eq — логическое сравнение, обозначающие равенствоif \[\[ "$source" -eq "$dest" ]]\# если они действительно равны, тоthen\#выводим сообщение об ошибке, т. к. $source и $dest у нас равныecho "Применим $dest и источник $source один и тот же файл!"\# выходим с ошибкой (1 — код ошибки)exit 1\# если же они не равныelse\# то выполняем команду cp: копируем источник в приёмникcp $source $destecho "Удачное копирование!"fi #обозначаем окончание условия.#### Результат выполнения скрипта:ite@ite-desktop:~$ ./primer2.sh 1 1«Применим 1» и «Источник 1» — один и тот же файл.ite@ite-desktop:~$ ./primer2.sh 1 2Удачное копирование! |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |


#### **Структура if-then-else используется следующим образом:**

**if**&lt;команда или набор команд, возвращающих код возврата (0 или 1)>

**then**&lt;если выражение после if истинно, выполняется этот блок>

**else**&lt;если выражение после if ложно, то этот>


#### Для построения многоярусных условий вида:

**if ...**

**then ...**

**else**

**if ...**

**then...**

**else ...**

Для краткости и читаемости кода можно использовать структуру:

**if ...**

**then ...**

**elif ...**

**then ...**

**elif ...**


#### **Условия. Множественный выбор**

Если нужно сравнивать какую-то одну переменную с большим количеством параметров, целесообразней использовать оператор**case**.

Пример:

| \#!/bin/bashecho "Выберите редактор для запуска:"echo "1 Запуск программы nano"echo "2 Запуск программы vi"echo "3 Запуск программы emacs"echo "4 Выход"\#здесь мы читаем в переменную $doing со стандартного вводаread doingcase $doing in1)/usr/bin/nano # если $doing содержит 1, то запустить nano;;2)/usr/bin/vi # если $doing содержит 2, то запустить vi;;3)/usr/bin/emacs # если $doing содержит 3, то запустить emacs;;4)exit 0;;\*) #если введено с клавиатуры то, что в case не описывается, выполнять следующее:echo "Введено неправильное действие"esac #окончание оператора case.    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |


### **Циклы**

| Пример цикла**for** в bash-скриптах — это перебор списка простых значений:_#!/bin/bash__for var in first second third fourth fifth__do__echo The $var item__done_                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Вот схема организации циклов**while**(выражение или команда, возвращающая код возврата):while команда проверки условияdoдругие командыdoneПример:_#!/bin/bash__count=0__while \[ $count -lt 10 ]__do__(( count++ ))__echo $count__done_ |
| **until** — выражение или команда, возвращающая код возврата. Схема:doкомандыdone_Пример:__#!/bin/bash__count=0__until \[ $count -gt 10 ]__do__(( count++ ))__echo $count__done_                                                        |


### **Команда cd**

Командаcd позволяет перейти в новый каталог.

| **Синтаксис**                    | **Объяснение**                                      |
| -------------------------------- | --------------------------------------------------- |
| **cd**                           | Перемещение в домашний каталог                      |
| **cd ~**                         | Перемещение в домашний каталог                      |
| **cd ..**                        | Перемещение на один уровень выше                    |
| **cd -**                         | Перемещение в предыдущий каталог                    |
| **cd Directory1**                | Перемещение в каталог Directory1                    |
| **cd Directory1/****Directory2** | Перемещение в каталог Directory2 по указанному пути |


### **Дополнительные команды**

| **Команда** | **Действие**                                                                                                                                                                                                |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **mkdir**   | Создаёт новый каталог в текущем каталоге                                                                                                                                                                    |
| **man**     | Отображает руководства по командам                                                                                                                                                                          |
| **cat**     | Считывает файл, переданный как аргумент, и выводит его содержимое по стандартному каналу вывода. Передача нескольких файлов в виде аргумента приведёт к выводу конкатенированного содержимого всех файлов   |
| **head**    | Читает первые 10 строк любого переданного текста и выводит их по стандартному каналу. Число выводимых строк можно изменить:| $ head -50 test.txt | | ------------------- |                                  |
| **tail**    | Работает аналогично командеhead, но читает строки с конца.Позволяет просматривать добавляемые к файлу строки в режиме реального времени при помощи флага-f:| $ tail -f test.txt | | ------------------ |    |



**less**— позволяет перемещаться по переданному файлу или куску текста, причём в обоих направлениях.

| **Обычные сочетания клавиш** | **Описание**                                                  |
| ---------------------------- | ------------------------------------------------------------- |
| **G**                        | Перемещает в конец файла                                      |
| **g**                        | Перемещает в начало файла                                     |
| **:50**                      | Перемещает на 50-ю строку файла                               |
| **q**                        | Выход из less                                                 |
| **/searchterm**              | Поиск строки, совпадающей с ‘searchterm’, ниже текущей строки |
| **/**                        | Перемещает на следующий подходящий результат поиска           |
| **?searchterm**              | Поиск строки, совпадающей с ‘searchterm’, выше текущей строки |
| **?**                        | Перемещает на следующий подходящий результат поиска           |
| **up**                       | Перемещает на одну строку выше                                |
| **down**                     | Перемещает на одну строку ниже                                |
| **pageup**                   | Перемещает на одну страницу выше                              |
| **pagedown**                 | Перемещает на одну страницу ниже                              |

**true** — всегда возвращает ноль в качестве выходного статуса для индикации успеха.

**false** — всегда возвращает не-ноль в качестве выходного статуса для индикации неудачи.

**$?** — переменная, которая содержит выходной статус последней запущенной команды. Под статусом обычно понимается [код возврата](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%B4_%D0%B2%D0%BE%D0%B7%D0%B2%D1%80%D0%B0%D1%82%D0%B0) программы. 0 означает успешное выполнение программы, любое значение больше 0 отражает тот факт, что в процессе выполнения возникли некоторые ошибки. Кстати, именно поэтому в Bash истиной (true) считается 0, а всё, что не 0, — ложью (false):

| $true $ echo $? 0 $ false $ echo $? 1 |
| ------------------------------------- |

**grep**—** **помогает осуществлять поиск переданной строки в указанном файле. Команда grep также может принимать несколько файлов и регулярных выражений для уточнения формата текста.

| **Обычные флаги** | **Описание**                           |
| ----------------- | -------------------------------------- |
| **-i**            | Отключение чувствительности к регистру |
| **-r**            | Рекурсивный поиск по директориям       |
| **-w**            | Поиск только целых слов                |
| **-c**            | Вывод количества найденных элементов   |
| **-n**            | Вывод всей строки, содержащей запрос   |
| **-v**            | Вывод инвертированного совпадения      |

**sed** — потоковый редактор, преобразующий входные текстовые данные. Обычно её используют для замены выражений так: s/regexp/replacement/g. Например, следующий код заменит все слова «Hello» на «Hi»:

| $cat test.txt Hello World $ sed 's/Hello/Hi/g' test.txt Hi World |
| ---------------------------------------------------------------- |

Вы можете ознакомиться с[руководством по sed](https://github.com/mikeizbicki/ucr-cs100/tree/2015winter/textbook/using-bash/sed).

**history** — выводит историю командной строки. Обычно её используют вместе с командой grep для поиска конкретной команды. Например, следующий код найдёт все команды, содержащие строку g++:

| $history \| grep g++ 155 g++ file1.txt 159 g++ file2.txt |
| -------------------------------------------------------- |

Здесь также используется символ | — это так называемый[конвейер](https://ru.wikipedia.org/wiki/%D0%9F%D0%B5%D1%80%D0%B5%D0%BD%D0%B0%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5_%D0%B2%D0%B2%D0%BE%D0%B4%D0%B0-%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D0%B0) (pipe). Благодаря ему можно перенаправлять вывод одной команды на вход другой — таким образом в примере выше вся история, которая в обычном режиме выводится командой history прямо в вывод терминала, будет перенаправлена в grep в качестве входных данных. Мы не увидим вывода команды history, но увидим вывод командыgrep.

Это может быть сложно для понимания без практики, поэтому поэкспериментируйте самостоятельно, например, с командамиls,history,ps (описана ниже), перенаправляя их вывод в grep,sed или less.

**export** — устанавливает переменные окружения для передачи дочерним процессам. Например, так можно передать переменную name со значением student:

| $export name=student |
| -------------------- |

**ps** — выводит информацию о запущенных процессах.

| $ps PID TTY TIME CMD 35346 pts/2 00:00:00 bash |
| ---------------------------------------------- |

Выводится четыре элемента:

- ID процесса (PID),
- тип терминала (TTY),
- время работы процесса (TIME),
- имя команды, запустившей процесс (CMD).

| **awk**   | Находит и заменяет текст в файлах по заданному шаблону:awk 'pattern {action}' test.txt                                                                            |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **wget**  | Скачивает файлы из сети и помещает их в текущий каталог                                                                                                           |
| **nc**    | Утилита для отладки сети. Также можно ознакомиться с[руководством по nc](https://github.com/mikeizbicki/ucr-cs100/tree/2015winter/textbook/using-bash/nctutorial) |
| **ping**  | Тестирует сетевое подключение                                                                                                                                     |
| **clear** | Очистка терминала                                                                                                                                                 |



### **Коннекторы**

Коннекторы позволяют запускать несколько команд одновременно.

| **Коннектор** | **Описание**                                                                             |
| ------------- | ---------------------------------------------------------------------------------------- |
| **&&**        | Первая команда исполняется всегда, вторая — только в случае успешного завершения первой  |
| **\|\|**      | Первая команда исполняется всегда, вторая — только в случае неудачного завершения первой |
| **;**         | Команды исполняются всегда                                                               |



| $ true && echo Hello Hello $ false \|\| echo Hello Hello $ echo Hello ; ls Hello test.txt file1.txt file2.txt |
| ------------------------------------------------------------------------------------------------------------- |


### **Конвейеры**

Конвейеры, или пайпы, позволяют соединять входные и выходные каналы различных команд. В следующем примере вывод командыls будет передан в head, и в результате будет напечатано лишь 10 первых элементов.

| $ ls -l \| head |
| --------------- |



### **Перенаправление ввода/вывода**


#### **Перенаправление вывода**

Для стандартного перенаправления вывода используются символы** ****>**** **и**>>**.

Например, этот код передаст вывод**ls** в файл, а не на экран:

| $ ls > files.txt $ cat files.txt file1.cpp sample.txt |
| ----------------------------------------------------- |

Если файл не существует, он создаётся, а если существует, то перезаписывается. Во избежание перезаписи стоит использовать команду**>>** — она дописывает данные в конец файла.


#### **Перенаправление ввода**

Для стандартного перенаправления ввода используется символ**&lt;**. В следующем примере**sort** берёт входные данные из файла, а не с клавиатуры:

| $ cat files.txt c b $ sort &lt; files.txt b c |
| --------------------------------------------- |

Команда** ****sort**** **выводит содержимое файла на экран, поскольку мы не перенаправили выход. Это можно сделать так:

| $ sort &lt; files.txt > files_sorted.txt |
| ---------------------------------------- |


#### **Продвинутое перенаправление**

Добавление**&** к **>** приводит к перенаправлению как стандартного потока выхода, так и потока ошибок. Например, файл test.cpp выведет строку stdout в cout и строку stderr в cerr.

| $ g++ test.cpp $ ./a.out >& test.txt $ cat test.txt stdout stderr |
| ----------------------------------------------------------------- |

Если вы хотите вывести конкретный файловый дескриптор, вы можете приписать его номер к**>**.

| **Имя**    | **Дескриптор** | **Описание**                    |
| ---------- | -------------- | ------------------------------- |
| **stdin**  | 0              | Стандартный поток ввода         |
| **stdout** | 1              | Стандартный поток вывода        |
| **stderr** | 2              | Стандартный поток вывода ошибок |

Например, для перенаправления**stderr**** **в** ****test.txt** нужно сделать следующее:

| $ g++ test.cpp $ ./a.out 2> test.txt stdout $ cat test.txt stderr |
| ----------------------------------------------------------------- |


### **Права доступа**

Команда**ls -l** выводит много информации о правах доступа к каждому файлу:

| $ ls -l test.txt -rw-rw-r-- 1 user group 1097374 January 26 2:48 test.txt |
| ------------------------------------------------------------------------- |



| **Вывод в примере** | **Описание / возможные выводы**              |
| ------------------- | -------------------------------------------- |
| **—**               | Тип файла:\- файл\- каталог                  |
| **rw-**             | Права доступа владельца файла                |
| **rw-**             | Права доступа членов группы владельцев файла |
| **r–**              | Права доступа прочих пользователей           |
| **user**            | Имя владельца файла                          |
| **group**           | Имя группы владельцев файла                  |



| **ls**      | Вывести список файлов и каталогов в текущем каталоге |
| ----------- | ---------------------------------------------------- |
| **ls /bin** | Вывести список файлов и каталогов в /bin             |
| **ls -a**   | Вывести подробную информацию (размер, дата)          |
| **ls -l**   | Показать скрытые файлы и каталоги                    |
| **ls -ld**  | Вывести информацию о текущем каталоге (не файлов)    |
| **ls my\*** | Вывести файлы с именем, начинающимся на my           |
| **tree**    | Показать дерево текущего каталога                    |

**chmod**—** **изменяет права доступа файла. Вот типичные сочетания флагов для изменения прав конкретных пользователей:

| **Буква** | **Пользователь**    |
| --------- | ------------------- |
| **u**     | Владелец            |
| **g**     | Член группы         |
| **o**     | Прочие пользователи |
| **a**     | Все пользователи    |



Вы можете вызватьchmod с описанием действий над конкретным файлом. Символ — обозначает удаление прав, символ + — добавление. Следующий пример сделает файл доступным для чтения и записи владельцу и группе:

| $ chmod ug+rw test.txt $ ls -l test.txt -rw-rw---- 1 user group 1097374 January 26 2:48 test.txt |
| ------------------------------------------------------------------------------------------------ |

Кроме того,chmod можно использовать с восьмеричными числами, где 1 — это наличие прав, а 0 — отсутствие: rwx= 111 = 7 rw- = 110 = 6 r-x = 101 = 5 r-- = 100 = 4



Следующая команда сработает так же, как и предыдущая:

| $ chmod 660 test.txt |
| -------------------- |

Можно ознакомиться с[руководством по правам доступа](https://github.com/mikeizbicki/ucr-cs100/tree/2015winter/textbook/using-bash/file-permission).

**chown** guille script.sh — сменить владельца файла script.sh на пользователя guille


### **Сочетания клавиш**

| **Сочетание** | **Описание**                        |
| ------------- | ----------------------------------- |
| **CTRL-A**    | Перемещение курсора в начало строки |
| **CTRL-E**    | Перемещение курсора в конец строки  |
| **CTRL-R**    | Поиск по истории                    |
| **CTRL-W**    | Вырезать последнее слово            |
| **CTRL-U**    | Вырезать всё до курсора             |
| **CTRL-K**    | Вырезать всё после курсора          |
| **CTRL-Y**    | Вернуть последнюю вырезанную строку |
| **CTRL-\_**   | Отмена                              |
| **CTRL-L**    | Очистка экрана терминала            |


### **Смена пользователей**

| **Команда**   | **Действие**                                                                         |
| ------------- | ------------------------------------------------------------------------------------ |
| **su**        | Смена текущего пользователя на администратора (root)                                 |
| **su -**      | Смена текущего пользователя на администратора (root), со сменой локальных переменных |
| **su maria**  | Смена текущего пользователя на maria                                                 |
| **sudo nano** | Выполнить команду nano от имени администратора (root)                                |


### **Копирование и вставка в буфер обмена**

| \# Linux**echo "Hello my friend!" \| xclip**копировать "Hello my friend!" в буфер обмена**xclip -o >> pasted_text.txt**вставить содержимое буфера в текст файла    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| \# macOSecho "Hello my friend!" \| pbcopy**копировать "Hello my friend!" в буфер обмена**pbpaste >> pasted_text.txt**вставить содержимое буфера в текст файла**    |


### **Копирование, перемещение и удаление через терминал**

| **Команда**                                              | **Действие**                                          |
| -------------------------------------------------------- | ----------------------------------------------------- |
| **rmdir movies**                                         | Удалить пустой каталог movies                         |
| **rm -rf movies**                                        | Удалить каталог movies и его файлы                    |
| **rm file1.txt**                                         | Удалить файл file1.txt                                |
| **mv** /home/michael/myfile.txt /home/john/important.txt | Переместить файл из /home/michael в /home/john        |
| **cp** /home/michael/myfile.txt /home/john/important.txt | Скопировать файл из /home/michael в /home/john        |
| **cp** **-R** letters/ memories/                         | Скопировать содержимое папки letters в папку memories |
| **cp** **-R** letters ~/Desktop                          | Скопировать папку letters и вставить на рабочий стол  |


### **Поиск файлов**

| **Команда**                               | **Действие**                                                                     |
| ----------------------------------------- | -------------------------------------------------------------------------------- |
| **find . -name hello.txt**                | Найти файл с названием hello.txt в текущем каталоге                              |
| **find /home/joe/Downloads -name \*.pdf** | Найти PDF-файлы в папке Downloads                                                |
| **find / -executable -atime -10**         | Найти исполняемые файлы в каталоге root, доступ к котором был 10 минут назад     |
| **find ~ -newer reference.txt**           | Найти в домашнем каталоге файл, который редактировался после файла reference.txt |


### **Вычисление контрольной суммы SHA256 файла**

| \# Linux**sha256sum file.txt**вычисление контрольной суммы SHA 256 файла**echo -n “foobar” \| sha256sum**вычисление контрольной суммы SHA 256 слова foobar          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \# macOS**shasum -a 256 file.txt**вычисление контрольной суммы SHA 256 файла**echo -n “foobar” \| shasum -a 256**вычисление контрольной суммы SHA 256 слова foobar  |


### **Сжатие и распаковка TAR/ZIP-файлов**

| **Команда**                          | **Действие**                                  |
| ------------------------------------ | --------------------------------------------- |
| **tar -cvzf myfile.tar myfolder**    | Сжатие папки my_folder в архив myfile.tar     |
| **tar -xvzf myfile.tar**             | Распаковка файла myfile.tar в текущий каталог |
| **tar -C /opt/abc -xvzf myfile.tar** | Распаковка файла myfile.tar в /opt/abc        |
| **zip -r myfile.zip myfolder**       | Сжатие папки my_folder в архив myfile.zip     |
| **unzip myfile.zip**                 | Распаковка файла myfile.zip в текущий каталог |


#### Свободное место на диске

| **Команда** | **Действие**                                              |
| ----------- | --------------------------------------------------------- |
| **df -k .** | Свободное место в текущем каталоге                        |
| **df -k**   | Доступное пространство в смонтированных файловых системах |