# Примеры кода
#programming

```
v = [1, 2, 3]; % Вектор-строка
m = [1, 2; 3, 4]; % Матрица 2x2
```

---

```
function y = square(x)
    y = x^2;
end
```

---

```
if a > b
    disp('a больше b');
else
    disp('a не больше b');
end

for i = 1:10
    disp(i);
end
```

---

```
x = 0:0.1:10; % Вектор от 0 до 10 с шагом 0.1
y = sin(x);
plot(x, y); % Построение графика
xlabel('x');
ylabel('sin(x)');
title('График синуса');
```

---

```
pkg install -forge package_name
```
