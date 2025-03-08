---
## Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Управление версиями"
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

Целью данной работы является изучение идеологии и применения средств контроля версий и освоение умений работать с git.

# Выполнение лабораторной работы

 **Установка git, установка gh**

![dnf install git](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-10-37.jpg){#fig:001 width=70%}


**Далее я задаю имя и email владельца репозитория,utf-8 в выводе сообщений git:**

![git config --global user.](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-11-23.jpg){#fig:002 width=70%}

**Настраиваю верификацию и подписание коммитов git. Создание  ssh ключа и добавление его на github**

![ ssh key](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-11-55.jpg){#fig:003 width=70%}
![ ssh key](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-12-55.jpg){#fig:004 width=70%}

**Создание ключа pgp**
Сначала я ввожу dnf insstall gnupg. Эта команда устанавливает GnuPG (GPG) — инструмент для шифрования, подписи данных и управления криптографическими ключами.Затем генерирую ключ

![ dnf insstall gnupg](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-11-31.jpg){#fig:005 width=70%}
![ gpg --full-generate-key](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-12-07.jpg){#fig:006 width=70%}

Далее с помощью консоли, собственного токена и API я добавляю gpg ключ к себе на гитхаб

![ добавление gpg ключа через консоль](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-12-17.jpg){#fig:007 width=70%}
![ проверка того, что gpg ключ успешно настроен](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-12-24.jpg){#fig:008 width=70%}


 **Настройка автоматических подписей коммитов**

![ git config --global](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-12-31.jpg){#fig:009 width=70%}
  **Настройка gh и создание рабочего пространства на основе шаблона**

![ подключение своей учетной записи gitgub](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-12-45.jpg){#fig:010 width=70%}

 **Создание шаблона рабочего пространства**
![ клонирование репозитория](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-13-16.jpg){#fig:011 width=70%}

**Настройка каталога курса**
![ echo os-intro > COURSE](/home/vboxuser/Desktop/labsreports/lab2/report/image/photo_2025-03-08_08-13-24.jpg){#fig:012 width=70%}
Далее отправляю файлы на сервер


# Выводы
Мы приобрели практические навыки работы с сервисом github.



# Контрольные вопросы:

1. Что такое системы контроля версий (VCS) и для решения каких задач они предназначаются?

Системы контроля версий (Version Control System, VCS) применяются при работе нескольких человек над одним проектом. Обычно основное дерево проекта хранится в локальном
или удалённом репозитории, к которому настроен доступ для участников проекта. При
внесении изменений в содержание проекта система контроля версий позволяет их
фиксировать, совмещать изменения, произведённые разными участниками проекта,
производить откат к любой более ранней версии проекта, если это требуется

2. Объясните следующие понятия VCS и их отношения: хранилище, commit, история, рабочая копия.

* хранилище - пространство на накопителе где расположен репозиторий
* commit - сохранение состояния хранилища 
* история - список изменений хранилища (коммитов)
* рабочая копия - локальная копия сетевого репозитория, в которой работает программист. Текущее состояние файлов проекта, основанное на версии, загруженной из хранилища (обычно на последней)

3. Что представляют собой и чем отличаются централизованные и децентрализованные VCS? Приведите примеры VCS каждого вида.

Централизованные системы контроля версий представляют собой приложения типа клиент-сервер, когда репозиторий проекта существует в единственном экземпляре и хранится на сервере. Доступ к нему осуществлялся через специальное клиентское приложение. В качестве примеров таких программных продуктов можно привести CVS, Subversion.

Распределенные системы контроля версий (Distributed Version Control System, DVCS) позволяют хранить репозиторий (его копию) у каждого разработчика, работающего с данной системой. При этом можно выделить центральный репозиторий (условно), в который будут отправляться изменения из локальных и, с ним же эти локальные репозитории будут синхронизироваться. При работе с такой системой, пользователи периодически синхронизируют свои локальные репозитории с центральным и работают непосредственно со своей локальной копией. После внесения достаточного количества изменений в локальную копию они (изменения) отправляются на сервер. При этом сервер, чаще всего, выбирается условно, т.к. в большинстве DVCS нет такого понятия как “выделенный сервер с центральным репозиторием”.

4. Опишите действия с VCS при единоличной работе с хранилищем.

Один пользователь работает над проектом и по мере необходимости делает коммиты, сохраняя определенные этапы.

5. Опишите порядок работы с общим хранилищем VCS.

Несколько пользователей работают каждый над своей частью проекта. При этом каждый должен работать в своей ветки. При завершении работы ветка пользователя сливается с основной веткой проекта. 

6. Каковы основные задачи, решаемые инструментальным средством git?

* Ведение истории версий проекта: журнал (log), метки (tags), ветвления (branches).
* Работа с изменениями: выявление (diff), слияние (patch, merge).
* Обеспечение совместной работы: получение версии с сервера, загрузка обновлений на сервер.

7. Назовите и дайте краткую характеристику командам git.

* git config - установка параметров
* git status - полный список изменений файлов, ожидающих коммита
* git add . - сделать все измененные файлы готовыми для коммита.
* git commit -m "[descriptive message]" - записать изменения с заданным сообщением.
* git branch - список всех локальных веток в текущей директории.
* git checkout [branch-name] - переключиться на указанную ветку и обновить рабочую директорию.
* git merge [branch] — соединить изменения в текущей ветке с изменениями из заданной.
* git push - запушить текущую ветку в удаленную ветку.
* git pull - загрузить историю и изменения удаленной ветки и произвести слияние с текущей веткой.

8. Приведите примеры использования при работе с локальным и удалённым репозиториями.

* git remote add [имя] [url] — добавляет удалённый репозиторий с заданным именем;
* git remote remove [имя] — удаляет удалённый репозиторий с заданным именем;
* git remote rename [старое имя] [новое имя] — переименовывает удалённый репозиторий;
* git remote set-url [имя] [url] — присваивает репозиторию с именем новый адрес;
* git remote show [имя] — показывает информацию о репозитории.

9. Что такое и зачем могут быть нужны ветви (branches)?

Ветвление — это возможность работать над разными версиями проекта: вместо одного списка с упорядоченными коммитами история будет расходиться в определённых точках. Каждая ветвь содержит легковесный указатель HEAD на последний коммит, что позволяет без лишних затрат создать много веток. Ветка по умолчанию называется master, но лучше назвать её в соответствии с разрабатываемой в ней функциональностью.

10. Как и зачем можно игнорировать некоторые файлы при commit?
Зачем: 
* Исключение временных и ненужных файлов (*.log, *.tmp).
* Защита конфиденциальных данных (config.json, .env).
* Исключение средовых файлов (node_modules/, venv/).
* Уменьшение размера репозитория.

Как:

* Создать .gitignore:
touch .gitignore

* Добавить в него правила, например:
*.log
node_modules/
.env

*Закоммитить .gitignore:
git add .gitignore
git commit -m "Добавлен .gitignore"
