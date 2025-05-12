# Круговая теория поля (версия 2.6‑rev, 12 мая 2025)

> **Фундаментальная модель фазово‑масштабного поля на логарифмическом цилиндре**  
> *Исправлено согласно итогам экспертного аудита (май 2025).*  

---

## I. Геометрия пространства

**Пространство**  
$\mathcal M = \mathbb R_t 	imes \mathbb R_
ho 	imes S^1_lpha$

**Метрика**  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 ds^2 = -dt^2 + e^{2
ho}\,(d
ho^2 + dlpha^2)
$$
</div>

Обратная метрика: $g^{
ho
ho}=g^{lphalpha}=e^{-2
ho}$

**Объёмная форма (пространственная)**  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \star 1 = e^{2
ho}\,d
ho\wedge dlpha
$$
</div>

---

## II. Поля и операторы

### Основные переменные
- $\phi(
ho,lpha,t)$ — скалярное поле  
- $\mathbf A=A_
ho\,d
ho+A_lpha\,dlpha$ — векторный потенциал (1‑форма)

### Дифференциальные операторы в $(
ho,lpha)$‑плоскости

| Оператор | Формула |
|----------|---------|
| Градиент \(
abla\phi\) | \(e^{-2
ho}(\partial_
ho\phi,\;\partial_lpha\phi)\) |
| Дивергенция \(
abla\!\cdot\!ec F\) | \(e^{-2
ho}igl[\partial_
ho(e^{2
ho}F_
ho)+\partial_lpha(e^{2
ho}F_lpha)igr]\) |
| Ротор \(
abla	imesec F\) | \(e^{-2
ho}(\partial_
ho F_lpha - \partial_lpha F_
ho)\) |
| Лапласиан \(
abla^2\phi\) | \(e^{-2
ho}igl[\partial_
ho(e^{2
ho}\partial_
ho\phi) + \partial_lpha(e^{2
ho}\partial_lpha\phi)igr]\) |
| Волновой оператор $\Box\phi$ | $\partial_t^2\phi-
abla^2\phi$ |

---

## III. Лагранжиан и уравнения движения

### Скалярное поле
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal L_\phi = 	frac12(\partial_t\phi)^2 - 	frac12 e^{-2
ho}igl[(\partial_
ho\phi)^2 + (\partial_lpha\phi)^2igr].
$$
</div>

### Векторный потенциал
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal L_A = -	frac14 F \wedge \star F, \qquad F = dA.
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
 
abla 	imes \mathbf B - \mu_0arepsilon_0\, \partial_t \mathbf E = 0.
$$
</div>

---

## IV. Электрическое и магнитное поля

Из потенциала $A$ определим  

<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 B(
ho,lpha,t) = e^{-2
ho}igl(\partial_
ho A_lpha - \partial_lpha A_
hoigr),
$$
</div>

<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 E_
ho = -\partial_t A_
ho, \qquad E_lpha = -\partial_t A_lpha.
$$
</div>

Они тождественно удовлетворяют закону Фарадея
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 
abla 	imes \mathbf E = -\partial_t B.
$$
</div>

---

## V. Энергия

Плотность энергии  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal U = 	frac12igl(E^2 + B^2igr),\qquad E^2 = g^{ij}E_iE_j = e^{-2
ho}(E_
ho^2 + E_lpha^2).
$$
</div>

Полная энергия в кольцевом сечении
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 \mathcal E = \int_{0}^{2\pi}\! dlpha \int_{-\infty}^{\infty}\! d
ho\, e^{2
ho}\, \mathcal U.
$$
</div>

---

## VI. Топология и калибровка

Калибровка: $A \mapsto A + d\chi$.

Топологический заряд  
<div style="background:#f9f9f9; padding:0.5em; border-left:3px solid #ccc;">
$$
 Q = rac{1}{2\pi} \int_{0}^{2\pi} \partial_lpha rg(\phi)\, dlpha \in \mathbb Z.
$$
</div>

---

## VII. Обсуждения

* Статическое кольцевое поле $B(
ho)$ **невозможно без тока**: при $A=A(
ho,lpha)$ возникает ток $ec J = rac{1}{\mu_0} 
abla 	imes ec B$. Согласованное решение без $J$ требует временной зависимости $A(
ho,lpha,t)$.  
* Скалярные и векторные моды локализуются по $
ho$ благодаря экспоненциальному фактору метрики, что формирует «радиальные резонансы».  
* При численном решении с корректными операторами выполняются тесты сохранения заряда $\partial_t 
ho + 
abla \cdot \mathbf J = 0$.

---

## VIII. Следующие шаги

1. Реализовать непрерывность тока и проанализировать распределение $\mathbf J$ для стоячих мод.  
2. Добавить нелинейность (например $\phi^4$) и исследовать солитоноподобные решения.  
3. Выполнить каноническое квантование в лог‑координатах.  
4. Спроектировать эксперимент: тороид с фазовой модуляцией $A(t)$; измерить $B(
ho_0)$ и ток $\mathbf J(
ho_0)$.  
5. Проверить численно условие $
abla \cdot \mathbf B = 0$ во всём объёме.  

---

*Документ отражает исправления, соответствующие римановой геометрии и уравнениям Максвелла. Утверждение о безтоковом $B$ удалено как ошибочное.*
