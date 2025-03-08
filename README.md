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

# Ejercicios 

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

Sustituyendo A en B 

$$ B = 5 - A : B = 5 - (-1) = 6 $$

$$ B = 6 $$

$$\frac{5s + 3}{(s+1)(s-2)} = \frac{-1}{s+1} + \frac{6}{s-2}$$

### 📚 2 Ejercicio

Encuentra las fracciones parciales de la siguiente expresión: 

$$\frac{7s + 9}{(s-1)(s+2)}$$

Solución:

Escribimos la fracción original como una suma de fracciones parciales: 

$$\frac{7s + 9}{(s-1)(s+2)} = \frac{A}{s-1} + \frac{B}{s+2}$$

$$7s + 9 = A(s + 2) + B(s - 1)$$
$$7s + 9 = As + 2A + Bs - B$$ 
$$7s + 9 = (A + B)s + (2A - B)$$

$$A + B = 7$$ 
$$2A - B = 9$$

De la primera ecuacion: 

$$B = 7 -A$$

Sustituyendo en la segunda:

$$2A - 7 - A = 9$$
$$2A -7 +A = 9$$
$$3A = 16$$

$$A = \frac{16}{3}$$

Sustituyendo A en B:

$$B = 7 - A : B = 7 - \frac{16}{3} =  \frac{21}{3} - \frac{16}{3} =  \frac{5}{3}$$
$$B = \frac{5}{3}$$

$$\frac{7s + 9}{(s-1)(s+2)} = \frac{\frac{16}{3}}{s-1} + \frac{\frac{5}{3}}{s+2}$$

# 2 CLASE

## Continuacion de fraciones parciales e inicio  transformada inversa de laplace

En esta clase, solucionamos otro ejercicio de fracciones parciales utilizando el método de sustitución. Este nuevo ejercicio tambien es del primer caso de fracciones parciales. Al final, analizamos la tabla de transformadas de Laplace para aplicar la transformada inversa correspondiente a las fracciones parciales definidas en el ejercicio. Este enfoque nos permitió comprender mejor cómo las fracciones parciales se utilizan en el contexto de las transformada inversa de Laplace.

### Transformada inversa de laplace
>🔑La transformada inversa de Laplace es una herramienta matemática que toma una función en el dominio de la frecuencia (variable "s") y la convierte de vuelta a una función en el dominio del tiempo (variable "t"), permitiendo obtener la solución de una ecuación diferencial en su forma original.

A continuacion se muestra el ejercicio realizado en clase:

$$ Y(s) = \frac{6s + 2}{(s+0.5)(s^2+3.4s+2.4)} $$
$$ \frac{6s+2}{(s+0.5)(s+1)(s+2.4)}= \frac{A}{s+0.5} + \frac{B}{s+1} + \frac{C}{s+2.4}$$

$$A(s+1)(s+2.4)+B(s+0.5)(s+2.4)+C(s+0.5)(s+1) = 6s + 2$$
$$A(s^2+3.4s+2.4)+B(s^2+2.9s+1.2)+C(s^2+1.5s+0.5) = 6s + 2$$

$$A+B+C = 0$$
$$3.4A+2.9B+1.5C = 6$$
$$2.4A+1.2B+0.5C = 2$$

$$A = -B-C$$
$$3.4(-B-C)+2.9B+1.5C = 6$$
$$0.5B-1.9C = 6$$
$$B=\frac{6+1.9C}{0.5}$$

$$2.4(\frac{6+1.9C}{0.5} -C)-1.2(\frac{6+1.9C}{0.5})+0.5C = 2$$
$$28.8+9.12C-2.4C-14.4-4.56C+0.5C = 2$$

$$2.66C = -12.4$$
$$C = \frac{-12.4}{2.66}= -4.66$$
$$B = \frac{6+1.9(-4.66}{-0.5}= 5.71$$

$$A = -5.71 + 4.66 = -1.05$$

$$ {\mathcal{L^-1} = \frac{-1.05}{s+0.5}+\frac{5.71}{s+1}-\frac{4.66}{s+2.4}} $$

$$ \mathcal{L}\{Y(t)\}= -1.05e^{-0.5t} + 5.71e^{-t} - 4.66e^{-2.4t} $$

# Ejercicios 

### 📚 1 Ejercicio

Encontrar la transformada inversa de Laplace de:

$$ Y(s) = \frac{4}{(s+1)(s+3)} $$

Solución:

Primero, descomponemos la función en fracciones parciales:

$$ \frac{4}{(s+1)(s+3)} = \frac{A}{s+1} + \frac{B}{s+3} $$

$$ 4 = A(s+3) + B(s+1) $$

$$ 4 = 2A $$
$$ A = 2 $$

$$ 4 = -2B $$
$$ B = -2 $$

$$ Y(s) = \frac{2}{s+1} - \frac{2}{s+3} $$

$$ \mathcal{L}^{-1}{Y(s)} = 2e^{-t} - 2e^{-3t} $$

### 📚 2 Ejercicio

Encontrar la transformada inversa de Laplace de:

$$ \frac{2s + 5}{(s+2)(s^2+1)} = \frac{A}{s+2} + \frac{Bs + C}{s^2+1} $$

$$ 2s + 5 = A(s^2+1) + (Bs + C)(s+2) $$

$$ 2(-2) + 5 = A((-2)^2+1) + (B(-2) + C)(-2+2) $$
$$ 1 = 5A $$
$$ A = \frac{1}{5} $$

$$ 2s + 5 = \frac{1}{5}(s^2+1) + Bs^2 + (2B+C)s + 2C $$

$$ 5 = \frac{1}{5} + 2C $$
$$ C = \frac{12}{5} $$

$$ 7 = \frac{2}{5} + 3B + 2C $$
$$ 7 = \frac{2}{5} + 3B + \frac{24}{5} $$
$$ 7 = \frac{26}{5} + 3B $$
$$ B = -\frac{1}{5} $$

$$ Y(s) = \frac{1}{5(s+2)} + \frac{-\frac{1}{5}s + \frac{12}{5}}{s^2+1} $$

$$ \mathcal{L}^{-1}{Y(s)} = \frac{1}{5}e^{-2t} - \frac{1}{5}\cos(t) + \frac{12}{5}\sin(t) $$



























































# 3 CLASE (VIRTUAL)

En esta clase comenzamos con un repaso conciso de las funcionalidades básicas de MATLAB, seguido de una demostración práctica sobre cómo calcular la transformada de Laplace utilizando este software. Posteriormente, realizamos un ejercicio de fracciones parciales, enfocándonos en el primer caso y empleando el método simplificado para facilitar el proceso de descomposición

>🔑MATLAB**: Un software matemático que permite realizar cálculos numéricos complejos, visualizar datos y programar algoritmos, ampliamente utilizado en ingeniería y ciencias.

```
syms s t
F = (s+3)/((s+1)*(s+2)); 
f = ilaplace(F, t); 
disp(f); 
ezplot(f, [0, 10]); 
```
En este codigo se muestra de manera sencilla como solucionar  una ecuacion con transformada inversa de laplace y su grafica. Hay que tener en cuenta que para poder generar esto debemos trabajar con variables simbolicas a las cual se refiere la biblioteca "syms".

### Ejercicio primer caso con el metodo simplificado:

$$  Y(s) = \frac{s+3}{(s+1)(s+2)} = \frac{A}{s+1} + \frac{B}{s+2} $$

$$ A= \left( \frac{(s+1)(s+3)}{(s+1)(s+2)}  \right)_{s=-1} = \frac{2}{1} = 2$$

$$B= \left( \frac{(s+2)(s+3)}{(s+1)(s+2)} \right)_{s=-2} = \frac{2+3}{-2+1} = -1$$

$$\mathcal{L}^-1{}{Y(s)} = \frac{2}{s+1} - \frac{1}{s+2}$$

$$ \mathcal{L}{Y(t)} = 2e^{-t} -e^{-2t} $$

# Ejercicios

### 📚 1 Ejercicio

Encontrar la transformada inversa de Laplace de:

$$ Y(s) = \frac{2s + 1}{(s+1)(s+3)} = \frac{A}{s+1} + \frac{B}{s+3} $$

$$ A = \left( \frac{(s+1)(2s+1)}{(s+1)(s+3)} \right)_{s=-1} = \frac{-2+1}{-1+3} = \frac{-1}{2} $$

$$ B = \left( \frac{(s+3)(2s+1)}{(s+1)(s+3)} \right)_{s=-3} = \frac{-6+1}{-3+1} = \frac{-5}{-2} = \frac{5}{2} $$

$$ \mathcal{L}^{-1}\{Y(s)\} = -\frac{1}{2}\frac{1}{s+1} + \frac{5}{2}\frac{1}{s+3} $$

$$ \mathcal{L}^{-1}\{Y(t)\} = -\frac{1}{2}e^{-t} + \frac{5}{2}e^{-3t} $$

### 📚 2 Ejercicio

Encontrar la transformada inversa de Laplace de:
$$ Y(s) = \frac{4s - 1}{(s+2)(s-1)} = \frac{A}{s+2} + \frac{B}{s-1} $$

$$ A = \left( \frac{(s+2)(4s-1)}{(s+2)(s-1)} \right)_{s=-2} = \frac{-8-1}{-2-1} = \frac{-9}{-3} = 3 $$

$$ B = \left( \frac{(s-1)(4s-1)}{(s+2)(s-1)} \right)_{s=1} = \frac{4-1}{1+2} = \frac{3}{3} = 1 $$

$$ \mathcal{L}^{-1}\{Y(s)\} = \frac{3}{s+2} + \frac{1}{s-1} $$

$$ \mathcal{L}^{-1}\{Y(t)\} = 3e^{-2t} + e^{t} $$

# 4 CLASE 
Para esta ocasión realizamos un ejercicio acerca de la descomposicion en fracciones parciales de: 

$$ G(s) = \frac {s^{2}+2s+3} {(s^{2}+2s+2)(s^{2}+2s+5)} = \frac {As+B} {(s^{2}+2s+2)} + \frac {Cs+D} {(s^{2}+2s+5)}  $$
$$ \frac {-2+-√4-8}{2} $$
$$ \frac {-2+-√4}{2} $$
$$ \frac {-2+-√4i}{2} $$
$$ -1+-i $$
Iniciaremos despejando las constantes A,B,C y D, se multiplican ambos lados de la ecuacion por el denominador mas comun 
$$ {s^{2}+2s+3} = {(As+B)} {(s^{2}+2s+5)} {(Cs+D)} {(s^{2}+2s+2)} $$
Igualaremos los coeficientes: 
$$ {s^{2}+2s+3} = {(As^{3}+2As^{2}+5As+Bs^{2}+2Bs+5B+Cs^{3}+2Cs^{2}+Ds^{2}+2Ds+2D)} $$
Posteriormente, vamos a obtener las siguientes ecuaciones
$$ {0 = A + C} $$
$$ {1 = 2A + B + 2C + D} $$
$$ {2 = 5A + 2B + 2C + 2D} $$
$$ {3 = 5B + 2D} $$
$$ {A = 0 -C}$$
$$ {1 = 2(0) + B + 2(0) + D}$$
$$ {1 = B + D} $$

# Ejercicios 

### 📚 1 Ejercicio
$$G(s) = \frac{s^2+3s+4}{(s^2+3s+2)(s^2+3s+6)}$$ 
$$G(s) = \frac{As+B}{(s^2+3s+2)} + \frac{Cs+D}{(s^2+3s+6)}$$
$$A = 0, B = 1, C = 0, D = -1$$
$$G(s) = \frac{1}{(s^2+3s+2)} - \frac{1}{(s^2+3s+6)}$$

### 📚 2 Ejercicio
$$G(s) = \frac{s+2}{(s+1)(s+3)}$$
$$G(s) = \frac{A}{s+1} + \frac{B}{s+3}$$
$$(s+1)(s+3)G(s) = A(s+3) + B(s+1)$$
$$s+2 = As+3A+Bs+B$$
$$1 = A+B$$
$$2 = 3A+B$$
$$A = \frac{1}{2}$$
$$B = \frac{1}{2}$$
$$G(s) = \frac{1/2}{s+1} + \frac{1/2}{s+3}$$

# 5 CLASE
En esta clase realizamos un ejercicio donde se aclaran dudas

$$G(s) = \frac{2s-3}{(s+2)(s+10^3)} = \frac{A}{(s+2)} - \frac{B}{(s+10^3)} - \frac{C}{(s+10^2)} - \frac{D}{(s+10)}$$

Para resolver A, se multiplica ambos lados de la ecuación por (s+2) y se evalúa en s = -2:

$$A = \left. \frac{(s+2)(2s-3)}{(s+2)(s+10^3)} \right|_{s=-2} = \frac{2(-2)-3}{(-2)+10^3} = \frac{-4-3}{8^3} = \frac{7}{512}$$

Para resolver B, se multiplica ambos lados de la ecuación por (s+10^3) y se evalúa en s = -10^3:

$$B = \left. \frac{(s+10^3)(2s-3)}{(s+2)(s+10^3)} \right|_{s=-10^3} = \frac{2(-10^3)-3}{(-10^3)+2^2} = \frac{-20-3}{8} = \frac{23}{8}$$

Para resolver C, se utiliza la derivada de la función:

$$C = \left. \frac{d}{ds} \frac{2s-3}{s+2} \right|{s=-10} = \left. \frac{2(s+2)-1(2s-3)}{(s+2)^2} \right|{s=-10} = \frac{-16+23}{64} = \frac{7}{64}$$

Para resolver D, se utiliza una fórmula similar a la de C:

$$D = \left. \frac{(2-2)(s+2^2)-2(s+2)(2(s+2)-2s-3)}{s+2^4} \right|_{s=-10} = \frac{-112}{4096}

# Ejercicios

### 📚 1 Ejercicio
$$G(s) = \frac{3s-2}{(s+1)(s+10)} = \frac{A}{(s+1)} - \frac{B}{(s+10)}$$
$$A = \frac{3(-1)-2}{-1+10} = \frac{-5}{9}$$
$$B = \frac{3(-10)-2}{-10+1} = \frac{-32}{-9} = \frac{32}{9}$$

### 📚 2 Ejercicio
$$G(s) = \frac{4s-5}{(s+2)(s+5)} = \frac{A}{(s+2)} - \frac{B}{(s+5)}$$
$$A = \frac{4(-2)-5}{-2+5} = \frac{-13}{3}$$
$$B = \frac{4(-5)-5}{-5+2} = \frac{-25}{-3} = \frac{25}{3}$$

$$ F_2(S)=  \frac{(5s+2)}{(s+1)(s+2)^2} $$
$$ \frac {A}{(s+1)} + \frac {B}{(s+2)^2} + \frac {C}{(s+2)}  $$
$$ A = (\frac {(s+1)(5s+2)} {(s+1) (s+2)^2} $$
$$  $$
$$  $$
$$  $$
$$  $$
$$  $$
