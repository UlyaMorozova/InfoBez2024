---
## Front matter
title: "Отчет к индивидуальному проекту, этап 1"
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

Цель работы установить дистрибутив Kali Linux в виртуальную машину.


# Выполнение проекта

Устанавливаем операционную систему также, как в лабораторной работе №1.

![Имя операционной системы](image/1.png)

![ОЗУ](image/2.png)

![Виртуальный жесткий диск](image/3.png)

![Итоговая конфигурация](image/4.png)

![Выбор носителей](image/5.png)

![Запуск виртуальной машины: выбор языка](image/6.png)

![Запуск виртуальной машины: выбор страны](image/7.png)

![Запуск виртуальной машины: загрузка компонентов](image/8.png)

![Настройка сети: имя компьютера](image/9.png)

![Настройка сети: имя домена](image/10.png)

![Настройка учетных записей: имя пользователя](image/11.png)

![Настройка учетных записей: пароль](image/12.png)

![Настройка времени](image/13.png)

![Разметка дисков](image/14.png)

![Файловая система](image/15.png)

![Разметка дисков 2](image/16.png)

![Установка базовой системы](image/17.png)

![Завершение установки](image/18.png)


# Выводы

Мы установили дистрибутив Kali Linux.  


::: {#refs}
:::
