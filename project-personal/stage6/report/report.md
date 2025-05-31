---
## Front matter
title: "Индивидуальный проект"
subtitle: " Этап 6"
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


# Задачи 6-го этапа

Размещение двуязычного сайта на Github.

Сделать поддержку английского и русского языков.
Разместить элементы сайта на обоих языках.
Разместить контент на обоих языках.
Сделать пост по прошедшей неделе.
Добавить пост на тему по выбору (на двух языках).


# Выполнение лабораторной работы

Для начала я убрала общее menus.yaml, так как собираюсь делать его на 2 языках. Далее создаю новую структуру. В content я создаю два каталога en и ru для англоязычного и русскоязычного контента соответственно. Туда я дублирую все папки post,publication и т.д, но информацию и посты пишу на нужных языках

![2 каталога для английского и русского контента](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-50-38.png){#fig:001 width=70%}

Добавляю в конфиг такой блок, чтобы Hugo понимал, что есть две языковые версии — английская и русская.

![конфиг](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-51-11.png){#fig:002 width=70%}

Теперь вся моя информация дублируется на двух языках. Предварительно я запустила hugo server, чтобы отслеживать изменения

![био на русском](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-52-25.png){#fig:003 width=70%}


![био на английском](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-52-37.png){#fig:004 width=70%}

Далее я добавляю weekly-update и пост на тему дискретной математики в жизни аналитика

![weekly-update 31/05/2025](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_22-22-52.png){#fig:005 width=70%}

![пост про дискретную математику](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_22-27-21.png){#fig:006 width=70%}

Далее ввожу hugo, чтобы забилдить сайт.Теперь я запускаю скрипт deploy.sh,который обновляет оид анные в удаленном репозитории на github

![комит](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_22-29-26.png){#fig:007 width=70%}



# Выводы
На данном этапе я разместила двуязычный сайт на Github.
