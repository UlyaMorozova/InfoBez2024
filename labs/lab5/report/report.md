---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "*дисциплина: Информационная безопасность*"
author: "Морозова Ульяна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: false # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.

# Подготовка к лабораторной работе

Перед тем как начнем выполнять задания убедимся, что у нас установлен компилятор gcc (рис. [-@fig:001]).

![gcc -v](image/1.png){#fig:001 width=70%}

# Выполнение лабораторной работы

## Создание программ

1. Зайдем  систему о имени пользователя ukmorozova и создадим файл simpleid.c (рис. [-@fig:002]).

![Создание файла](image/2.png){#fig:002 width=70%}

2. Скомпилируем программу и убедимся, что исполнительный файл был создан, затем выполним пррограмму simpleid и сравним ее с выполнением команды id (рис. [-@fig:003] - рис. [-@fig:004])

![Выполнение программы simpleid](image/3.png){#fig:003 width=70%}

![Выполнение команды id](image/4.png){#fig:004 width=70%}

Как видно, команды выводят одинаковую информацию.

3. Усложним программу (рис. [-@fig:005]) скомпилируем и запустим ее (рис. [-@fig:006]).

![simpleid2.c](image/5.png){#fig:005 width=70%}

![Запуск simpleid2](image/6.png){#fig:006 width=70%}

4. От имени суперпользователя выполняем следующие команды
```bash
chown root:guest /home/guest/simpleid2
chmod u+s /home/guest/simpleid2
```
и проверяем правильность выполнения команд (рис. [-@fig:007]).

![Изменение атрибута s](image/7.png){#fig:007 width=70%}

Запускаем программу simpleid2 и команду id (рис. [-@fig:008]).

![Выполнение команд](image/9.png){#fig:008 width=70%}

5. Создаем программу readfile.c (рис. [-@fig:009]) и откомпилируем ее (рис. [-@fig:010])

![readfile.c](image/10.png){#fig:009 width=70%}

![Компиляция программы](image/11.png){#fig:010 width=70%}

Меняем владельца файла, что ukmorozova не мог прочитать его (рис. [-@fig:011]), проверяем (рис. [-@fig:012]).

![Смена владельца](image/12.png){#fig:011 width=70%}

![Проверка](image/13.png){#fig:012 width=70%}

Установим SetU'D-бит (рис. [-@fig:013]).

![SetU'D-бит](image/14.png){#fig:013 width=70%}

6. Пробуем прочитать разные файлы с помощью программы readfile.c (рис. [-@fig:014] - рис. [-@fig:016]))

![Чтение файлов](image/15.png){#fig:014 width=70%}

![Чтение файлов](image/16.png){#fig:015 width=70%}

![Чтение файлов](image/17.png){#fig:016 width=70%}

## Исследование Sticky-бита

1. Выясним, установлен ли атрибут Sticky на директории /tmp и создадим файл file01.txt в директории /tmp со словом test (рис. [-@fig:017]).

![tmp](image/18.png){#fig:017 width=70%}

3. Просмотрим атрибуты у только что созданного файла и разрешим чтение и запись для категории пользователей «все остальные» (рис. [-@fig:018])

![Изменение прав](image/19.png){#fig:018 width=70%}

4. От имени другого пользователя попробуем прочитать файл /tmp/file01.txt (рис. [-@fig:019]).

![Чтение файла](image/20.png){#fig:019 width=70%}

5. Попробуем дозаписать в файл /tmp/file01.txt слово test2 командой и проверим содержимое файла, затем попробуем удалить его (рис. [-@fig:020]).

![Работа с файлом](image/21.png){#fig:020 width=70%}

6. Повысим свои права до суперпользователя и выполним команду, снимающую атрибут t (Sticky-бит) с директории /tmp (рис. [-@fig:021]).

![Убираем атрибут](image/22.png){#fig:021 width=70%}

Проверим выполнение команды от имени guest2 (рис. [-@fig:022]) и повторим шаги выше (рис. [-@fig:023]).

![Проверка](image/23.png){#fig:022 width=70%}

![Повторение команд](image/24.png){#fig:023 width=70%}

После всего возвращаем атрибут t (рис. [-@fig:024]).

![Возврат атрибута](image/25.png){#fig:024 width=70%}

# Выводы

Изучили механизмы изменения идентификаторов, применили SetUID- и Sticky-битов.

# Список литературы{.unnumbered}

::: {#refs}
:::
