---
## Front matter
title: "Лабораторнаят работа №1"
subtitle: "Основы информационной безопасности"
author: "Оширова Юлия Николаевна"

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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Установить дистрибутив Rocky. Выполнить домашнее задание. Сделать отчет и презентацию по данной лабораторной работе.

# Теоретическое введение

Rocky Linux — это дистрибутив Linux, разработанный Rocky Enterprise Software Foundation. Предполагается, что это будет полный бинарно-совместимый выпуск, использующий исходный код операционной системы Red Hat Enterprise Linux. 

# Выполнение лабораторной работы

***Подготовка виртуальный машины***

Создадим виртуальную машину:

![Подготовка виртуальный машины](image/1.jpg){#fig:001 width=70%}

Добавим в нее раздел на 20 ГБ памяти, а также подключим iso образ инсталятора Rocky Linux, а также установим виртуальный жесткий диск и т.д.:

![Подготовка виртуальный машины](image/2.jpg){#fig:002 width=70%}

![Подготовка виртуальный машины](image/3.jpg){#fig:003 width=70%}

![Подготовка виртуальный машины](image/4.jpg){#fig:004 width=70%}

Запустим и перейдем к установке.

***Установка Rocky Linux***

Выбираем язык English и язык English (United States):

![Выбор языка](image/5.jpg){#fig:005 width=70%}

Выбираем автоматическую разметку диска:

![Разметка диска](image/6.jpg){#fig:006 width=70%}

Добавляем нового пользователя, учитывая соглашение об именовании.

В предустанавливаемом ПО выбираем базовое окружение “Сервер с GUI” и группу “Developments tool”:

![Выбираем базовое окружение и группу](image/8.jpg){#fig:008 width=70%}

Отключаем kdump:

![Отключаем](image/7.jpg){#fig:007 width=70%}

Проверяем installation destination:

![Installation destination](image/7.jpg){#fig:007 width=70%}

Выставляем пароль для рута:

![Создаем пароль](image/11.jpg){#fig:011 width=70%}

Задаем hostname:

![Задаем](image/10.jpg){#fig:010 width=70%}

![Создаем пользователя](image/12.jpg){#fig:012 width=70%}

Принимаем лицензию:

![Лицензия](image/13.jpg){#fig:013 width=70%}

Запускаем установку:

![Установка завершилась](image/14.jpg){#fig:014 width=70%}

Проверяем правильность установленного hostname и username (согласно соглашению об именовании).

Подключаем образ диска дополнений гостевой ОС:

![Подготовка виртуальный машины](image/15.jpg){#fig:015 width=70%}

![Подготовка виртуальный машины](image/18.jpg){#fig:018 width=70%}

***Домашнее задание***

Команда dmesg:

![Команда dmesg](image/16.jpg){#fig:016 width=70%}

Версия ядра:

![Версия ядра](image/17.jpg){#fig:017 width=70%}

Частота процессора модель процессора и объем памяти:

![Частота процессора, модель процессора и объем памяти](image/19.jpg){#fig:019 width=70%}

Гипервизор:

![Гипервизор](image/20.jpg){#fig:020 width=70%}

Тип FS и последовательность монтирования:

![Тип FS](image/21.jpg){#fig:021 width=70%}

# Выводы

В ходе данной лабораторной работы мы ознакомились и установили новый дистрибутив Rocky. Выполнили домашнее задание с командой «dmesg».

# Контрольные вопросы

1. Учётная запись, как правило, содержит сведения, необходимые для опознания пользователя при подключении к системе, сведения для авторизации и учёта. Это идентификатор пользователя (login) и его пароль. Пароль или его аналог, как правило, хранится в зашифрованном или хэшированном виде для обеспечения его безопасности.

2. manual (man) — для получения полной справочной информации по другой команде.

Для перемещения и переименования файлов и каталогов используется команда mv (move).

Для просмотра содержимого каталога используется команда ls.

Для просмотра размеров папок на диске используется команда du.

Touch — создать файл.

Для удаления директорий используется команда rmdir имя_директории.

Команда rm применяется для удаления ненужных файлов.

Команда chmod (change mode – сменить режим) предназначена для изменения прав доступа к файлам.

Достаточно выполнить команду history, для просмотра истории команд.

3. Файловая система — это структура, используемая операционной системой для организации и управления файлами на устройстве хранения, например на жестком диске, твердотельном накопителе (SSD) или USB-накопителе.

4. Команда findmnt — это простая утилита командной строки, используемая для отображения списка смонтированных файловых систем или поиска файловой системы в /etc/fstab, /etc/mtab и /proc/self/mountinfo.

5. Один из способов «убить», запущенное приложение или процесс в Linux, это использование таких команд, как kill или killall.

# Список литературы

[Что такое Роки?](https://ru.wikipedia.org/wiki/Rocky_Linux)
