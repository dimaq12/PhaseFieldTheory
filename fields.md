
# Круговая теория поля (версия 2.6)

> **Фундаментальная модель фазово-масштабного поля на логарифмическом цилиндре**

---

## I. Геометрия пространства

Пространство:  
**$\mathcal{M} = \mathbb{R}_t \times \mathbb{R}_\rho \times S^1_\alpha$**

Метрика:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
ds^2 = -dt^2 + e^{2\rho}(d\rho^2 + d\alpha^2)
$$
</div>

Объемная форма:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\star 1 = e^{2\rho} \, d\rho \wedge d\alpha
$$
</div>

---

## II. Поля и операторы

**Основные переменные:**
- **$\phi(\rho, \alpha, t)$** — скалярное поле  
- **$\mathbf{A} = A_\rho d\rho + A_\alpha d\alpha$** — векторный потенциал (1-форма)

**Дифференциальные операторы:**

| Оператор                | Формула |
|-------------------------|---------|
| Градиент $\nabla \phi$         | $\frac{1}{e^\rho}(\partial_\rho \phi, \frac{1}{e^\rho}\partial_\alpha \phi)$ |
| Дивергенция $\nabla \cdot \vec{F}$ | $\frac{1}{e^{2\rho}}(\partial_\rho F_\rho + \partial_\alpha F_\alpha)$ |
| Ротор $\nabla \times \vec{F}$     | $\frac{1}{e^{2\rho}}(\partial_\rho F_\alpha - \partial_\alpha F_\rho)$ |
| Лапласиан $\nabla^2 \phi$        | $\frac{1}{e^{2\rho}}\left[ \partial_\rho(e^{2\rho} \partial_\rho \phi) + \partial^2_\alpha \phi \right]$ |
| Волновой оператор $\Box \phi$     | $\partial_t^2 \phi - \nabla^2 \phi$ |

---

## III. Лагранжиан и уравнения движения

Скалярное поле:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\mathcal{L}_\phi = \frac{1}{2}(\partial_t \phi)^2 - \frac{1}{2e^{2\rho}}\left[(\partial_\rho \phi)^2 + (\partial_\alpha \phi)^2 \right]
$$
</div>

Векторный потенциал:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\mathcal{L}_A = -\frac{1}{4} F \wedge \star F \quad \text{где } F = dA
$$
</div>

Уравнения Эйлера–Лагранжа:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\Box \phi = 0 \qquad d \star dA = 0
$$
</div>

---

## IV. Электрическое и магнитное поле

Из векторного потенциала:

- Магнитное поле:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
B(\rho, \alpha, t) = \frac{1}{e^{2\rho}}(\partial_\rho A_\alpha - \partial_\alpha A_\rho)
$$
</div>

- Электрическое поле:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
E_\alpha = -\partial_t A_\alpha \qquad E_\rho = -\partial_t A_\rho
$$
</div>

Проверка уравнения Максвелла:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\nabla \times \vec{E} = -\partial_t \vec{B}
$$
</div>
✅ Подтверждено численно в лог-пространстве для волнового случая.

---

## V. Энергия и аподизация

Плотность энергии:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\mathcal{U} = \frac{1}{2}(\partial_t \mathcal{A})^2 + \frac{1}{2e^{2\rho}}\left[(\partial_\rho \mathcal{A})^2 + (\partial_\alpha \mathcal{A})^2\right]
$$
</div>

Аподизация:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
\mathcal{A}(\rho) = e^{-\rho^2} \cdot f(\rho, \alpha, t)
$$
</div>

---

## VI. Топология и калибровка

- Калибровка: $A \rightarrow A + d\chi$
- Топологический заряд:
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
Q = \frac{1}{2\pi} \int_0^{2\pi} \partial_\alpha \arg(\phi) \, d\alpha = n
$$
</div>

---

## VII. Выводы и наблюдения

- Потенциал $A$ способен формировать замкнутые кольцевые магнитные поля $B$, но **только в динамике** ($\partial_t A \ne 0$).
- В статике ($\partial_t A = 0$), $\nabla \times \vec{B} = \mu_0 \vec{J}$ требует наличия тока — проверено аналитически.
- Уравнение $\nabla \times \vec{E} = -\partial_t \vec{B}$ выполнено (численно подтверждено).
- Поле $\vec{E}$ вихревое и замкнутое по фазе, с масштабной локализацией.
- Энергия фокусируется в радиальном окне — эффект масштабной резонансной моды.
- Вся динамика построена без точечных источников, **в динамическом режиме**.

---

## VIII. Следующие шаги

- Ввести непрерывность тока $\partial_t \rho + \nabla \cdot \vec{J} = 0$
- Построить лагранжиан с нелинейностью (например, $\phi^4$)
- Провести квантование в лог-пространстве
- Спроектировать эксперимент: тороид с фазовой модуляцией и измерение $B$ на заданном $\rho_0$
- Проверить $\nabla \cdot \vec{B} = 0$ и поведение эффективной плотности
