---
## Front matter
title: "Отчёт по лабораторной работе №1"
subtitle: "Развертывание виртуальной машины"
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов

# Выполнение лабораторной работы

Устанавливаю Fedora Sway с помощью Oracle VirtualBoxManager. Он был у меня уже до этого установлен, поэтому я просто добавляю новую машину и выбираю скачанный файл Fedora Sway Spin 41 

![Fedora Sway Spin 41](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image.png){#fig:001 width=70%}


Далее я выделяю оптимальное количество памяти и количество CPu 

![Base memory и Processors](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image2.png){#fig:002 width=70%}

Настраиваю образ

![ настройка iso файла](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image3.png){#fig:003 width=70%}

Далее в настройках машины я захожу в Storage  и в conctroller IDE я добавляю iso file 

![ настройка iso файла](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image4.png){#fig:004 width=70%}

делаю так чтобы оптический диск был на первом месте для того чтобы загрузить fedora 

![ настройка boot order](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image5.png){#fig:005 width=70%}

открываю машину и начинаю загрузку, следуя инструкциям на экране

![ установка  Fedora Sway](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image6.png){#fig:006 width=70%}

  Выбираю язык 
![ установка  Fedora Sway](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image7.png){#fig:007 width=70%}

создаю учетную запись
![ создание учетной записи root Fedora Sway](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image8.png){#fig:008 width=70%}

задаю пароль 
![ установка  пароля и имени пользователя](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image9.png){#fig:009 width=70%}

Далее удаляю оптический диск из controller IDE, hard disk ставлю на первое место. Перезапускаю машину. Вхожу в ОС под заданной вами при установке учётной записью.
![ вход в учетную запись](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image10.png){#fig:010 width=70%}

переключаюсь на супер-пользователя. Устанавливаю средства разработки, обновляю все пакеты. Далее устанавливаю tmux для для удобства работы в консоли. Я задаю автоматическое обновление, отключаю SELinux. Настраиваю раскладку клавиатуры 

![ tmux, отключение  SELinux](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image 11.png){#fig:011 width=70%}

Далее перехожу к установке программного обеспечения для создания документации. Сначала устаналиваю pandoc-crossref и обращаю внимание, для какой версии pandoc он скомпилён 
Я перехожу на сайт pandoc-crossref на github.com, нахожу последнюю стабильную версию и скачиваю архив с бинарным файлом
![ gitnub и архивный файла pandoc-crossref](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image12.png){#fig:012 width=70%}
![ установка архивного файла pandoc-crossref](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image13.png){#fig:013 width=70%}

Далее я распаковываю этот файл. Перемещаю исполняемый файл в usr/local/bin.  Даю файлу право на выполнение и проверяю установку
![ распаковка архивного файла pandoc-crossref](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image14.png){#fig:014 width=70%}

Теперь когда я скачала pandoc-crossref, я скачиваю соответсвтвующую версию  pandoc. у меня установлена версия pandoc-crossref, которая скомпилирована с Pandoc v3.6.2, поэтому я должна скачать версию pandoc, которая с ним совместима. Перехожу на страницу релизов pandoc на GitHub. Также скачиваю архив, распаковываю его и перемещаю в usr/local/bin 
![ установка pandoc](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image15.png){#fig:015 width=70%}

Устанавливаю дистрибутив TeXlive
![ установка TeXlive](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image16.png){#fig:016 width=70%}

# Домашнее задание

Я получила следующую информацию:

1. Версия ядра Linux (Linux version).
![ Linux version](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image17.png){#fig:017 width=70%}

2. Частота процессора (Detected Mhz processor).
![ Detected Mhz processor](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image19.png){#fig:019 width=70%}

3. Модель процессора (CPU0). 
![ CPU0](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image18.png){#fig:018 width=70%}

4. Объём доступной оперативной памяти (Memory available).
![ Memory available](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image20.png){#fig:020 width=70%}

5. Тип обнаруженного гипервизора (Hypervisor detected).
![ Hypervisor detected](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image21.png){#fig:021 width=70%}

6. Тип файловой системы корневого раздела.
![ Тип файловой системы корневого раздела.](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image22.png){#fig:022 width=70%}

7. Последовательность монтирования файловых систем.
![ Последовательность монтирования файловых систем](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image23.png){#fig:023 width=70%}


# Выводы
Мы приобрели практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.



# Контрольные вопросы:

1. Какую информацию содержит учётная запись пользователя?

* входное имя пользователя (Login Name);
* пароль (Password);
* внутренний идентификатор пользователя (User ID);
* идентификатор группы (Group ID);
* анкетные данные пользователя (General Information);
* домашний каталог (Home Dir);
* указатель на программную оболочку (Shell).

2. Укажите команды терминала и приведите примеры:

* для получения справки по команде - man;
* для перемещения по файловой системе - cd;
* для просмотра содержимого каталога - ls;
* для определения объёма каталога - ls -l;
* для создания / удаления каталогов / файлов - touch, mkdir, rm, rmdir;
* для задания определённых прав на файл / каталог - chmod;
* для просмотра истории команд - history.

3. Что такое файловая система? Приведите примеры с краткой характеристикой.

Файловая система (англ. file system) — порядок, определяющий способ организации, хранения и именования данных на носителях информации в компьютерах, а также в другом электронном оборудовании.

FAT. Числа в FAT12, FAT16 и FAT32 обозначают количество бит, используемых для перечисления блока файловой системы. FAT32 является фактическим стандартом и устанавливается на большинстве видов сменных носителей по умолчанию. Одной из особенностей этой версии ФС является возможность применения не только на современных моделях компьютеров, но и в устаревших устройствах и консолях, снабженных разъемом USB.
Пространство FAT32 логически разделено на три сопредельные области: зарезервированный сектор для служебных структур; табличная форма указателей; непосредственная зона записи содержимого файлов. 

Стандарт NTFS разработан с целью устранения недостатков, присущих более ранним версиям ФС. Впервые он был реализован в Windows NT в 1995 году, и в настоящее время является основной файловой системой для Windows. Система NTFS расширила допустимый предел размера файлов до шестнадцати гигабайт, поддерживает разделы диска до 16 Эб (эксабайт, 1018 байт). Использование системы шифрования Encryption File System (метод «прозрачного шифрования») осуществляет разграничение доступа к данным для различных пользователей, предотвращает несанкционированный доступ к содержимому файла. Файловая система позволяет использовать расширенные имена файлов, включая поддержку многоязычности в стандарте юникода UTF, в том числе в формате кириллицы. Встроенное приложение проверки жесткого диска или внешнего накопителя на ошибки файловой системы chkdsk повышает надежность работы харда, но отрицательно влияет на производительность.

Ext2, Ext3, Ext4 или Extended Filesystem– стандартная файловая система, первоначально разработанная еще для Minix. Содержит максимальное количество функций и является наиболее стабильной в связи с редкими изменениями кодовой базы. Начиная с ext3 в системе используется функция журналирования. Сегодня версия ext4 присутствует во всех дистрибутивах Linux. 

XFS рассчитана на файлы большого размера, поддерживает диски до 2 терабайт. Преимуществом системы является высокая скорость работы с большими файлами, отложенное выделение места, увеличение разделов на лету, незначительный размер служебной информации. К недостаткам относится невозможность уменьшения размера, сложность восстановления данных и риск потери файлов при аварийном отключении питания.

4. Как посмотреть, какие файловые системы подмонтированы в ОС?

командой du.

5. Как удалить зависший процесс?

командой kill.
