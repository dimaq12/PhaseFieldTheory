# 🔁 ОСНОВЫ КРУГОВОГО МАТЕМАТИЧЕСКОГО АНАЛИЗА

## Общая идея

В духе круговой математики основным геометрическим объектом является круг или окружность, а операции над функциями интерпретируются через вращение, масштабирование и инверсию.

Важно: мы не вводим новых математических объектов, а создаем единый геометрический язык для классического анализа, основанный на круге, фазе и вращении. Это не замена традиционной математики, а её дополнение — с прицелом на интуицию, симметрию и образовательную наглядность.

Потенциал этого подхода проявляется особенно ясно в системах с логарифмическим масштабом, топологической компактностью, вращательной инвариантностью и спиральной структурой. Некоторые свойства здесь формулируются так, как если бы время, масштаб и фаза имели общую природу. Возникают отображения, устойчивые к двойственным преобразованиям, и спектры, допускающие циклическую декомпозицию.

---

## 1. 🔹 Круговой предел (фазовый предел)

**Определение:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\lim_{\alpha \to \alpha_0} f(e^{i\alpha}) = L
$$
</div>

**Смысл:**

Мы исследуем поведение функции по мере прохождения дуги на единичной окружности. Отказ от линейного интервала в пользу фазы означает, что переход **α → α₀** — это вращение.

Такая форма предела допускает не только обычные граничные переходы, но и периодические асимптотики, орбитальную сходимость, спиральную сходимость и потенциально — устойчивые структуры, повторяющиеся через кратные обороты.

---

## 2. 🔹 Круговая производная

**Определение:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d f}{d\alpha} = \lim_{\Delta \alpha \to 0} \frac{f(re^{i(\alpha + \Delta \alpha)}) - f(re^{i\alpha})}{\Delta \alpha}
$$
</div>

Если **z = re^{iα}**, то:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d f}{d\alpha} = i z \cdot \frac{df}{dz}
$$
</div>

Также:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{\partial f}{\partial \alpha} = i z \frac{\partial f}{\partial z} - i \bar z \frac{\partial f}{\partial \bar z}
$$
</div>

**Смысл:**

Это угловая скорость изменения функции в процессе её вращения вдоль окружности. Является производной по фазе при фиксированном радиусе.

Такая производная естественна в задачах с круговой калибровкой, фазовой задержкой, спиральным переносом и локальной симметрией при вращении.

---

## 3. 🔹 Фазовый интеграл (круговой интеграл)

**Определение:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\int_0^{2\pi} f(e^{i\alpha})\, d\alpha \quad \text{или} \quad \int_{\gamma} f(z) \, \frac{dz}{iz}
$$
</div>

Явный пример:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\oint_{|z|=1} z^n\, \frac{dz}{iz} = 2\pi \delta_{n,-1}
$$
</div>

Мера в координатах **z = e^{ρ + iα}**:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
d\mu = e^{2\rho} \, d\rho \, d\alpha
$$
</div>

**Смысл:**

Интеграл по дуге — это сумма локальных фазовых взаимодействий. Геометрия накопления вращения — как сумма поворотов или угловых импульсов.

---

## 4. 🔹 Фазовая непрерывность

**Определение:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\forall \varepsilon > 0, \exists \delta > 0 : |\alpha - \alpha_0| < \delta \Rightarrow |f(e^{i\alpha}) - f(e^{i\alpha_0})| < \varepsilon
$$
</div>

**Смысл:**

Непрерывность измеряется по углу, а не по линейному расстоянию. Это означает: малый поворот вызывает малое изменение функции.

Фазовая непрерывность допускает трактовку как локальная калибровка по циклу и позволяет формулировать круговые условия согласованности и квазипериодичности. В пределе это связывается с гомотопиями на пространстве фаз.

---

## 5. 🔹 Расширение координат: фазово-радиальная система

Переход от одного фазового измерения к цилиндрическим координатам:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
z = e^{\rho + i\alpha}, \quad \rho = \ln r
$$
</div>

Частные производные:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{\partial f}{\partial \alpha}, \quad \frac{\partial f}{\partial \rho}
$$
</div>

**Инверсия:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\rho \mapsto -\rho, \quad \alpha \mapsto -\alpha
$$
</div>

**Смысл:**

Логарифм радиуса становится осью масштабного течения. Возникают структуры, инвариантные к логарифмическим сдвигам, а также самоподобные моды и траектории.

---

## 6. 🔹 Круговые дифференциальные уравнения (фазовые дифуры)

**ОДУ:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{df}{d\alpha} = g(f)
$$
</div>

Пример:

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{df}{d\alpha} = i f \Rightarrow f(\alpha) = A e^{i\alpha}
$$
</div>

**Второй порядок:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d^2 f}{d\alpha^2} + f = 0 \Rightarrow f(\alpha) = A \cos(\alpha) + B \sin(\alpha)
$$
</div>

**Система:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d\vec{z}}{d\alpha} = M(\alpha) \vec{z}
$$
</div>

**Радиальная зависимость:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{\partial f}{\partial \rho} = \lambda f \Rightarrow f(\rho, \alpha) = e^{\lambda \rho} g(\alpha)
$$
</div>

**Смысл:**

Эти уравнения позволяют описывать круговые потоки, спектральные циклы и спиральные режимы, где логарифмическая и фазовая зависимости объединяются.

---

## 7. 🔹 Круговая гладкость и спектральность

**Определение гладкости:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
f(\alpha) \in C^\infty \iff \forall k, \; c_n = \mathcal{O}(n^{-k})
$$
</div>

**Базис:**

<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
e^{n\rho + i n\alpha}, \quad n \in \mathbb{Z}
$$
</div>

**Смысл:**

Гладкость выражается через спад Фурье-компонент. Это открывает путь к спектральной теории в цилиндрической геометрии и свёртке по орбитам спирального действия.

---

## 🔷 Примеры и приложения

1. **Фазовый маятник:**
<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d^2\theta}{d\alpha^2} + \sin(\theta) = 0
$$
</div>

2. **Автоколебания:**
<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d\theta}{d\alpha} = \omega - a \sin(\theta)
$$
</div>

3. **Потенциал:**
<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{d\phi}{d\alpha} = -\frac{dV}{d\phi}
$$
</div>

4. **Радиальное затухание:**
<div style="background:#f9f9f9; padding: 0.5em; border-left: 3px solid #ccc;">
$$
\frac{\partial f}{\partial \rho} = -\mu f
$$
</div>



