#aalto 

### Производная параметрически заданной функции:
$$
r'( t) =x'( t) i+y'( t) j+z'( t) k
$$


<br><br>

### Формула длины дуги
- Обычной функции
$$
L = \int_{a}^{b} \sqrt{ 1+\left( \frac{dy}{dx} \right)^{2} }dx
$$
- Парметризованной функции
$$
\ell (C) = \int_{a}^{b} ||r'(t)|| dt
$$

#### Пример
$$
\begin{gather*}
r(t) = (r \cos t,r \sin t) \text{ - круг с радиусом } r\\ 
r'(t) = (-r \sin t, r \cos t) \hspace{10mm} ||r'(t)|| =  \sqrt{ r^{2}( \sin ^{2}t + \cos ^{2}t )} = r\\
\int_{0}^{2 \pi} r\ dt= 2 \pi r
\end{gather*}
$$

<br><br>

### Метод полярных координат для пределов функций нескольких переменных:
$$
\begin{gather*}
\lim _{( x,\ y) \to ( 0,\ 0)} f( x,\ y)\\
x\ =\ r\cos( \theta ) ,\ \ \ \ \ y=r\sin( \theta )\\
\lim _{( x,\ y) \to ( 0,\ 0)} f( x,\ y) =\lim _{r\to 0} f( r\cos( \theta ) ,\ r\sin( \theta ))\\
\end{gather*}
$$
- Проверяем зависимость от $\theta$. Если зависимости нет, то предел существует.  
- Если предел не стремится к точке $(0, 0)$, то делаем сдвиг.  
- Также можно просто подставить несколько траекторий и сравнить результаты. Если результаты одинаковые, значит предел существует.

<br><br>

### Производная сложной функции (Цепное правило для функции двух переменных):
$$
\begin{gather*}
z=z( x,\ y) =z( x( t) ,\ y( t))\\ \\
x=x( t) , \hspace{10mm} y=y( t)\\ \\
\frac{\partial z}{\partial t} =\frac{\partial z}{\partial x}\frac{\partial x}{\partial t} +\frac{\partial z}{\partial y}\frac{\partial y}{\partial t}
\end{gather*}
$$

<br><br>

### Матрица Якоби:
$$
\begin{gather*}
J_{F} =\begin{bmatrix}
\frac{\partial f_{1}}{\partial x_{1}} & \frac{\partial f_{1}}{\partial x_{2}} & \cdots  & \frac{\partial f_{1}}{\partial x_{n}}\\
\frac{\partial f_{2}}{\partial x_{1}} & \frac{\partial f_{2}}{\partial x_{2}} & \cdots  & \frac{\partial f_{2}}{\partial x_{n}}\\
\vdots  & \vdots  & \ddots  & \vdots \\
\frac{\partial f_{m}}{\partial x_{1}} & \frac{\partial f_{m}}{\partial x_{2}} & \cdots  & \frac{\partial f_{m}}{\partial x_{n}}
\end{bmatrix}
\end{gather*}
$$
**Якобиан** - $\det Df( x)$
Цепное правило в многомерном случае (матрицы Якоби):
$$
D( f\circ g)( x) =Df( g( x)) \ Dg( x)
$$
##### Пример:
$$
\begin{gather*}
F( u,\ v) =\begin{bmatrix}
f_{1} =u^{2} +v^{2}\\
f_{2} =uv
\end{bmatrix} ,\hspace{10mm} u=x^{2} -y,  \hspace{10mm}   v=x+y^{2}\\
\\
J_{F} =\begin{bmatrix}
2u & 2v\\
v & u
\end{bmatrix} \hspace{10mm}  J_{G} =\begin{bmatrix}
2x & -1\\
1 & 2y
\end{bmatrix}\\
\\
J_{H} =J_{F} \ *\ J_{G} =\begin{bmatrix}
2u & 2v\\
v & u
\end{bmatrix} *\begin{bmatrix}
2x & -1\\
1 & 2y
\end{bmatrix}\\
\end{gather*}
$$

<br><br>

### Градиент:

Вектор, своим направлением указывающий направление наискорейшего роста некоторой скалярной величины:
$$
\triangledown f=grad\ f=\left(\frac{\partial f}{\partial x_{1}} ,\ \frac{\partial f}{\partial x_{2}} ,\ ...\ ,\ \frac{\partial f}{\partial x_{N}}\right)
$$
Допустим $\vec{e} =(\cos \theta ,\ \sin \theta )$. Чтобы найти производную в точке $(a, b)$ с направлением $\vec{e}$ (единичный вектор), где $\theta$ — это угол направления, нужно вычислить скалярное произведение градиента и единичного вектора направления:
$$
D_{e} f=\langle \triangledown f,\ e\rangle =\frac{\partial f}{\partial x}\cos \theta +\frac{\partial f}{\partial y}\sin \theta 
$$

<br><br>

### Формула касательной к функции в точке $a$:
$$
L( x) =f( a) +f'( a)( x-a)
$$
### Формула касательной плоскости:
$$
L( x,\ y) =f( a,\ b) +f_{1}( a,\ b)( x-a) +f_{2}( a,\ b)( y-b)
$$
### Нормаль к поверхности
Нормаль — это вектор, перпендикулярный касательной плоскости в точке $(x_{0}, y_{0}, z_{0})$.
$$
n=\left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, -1 \right)
$$

<br><br>

### Ряд Тейлора:
$$
\sum _{n=0}^{\infty }\frac{f^{( n)}( a)}{n!}( x-a)^{n}
$$
- $a$ — вещественное или комплексное число, 
- $f^{(n)}(a)$ — $n$-я производная функции $f$, вычисляемая в точке $a$.

<br><br>

### Матрица Гессе:
$$
\begin{gather*}
H_{f}\left( x\right) =\begin{bmatrix}
\frac{\partial ^{2}}{\partial x_{1}^{2}} f\left( x\right) & \frac{\partial ^{2}}{\partial x_{2} \partial x_{1}} f\left( x\right) & \cdots  & \frac{\partial ^{2}}{\partial x_{n} \partial x_{1}} f\left( x\right)\\
\frac{\partial ^{2}}{\partial x_{1} \partial x_{2}} f\left( x\right) & \frac{\partial ^{2}}{\partial x_{2}^{2}} f\left( x\right) & \cdots  & \frac{\partial ^{2}}{\partial x_{n} \partial x_{2}} f\left( x\right)\\
\vdots  & \vdots  & \ddots  & \vdots \\
\frac{\partial ^{2}}{\partial x_{1} \partial x_{n}} f\left( x\right) & \frac{\partial ^{2}}{\partial x_{2} \partial x_{n}} f\left( x\right) & \cdots  & \frac{\partial ^{2}}{\partial x_{n}^{2}} f\left( x\right)
\end{bmatrix}
\end{gather*}
$$
- Это симметричная матрица, то есть $\frac{\partial ^{2}}{\partial x_{i} \partial x_{j}} f\left( x\right) =\frac{\partial ^{2}}{\partial x_{j} \partial x_{i}} f\left( x\right)$.
- Матрица Гессе используется для нахождения экстремумов и анализа выпуклости функций:
	 - Если $H_{f}$​ **положительно** определённая (все её собственные числа положительны), то точка — локальный **минимум**.
	 - Если $H_{f}$​ **отрицательно** определённая (все её собственные числа отрицательны), то точка — локальный **максимум**.
	 - Если у $H_{f}$​ есть собственные числа разных **знаков**, то точка — **седловая** (перегиб).

<br><br>

### Множители Лагранжа:

Используется для нахождения точек экстремума при ограничении.  
$f\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n}\right)$ — функция (нужно найти её точки экстремума).  
$g\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n}\right) =0$ — ограничение в виде уравнения.

Вводим новую функцию:
$$
\mathcal{L}\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n} ,\ \lambda \right) =f\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n}\right) -\lambda g\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n}\right)
$$
Решаем систему уравнений:
$$
\begin{gather*}
\begin{cases}
\frac{\partial \mathcal{L}}{\partial x_{1}} =0,\\
\vdots \\
\frac{\partial \mathcal{L}}{\partial x_{n}} =0,\\
\frac{\partial \mathcal{L}}{\partial \lambda } =0
\end{cases} \hspace{10mm} x_{1} ,\ x_{2} ,\ ...,\ x_{n} - \text{точки экстремума}
\end{gather*}
$$
Функция Лагранжа для нескольких ограничений:
$$
\begin{gather*}
\mathcal{L}\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n} ,\ \lambda _{1} ,\ \lambda _{2} ,\ ...\ ,\ \lambda _{k}\right) = \\
= f\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n}\right) -\sum _{i=1}^{k} \lambda _{i} g_{i}\left( x_{1} ,\ x_{2} ,\ ...\ ,\ x_{n}\right)
\end{gather*}
$$

<br><br>

### Метод наименьших квадратов:

**Функция ошибки:** 
$$
S( a,\ b) =\sum _{i=1}^{n}( y_{i} -f( x_{i}))^{2}
$$
Для линейной функции:
$$
S( a,\ b) =\sum _{i=1}^{n}( y_{i} -ax_{i} -b)^{2}
$$

- Нужно подобрать такие $a$ и $b$, чтобы функция ошибки была минимальной. Для этого минимизируем функцию по $a$ и $b$.

Для линейной функции:
$$
\begin{cases}
\frac{\partial S}{\partial a} =-2\sum _{i=1}^{n} x_{i}( y_{i} -ax_{i} -b)^{2} =0\\
\frac{\partial S}{\partial b} =-2\sum _{i=1}^{n}( y_{i} -ax_{i} -b)^{2} =0
\end{cases}
$$
- Решая систему уравнений, получаем $a$ и $b$.

**Второй способ:**
$$
a=\frac{\sum _{i}( x_{i} -\overline{x})( y_{i} -\overline{y})}{\sum _{i}( x_{i} -\overline{x})^{2}} ,\hspace{10mm} b=\overline{y} -a\overline{a}
$$
$\overline{x}$, $\overline{y}$​ — средние значения.

<br><br>

### Метод Ньютона:
$$
x_{n+1} =x_{n} -\frac{f( x_{n})}{f'( x_{n})}
$$
Метод Ньютона для многих переменных:
$$
x_{n+1} = x_{n}- J^{-1}(x_{n}) \times F(x_{n})
$$
- $x_{n}$ — текущее приблежение на n-й итерации
- $J^{-1}(x_{n})$ — обратная матрица якоби 
- $F(x_{n})$ — вектор значений функции в точке $x$
$$
F(x) = \begin{pmatrix}
f_{1}(x) \\ f_{2}(x) \\ \vdots \\ f_{n}(x)
\end{pmatrix}
$$

<br><br>

### Замена переменных в плоских и пространственных интегралах:
$$
\begin{gather*}
x=x( u,\ v) ,\hspace{10mm} y=y( u,\ v)\\
\int \int _{D} f( x,\ y) dxdy=\int \int _{G} f( x( u,\ v) ,\ y( u,\ v)) \ |J( u,\ v) |\ dudv
\end{gather*}
$$
$J( u,\ v)$ — якобиан функций $x$ и $y$ по $u$ и $v$.

##### Пример:
$$
\begin{gather*}
x=r\cos \theta ,\ \ \ \ \ \ y=\sin \theta \\
J( r,\ \theta ) =\begin{vmatrix}
\cos \theta  & -r\sin \theta \\
\sin \theta  & r\cos \theta 
\end{vmatrix} =r\left(\cos^{2} \theta +\sin^{2} \theta \right) =r\\
\int \int _{D} f( x,\ y) dxdy=\int \int _{G} f( r\cos \theta ,\ r\sin \theta ) \cdot r\ drd\theta 
\end{gather*}
$$

<br><br>

### Замена переменных для перехода в другие координаты:
- Полярные координаты:
$$
x=r\cos \theta ,\hspace{10mm} y=r\sin \theta
$$
- Цилиндрические координаты:
$$
x=r\cos \theta ,\hspace{10mm} y=r\sin \theta ,\hspace{10mm} z=z
$$
- Сферические координаты:
$$
x=\rho \sin \phi \cos \theta ,\hspace{10mm} y=\rho \sin \phi \sin \theta ,\hspace{10mm} z=\rho \cos \phi
$$

<br><br>

### Формула площади для полярных координат:
$$
A=\frac{1}{2}\int _{b}^{a} r^{2} d\theta
$$
- $r$ — радиус, 
- $\theta$ — угол от $a$ до $b$.
 
<br><br>

### Поверхностный интеграл:
- Для $r( u,\ v) =( x( u,\ v) ,\ y( u,\ v) ,\ z( u,\ v))$
$$
\begin{gather*}
dS=\begin{vmatrix}
\frac{\partial r}{\partial u} \times \frac{\partial r}{\partial v}
\end{vmatrix} dudv
\end{gather*}
$$
- Для $z=f(x, y)$:
$$
dS=\sqrt{1+\left(\frac{\partial f}{\partial x}\right)^{2} +\left(\frac{\partial f}{\partial y}\right)^{2}} dxdy
$$

<br><br>

