---
## Front matter
title: "Индивидуальный проект"
subtitle: " Этап 3"
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


# Задачи 3-го этапа

Добавить к сайту достижения.

Список достижений:
Добавить информацию о навыках (Skills).
Добавить информацию об опыте (Experience).
Добавить информацию о достижениях (Accomplishments).
Сделать пост по прошедшей неделе.
Добавить пост на тему по выбору:
Легковесные языки разметки.
Языки разметки. LaTeX.
Язык разметки Markdown.


# Выполнение лабораторной работы

Сначала я запускаю hugo server, чтобы видеть как изменения файлов влияют на мой сайт

Добавила достижения в файл /home/vboxuser/work/blog/content/authors/_index.md

![изменение файла _index.md](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_12-59-33.jpg){#fig:001 width=70%}


![достижения](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-02-55.jpg){#fig:002 width=70%}

![достижения](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-03-01.jpg){#fig:003 width=70%}

Теперь я перехожу к каталогу content/posts и внутри него создаю md файл для поста об Markdown,внутри каталога /home/vboxuser/work/blog/content/post/weekly-update я просто создаю еще один текстовый файл для описания прошлой недели

![добавление постов](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-06-49.jpg){#fig:004 width=70%}

Проверяю на локальном сервере как теперь выглядят мои посты

![мои новые посты на сайте](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-08-21.jpg){#fig:005 width=70%}

![мои новые посты на сайте](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-08-27.jpg){#fig:006 width=70%}

Теперь у меня 4 поста на сайте

![мои 4 поста](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-09-37.jpg){#fig:007 width=70%}

Затем я перехожу в каталог blog и ввожу команду ~/bin/hugo начинает создаваться мой сайт. Теперь я копирую новое содержимое папки /home/vboxuser/work/blog/public в /home/vboxuser/work/karinashved.github.io. Затем добавляю изменения и фиксирую их на github. Теперь я могу открыть свой сайт в Интернете

![мой сайт в интернете](/home/vboxuser/Desktop/personalsitereports/3d step/report/image/photo_2025-04-12_13-11-29.jpg){#fig:008 width=70%}



# Выводы
На данном этапе я добавила достижения на свой сайт, а также 2 поста на тему прошедшей недели и статью о Markdown
