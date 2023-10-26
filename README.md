# ODE-solver
Finite-difference ODE solver for linear/non-linear ODEs.

Решается нелинейная краевая задача второго порядка $y''(x)=f(x, y, y')$ методом итераций Ньютона. <br />
Неравномерная сетка $x_m= x_L + (\frac{m^2S}{M^2}+\frac{m(1-S)}{M}))(x_L - x_R)$ <br />
Точность решения $\epsilon = 10^{-4}$ <br />
**Порядок сходимости решения на линейных разностных задачах на Ньютоновских итерациях $=2$** <br />
Континуальное решение получено из разностного путём интерполяции полиномами Лагранжа по двум ближайшим точкам <br />
Начальное приближение - выпуклая комбинация точного аналитического решения и линейной функции, удовлетворяющей граничным условиям. <br />
Критерий завершения "внутренней" итерации - норма поправки $||v_h||<\frac{\epsilon}{2}$
