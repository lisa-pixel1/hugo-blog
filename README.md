Отчёт по выполнению заданий
Дата: 6 октября 2026
Использованные команды GameShell:
- `gsh goal` — узнать цель текущей миссии
- `gsh check` — проверить выполнение миссии
- `gsh help` — список доступных команд
- `gsh reset` — начать миссию заново
- `gsh exit` — выйти из GameShell
- `cd LOCATION` — перейти в указанное место
- `cd` — вернуться в начальную локацию
- `cd ..` — перейти на уровень вверх
- `cd LOCATION1/LOCATION2` — выполнить несколько перемещений одной командой
- `pwd` — показать путь к текущему местоположению
- `ls` — показать список доступных мест
- `ls -A` — вывести все файлы, включая скрытые (начинаются с точки)
- `mkdir DIRECTORY` — создать новый каталог
- `rm FILE1 FILE2 ...` — удалить файлы
- `mv FILE1 FILE2 ... DIRECTORY` — переместить файлы
- `cp FILE DIRECTORY` — скопировать файл
- `~` — обозначение домашнего каталога
- `*` — заменяет любую последовательность символов
- `?` — заменяет любой одиночный символ
- `Tab` — автодополнение имени файла/каталога

Mission 1: Навигация по папкам (`cd` и `ls`)
Задача: Подняться на вершину башни замка
Использованные команды: `cd`, `ls`
Решение:
 
<img width="485" height="638" alt="миссия1" src="https://github.com/user-attachments/assets/654a9ef5-7afa-4bde-a64a-a339ba21f9de" />


Mission 2: Возврат назад и проверка пути (cd .. и pwd)
Задача: Научиться возвращаться на уровень вверх и проверять текущий путь
Использованные команды: cd, cd .., pwd, ls
Решение:
  cd
  pwd
  cd ..
  ls
  cd ..
  ls
  cd Cellar
  gsh check
<img width="572" height="577" alt="миссия2" src="https://github.com/user-attachments/assets/34a350f3-b759-4142-994c-5ddaf69e340c" />


Mission 3: Быстрый переход в глубокую папку
Задача: Перейти сразу в тронный зал одной командой, указав полный путь
Использованные команды: cd с полным путём
Решение:
  cd
  cd Castle/Main_building/Throne_room
  gsh check
<img width="489" height="179" alt="миссия3" src="https://github.com/user-attachments/assets/72c4355d-4eb5-4af7-8d57-ac3b05c47544" />


Mission 4: Создание папок (mkdir)
Задача: Создать хижину в лесу и сундук внутри неё
Использованные команды: cd, mkdir
Решение:
  cd
  cd Forest
  mkdir Hut
  cd Hut
  mkdir Chest
  gsh check
<img width="488" height="361" alt="миссия4" src="https://github.com/user-attachments/assets/704f033b-ac00-4033-aaed-58053abfb326" />


Mission 5: Удаление файлов (rm)
Задача: Избавиться от пауков в подвале замка
Использованные команды: cd, ls, rm
Решение:
  cd
  cd Castle
  cd Cellar
  ls
  rm spider_1 spider_2 spider_3
  gsh check
<img width="515" height="443" alt="миссия5" src="https://github.com/user-attachments/assets/6fdd56a3-5e18-4798-96c1-06bced7c358f" />


Mission 6: Перемещение файлов (mv)
Задача: Переместить монеты из сада в сундук в хижине
Использованные команды: mv, ~ (домашний каталог)
Решение:
  cd
  mv coin_1 coin_2 coin_3 ~/Forest/Hut/Chest
  gsh check
<img width="501" height="127" alt="миссия6" src="https://github.com/user-attachments/assets/8170c3e5-b425-48fd-bfdd-2e6de44d3b3d" />


Mission 7: Работа со скрытыми файлами (ls -A и mv)
Задача: Найти скрытые монеты (имена начинаются с точки) и переместить их в сундук
Использованные команды: ls -A, mv, ~
Решение:
  ls -A
  mv .15239_coin_3 .15719_coin_1 .6618_coin_2 ~/Forest/Hut/Chest
  gsh check
<img width="629" height="174" alt="миссия7" src="https://github.com/user-attachments/assets/27a9cfde-4913-4c0c-b23d-2d730005f6c9" />


Mission 8: Удаление по шаблону (rm *spider*)
Задача: Удалить все файлы, содержащие "spider" в имени, с помощью подстановочного символа
Использованные команды: cd, ls -A, rm, *
Решение:
  cd
  cd Castle
  cd Cellar
  ls -A
  rm *spider*
  ls -A
  gsh check
<img width="1910" height="621" alt="миссия8" src="https://github.com/user-attachments/assets/03e92d22-fe60-4849-ae9f-1349ac3c9fd8" />


Mission 9: Удаление скрытых файлов по шаблону (rm .*spider*)
Задача: Удалить скрытые файлы с пауками (имена начинаются с точки)
Использованные команды: ls -A, rm, .*
Решение:
  ls -A
  rm .*spider*
  gsh check
<img width="1867" height="259" alt="миссия9" src="https://github.com/user-attachments/assets/6103f282-aaa1-4328-8226-b56cc3d39906" />


Mission 10: Копирование файлов по шаблону (cp *standard*)
Задача: Скопировать стандартные доспехи из большого зала в сундук
Использованные команды: cd, ls -A, cp, *
Решение:
  cd
  cd Castle
  cd Great_hall
  ls -A
  cp *standard* ~/Forest/Hut/Chest
  gsh check
<img width="891" height="443" alt="миссия10" src="https://github.com/user-attachments/assets/f34d6dbd-5a4a-4d89-ad6c-3e70d6eb36a9" />


Дата: 13 октября 2026
CTF-уровни

Уровень 0: Поиск пароля в файле
Задача: Найти пароль для level1 в домашней директории. Он лежит в файле readme.txt.
Использованные команды: ls, cat
Решение:
  cat readme.txt
<img width="530" height="210" alt="уровень0" src="https://github.com/user-attachments/assets/999c6473-6b3e-42a7-9822-9ba151820970" />


Уровень 1: Поиск пароля в скрытом файле
Задача: Найти пароль, который спрятан в скрытом файле внутри папки inhere.
Использованные команды: cd, ls -A, cat
Решение:
  cd inhere
  ls -A
  cat .hidden
<img width="544" height="274" alt="уровень1" src="https://github.com/user-attachments/assets/11654654-2be3-44de-a29e-a14c0eaf8c26" />


Уровень 2: Поиск строки в файле
Задача: Найти строку со словом 'millionth' в файле data.txt.
Использованные команды: grep
Решение:
  grep 'millionth' data.txt
<img width="544" height="171" alt="уровень2" src="https://github.com/user-attachments/assets/527d4da0-a265-4ac9-97bc-0b85e3b21af0" />


Уровень 3: Поиск файла с необычным именем
Задача: Найти файл readme с необычным именем (начинается с дефиса и пробела) и прочитать его.
Использованные команды: ls, cat
Решение:
  ls
  cat './- readme!'
<img width="544" height="283" alt="уровень3" src="https://github.com/user-attachments/assets/203d4fc8-a19e-4290-9048-d7b7da6e194a" />


Уровень 4: Работа с архивом
Задача: Найти ключ, который спрятан внутри архива archive.tar.gz в домашнем каталоге.
Использованные команды: ls -la, tar, cd, cat
Решение:
  ls -la
  tar -xzf archive.tar.gz -C /tmp
  cd /tmp
  ls -la
  cat readme
<img width="544" height="463" alt="уровень4" src="https://github.com/user-attachments/assets/9342e13e-aad7-47c5-bc1b-8296b992b5e9" />


Уровень 5: Расшифровка ROT13
Задача: Файл data.txt закодирован шифром ROT13. Нужно его расшифровать и получить пароль.
Использованные команды: cat, tr
Решение:
  ls
  cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
<img width="565" height="189" alt="уровень5" src="https://github.com/user-attachments/assets/92a0ec95-a234-4415-9898-a80654fb474f" />


Дата: 20 октября 2026
Command Challenge
Мы решали интерактивные задачи на сайте cmdchallenge.com. Каждое задание было обозначено иконкой животного или насекомого. 
Чтобы пройти уровень, нужно написать правильную команду в терминале. 
Задания были разной сложности: от простых, например посчитать сумму чисел в файле, до более сложных, где требовалась работа с текстом, фильтрация и сортировка данных.
<img width="914" height="384" alt="кошечкисобачки" src="https://github.com/user-attachments/assets/6f51f283-16a4-4bbf-b260-0a3fdbfae52c" />






