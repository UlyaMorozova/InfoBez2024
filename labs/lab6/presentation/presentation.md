---
## Front matter
lang: ru-RU
title: Лабораторная работа №6
author:
  - Морозова У.К.
institute:
  - Российский университет дружбы народов, Москва, Россия

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель работы

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1.
Проверить работу SELinx на практике совместно с веб-сервером Apache.

# Подготовка к лабораторной работе 

![Установка обновлений](image/1.png){#fig:001 width=70%}

![Скачивание Apache](image/2.png){#fig:002 width=70%}

# Выполнение лабораторной работы

## 1

![getenforce и sestatus](image/3.png){#fig:003 width=70%}

## 2

![httpd](image/4.png){#fig:004 width=70%}

## 3

![веб-сервер Apache](image/5.png){#fig:005 width=70%}

## 4

![переключатели SELinux](image/6.png){#fig:006 width=70%}

## 5

![seinfo](image/7.png){#fig:007 width=70%}

## 6

![/var/www](image/8.png){#fig:008 width=70%}

## 7

![/var/www/html](image/9.png){#fig:009 width=70%}

## 8

![Создание файла](image/10.png){#fig:010 width=70%}

![test.html](image/11.png){#fig:011 width=70%}

## 9

![контекст test.html](image/12.png){#fig:012 width=70%}

## 10

![test.html](image/13.png){#fig:013 width=70%}

## 11

![Изменение контекста](image/14.png){#fig:014 width=70%}

## 12

![Ошибка](image/15.png){#fig:015 width=70%}

## 13

![log-файлы веб-сервера Apache](image/16.png){#fig:016 width=70%}

## 14

![Listen 81](image/17.png){#fig:017 width=70%}

## 15

![лог-файлы](image/18.png){#fig:018 width=70%}

## 16

![error_log](image/19.png){#fig:019 width=70%}

## 17

![веб-сервер Apache](image/21.png){#fig:021 width=70%}

# Выводы

Развили навыки администрирования ОС Linux. Получили первое практическое знакомство с технологией SELinux1.
Проверили работу SELinx на практике совместно с веб-сервером Apache.
