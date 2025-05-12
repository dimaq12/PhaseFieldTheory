# Круговая теория поля (версия 2.6‑rev, 12 мая 2025)

> **Фундаментальная модель фазово‑масштабного поля на логарифмическом цилиндре**  
> *Исправлено согласно итогам экспертного аудита (май 2025).*  

---

## I. Геометрия пространства

**Пространство**  
$\mathcal M = \mathbb R_t \times \mathbb R_\rho \times S^1_\alpha$

**Метрика**  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 ds^2 = -dt^2 + e^{2\rho}\,(d\rho^2 + d\alpha^2)
$$
</div>

Обратная метрика: $g^{\rho\rho}=g^{\alpha\alpha}=e^{-2\rho}$

**Объёмная форма (пространственная)**  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \star 1 = e^{2\rho}\,d\rho\wedge d\alpha
$$
</div>

---

## II. Поля и операторы

### Основные переменные
- $\phi(\rho,\alpha,t)$ — скалярное поле  
- $\mathbf A=A_\rho\,d\rho+A_\alpha\,d\alpha$ — векторный потенциал (1‑форма)

### Дифференциальные операторы в $(\rho,\alpha)$‑плоскости

| Оператор | Формула |
|----------|---------|
| Градиент $\nabla\phi$ | $e^{-2\rho}\bigl(\partial_\rho\phi,\;\partial_\alpha\phi\bigr)$ |
| Дивергенция $\nabla\!\cdot\!\mathbf F$ | $e^{-2\rho}\!\bigl[\partial_\rho\!\bigl(e^{2\rho}F_\rho\bigr)+\partial_\alpha\!\bigl(e^{2\rho}F_\alpha\bigr)\bigr]$ |
| Ротор $\nabla\times\mathbf F$ (скаляр) | $e^{-2\rho}\bigl(\partial_\rho F_\alpha-\partial_\alpha F_\rho\bigr)$ |
| Лапласиан $\nabla^2\phi$ | $e^{-2\rho}\!\bigl[\partial_\rho\!\bigl(e^{2\rho}\partial_\rho\phi\bigr)+\partial_\alpha\!\bigl(e^{2\rho}\partial_\alpha\phi\bigr)\bigr]$ |
| Волновой оператор $\Box\phi$ | $\partial_t^2\phi-\nabla^2\phi$ |

---

## III. Лагранжиан и уравнения движения

### Скалярное поле
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal L_\phi = \tfrac12(\partial_t\phi)^2 - \tfrac12 e^{-2\rho}\bigl[(\partial_\rho\phi)^2 + (\partial_\alpha\phi)^2\bigr].
$$
</div>

### Векторный потенциал
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal L_A = -\tfrac14 F \wedge \star F, \qquad F = dA.
$$
</div>

### Уравнения Эйлера–Лагранжа
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \Box \phi = 0, \qquad d\star dA = \mu_0\, J.
$$
</div>

Для $J=0$ возможно лишь **динамическое** решение, удовлетворяющее уравнению Ампера–Максвелла
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \nabla \times \mathbf B - \mu_0\varepsilon_0\, \partial_t \mathbf E = 0.
$$
</div>

---

## IV. Электрическое и магнитное поля

Из потенциала $A$ определим  

<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 B(\rho,\alpha,t) = e^{-2\rho}\bigl(\partial_\rho A_\alpha - \partial_\alpha A_\rho\bigr),
$$
</div>

<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 E_\rho = -\partial_t A_\rho, \qquad E_\alpha = -\partial_t A_\alpha.
$$
</div>

Они тождественно удовлетворяют закону Фарадея
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \nabla \times \mathbf E = -\partial_t B.
$$
</div>

---

## V. Энергия

Плотность энергии  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal U = \tfrac12\bigl(E^2 + B^2\bigr),\qquad E^2 = g^{ij}E_iE_j = e^{-2\rho}(E_\rho^2 + E_\alpha^2).
$$
</div>

Полная энергия в кольцевом сечении
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal E = \int_{0}^{2\pi}\! d\alpha \int_{-\infty}^{\infty}\! d\rho\, e^{2\rho}\, \mathcal U.
$$
</div>

---

## VI. Топология и калибровка

Калибровка: $A \mapsto A + d\chi$.

Топологический заряд  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 Q = \frac{1}{2\pi} \int_{0}^{2\pi} \partial_\alpha \arg(\phi)\, d\alpha \in \mathbb Z.
$$
</div>

---

## VII. Обсуждения

* Статическое кольцевое поле $B(\rho)$ **обязательно** требует ток $\mathbf J \neq 0$; безтоковые конфигурации возможны лишь динамически, когда вклад $-\mu_0\varepsilon_0\, \partial_t \mathbf E$ компенсирует ротор $\nabla \times \mathbf B$.  
* Скалярные и векторные моды локализуются по $\rho$ благодаря экспоненциальному фактору метрики, что формирует «радиальные резонансы».  
* При численном решении с корректными операторами выполняются тесты сохранения заряда $\partial_t \rho + \nabla \cdot \mathbf J = 0$.

---

## VIII. Следующие шаги

1. Реализовать непрерывность тока и проанализировать распределение $\mathbf J$ для стоячих мод.  
2. Добавить нелинейность (например $\phi^4$) и исследовать солитоноподобные решения.  
3. Выполнить каноническое квантование в лог‑координатах.  
4. Спроектировать эксперимент: тороид с фазовой модуляцией $A(t)$; измерить $B(\rho_0)$ и ток $\mathbf J(\rho_0)$.  
5. Проверить численно условие $\nabla \cdot \mathbf B = 0$ во всём объёме.  

---

*Документ отражает минимально необходимые математические исправления, выявленные аудитом (май 2025), и устраняет противоречие с уравнением Ампера–Максвелла.*
