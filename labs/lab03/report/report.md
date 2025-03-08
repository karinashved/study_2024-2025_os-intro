---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Markdown"
author: "Швед Карина Дмитриевна"

## Generic options
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

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.


# Задание

* Сделайте отчёт по предыдущей лабораторной работе в формате Markdown.
* В качестве отчёта просьба предоставить отчёты в 3 форматах: pdf, docx и md (в архиве,
поскольку он должен содержать скриншоты, Makefile и т.д.)


##Для начала я захожу в папку lab02 и начинаю оформлять Markdown файл


![редактирование md файла](/home/vboxuser/Desktop/labsreports/lab3/report/image/photo_2025-03-08_11-58-54.jpg){#fig:001 width=70%}

**я заранее скачала изображения и поместила их в папку image**

![изображения в папке image](/home/vboxuser/Desktop/labsreports/lab3/report/image/photo_2025-03-08_11-59-17.jpg){#fig:002 width=70%}

**После того, как я отредактировала md файл и вставила изображения, я открываю папку report в терминале и выполняю команды для создания pdf,docx файла из md**

![ создание  файлов report  в форматах pdf, doсx](/home/vboxuser/Desktop/labsreports/lab3/report/image/photo_2025-03-08_11-59-25.jpg){#fig:003 width=70%}

![ файлы report  в форматах pdf, doсx](/home/vboxuser/Desktop/labsreports/lab3/report/image/Pasted image.png){#fig:004 width=70%}

![мой полученный pdf файл наглядно](/home/vboxuser/Desktop/labsreports/lab3/report/image/Pasted image2.png){#fig:005 width=70%}


# Выводы
Я изучила синтаксис языка разметки Markdown, получила отчет из шаблона при помощи Makefile


