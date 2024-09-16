---
## Front matter
title: "Отчет по лабораторной работе №3"
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
lot: true # List of tables
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

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Выполнение лабораторной работы

1. В установленной операционной системе создаем учётную запись пользователя guest1 (использую учётную запись администратора) и задаем пароль для пользователя guest1 (использую учётную запись администратора). Аналогично создаем второго пользователя guest2.

![Создание пользователей](image/1.png){#fig:001 width=70%}

2. Добавляем пользователя guest2 в группу guest:

![Группировка пользователей](image/2.png){#fig:001 width=70%}

3. Осуществим вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли, и определим директорию для обоих пользователей.

![guest1](image/3.png){#fig:001 width=70%}

![guest2](image/5.png){#fig:001 width=70%}

4. Уточним имя наших пользователей, их группу. 

![guest1](image/4.png){#fig:001 width=70%}

![guest2](image/6.png){#fig:001 width=70%}

![guest2](image/7.png){#fig:001 width=70%}

![guest1](image/8.png){#fig:001 width=70%}

5. Просмотрим файл командой
cat /etc/group

![guest1](image/9.png){#fig:001 width=70%}

![guest2](image/10.png){#fig:001 width=70%}

6. От имени пользователя guest2 выполним регистрацию пользователя guest2 в группе guest командой newgrp guest.

![guest2](image/11.png){#fig:001 width=70%}

7. От имени пользователя guest изменим права директории /home/guest, разрешив все действия для пользователей группы:
chmod g+rwx /home/guest и снимим с директории /home/guest/dir1 все атрибуты командой chmod 000 dirl

![Изменение прав доступ](image/12.png){#fig:001 width=70%}

8. Таблица прав доступа 

![](image/13.png){#fig:001 width=70%}

![](image/14.png){#fig:001 width=70%}

![](image/15.png){#fig:001 width=70%}

![](image/16.png){#fig:001 width=70%}

![](image/17.png){#fig:001 width=70%}

![](image/18.png){#fig:001 width=70%}

![](image/19.png){#fig:001 width=70%}

![](image/20.png){#fig:001 width=70%}


# Выводы

Мы получили практические навыки работы в консоли с атрибутами файлов для групп пользователей.

# Список литературы{.unnumbered}

::: {#refs}
:::
