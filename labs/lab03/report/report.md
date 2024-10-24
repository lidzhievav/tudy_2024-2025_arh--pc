---
## Front matter
title: "Лабораторная работа 3"
subtitle: "Язык разметки Markdown"
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
1.Цель работы 
2.Задание 
3.Теоретическое введение 
4.Выполнение лабораторной работы 
5.Вывод
6.Список литературы 

# Цель работы
Ознакомиться с работой языка разметки Markdown, выполнить задания в соответствии с лабораторной работой, а также составить отчет о выполненной работе


# Задание
1.Ознакомиться с базовыми сведениями о Markdown
2.Перейти в каталог “arch-pc” выполнить команду git pull
3.Выполнить команду make для компиляция шаблона
4.Удалите полученный файлы с использованием Makefile
5.Откройте файл report.md c помощью любого текстового редактора
6.Заполните отчет и скомпилируйте отчет с использованием Makefile.
7.Загрузить файлы на Github
8.Выполнить задание для самостоятельной работы


# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

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

1. Выполнение git pull (См Рис 1) 

![git pull](image/photo1.png){width=70%}


2. Выполнение make (Рис 2)

![make](image/photo2.png){width=70%}

3. Удаление файлов (Рис 3)

![make clean](image/photo3.png){width=70%}

4. Открыть файл report.md (Рис 4)

![report.md](image/photo4.png){width=70%}

5. Заполнить и скомпилировать отчет (См Рис 5)

![](image/photo5.png){width=70%}

6. Загрузить файлы на гитхаб (См Рис 6)

![](image/photo6.png){width=70%}


# Выводы

В процессе выполнения работы,я ознакомилась с языком разметки Markdown.




# Список литературы{.unnumbered}
1.GDB: The GNU Project Debugger. — URL: https://www.gnu.org/software/gdb/.

2.GNU Bash Manual. — 2016. — URL: https://www.gnu.org/software/bash/manual/.

3.Midnight Commander Development Center. — 2021. — URL: https://midnight-commander.org/.

4.NASM Assembly Language Tutorials. — 2021. — URL: https://asmtutor.com/.

5.Newham C. Learning the bash Shell: Unix Shell Programming. — O’Reilly Media, 2005. —
354 с. — (In a Nutshell). — ISBN 0596009658. — URL: http://www.amazon.com/Learning-
bash-Shell-Programming-Nutshell/dp/0596009658.

6.Robbins A. Bash Pocket Reference. — O’Reilly Media, 2016. — 156 с. — ISBN 978-1491941591.

7.The NASM documentation. — 2021. — URL: https://www.nasm.us/docs.php.

8.Zarrelli G. Mastering Bash. — Packt Publishing, 2017. — 502 с. — ISBN 9781784396879.

9.Колдаев В. Д., Лупин С. А. Архитектура ЭВМ. — М. : Форум, 2018.

10.Куляс О. Л., Никитин К. А. Курс программирования на ASSEMBLER. — М. : Солон-Пресс,
2017.

11.Новожилов О. П. Архитектура ЭВМ и систем. — М. : Юрайт, 2016.

12.Расширенный ассемблер: NASM. — 2021. — URL: https://www.opennet.ru/docs/RUS/nasm/.

13.Робачевский А., Немнюгин С., Стесик О. Операционная система UNIX. — 2-е изд. — БХВ-
Петербург, 2010. — 656 с. — ISBN 978-5-94157-538-1.

14.Столяров А. Программирование на языке ассемблера NASM для ОС Unix. — 2-е изд. —
М. : МАКС Пресс, 2011. — URL: http://www.stolyarov.info/books/asm_unix.

15.Таненбаум Э. Архитектура компьютера. — 6-е изд. — СПб. : Питер, 2013. — 874 с. —
(Классика Computer Science).

16.Таненбаум Э., Бос Х. Современные операционные системы. — 4-е изд. — СПб. : Питер,
2015.-- 1120 с. — (Классика Computer Science).

::: {#refs}
:::
