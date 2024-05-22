import numpy as np
import matplotlib.pyplot as plt
# Задана функція
def f(x):
    return np.exp(-x) + x**2
# Значення xi та yi
xi = np.array([0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1])
yi = f(xi)
# Знайдені коефіцієнти для прямої та параболи
m = 0.3637
c = 0.5782
a = 22.1006
b = -8.579
c_parabola = 4.64485
# Генеруємо значення для прямої та параболи
x_values = np.linspace(0, 1, 100)
y_linear = m * x_values + c
y_parabola = a * x_values**2 + b * x_values + c_parabola
# Побудова графіка
plt.figure(figsize=(10, 6))
plt.scatter(xi, yi, label='Точки (xi, yi)', color='red')
plt.plot(x_values, y_linear, label='Наближена пряма', color='blue')
plt.plot(x_values, y_parabola, label='Наближена парабола', color='green')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Побудова наближень прямою та параболою')
plt.legend()
plt.grid(True)
plt.show()


# -
