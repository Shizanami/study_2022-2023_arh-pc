---
## Front matter
title: "Лабораторная работа №5"
subtitle: "Архитектура вычислительных систем"
author: "Дадилов Руслан"

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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Задание

1. Создайте копию файла lab6-1.asm. Внесите изменения в программу (без использования внешнего файла in_out.asm), так чтобы она работала по следующему алгоритму: 
• вывести приглашение типа “Введите строку:”; 
• ввести строку с клавиатуры; 
• вывести введённую строку на экран.
2. Получите исполняемый файл и проверьте его работу. На приглашение ввести строку введите свою фамилию. 
3. Создайте копию файла lab6-2.asm. Исправьте текст программы с использование подпрограмм из внешнего файла in_out.asm, так чтобы она работала по следующему алгоритму: 
• вывести приглашение типа “Введите строку:”; 
• ввести строку с клавиатуры; 
• вывести введённую строку на экран. 
4. Создайте исполняемый файл и проверьте его работу.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно об Unix см. в [@gnu-doc:bash;@newham:2005:bash;@zarrelli:2017:bash;@robbins:2013:bash;@tannenbaum:arch-pc:ru;@tannenbaum:modern-os:ru].

# Выполнение лабораторной работы

1. Открываем mc.

![mc](image/51.png){ #fig:001 width=90% }


2. Создаем директорию по условию задания .
 Создаем файл lab5-1 с помощью F7.

![mc](image/52.png){ #fig:002 width=90% }

3. Вводим текст программы из задания в туис.

![mc](image/53.png){ #fig:003 width=90% }

4. Вводим данные ФИ

![mc](image/54.png){ #fig:004 width=90% }

5. Создаем файл lab5-2.

![mc](image/55.png){ #fig:005 width=90% }

6. Изменяем код в lab5-2.

![mc](image/56.png){ #fig:006 width=90% }

7. Похожие действия выполняем с lab5-3.

![mc](image/57.png){ #fig:007 width=90% }

![mc](image/58.png){ #fig:008 width=90% }
 


# Самостоятельная работа

1. Создаем копию файла lab5-1.asm. Внесем изменения в программу), так чтобы она работала по следующему алгоритму:
• вывести приглашение типа “Введите строку:”; 
• ввести строку с клавиатуры; 
• вывести введённую строку на экран. 

Копируем файл. 

![mc](image/59.png){ #fig:009 width=90% }

![mc](image/510.png){ #fig:010 width=90% }

2. Дописываем 4 строки после call sread вызывающие функцию sprintLF.
Создаем исполняемый файл и проверяем его работу.

![mc](image/511.png){ #fig:011 width=90% }




# Выводы

В ходе выполнения данной лабораторной работы были приобретены практические навыки работы в Midnight Commander. Были освоены инструкции языка ассемблера mov и int.

# Список литературы{.unnumbered}

::: {#refs}:
