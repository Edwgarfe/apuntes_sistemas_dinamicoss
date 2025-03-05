# 1 CLASE
## Introducción Sistemas Dinamicos
**Esta es la primera clase del semestre**, donde se habló de los acuerdos de la clase, incluyendo cómo van a ser los porcentajes evaluativos y las calificaciones. Después de esto, comenzamos con los temas a ver, que son: **Transformada de Laplace**, **Transformada Inversa** y **Descomposición en Fracciones Parciales**.
### Descomposicion en Fracciones Parciales
>🔑La descomposición en fracciones parciales es un método utilizado en cálculo y álgebra para expresar una fracción racional como la suma de fracciones más simples, cuyos denominadores son factores del denominador original.

A continuacion se muestra el primer ejercicio realizado en clase, donde se muestra el 1 caso de fracciones parciales(raices reales y simples):

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

Dado que:

$$ A = 2 - B - C $$

Sustituyendo en la ecuación original:

$$ -5(2 - B - C) - 2B - C = 0 $$

Simplificando:

$$ -10 + 3B + 4C = 0 $$
$$ C = \frac{10 - 3B}{4} $$

Sustituyendo \( C \) en la ecuación:

$$ 6(2 - B - C) - 3B - 2\left( \frac{10 - 3B}{4} \right) = -4 $$
$$ 12 - 6B - \left( \frac{60 - 18B}{4} \right) - 3B + \left( \frac{6B}{4} \right) = -4 $$
$$ 12 - 6B - 15 - 5 - 6B + \left( \frac{18B}{4} \right) - 3B + \left( \frac{6B}{4} \right) = -4 $$

Resolviendo para \( B \):

$$ B = -\frac{4}{3} $$

Sustituyendo \( B \) en la ecuación de \( C \):

$$ C = 10 - \frac{3(-4/3)}{4} = \frac{14}{4} = \frac{7}{2} $$

Sustituyendo \( B \) y \( C \) en la ecuación de \( A \):

$$ A = 2 - \frac{7}{2} - \left(-\frac{4}{3}\right) = 2 - 7 + \frac{4}{6} = -\frac{1}{6} $$

#Ejercicios 

### 📚 1 Ejercicio
Encuentra las fracciones parciales de la siguiente expresión: 

$$  \frac{5s + 3}{(s+1)(s-2)}  $$

Solución:

Escribimos la fracción original como una suma de fracciones parciales: 

$$ \frac{5s + 3}{(s+1)(s-2)} = \frac{A}{s+1} + \frac{B}{s-2} $$

$$ 5s + 3 = A(s - 2) + B(s + 1) $$

$$ A + B = 5 $$ 
$$ B - 2A = 3 $$

De la primera ecuación

$$ B = 5 - A $$

Sustituyendo en la segunda

$$ 5 - A - 2A= 3 $$
$$ -3A = -2 $$
$$ 2 -3 = A $$
$$ -1 = A $$

$$ A = -1 $$


