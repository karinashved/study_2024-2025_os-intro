---
## Front matter
lang: ru-RU
title: Установка ОС на виртуальную машину
author: |
	 Швед Карина\inst{1}

institute: |
	\inst{1}Российский Университет Дружбы Народов

date: 7 марта, 2025, Москва, Россия

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

## Цель лабораторной работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов

# Процесс выполнения лабораторной работы

## Создаю виртуальную машину

Устанавливаю Fedora Sway с помощью Oracle VirtualBoxManager. Он был у меня уже до этого установлен, поэтому я просто добавляю новую машину и выбираю скачанный файл Fedora Sway Spin 41 

![Fedora Sway Spin 41](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image.png){#fig:001 width=70%}

## Далее я выделяю оптимальное количество памяти и количество CPu  

![Base memory и Processors](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image2.png){#fig:002 width=70%}

## Настраиваю образ

![ настройка iso файла](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image3.png){#fig:003 width=70%}

## Далее в настройках машины я захожу в Storage  и в conctroller IDE я добавляю iso file 

![ настройка iso файла](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image4.png){#fig:004 width=70%}

## делаю так чтобы оптический диск был на первом месте для того чтобы загрузить fedora 

![ настройка boot order](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image5.png){#fig:005 width=70%}

## открываю машину и начинаю загрузку, следуя инструкциям на экране


![ установка  Fedora Sway](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image6.png){#fig:006 width=70%}

## Установка языка

![ установка  Fedora Sway](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image7.png){#fig:007 width=70%}

## Создание учетной записи

![ создание учетной записи root Fedora Sway](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image8.png){#fig:008 width=70%}

## Создание пароля

![ установка  пароля и имени пользователя](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image9.png){#fig:009 width=70%}

## Далее удаляю оптический диск из controller IDE, hard disk ставлю на первое место. Перезапускаю машину. Вхожу в ОС под заданной вами при установке учётной записью.

![ вход в учетную запись](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image10.png){#fig:010 width=70%}

## Устанавливаю средства разработки, обновляю все пакеты.

![ tmux, отключение  SELinux](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image 11.png){#fig:011 width=70%}

## Установка программного обеспечения для создания документации

![ установка pandoc](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image15.png){#fig:015 width=70%}

## Устанавливаю дистрибутив TeXlive

![ установка TeXlive](/home/vboxuser/Desktop/labsreports/lab1/report/image/Pasted image16.png){#fig:016 width=70%}

## Рабочая система

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


# Выводы по проделанной работе

## Вывод

Мы приобрели практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.
