#programming
# matplotlib in python

```python
import matplotlib.pyplot as plt
import numpy as np

# Создаем данные
x = np.linspace(0, 10, 100)  # 100 точек от 0 до 10
y = np.sin(x)  # Значения функции синуса

# Создаем график
plt.figure(figsize=(10, 5))  # Размер графика
plt.plot(x, y, label='sin(x)', color='blue')  # Линия графика
plt.title('График функции синуса')  # Заголовок графика
plt.xlabel('x')  # Подпись оси x
plt.ylabel('sin(x)')  # Подпись оси y
plt.axhline(0, color='black', linewidth=0.5, ls='--')  # Горизонтальная линия на уровне 0
plt.axvline(0, color='black', linewidth=0.5, ls='--')  # Вертикальная линия на уровне 0
plt.grid()  # Сетка
plt.legend()  # Легенда

# Сохраняем график в файл
plt.savefig('graph.png', dpi=300)  # Сохранение с разрешением 300 dpi

# Показать график
# plt.show()  # Показать график
```

# SymPy

```python
from sympy import symbols, diff, integrate, solve, Eq, simplify

# Определяем символы
x = symbols('x')

# Определяем выражение
expr = x**2 + 2*x + 1

# Упрощаем выражение
simplified_expr = simplify(expr)

# Находим производную
derivative = diff(expr, x)

# Находим интеграл
integral = integrate(expr, x)

# Решаем уравнение
equation = Eq(expr, 0)
solutions = solve(equation, x)

print("Упрощенное выражение:", simplified_expr)
print("Производная:", derivative)
print("Интеграл:", integral)
print("Решения уравнения:", solutions)
```


# SageMath
``` 
source ~/miniforge3/etc/profile.d/conda.sh
conda activate sage

```