---
## Front matter
title: "Отчёт по лабораторной работе №11"
subtitle: "Текстовой редактор emacs"
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs.



# Выполнение лабораторной работы

установливаю Emacs через пакетный менеджер. sudo dnf install emacs
![устанвка emacs](/home/vboxuser/Desktop/labsreports/lab11/report/image/photo_2025-04-26_08-11-51.jpg){#fig:001 width=70%}

открываю emacs.Нажимаю: C-x C-f, ввожу lab07.sh, затем сохраняю C-x C-s

![emacs открытие](/home/vboxuser/Desktop/labsreports/lab11/report/image/photo_2025-04-26_08-12-12.jpg){#fig:002 width=70%}

Далее проделываю с текстом стандартные процедуры редактирования, каждое действие осуществляюя комбинацией клавиш.
5.1. Вырезать одной командой целую строку (С-k).
5.2. Вставить эту строку в конец файла (C-y).
5.3. Выделить область текста (C-space).
5.4. Скопировать область в буфер обмена (M-w).
5.5. Вставить область в конец файла.
5.6. Вновь выделить эту область и на этот раз вырезать её (C-w).
5.7. Отмените последнее действие (C-/).

![редактирование файла в emacs](/home/vboxuser/Desktop/labsreports/lab11/report/image/photo_2025-04-26_08-12-21.jpg){#fig:003 width=70%}

![пример редактирование файла в emacs](/home/vboxuser/Desktop/labsreports/lab11/report/image/photo_2025-04-26_08-12-30.jpg){#fig:004 width=70%}

![список активных буферов](/home/vboxuser/Desktop/labsreports/lab11/report/image/photo_2025-04-26_08-12-38.jpg){#fig:005 width=70%}

![переключение между окнами](/home/vboxuser/Desktop/labsreports/lab11/report/image/photo_2025-04-26_08-12-45.jpg){#fig:006 width=70%}


# Выводы
Я познакомилась с операционной системой Linux. Получила практические навыки работы с редактором Emacs.



# Контрольные вопросы

**1.  Какие особенности данного редактора могут сделать его сложным для освоения новичком?**  
Emacs — это мощный и расширяемый текстовый редактор, который предоставляет широкие возможности для редактирования текста, написания программ и работы с различными форматами файлов. Он поддерживает множество языков программирования, расширяется с помощью плагинов и макросов, а также позволяет пользователю кастомизировать интерфейс.


**2. Какие особенности данного редактора могут сделать его сложным для освоения новичком?**  
Особенности, которые могут затруднить освоение новичком: необычные сочетания клавиш, необходимость изучения команд, работа через командную строку, отсутствие графического интерфейса, а также большое количество настроек и плагинов, которые требуют времени на освоение.

**3.  Своими словами опишите, что такое буфер и окно в терминологии emacs’а.**

В Emacs буфер — это область памяти, которая хранит данные открытого файла или другого контента. Окно — это часть экрана, которая отображает один или несколько буферов одновременно, позволяя пользователю работать с ними

**4. Можно ли открыть больше 10 буферов в одном окне?**  
Да, в Emacs можно открыть больше 10 буферов в одном окне. Количество буферов не ограничено количеством окон, и их можно свободно переключать между собой.

**5.  Какие буферы создаются по умолчанию при запуске emacs?**

При запуске Emacs создаются несколько стандартных буферов, таких как *scratch* (буфер для незавершенных заметок), *Messages* (вывод сообщений об ошибках и информационных сообщений), а также *Help* (система помощи).

**6.  Какие клавиши вы нажмёте, чтобы ввести следующую комбинацию C-c | и C-c C-|?**

Для ввода комбинации C-c | нужно нажать Ctrl + c, затем клавишу |. Для C-c C-| нужно сначала нажать Ctrl + c, затем снова Ctrl + |.
**7.  Как поделить текущее окно на две части?**

Чтобы поделить текущее окно на две части в Emacs, надо использовать команду C-x 2.

**8.  В каком файле хранятся настройки редактора emacs?**  
Настройки Emacs обычно хранятся в файле .emacs или init.el, который находится в домашней директории пользователя.

**9. Какую функцию выполняет клавиша и можно ли её переназначить?**

Клавиша C-x выполняет различные команды в Emacs, такие как закрытие буферов, сохранение файлов и другие операции. Она может быть переназначена в конфигурационных файлах, если это необходимо.

**10.  Какой редактор вам показался удобнее в работе vi или emacs? Поясните почему**  
Лично мне удобнее работать с Emacs, так как он предоставляет более широкие возможности для кастомизации, поддерживает множество плагинов и позволяет адаптировать редактор под конкретные задачи. В отличие от vi, Emacs обладает более гибкой настройкой и возможностями для работы с текстом, что делает его более удобным для долгосрочной работы.


