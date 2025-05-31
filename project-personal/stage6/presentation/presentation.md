---
## Front matter
lang: ru-RU
title:  Индивидуальный проект.Этап 6
author: |
	  Швед Карина\inst{1}

institute: |
	\inst{1}Российский Университет Дружбы Народов

date: 4 апреля, 2025, Москва, Россия

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true

---

# Цели и задачи работы

## Задачи 3-го этапа

Размещение двуязычного сайта на Github.

Сделать поддержку английского и русского языков.
Разместить элементы сайта на обоих языках.
Разместить контент на обоих языках.
Сделать пост по прошедшей неделе.
Добавить пост на тему по выбору (на двух языках).


# Выполнение

##  убрала общее menus.yaml, так как собираюсь делать его на 2 языках. Далее создаю новую структуру. В content я создаю два каталога en и ru для англоязычного и русскоязычного контента соответственно

![2 каталога для английского и русского контента](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-50-38.png){#fig:001 width=70%}

# Добавляю в конфиг такой блок, чтобы Hugo понимал, что есть две языковые версии — английская и русская.

![конфиг](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-51-11.png){#fig:002 width=70%}

# Теперь вся моя информация дублируется на двух языках. Предварительно я запустила hugo server, чтобы отслеживать изменения

![био на русском](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_21-52-37.png){#fig:003 width=70%}

#  Далее я добавляю weekly-update и пост на тему дискретной математики в жизни аналитика

![пост про дискретную математику](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_22-27-21.png){#fig:006 width=70%}

# Далее ввожу hugo, чтобы забилдить сайт.Теперь я запускаю скрипт deploy.sh,который обновляет оид анные в удаленном репозитории на github

![комит](/home/vboxuser/Desktop/personalsitereports/6th step/report/image/image_2025-05-31_22-29-26.png){#fig:007 width=70%}


# Выводы
На данном этапе я разместила двуязычный сайт на Github.

