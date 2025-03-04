# 1 CLASE
## Introducción Sistemas Dinamicos
**Esta es la primera clase del semestre**, donde se habló de los acuerdos de la clase, incluyendo cómo van a ser los porcentajes evaluativos y las calificaciones. Después de esto, comenzamos con los temas a ver, que son: **Transformada de Laplace**, **Transformada Inversa** y **Descomposición en Fracciones Parciales**.
### Descomposicion en Fracciones Parciales
>🔑La descomposición en fracciones parciales es un método utilizado en cálculo y álgebra para expresar una fracción racional como la suma de fracciones más simples, cuyos denominadores son factores del denominador original.

A continuacion se muestra el primer y unico  ejercicio realizado en clase:

$$ G(s) = \frac{2s^2 - 4}{(s+1)(s-2)(s-3)} $$

Queremos descomponerla en fracciones parciales:

$$ G(s) = \frac{A}{s+1} + \frac{B}{s-2} + \frac{C}{s-3} $$

Igualando términos:

$$ A(s-2)(s-3) + B(s+1)(s-3) + C(s+1)(s-2) = 2s^2 - 4 $$

Desarrollando los productos:

$$ A(s^2 - 5s + 6) + B(s^2 - 2s - 3) + C(s^2 - s - 2) = 2s^2 - 4 $$

Igualando coeficientes:

$$ A + B + C = 2 $$
$$ -5A - 2B - C = 0 $$
$$ 6A - 3B - 2C = -4 $$




