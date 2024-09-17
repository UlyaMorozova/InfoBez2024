---
## Front matter
title: "Отчет по лабораторной работе №1"
subtitle: "*дисциплина: Операционные системы*"
author: "Морозова Ульяна Константиновна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: false # List of figures
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

# **Цель работы**

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.


# Выполнение лабораторной работы

1.Заходим в терминал и переходим в каталог /var/tmp с помощью команды cd, создаем папку ukmorozova и запускаем VirtualBox. (рис. [-@fig:001]).

![Консоль](image/1.png){#fig:001 width=70%}

2. Создаем новую виртуальную машину (рис. [-@fig:002]). Указываем необходимые характеристики. (рис. [-@fig:003] - [-@fig:004])

3. Добавляем оптический диск через "Носитель". (рис. [-@fig:005] - [-@fig:006])

4. Запускаем нашу виртуальную машину. (рис. [-@fig:007])

5. После запуска продолжаем настройку виртуальной машины. Выбираем английский язык (рис. [-@fig:008] - [-@fig:009]), и настраиваем все остальное (рис. [-@fig:010] - [-@fig:014]).

6. После завершения настройки перезагружаем машину. (рис. [-@fig:015] - [-@fig:016]) Создаем пользователя (рис. [-@fig:017]) и выполняем домашнее задание  (рис. [-@fig:018]).


![Создание вирт.машины](image/2.png){#fig:002 width=70%}

![Память машины](image/3.png){#fig:003 width=70%}

![Основной диск](image/4.png){#fig:004 width=70%}

![Носитель](image/5.png){#fig:005 width=70%}

![Оптический диск](image/6.png){#fig:006 width=70%}

![Запуск](image/7.png){#fig:007 width=70%}

![Выбор языка](image/8.png){#fig:008 width=70%}

![Настройка виртуальной машины](image/9.png){#fig:009 width=70%}

![KDUMP](image/10.png){#fig:010 width=70%}

![Место установки](image/11.png){#fig:011 width=70%}

![Пользователь](image/12.png){#fig:012 width=70%}

![Сеть и имя узла](image/13.png){#fig:013 width=70%}

![Завершение настройки](image/14.png){#fig:014 width=70%}

![Запуск виртуальной машины](image/15.png){#fig:015 width=70%}

![Перезагрузка](image/16.png){#fig:016 width=70%}

![Создание пользователя](image/17.png){#fig:017 width=70%}

![Домашнее задание](image/18.png){#fig:018 width=70%}


# Выводы

Мы приобрели практические навыки в установке операционной системы на виртуальную машину и настройке минимально необходимых для дальнейшей работы сервисов.

::: {#refs}
:::