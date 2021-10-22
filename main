import matplotlib.pyplot as plt
import numpy

n_1 = 2
n_2 = 4
n_3 = 5
y_0 = 0
x_0 = 0


def func(x):
    return x / (x + 1)


def Euler(steps, mark="o"):
    h = 1 / steps
    print(h)
    y = numpy.zeros(steps + 1)
    x = numpy.zeros(steps + 1)
    x[0] = x_0
    y[0] = y_0
    for i in range(steps):
        x[i + 1] = x[i] + h
        y[i + 1] = y[i] + h * f_x_y(x[i], y[i])
        print(f"{i} шаг f(x,y) {f_x_y(x[i], y[i])}")
    for i in range(steps+1):
        print("X {:.4f}  y {:.4f}".format(x[i], y[i]))
    plt.plot(x, y)
    plt.scatter(x, y, label=f"h = {h}", marker=mark)


def f_x_y(x, y):
    return (-1 / (x + 1)) * y + (1 / (x + 1))


iter = numpy.linspace(0, 1, 11)

print("Аналитическое решение")

for i in range(11):
    print("X {:.4f}  y {:.4f}".format(iter[i], func(iter[i])))

plt.plot(iter, func(iter), label="Аналитическое решение")
print("Разбиение на 2 отрезка")
Euler(n_1)

print("Разбиение на 4 отрезка")
Euler(n_2, "*")

print("Разбиение на 5 отрезков")
Euler(n_3, "s")
plt.legend()
plt.grid()
plt.show()
