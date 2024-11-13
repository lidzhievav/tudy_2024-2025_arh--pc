---
## Front matter
title: "Отчет по лабораторной работе №4"
subtitle: "Язык ассемблера NASM"
author: "Лиджиева В.Д."

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

Освоение процедуры компиляции и сборки программ,написанных на ассемблере NASM.

# Задание
 ПрограммаHelloworld!
 создать каталог для работы с программами на языке ассемблера NASM 1.2 перейти в созданный каталог
 создать текстовый файл с именем hello.asm
 открыть этот файл
 ввести в него указанный текст
 ТрансляторNasm
 выполнить комппиляцию в объектный код
 Расширенный синтаксис
 выполнить компиляцию исходного файла
 КомпановщикLD
 передать объектный файл на обработку компановщику
 Запустить исполняемый файл
 Задания для самостоятельнойработы
 создать копию файла hello.asm с именем lab4.asm
изменить скопированный файл, чтобы выводилась строка с именем и фамилией


# Теоретическое введение


Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

1. Создайте каталог для работы с программами на языке ассемблера NASM:

![Создание каталога](image/11.jpg){#fig:001 width=70%}

2. Перейдём в созданный каталог:

![Переход в каталог](image/12.jpg){#fig:002 width=70%}

3. Создадим текстовый файл с именем hello.asm и откроем этот файл с помощью текстового редактора:

![Создание текстового файла и открытие файла](image/13.jpg){#fig:003 width=70%}

4. Введём в него текст:

![Ввод текста](image/15.jpg){#fig:004 width=70%}

5. Скомпилируем данный текст и проверим, что объектный файл был создан:

![Компиляция текста и проверка, что объектный файл был создан](image/16.jpg){#fig:005 width=70%}

6. Скомпилируем исходный файл hello.asm в obj.o и создадим файл листинга

list.lst и проверим, что файлы были созданы.

![Создание файлов и проверка, что файлы были созданы.](image/17.jpg){#fig:006 width=70%}

7. Передадим объектный файл на обработку компоновщику и проверим, что исполняемый файл hello был создан.

![Передача файла на компоновку и проверка, что исполняемый файл hello был создан](image/18.jpg){#fig:007 width=70%}

8. Зададим имя создаваемого исполняемого файла,запустим на выполнение созданный исполняемый файл, находящийся в

текущем каталоге.

![Зададим имя создаваемого исполняемого файла и запуск на выполнение ](image/19.jpg){#fig:008 width=70%}

9. Создадим копию файла hello.asm с именем lab4.asm

![Создание копии файла с именем lab4.asm](image/20.jpg){#fig:009 width=70%}

10. Внесём изменения в текст программы в файле lab5.asm

![Внесение изменения в текст программы](image/21.jpg){#fig:010 width=70%}

11. Оттранслируем полученный текст программы lab5.asm в объектный файл.

Выполним компоновку объектного файла и запустим получившийся исполняемый файл.

![Оттранслирование, компоновка, запуск](image/22.jpg){#fig:011 width=70%}

12. Скопировала файлы hello.asm и lab4.asm в локальный репозиторий в каталог ~/work/study/2023-2024/“Архитектура 

компьютера”/arch-pc/labs/lab04/ спомощью утилиты ср и проверил наличие файлов с помощью утилиты ls

![Копирование файлов в локальный репозиторий](image/23.jpg){#fig:012 width=70%}

13. Загружаю файлы на Github

![Загрузка файлов на гитхаб](image/24.jpg){#fig:013 width=70%}

# Выводы

В ходе выполнения работы, я освоила процедуры компиляции и сборки про-
грамм, написанных на ассемблере NASM.

# Список литературы{.unnumbered}

::: {#refs}
:::
