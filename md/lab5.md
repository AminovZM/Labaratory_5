---
# Front matter
lang: ru-RU
title: "ОТЧЕТ ПО ЛАБОРАТОРНОЙ РАБОТЕ №5"
subtitle: "Подгонка полиномиальной кривой"
author: "Аминов Зулфикор Мирзокаримович"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Ход работы:

В матрице заданы значения 𝑥 в столбце 1 и значения 𝑦 в столбце 2.
Введём матрицу данных в Octave и извлечём вектора 𝑥 и 𝑦.

![рисунка 1](img/1/1.PNG){ #fig:001 width=70% }
![рисунка 2](img/1/2.PNG){ #fig:001 width=70% }

Нарисуем точки на графике.

![рисунка 3](img/1/3.PNG){ #fig:001 width=70% }
![рисунка 4](img/1/4.PNG){ #fig:001 width=70% }

Построим уравнение вида 𝑦 = 𝑎𝑥2 + 𝑏𝑥 + 𝑐.

![рисунка 5](img/1/5.PNG){ #fig:001 width=70% }
![рисунка 6](img/1/6.PNG){ #fig:001 width=70% }

Решение по методу наименьших квадратов получается из решения уравнения 𝐴^𝑇𝐴𝑏 = 𝐴^𝑇𝑦, где 𝑏 – вектор коэффициентов полинома Используем Octave для построения уравнений.

![рисунка 7](img/1/7.PNG){ #fig:001 width=70% }

Решим задачу методом Гаусса. Запишем расширенную матрицу:

![рисунка 8](img/1/8.PNG){ #fig:001 width=70% }

Таким образом, искомое квадратное уравнение имеет вид:

𝑦 = −0.89286𝑥^2 + 5.65𝑥 − 4.4.

Построим соответствующий график параболы

![рисунка 9](img/1/9.PNG){ #fig:001 width=70% }
![рисунка 10](img/1/10.PNG){ #fig:001 width=70% }
![рисунка 11](img/1/11.PNG){ #fig:001 width=70% }
![рисунка 12](img/1/12.PNG){ #fig:001 width=70% }

Получим подгоночный полином.

![рисунка 13](img/1/13.PNG){ #fig:001 width=70% }
![рисунка 14](img/1/14.PNG){ #fig:001 width=70% }

Построим исходные и подгоночные данные.

![рисунка 15](img/1/15.PNG){ #fig:001 width=70% }
![рисунка 16](img/1/16.PNG){ #fig:001 width=70% }
![рисунка 17](img/1/17.PNG){ #fig:001 width=70% }
![рисунка 18](img/1/18.PNG){ #fig:001 width=70% }

# Матричные преобразования

Введём матрицу данных.

![рисунка 19](img/2/1.PNG){ #fig:001 width=70% }

Извлечём вектора 𝑥 и 𝑦 и нарисуем этот граф.

![рисунка 20](img/2/2.PNG){ #fig:001 width=70% }
![рисунка 21](img/2/3.PNG){ #fig:001 width=70% }

# Вращение

Чтобы произвести повороты матрицы данных 𝐷, нам нужно вычислить произведение матриц 𝑅𝐷.

Повернём граф дома на 90∘ и 225∘. Вначале переведём угол в радианы.

![рисунка 22](img/3/1.PNG){ #fig:001 width=70% }
![рисунка 23](img/3/2.PNG){ #fig:001 width=70% }
![рисунка 24](img/3/3.PNG){ #fig:001 width=70% }
![рисунка 25](img/3/4.PNG){ #fig:001 width=70% }
![рисунка 26](img/3/5.PNG){ #fig:001 width=70% }
![рисунка 27](img/3/6.PNG){ #fig:001 width=70% }
![рисунка 28](img/3/7.PNG){ #fig:001 width=70% }
![рисунка 29](img/3/8.PNG){ #fig:001 width=70% }

# Отражение

Отразим граф дома относительно прямой 𝑦 = 𝑥. Зададим матрицу отражения (поясните, почему она такая).

![рисунка 30](img/4/1.PNG){ #fig:001 width=70% }
![рисунка 31](img/4/2.PNG){ #fig:001 width=70% }
![рисунка 32](img/4/3.PNG){ #fig:001 width=70% }
![рисунка 33](img/4/4.PNG){ #fig:001 width=70% }

# Дилатация

Увеличим граф дома в 2 раза.

![рисунка 34](img/5/1.PNG){ #fig:001 width=70% }
![рисунка 35](img/5/2.PNG){ #fig:001 width=70% }
![рисунка 36](img/5/3.PNG){ #fig:001 width=70% }
![рисунка 37](img/5/4.PNG){ #fig:001 width=70% }

# Вывод

В octave научился работать с подгонки полиномиальной кривой, с матричным преобразованием, вращений, отражений и дилатацией.
