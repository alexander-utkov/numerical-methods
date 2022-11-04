# 1 Введение

Настоящий документ специфицирует требования к разработке программного изделия по
теме «решение численными методами».

Программное изделие «Numerical Methods» специализируется на решении интерполяции
методом Лагранжа. Основное применение заключается в нахождении интерполирующей
функции, а вторичное - в просмотре пошагового решения, графика интерполирующей
функции, а также в вычислении значений интерполирующей функции. Применение
программного изделия имеет следующие выгоды:

- быстрое нахождение интерполирующей функции;
- вычисления без ошибок с пошаговым решением.

> Вычисления в массе хоть и содержат математику седьмого класса, но, допуская по
> невнимательности ошибки, на решение одной задачи я потратил более шести часов.
> Однако, данную задачу я решил за 30 минут программирования... Поэтому да, это
> полезная программа.

## 1.1 Определения

1.1.1 Абсцисса: значение точки (x) на оси абсцисс (OX).
1.1.1 Ордината: значение точки (y) на оси ординат (OY).

## 1.2 Краткий обзор

Настоящий документ построен в свободном стиле. Второй раздел в общем определяет
функции программного изделия. Третий раздел специфицирует данные функции или же
общие функциональные требования к программному изделию.

# 2 Функции изделия

## 2.1 Определить функцию

Настоящая функция предоставляет возможность определить функцию таблицей значений
абсцисс и ординат.

> TODO: Значения ординат можно задать исходной функцией.

## 2.2 Интерполировать

Настоящая функция предоставляет интерполяционную функцию для заданной. При этом,
по запросу пользователя, предоставляется пошаговое решение ее нахождения.

## 2.3 Построить график

Настоящая функция предоставляет возможность построить график в заданной области
определения с заданным шагом между точками.

# 3 Функциональные требования

## 3.1 Отображение формул

Система должна использовать LaTeX для отображения формул и вычислений.

## 3.2 Отображение графиков

> TODO: Построить график исходной функции, если ею определялись ординаты.

### 3.2.1 Область определения

Область определения по умолчанию должна соответствовать крайним абсциссам с
удалением от графика на единицу ($`[a-1; b+1]`$).

### 3.2.2 Шаг

Шаг между точками по умолчанию должен быть $`\\frac{b-a}{100}`$, где `a` и `b` -
область определения. Говоря иначе, шаг должен быть таким, чтобы в построении
графика участвовало столько точек, сколько объявленное в деноминаторе дроби.

# 4 Приложение А

Настоящее приложение содержит теоретическую базу программного продукта.

Формула Лагранжа:

```math
P_n(x)\\approx\\sum_{i=0}^{n}{\\frac{y_i\\varphi(x)}{{\\varphi}'(x_i)(x-x_i)}}
```

Формула вспомогательной функции $`\\varphi(x)`$:

```math
\\varphi(x)=(x-x_0)(x-x_1)*...*(x-x_n)
```