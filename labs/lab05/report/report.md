---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Архитектура компьютеров и операционные системы"
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

Получение навыков как правильно работать с pass,а также управлять файлами конфигурации


# Выполнение лабораторной работы

**Browserpass**

Откыла терминал и установила pass и pass-otp (это дополнение для двухфакторной аутентификации) через пакетный менеджер dnf

![Установка pass](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-12-14.jpg){#fig:001 width=70%}

Далее перехожу к настройке.  Сначала я проверила , есть ли у меня уже секретные ключи GPG:

![проверка gpg keys](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-12-40.jpg){#fig:002 width=70%}

У меня уже есть секретный ключ GPG, который я можешь использовать для шифрования паролей с помощью менеджера паролей pass.

Теперь я  продолжаю настройку хранилища паролей. Следующий шаг — инициализация хранилища с использованием этого ключа .Я ввожу  команду для инициализации хранилища паролей с использованием моего GPG-ключа. Я использую либо адрес электронной почты, связанный с этим ключом

![инициализация хранилища с использованием этого ключа](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-12-46.jpg){#fig:003 width=70%}
Теперь  хранилище паролей настроено и готово к использованию. Я хочу  синхронизировать базу паролей через Git, поэтому настраиваю Git-репозиторий в каталоге .password-store. Был создан новый Git-репозиторий в каталоге .password-store на моей машине.

![настройка Git-репозитория в каталоге .password-store](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-12-52.jpg){#fig:004 width=70%}

Чтобы синхронизировать пароли с удаленным репозиторием, я добавляю удаленный репозиторий GitHub, предварительно создав его

![создание репозитория](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-12-58.jpg){#fig:005 width=70%}

Теперь мой репозиторий для паролей доступен через GitHub

![репозиторий](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-03.jpg){#fig:006 width=70%}
Далее я выполняю настройку интерфейса с браузером (через Browserpass). Она необходима для того, чтобы интегрировать мой менеджер паролей (pass) с веб-браузером. Это позволитт автоматически заполнять пароли на веб-сайтах и управлять паролями прямо из браузера.

Browserpass — это расширение для браузера, которое взаимодействует с менеджером паролей на моем компьютере (в моем случае с pass), чтобы я могла получать пароли прямо из браузера без необходимости вручную их копировать. Сначала  я установила плагин в браузер

![настройка Browserpass](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-09.jpg){#fig:007 width=70%}

теперь установим необходимые зависимости и программы для работы с интерфейсом native messaging

![ native messaging](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-15.jpg){#fig:008 width=70%}

Я добавила собственный пароль и затем заменила его на автоматически сгенерированный

![ native messaging](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-21.jpg){#fig:009 width=70%}

**Управление файлами конфигурации**

Для начала, нужно установить несколько утилит, которые помогут настроить рабочее окружение и расширят возможности системы (ПО и шрифты). Проверка шрифтов

![ установка шрифтов и ПО. Проверка шрифтов](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-27.jpg){#fig:010 width=70%}

chezmoi — это инструмент для управления конфигурационными файлами. Устанавливаю его

![ установка chezmoi](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-44.jpg){#fig:011 width=70%}

Создаю новый репозиторий для моих конфигурационных файлов на GitHub на основе шаблона. Далее инициализирую chezmoi с моим репозиторием dotfiles. Проверила какие изменения внесёт chezmoi в домашний каталог, принимаю их

![ создание нового репозитория для моих конфигурационных файлов на GitHub](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-50.jpg){#fig:012 width=70%}

Я хочу  настроить такую же конфигурацию на другой машине ( ubuntu).  Для это я cначала скачиваю chezmoi на Ubuntu

![ скачиваю chezmoi на Ubuntu](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-13-56.jpg){#fig:013 width=70%}

Теперь я хочу внести небольшие изменения и проверить, как работает синхронизация с помощью chezmoi.Перед внесением изменений я  сделала резервные копии файлов, чтобы в случае ошибки их восстановить.  Затем открываю файл echo "Hello from Bash" и пишу туда echo "Hello from Bash". Проверяю изменения.Так как это были тестовые изменения я не принимаю их и нажимаю skip

![ изменение конфигурационного файла](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-14-01.jpg){#fig:014 width=70%}

Для включения автоматической фиксации и отправки изменений в репозиторий я отредактировала файл конфигурации chezmoi.toml.Теперь, когда я будете вносить изменения в файлы через chezmoi, эти изменения будут автоматически коммититься и отправляться в мой  репозиторий на GitHub

![ настройка автоматизации](/home/vboxuser/Desktop/labsreports/lab5/report/image/photo_2025-03-15_11-14-06.jpg){#fig:015 width=70%}

# Выводы

Я получила навыки как правильно работать с pass,а также управлять файлами конфигурации




