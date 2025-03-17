#programming 

# Вход

``` 
source ~/miniforge3/etc/profile.d/conda.sh
conda activate sage
```

# Дроби

```
sage: 1/3 + 1/6
1/2
sage: (2/5 + 3/7).n()  # Численный ответ
0.685714285714286
```

# Переменные и выражения

```
sage: x, y = var('x y')  # Объявляем x и y
sage: expr = x^2 + 3*x + 2
sage: expr
x^2 + 3*x + 2
```

# Символьная алгебра

- Разложение на множители:
```
sage: factor(x^2 + 3*x + 2)
(x + 1) * (x + 2)
```

- Раскрытие скобок:
```
sage: expand((x + 1) * (x + 2))
x^2 + 3*x + 2
```

- Подстановка значений:
```
sage: expr.subs(x=2)
12
```

# Дифференцирование и интегрирование

- Производная:
```
sage: diff(sin(x) * cos(x), x)
cos(x)^2 - sin(x)^2
```

- Интеграл:
```
sage: integrate(sin(x) + cos(x), x)
-cos(x) + sin(x)
```

- Численное интегрирование:
```
sage: numerical_integral(sin(x), 0, pi)
(2.0, 2.220446049250313e-14)
```

# Решение уравнений

- Решим уравнение $x^{2} - 4 = 0$:
```
sage: solve(x^2 - 4 == 0, x)
[x == -2, x == 2]
```

- Системы уравнений:
```
sage: solve([x + y == 3, x - y == 1], x, y)
[[x == 2, y == 1]]
```

# Работа с матрицами

- Создание матрицы:
```
sage: A = Matrix([[1, 2], [3, 4]])
sage: A
[1 2]
[3 4]
```

- Определитель:
```
sage: A.det()
-2
```

- Обратная матрица:
```
sage: A.inverse()
[-2   1]
[3/2 -1/2]
```

# Построение графиков

- График функции:
```
sage: plot(sin(x), (x, -pi, pi))
```

- График нескольких функций:
```
sage: plot([sin(x), cos(x)], (x, -pi, pi))
```

- 3D-график:
```
sage: plot3d(x^2 + y^2, (x, -2, 2), (y, -2, 2))
```

# Использование LaTeX

- Sage умеет красиво выводить формулы в LaTeX:
```
sage: latex(integrate(x^2, x))
'x^{3}/3'
```

- Если в Jupyter, используй `show()`:
```
sage: show(integrate(x^2, x))
```










