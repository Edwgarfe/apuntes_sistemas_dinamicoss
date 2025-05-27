## TERCER CORTE 
# 1 CLASE
## Sistemas Hidraulicos 
### Sitemas de tanques 
>🔑 En sistemas industriales de tanques es deseable manteber flujo o nivel constante.

### Modelo de un tanque 
![Imagen tanque](/imagen_tanques.png)

$$ q_{i} , q_{o}; -Flujos-de-entrada-y-salida-del-liquido  $$ 
$$ R_{1}; -Resistencia-al-flujo $$
$$ A_{1};-Área-transversal-del-tanque $$
$$ h_{1};-Nivel-de-líquido-en-el-tanque $$

##### Flujo de salida del tanque 
$$ q_{1}= \frac{h_{1}}{R_{1}} $$
##### intercambio de energia 
$$ A_{1}\frac{dh_{1}}{dt} = q_{i} - q_{1} $$

#### Modelo q1 como entrada y  h1 como salida

$$ q_{1}= \frac{h_{1}}{R_{1}} $$
$$  A_{1}\frac{dh_{1}}{dt} = q_{i} - q_{1} $$

$$ A_{1}\frac{dh_{1}}{dt} = q_{i} - \frac{h_{1}}{R_{1}} $$

#### Modelo qi como entrada y q1 como salida 

$$ q_{1}= \frac{h_{1}}{R_{1}} $$
$$  A_{1}\frac{dh_{1}}{dt} = q_{i} - q_{1} $$

> Oposicion al flujo

$$ h_{1} = q_{1}*R1 $$

$$ R_{1}A_{1}\frac{dq_{1}}{dt} = q_{i} - q_{1} $$


### Modelos 2 tanques 
![tanques interconectados](/tanques_interconectados.jpg)

$$ q_{1}= \frac{h_{1}}{R_{1}} ==> h_{1}=q_{1}*R_{1} $$
$$  A_{1}\frac{dh_{1}}{dt} = (q_{i} - q_{1}) $$
$$  A_{2}\frac{dh_{2}}{dt} = (q_{1} - q_{2}) $$

$$ q_{1} = \frac{h_{1}-h_{2}}{R_{1}} $$
$$ A_{1}\frac{dh_{1}}{dt} = (q_{i} - q{1} $$

$$ q_{2} = \frac{h_{2}} {R_{2}} $$
$$ A_{2}\frac{dh_{2}}{dt} = (q_{1} - q{2} $$

$$ R_{2}A_{2}\frac{dq_{2}}{dt} = (q_{1}- q_{2}) $$
$$ R_{2}A_{2}\frac{dq_{2}}{dt} + q_{2} = q_{1} $$

$$ A_{1}\frac{dh_{1}}{dt} = (q_{i} - R_{2}A_{2}\frac{dq_{2}}{dt}+q_{2}) $$

$$ R_{1}q_{1} + h_{2} = h_{1} $$
$$ R_{1}(R_{2}A_{2}\frac{dq_{2}}{dt}+q_{2}) + R_{2}q_{2} = h_{1} $$

$$ A_{1}\frac{d(R_{1}(R_{2}A_{2}\frac{dq_{2}}{dt}+q_{2})+R_{2}q_{2})}{dt} =  (q_{i}-R_{2}A_{2}\frac{dq_{2}}{dt}+q_{2})$$


El sistema de un solo tanque se describe mediante una ecuación diferencial de primer orden, lo que implica una respuesta exponencial característica. Esto significa que el sistema se asienta en un nuevo estado de equilibrio de manera suave, sin oscilaciones. Su comportamiento está dominado por una única constante de tiempo.

En contraste, el sistema de dos tanques interconectados se modela con una ecuación diferencial de segundo orden. Esta mayor complejidad permite una gama más rica de respuestas dinámicas, incluyendo la posibilidad de respuestas oscilatorias (subamortiguadas) o respuestas más lentas y prolongadas (sobreamortiguadas o críticamente amortiguadas).


# Ejercicios 

### 📚 1 Ejercicio
![Imagen tanque primer ejemplo](/tanque_ejeemplo.jpg)
##### Variables dentro del sistema:
$$ q_{i} -  Flujo de entrada de líquido$$
$$ q_{1} - Flujo de salida de líquido$$
$$ h_{1} -Nivel de líquido en el tanque$$
$$ A_{1}-Área transversal del tanque $$
$$ R_{1} -Resistencia al flujo de salida$$
$$ t -Tiempo$$


##### Ecuaciones 

$$ A_{1}\frac{dh_{1}}{dt} = qi -q1 $$
$$ q_{1} = \frac{h_{1}}{R_{1}}$$
$$ h_{1} = q_{1}R_{1} $$
$$ \frac{dh_{1}}{dt} = R_{1}\frac{dq_{1}}{dt}$$

Se sustituye  

$$ A_{1}(R_{1}\frac{dq_{1}}{dt})= q_{i} - q_{1} $$

$$ q_{i} = A_{1}R_{1}\frac{dq_{1}}{dt}+q_{1} $$

### 📚 2 Ejercicio
![ejemplo 2 tanques](/2_tanques.jpg)

##### Ecuaciones Fundamentales 
$$ A_{1}\frac{dh_{1}}{dt}= q_{i}-q_{1} $$
$$ A_{2}\frac{dh_{2}}{dt} = q_{1} - q_{2} $$
$$ q_{1} = \frac{h1-h2}{R1} $$
$$ q_{2} = \frac{h_{2}}{R_{2}} $$

##### Ecuacion 1
$$ A_{1}\frac{dh_{1}}{dt} = q_{i}-\frac{h_{1}-h_{2}}{R_{1}} $$
##### Ecuacion 2
$$ A_{2}\frac{dh_{2}}{dt} = \frac{h_{1}-h_{2}}{R_{1}} - \frac{h_{2}}{R_{2}} $$

##### De la ecuacion 2 despejamos h1:
$$ A_{2}\frac{dh_{2}}{dt} = \frac{h_{1}}{R_{1}} - \frac{h_{2}}{R_{1}} -\frac{h_{2}}{R_{2}} $$
$$ \frac{h_{1}}{R_{1}} = A_{2}\frac{dh_{2}}{dt} +h_{2}(\frac{1}{R_{1}}+\frac{1}{R_{2}}) $$
$$ h_{1} = R_{1}A_{2}\frac{dh_{2}}{dt} +h_{2}(1+\frac{1}{R_{2}}) $$

$$ \frac{dh_{1}}{dt} = R_{1}A_{2}\frac{dh_{2}^{2}}{dt^{2}}+(1+\frac{R_{1}}{R_{2}})\frac{dh_{2}}{dt} $$


$$ A_{1}R_{1}A_{2}\frac{d^{2}h_{2}}{dt^{2}}+A_{1}(1+\frac{R_{1}}{R_{2}})\frac{dh_{2}}{dt} = qi - A_{2}\frac{dh_{2}}{dt}-h_{2}(\frac{1}{R_{2}}) $$

##### Ecuacion diferencial 

$$ A_{1}R_{1}A_{2}\frac{d^{2}h_{2}}{dt^{2}} + (A_{1} + \frac{A_{1}R_{1}}{R2}+A_2)\frac{dh_{2}}{dt} + \frac{1}{R_{2}}h_{2}=q_{i} $$

# 28 Abril
## Ejemplo - Transformada de Laplace en Ecuaciones Diferenciales

###  Ejemplo
Hallar y(t) para la siguiente ecuación diferencial:

$$
\ddot{y}(t) + 3\dot{y}(t) + 2y(t) = 3\dot{u}(t) + 3u(t)
$$

### Aplicando la Transformada de Laplace:

$$
s^2Y(s) - y(0) - \dot{y}(0) + 3(sY(s) - y(0)) + 2Y(s) = 3(sU(s) - u(0)) + 3U(s)
$$

### Despejando Y(s) :

$$
Y(s) = \frac{U(s)(3s+3) - 3u(0) + y(0) + \dot{y}(0) + 3y(0)}{s^2 + 3s + 2}
$$

### Paso Final
Aplicar la **transformada inversa de Laplace** para obtener y(t) en el dominio del tiempo.

Este ejemplo muestra cómo resolver una ecuación diferencial de segundo orden utilizando la transformada de Laplace. La técnica transforma la ecuación del dominio del tiempo al dominio de la frecuencia (s), lo cual facilita el manejo algebraico. Luego de despejar Y(s), se aplica la transformada inversa para obtener la solución y(t) en el dominio original.
# Función de Transferencia

## ¿Qué es una función de transferencia?

- En el área de control se usa otro tipo de representación matemática denominada **función de transferencia**.
- Consiste en la **transformada de Laplace de la ecuación diferencial**.

> Se despeja:  
> $$
\frac{\text{Salida}}{\text{Entrada}} = \frac{Y(s)}{U(s)}
$$

> _Todas las condiciones iniciales de la ecuación diferencial son iguales a 0_

> ⚠️ **OJO:** Esto solo aplica cuando se van a hacer funciones de transferencia.  
> En el caso de querer solucionar la ecuación diferencial sí son necesarias las condiciones iniciales y no necesariamente son cero.

---

## Clasificación de las funciones de transferencia

Una función de transferencia se puede expresar como:

$$
G(s) = \frac{N(s)}{D(s)}
$$

- Donde \( N(s) \) y \( D(s) \) son polinomios en la variable \( s \).
- Si denominamos \( n \) al grado del polinomio del numerador.
- Si denominamos \( m \) al grado del polinomio del denominador.
- Existen tres casos posibles:

| Relación entre grados | Clasificación           |
|------------------------|--------------------------|
| \( n > m \)            | Impropia                 |
| \( m > n \)            | Estrictamente propia     |
| \( n = m \)            | Bipropia                 |

### Ejemplos

| Función de transferencia         | Clasificación         |
|----------------------------------|------------------------|
| $$s^2 + 1$$                      | Impropia              |
| $$2$$                            | Bipropia              |
| $$\frac{1}{s + 1}$$              | Estrictamente propia  |
| $$\frac{s^2 - 1}{s + 1}$$        | Impropia              |
| $$\frac{s - 1}{s + 1}$$          | Bipropia              |

---

## Zeros de una función de transferencia

- Si se iguala \( N(s) = 0 \), se obtienen los valores de \( s \) que cumplen la condición.
- Si el numerador se hace 0, toda la función de transferencia se vuelve 0.
- Por eso se les llama **"zeros"** de la función.
- Los valores de \( s \) pueden ser reales o complejos, y se pueden ubicar en el plano cartesiano.

---

## Ejemplo: Hallar los zeros

Dada la función de transferencia:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}
$$

Para hallar los ceros, igualamos el numerador a cero:

$$
N(s) = 0 \Rightarrow 3s - 1 = 0
$$

$$
s = \frac{1}{3}
$$
 Resultado: $$ s = \frac{1}{3}$$

 # Ejemplo: Hallar los Zeros de una Función de Transferencia

Queremos hallar los **zeros** de la siguiente función de transferencia:

$$
G(s) = \frac{s^2 + 4s + 1}{s^4 + 3s^3 + 3s^2 + s + 2}
$$

## Paso 1: Igualar el numerador a cero

Para encontrar los **zeros**, igualamos el numerador a cero:

$$
s^2 + 4s + 1 = 0
$$

## Paso 2: Resolver la ecuación cuadrática

Aplicamos la fórmula general:

$$
s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

Donde:  
- ( a = 1 )  
- ( b = 4 )  
- ( c = 1 )

Sustituyendo:

$$
s = \frac{-4 \pm \sqrt{16 - 4(1)(1)}}{2(1)} = \frac{-4 \pm \sqrt{12}}{2}
$$

$$
s = \frac{-4 \pm 2\sqrt{3}}{2} = -2 \pm \sqrt{3}
$$

## Resultado

Los zeros de la función de transferencia son:

$$
s = -2 + \sqrt{3} \quad \text{y} \quad s = -2 - \sqrt{3}
$$

Estos valores corresponden a las raíces del numerador, es decir, los valores de (s) para los cuales la salida del sistema es cero.


#  Ejercicio 1

Hallar los zeros de la siguiente función de transferencia:

$$
G(s) = \frac{s + 3}{s^2 + 5s + 6}
$$

### Paso 1: Igualamos el numerador a cero

$$
s + 3 = 0
$$

### Paso 2: Resolución

$$
s = -3
$$

**Resultado:** 

$$
s = -3
$$

---

# Ejercicio 2

Hallar los zeros de la siguiente función de transferencia:

$$
G(s) = \frac{s^2 - 2s}{s^2 + s + 1}
$$

### Paso 1: Igualamos el numerador a cero

$$
s^2 - 2s = 0
$$

### Paso 2: Factorizamos

$$
s(s - 2) = 0
$$

### Soluciones

- \( s = 0 \)
- \( s = 2 \)

**Resultado:** 
$$
s = 0 \quad \text{y} \quad s = 2
$$
# Polos de una Función de Transferencia

## Conceptos Clave

- Si se iguala \( D(s) = 0 \), se obtienen los valores de \( s \) que cumplen con la condición.
- Si el denominador se hace cero, toda la función de transferencia se vuelve infinita; de ahí el nombre "polos" para estos valores de \( s \).
- Estos valores pueden ser reales o complejos, por lo tanto se pueden ubicar en un plano cartesiano.

---

## Hallar los Polos de una Función de Transferencia

La función de transferencia está dada por:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}
$$

El polinomio característico es:

$$
D(s) = s^2 + 3s + 2
$$

Para encontrar los polos, igualamos el denominador a cero:

$$
D(s) = 0
$$

$$
s^2 + 3s + 2 = 0
$$

Factorizando:

$$
(s + 1)(s + 2) = 0
$$

Por lo tanto, los polos son:

$$
s = -1, \quad s = -2
$$

# Hallar los Polos de una Función de Transferencia

## Paso 1: Escribir la función de transferencia

La función de transferencia se representa como:

$$
G(s) = \frac{Y(s)}{U(s)} = \frac{3s - 1}{s^2 + 3s + 2} = \frac{N(s)}{D(s)}
$$

Donde:
- \( Y(s) \) es la salida del sistema en el dominio de Laplace.
- \( U(s) \) es la entrada del sistema.
- \( N(s) = 3s - 1 \) es el numerador.
- \( D(s) = s^2 + 3s + 2 \) es el denominador, también llamado **polinomio característico**.


## Paso 2: Encontrar el polinomio característico

El polinomio característico es:

$$
D(s) = s^2 + 3s + 2
$$

---

## Paso 3: Igualar a cero para encontrar los polos

Para encontrar los polos del sistema, igualamos el denominador a cero:

$$
D(s) = 0
$$

$$
s^2 + 3s + 2 = 0
$$

---

## Paso 4: Factorizar el polinomio

Factorizamos la ecuación cuadrática:

$$
(s + 1)(s + 2) = 0
$$

---

## Paso 5: Solucionar para \( s \)

Resolviendo la ecuación factorizada:

$$
s = -1, \quad s = -2
$$

## Resultado

Los **polos** del sistema son $$s = -1$$ y $$s = -2$$.  
Estos valores son importantes porque determinan la estabilidad y el comportamiento dinámico del sistema.

# Ejemplo: Hallar los Polos de una Función de Transferencia

## Función de transferencia dada:

$$
G(s) = \frac{s + 2}{(s + 3)(s^2 + 0.5s + 1)}
$$
## Hallar los polos
Los polos son los valores de \( s \) que anulan el denominador.
## Paso 1: Escribir el denominador

$$
D(s) = (s + 3)(s^2 + 0.5s + 1)
$$

## Paso 2: Igualar a cero

$$
(s + 3)(s^2 + 0.5s + 1) = 0
$$

Esto implica:

- $$s + 3 = 0 \Rightarrow s = -3$$
- $$s^2 + 0.5s + 1 = 0$$

## Paso 3: Resolver la ecuación cuadrática

Usamos la fórmula general:

$$
s = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

Para la ecuación cuadrática:

- \( a = 1 \)
- \( b = 0.5 \)
- \( c = 1 \)

Sustituyendo:

$$
s = \frac{-0.5 \pm \sqrt{0.25 - 4}}{2} = \frac{-0.5 \pm \sqrt{-3.75}}{2}
$$

$$
s = \frac{-0.5 \pm j\sqrt{3.75}}{2}
$$

$$
s = -0.25 \pm j\cdot \frac{\sqrt{15}}{4} \approx -0.25 \pm j0.9682
$$

---

## Resultado

Los **polos** del sistema son:

- $$s = -3$$
- $$s = -0.25 + j0.9682$$
- $$s = -0.25 - j0.9682$$

# Ejercicio 1

Hallar los polos de la siguiente función de transferencia:

$$
G(s) = \frac{5}{(s + 4)(s^2 + 2s + 5)}
$$

### Paso 1: Identificar el denominador

$$
D(s) = (s + 4)(s^2 + 2s + 5)
$$

### Paso 2: Igualar a cero

$$
(s + 4)(s^2 + 2s + 5) = 0
$$

Esto implica:

- $$s + 4 = 0 \Rightarrow s = -4$$

- $$s^2 + 2s + 5 = 0$$

### Paso 3: Resolver la ecuación cuadrática

Usamos la fórmula:

$$
s = \frac{-2 \pm \sqrt{2^2 - 4(1)(5)}}{2(1)} = \frac{-2 \pm \sqrt{4 - 20}}{2}
$$

$$
s = \frac{-2 \pm \sqrt{-16}}{2} = \frac{-2 \pm 4j}{2}
$$

$$
s = -1 \pm 2j
$$
### Polos del sistema:

- $$s = -4$$
- $$s = -1 + 2j$$
- $$s = -1 - 2j$$

## Ejercicio 2

Hallar los polos de la siguiente función de transferencia:

$$
G(s) = \frac{s + 1}{(s + 2)(s^2 + 4)}
$$
### Paso 1: Identificar el denominador

$$
D(s) = (s + 2)(s^2 + 4)
$$
### Paso 2: Igualar a cero

$$
(s + 2)(s^2 + 4) = 0
$$

Esto implica:

- $$s + 2 = 0 \Rightarrow s = -2$$
- $$s^2 + 4 = 0$$
### Paso 3: Resolver la ecuación cuadrática

$$
s^2 + 4 = 0 \Rightarrow s = \pm j2
$$
### Polos del sistema:

- $$s = -2$$
- $$s = +2j$$
- $$s = -2j$$

# 9 MAYO

# Diagramas de Flujo de Señales

- Este tipo de diagramas permite otra forma de representación de los sistemas más complejos.
- Se utilizan para obtener de una manera más sencilla la función de transferencia total del sistema.
- La **fórmula de Mason** permite calcular la función de transferencia de sistemas muy complejos.
## Elementos de los Diagramas de Flujo de Señal

### Nodo

- Representan las señales de entrada o salida del sistema.
- Se representa por medio de un **círculo con una etiqueta** que indique el nombre de la señal.

- Nodo de entrada:

  $$
  V(s)
  $$

- Nodo de salida:

  $$
  T(s)
  $$

Estos se representan gráficamente como círculos:

- Nodo blanco para entrada
- Nodo negro para salida

### Flecha

- Representa la **relación entre las variables del sistema**.
- Se representa por medio de flechas que indican el sentido de la relación.
- La flecha **sale del nodo de entrada** y **llega al nodo de salida**.
- Se **etiqueta la flecha** con la función de transferencia correspondiente.
## Interpretación de los Diagramas de Flujo de Señales

### Nodos y Ramas

Si una señal \( X(s) \) pasa por una función de transferencia \( F(s) \) y se convierte en \( Y(s) \), esto se representa así: 
X(s) ——— F(s) ———> Y(s)

La expresión matemática correspondiente es:

$$
Y(s) = F(s) \cdot X(s)
$$


### Suma de Señales
Cuando múltiples señales entran a un nodo, se suman o restan de acuerdo con el signo de su función de transferencia.

X1(s) ——— F1(s)
               \
                ➕———> Y(s)
               /
X2(s) ——— F2(s)
               \
X3(s) ——— -F3(s)

$$
Y(s) = F_1(s)X_1(s) + F_2(s)X_2(s) - F_3(s)X_3(s)
$$

# Comparación: Diagramas de Bloques vs. Diagramas de Flujo de Señales

La imagen muestra dos formas de representar un mismo sistema dinámico:

## Diagrama de Bloques (Parte Superior)
Este diagrama representa gráficamente la relación entre variables usando bloques funcionales conectados mediante señales de entrada y salida.

- Los bloques \( G_1, G_2, \dots, G_6 \) son funciones de transferencia.
- Las sumas se indican con círculos con signos \( + \) o \( - \).
- Las señales intermedias son \( n_1, n_2, n_3, n_4 \), etc.
- El flujo va desde la entrada \( u \) hasta la salida \( y \).

## Diagrama de Flujo de Señales (Parte Inferior)
Este diagrama representa el mismo sistema, pero usando nodos y ramas dirigidas:

- Los nodos representan señales (\( u, y, n_1, n_2, \dots \)).
- Las ramas entre nodos están etiquetadas con funciones de transferencia \( G_i \).
- La dirección de las flechas muestra el sentido de la señal.
- Este diagrama facilita el uso de la **fórmula de Mason** para encontrar la función de transferencia total del sistema.

## Conclusión

Ambos diagramas son equivalentes, pero:

- El **diagrama de bloques** es más intuitivo para visualizar la estructura del sistema.
- El **diagrama de flujo de señales** es más útil para cálculos sistemáticos, como la función de transferencia total mediante la fórmula de Mason.

# Definiciones 

- **Camino o Trayectoria** Un camino o trayectoria es un recorrido de ramas conectadas en el sentido de las flechas de las ramas.
- **Camino abierto**: Si no se cruza ningún nodo más de una vez, el camino o trayecto es **abierto**.
- **Camino cerrado**: Si el camino finaliza en el mismo nodo del cual partió, y no cruza ningún otro nodo más de una vez, es un **camino cerrado**.
- **Ganancia de lazo**: Es el producto de las ganancias de ramas de un lazo.
- **Trayecto o camino directo**: Es el trayecto de un nodo de entrada a un nodo de salida sin cruzar ningún nodo más de una vez.
- **Ganancia de trayecto directo**: Es el producto de las ganancias de rama de un camino o trayecto directo.
- **Lazo**: Un lazo es un camino o trayecto cerrado.
- **Ganancia de lazo**: Como se mencionó, es el producto de las ganancias de ramas del lazo.

Diagrama de Bloques y Trayectorias Directas  
Fecha: 05/05/2025

---

## Introducción

Los diagramas de bloques son representaciones gráficas esenciales para describir sistemas complejos y dinámicos de forma simplificada.  
Permiten visualizar cómo las señales o datos fluyen a través de distintas etapas o componentes del sistema.  

Este método es muy utilizado en ingeniería, ciencias aplicadas y áreas tecnológicas para el análisis, diseño y simulación de sistemas, especialmente en control automático y procesamiento de señales.

---

## Historia y Evolución

- Surgieron en el siglo XX con la ingeniería de control.  
- La transformada de Laplace permitió su uso en el dominio 👦s👦.  
- Actualmente se utilizan en software como MATLAB, Simulink, LabVIEW, y más.

---

## Bloque Funcional

### ¿Qué es un bloque funcional?

Un bloque funcional es un componente que recibe una señal de entrada y produce una señal de salida, generalmente mediante una función matemática.

Se representa gráficamente como un rectángulo con una o más entradas y salidas.

---

### Características

- Puede representar desde una ganancia simple hasta filtros complejos.  
- Maneja funciones de transferencia 👦G(s)👦 en sistemas lineales.  
- Permite modelar procesos modulares en sistemas dinámicos.

---

### Matemáticamente

Para entrada 👦u(t)👦 y salida 👦y(t)👦:

\[
y(t) = \mathcal{F}[u(t)]
\]

En dominio Laplace:

\[
Y(s) = G(s) U(s)
\]

---

### Ejemplos comunes

- Ganancia constante: 👦G(s) = K👦.  
- Integrador: 👦G(s) = \frac{1}{s}👦.  
- Derivador: 👦G(s) = s👦.  
- Filtro paso bajo: 👦G(s) = \frac{\omega_c}{s + \omega_c}👦.

---

### Ejemplo visual

![Bloque Funcional](https://upload.wikimedia.org/wikipedia/commons/5/5a/Block_diagram_with_labels.svg)  
Figura 1: Bloque funcional básico.

---

## Punto Suma

### Definición

Un punto suma combina señales de entrada, sumándolas algebraicamente según los signos indicados.

---

### Matemáticas

\[
y = \sum_{i=1}^n \sigma_i x_i
\]

donde 👦\sigma_i = \pm 1👦 según el signo de la entrada.

---

### Aplicaciones

- Cálculo de error en controladores.  
- Combinación de señales múltiples.

---

### Precauciones

- Unidades compatibles.  
- Signos adecuados para reflejar realidad.

---

### Ejemplo visual

![Punto Suma](https://upload.wikimedia.org/wikipedia/commons/8/87/Block_sum_symbol.svg)  
Figura 2: Punto suma.

---

## Punto de Ramificación

### Definición

Permite dividir una señal para enviarla a múltiples destinos idénticos.

---

### Aplicación

- Alimentar varios bloques con la misma señal.  
- Facilitar análisis en paralelo.

---

### Ejemplo visual

![Punto Ramificación](https://upload.wikimedia.org/wikipedia/commons/c/cf/Block_branching.svg)  
Figura 3: Punto de ramificación.

---

## Interpretación de Diagramas

### Dominio 👦s👦

- Complejo para análisis dinámico.  
- Transformada de Laplace convierte señales temporales en algebraicas.

---

### Ejemplo

Para 👦G(s) = \frac{10}{s + 5}👦, la salida es:

\[
Y(s) = \frac{10}{s + 5} U(s)
\]

---

### Visual

![Bloque con función de transferencia](https://upload.wikimedia.org/wikipedia/commons/1/1b/Block_Diagram_Control_System.svg)  
Figura 4: Bloque con función de transferencia.

---

## Bloques en Cascada

### Concepto

Salida de un bloque es entrada del siguiente.

---

### Función total

\[
G_{total}(s) = G_1(s) \times G_2(s) \times \cdots \times G_n(s)
\]

---

### Aplicación

Divide sistemas complejos en subsistemas.

---

### Visual

![Bloques en cascada](https://upload.wikimedia.org/wikipedia/commons/6/64/Block_diagram_series.svg)  
Figura 5: Bloques en cascada.

---

## Bloques en Paralelo

### Concepto

Mismo origen de entrada, salidas sumadas.

---

### Función total

\[
G_{total}(s) = G_1(s) + G_2(s) + \cdots + G_n(s)
\]

---

### Visual

![Bloques en paralelo](https://upload.wikimedia.org/wikipedia/commons/3/3f/Block_diagram_parallel.svg)  
Figura 6: Bloques en paralelo.

---

## Retroalimentación (Feedback)

### Definición

La salida influye en la entrada para corregir el sistema.

---

### Función de transferencia

Para retroalimentación negativa:

\[
T(s) = \frac{G(s)}{1 + G(s)H(s)}
\]

---

### Visual

![Retroalimentación](https://upload.wikimedia.org/wikipedia/commons/d/d1/Block_diagram_feedback.svg)  
Figura 7: Retroalimentación negativa.

---

## Trayectorias Directas

### Definición

Camino único desde entrada a salida, sin repetir nodos.

---

### Importancia

Base para aplicar fórmula de Mason.

---

### Visual

![Trayectorias](https://upload.wikimedia.org/wikipedia/commons/3/37/Mason_formula_example_01.svg)  
Figura 8: Trayectorias directas.

---

## Bucles de Retroalimentación

### Definición

Caminos cerrados que afectan la estabilidad.

---

### Clasificación

- Bucles simples e independientes.  
- Bucles múltiples con interacción.

---

## Fórmula de Mason

### Fórmula

\[
T = \frac{\sum_{k=1}^N P_k \Delta_k}{\Delta}
\]

Donde:  
- 👦P_k👦: ganancia trayectoria 👦k👦  
- 👦\Delta👦: determinante general  
- 👦\Delta_k👦: determinante sin bucles que tocan 👦P_k👦

---

### Cálculo de 👦\Delta👦

\[
\Delta = 1 - \sum L_i + \sum L_iL_j - \sum L_iL_jL_k + \cdots
\]

---

### Ejemplo

Sistema con dos trayectorias y dos bucles:

- 👦P_1 = G_1 G_2👦  
- 👦P_2 = G_3👦  
- Bucles 👦L_1 = H_1👦, 👦L_2 = H_2👦

---## Trayectorias Directas en Diagramas de Bloques

---

### Definición Formal

Una trayectoria directa es un camino que va desde la entrada hasta la salida de un sistema, siguiendo las conexiones de bloques y puntos suma o ramificación, sin pasar más de una vez por ningún nodo o bloque.

Esto significa que en el camino recorrido:

- No se visitan nodos repetidos (no hay ciclos en la trayectoria directa).  
- El camino comienza en la señal de entrada inicial y termina en la señal de salida final.

---

### Importancia de las Trayectorias Directas

- Son fundamentales para determinar la función de transferencia total del sistema mediante la fórmula de Mason.  
- Permiten identificar los diferentes "caminos" que la señal puede tomar para llegar a la salida.  
- Ayudan a entender cómo las señales se propagan y se combinan en sistemas complejos con múltiples rutas y retroalimentaciones.

---

### Propiedades Clave

1. Trayectorias simples: Cada trayectoria directa es un camino simple sin bucles ni repeticiones.  
2. Multiplicidad: Un sistema puede tener una o varias trayectorias directas.  
3. Ganancia de trayectoria: El producto de las funciones de transferencia de los bloques que componen la trayectoria directa.  
4. Independencia: Las trayectorias directas son independientes entre sí, no comparten nodos (aunque pueden compartir bloques si no se repiten en la trayectoria).

---

### Cálculo de la Ganancia de una Trayectoria Directa

Si una trayectoria directa pasa por los bloques 👦G_1, G_2, \ldots, G_m👦, entonces su ganancia 👦P👦 es:

\[
P = G_1 \times G_2 \times \cdots \times G_m
\]

---

### Ejemplo Básico

Considere un sistema con tres bloques conectados en serie desde la entrada hasta la salida:

\[
U \rightarrow G_1 \rightarrow G_2 \rightarrow G_3 \rightarrow Y
\]

Existe una única trayectoria directa con ganancia:

\[
P = G_1 G_2 G_3
\]

---

### Ejemplo con Múltiples Trayectorias

En sistemas más complejos con caminos paralelos y retroalimentaciones, puede haber varias trayectorias directas. Por ejemplo:

- 👦P_1 = G_1 G_2👦  
- 👦P_2 = G_3👦

Ambas van desde la entrada a la salida, pero por rutas distintas.

---

### Identificación en Diagramas

Para encontrar las trayectorias directas:

1. Localiza la señal de entrada y la salida.  
2. Traza todos los caminos posibles que vayan de entrada a salida sin repetir nodos.  
3. Anota los bloques que forman cada camino.  
4. Calcula la ganancia multiplicando las funciones de transferencia de esos bloques.

---

### Trayectorias y Bucles

- Los bucles son caminos cerrados que comienzan y terminan en el mismo nodo sin pasar dos veces por un nodo intermedio.  
- La fórmula de Mason usa las trayectorias directas junto con los bucles para calcular la función total del sistema.  
- Para cada trayectoria directa 👦P_k👦, se calcula un determinante 👦\Delta_k👦 excluyendo los bucles que interfieren con esa trayectoria.

---

### Ejemplo Visual

![Ejemplo Trayectorias Directas](https://upload.wikimedia.org/wikipedia/commons/3/37/Mason_formula_example_01.svg)  
Figura: Sistema con múltiples trayectorias directas y bucles.

---

### Trayectorias en Sistemas con Retroalimentación

En sistemas con retroalimentación, las trayectorias directas no pasan por los bucles de retroalimentación. Esto es importante para calcular correctamente las ganancias y aplicar la fórmula de Mason.

---

### Algoritmo para Encontrar Trayectorias Directas (Resumen)

1. Inicia en la entrada.  
2. Explora todas las conexiones hacia adelante.  
3. Evita regresar a nodos ya visitados.  
4. Cuando llegues a la salida, registra la trayectoria.  
5. Repite hasta explorar todos los caminos.

---

### Relevancia Práctica

- Facilitan el análisis de sistemas eléctricos, mecánicos, hidráulicos y de control.  
- Ayudan a simplificar sistemas complejos en partes manejables.  
- Permiten diseñar controladores precisos analizando caminos y efectos de retroalimentación.

---

### Ejemplo Numérico

Suponga un sistema con dos trayectorias:

- 👦P_1 = 5 \times 2 = 10👦  
- 👦P_2 = 3👦

Donde los valores representan las ganancias de los bloques en la trayectoria. Si se conocen los bucles y su interacción, la función total se puede calcular usando la fórmula de Mason con estas ganancias.


# Diagrama de bloques 
## Modelos de los sistemas complejos 
Se podrían modelar sistemas como un todo hallando las funciones de transferencia de cada componente
Otro enfoque es utilizar modelos ya desarrollados ampliamente para construir modelos más complejos
Aún usando este enfoque hay muchos tipos de procesos y dispositivos
## Solenoide
Un solenoide está formado por un circuito eléctrico, un acoplamiento electromecánico (transductor) y un sistema mecánico de traslación.
![Solenoide](/solenoide.jpg)

$$L\frac{di}{dt}+Ri=v(t)$$

$$I(s)=V(s)\frac{1}{Ls+R}$$

Modelo del circuito electromagnetico


$$F_{(s)}=K_{(s)}i$$

$$F_{s}(s)=K_{s}I(s)$$

Acople entre la parte electromagnetica y la parte mecanica

Cuando tenemos modelos lineales, modelos estaticos, la funcion de transferencia es constante, cuando tenemos modelos con terminos de ecuacion diferencial, es decir, derivadas de diferente orden o integrales, nos aparecerá en terminos de (s)

$$m\frac{{d}^2x}{d{t}^2}+b\frac{dx}{dt}+kx=f(t)$$

$$X(s)=F(s)\frac{1}{ms^2+bs+k}$$

Sistema mecanico


# Representación en bloques
![Bloque](/1bloque.jpg)

![Bloque1](/2bloque.jpg)

## Como modelar un motor DC

![Bloque](/motordc.jpg)

El motor de corriente continua, denominado también motor de corriente directa, motor CC o motor DC es una máquina que convierte energía eléctrica en energía mecánica, provocando un movimiento rotatorio, gracias a la acción de un campo magnético.
# Motor DC (corriente de campo)

### Circuito electromagnetico
![Motor](/2motorDC.jpg)

$$L_{c}\frac{di_{c}}{dt}+R_{c} i_{c}=v_{c}(t)$$

$$I_{c}(s)=V_{c}(s)\frac{1}{(sL_{c}+R_{c})}$$


El flujo Φ en el entrehierro es proporcional a la corriente de campo

$$Φ=K_{c}I_{c}$$

El torque desarrollado es proporcional al Φ y a la corriente de armadura

$$T_{m}=K_{a}I_{a}(t)K_{c}i_{c}(t)$$

$$T_{m}(s)=(K_{a}K_{c}I_{a})I_{c}(s)K_{m}I_{c}(s)$$

El torque aplicado a la carga es el desarrollado por el motor menos la inercia de la carga

$$T_{c}(s)=(T_{m}(s)-T_{p}(s)$$

El torque aplicado (parte mecánica) a la carga se comporta como un Sistema rotacional clásico que considera la inercia y la fricción mecánica

$$J\frac{d^2\theta }{dt^2}+b\frac{d\theta }{dt}+k\theta=\tau (t)$$

$$O(s)=T_{c}(s)\frac{1}{(s^2J+bs)}$$

## Motor DC (Corriente de campo)

### La conexión de los modelos se realiza de la siguiente manera:

![DC](/corrientedecampo.jpg)

![ecuacion](/ecuacion.jpg)

# Motor DC (Corriente de armadura)

La corriente de campo se supone constate por lo tanto el Torque es:

$$T_{m}(s)=(K_{a}K_{c}I_{c})I_{a}(s)=K_{m}I_{a}(s)$$

La corriente de armadura se relaciona con el voltaje aplicado a la armadura por:

$$V_{a}(s)=(sL_{a} R_{a})I_{a}(s) V_{b}(s)$$

El voltaje inducido en la armadura es proporcional a la velocidad angular del eje:

$$V_{a}(s)=(sL_{a} R_{a})I_{a}(s) V_{b}(s)$$
$$V_{b}(s)=K_{b}\omega(s)$$

Combinando estas ecuaciones se obtiene

$$I_{a}(s)=\frac{V_{a}(s)-K_{b}\omega (s)}{sL_{a} R_{a}}$$

La parte mecánica se comporta de la misma manera que en el caso anterior:

$$T_{c}(s)=(T_{m}(s)-T_{p}(s)$$

$$O(s)=(T_{c}(s)\frac{1}{(s^2J+bs)}$$

## Diagrama de bloques resultante
![bloque](/bloque.jpg)


# Engranajes y poleas

J y Km cambian si se tiene en cuenta el efecto de los engranaje o poleas 

![polea](/poleas.jpg)

### Diagrama de bloques

![bloque2](/bloque2.jpg)

### Transmision rotacional a lineal 





# Sistemas de Primer Orden 

La estructura general de una ecuacion de primer orden es : 

$$ ay'(t)+by(t) = cu(t) $$

Hallando la funcion de transferencia y aplicando la transformada de laplace es:

$$ asY(s)+bY(s) = cU(s) $$

Despejando salida/entrada:

$$ \frac{Y(s)}{U(s)}=\frac{c}{as+b} $$


>Las funciones de trasnferencia de primer orden proviene de una eciación diferencial de primer orden
>Los parametros a, b y c son los parametros fisicos del sistema que definen la dinamica del sistema.

## Forma canonica de los sistemas de primer orden
Esta forma permite identificar directamente los parametros temporales del sistema.

$$ \frac{Y(s)}{U(s)}=\frac{c}{as+b} = \frac{\frac{c}{b}}{\frac{a}{b}s+1}$$

>🔑 Se divide por b todos los terminos para no alterar la funcion y dejar la funcion de transferencia asi:

##### Constante de tiempo

>🔑 Esto indica cuanto se demora en responder el sistema 

$$ \tau  = \frac{a}{b} $$

##### Ganancia estatica

$$ K = \frac{c}{b}  $$

##### Forma canonica sistema de primer orden

$$ \frac{Y(s)}{U(s)}= \frac{K}{\tau S + 1}$$

### Ejemplos

![identificacion de forma canonica](/identificacion_forma_canonica.jpg)


Indentificar T y K para el siguiente sistema:

##### Ejemplo 1

$$ \frac{Y(s)}{U(s)}= \frac{0.8}{s+4} $$


$$ \frac{Y(s)}{U(s)}= \frac{0.8}{s+4} = \frac{\frac{0.8}{4}}{\frac{s}{4}+\frac{4}{4}} = \frac{0.2}{0.25*s+1} $$

$$ \tau= 0.25$$
$$ K = 0.2 $$

##### Ejemplo 2

$$ \frac{Y(s)}{U(s)}= \frac{5}{2s+16} $$

$$ \frac{Y(s)}{U(s)}= \frac{5}{2s+16} = \frac{\frac{5}{16}}{\frac{2}{16}s+1} = \frac{0.31}{0.125s+1} $$

$$ \tau= 0.125$$
$$ K = 0.31 $$

## Respuesta temporal de un sistema de primer orden 

![respuesta escalon](/respuesta_escalon.jpg)

$$ Y(s) = \frac{U(s)K}{\tau s +1} =  \frac{\frac{A}{s}K}{\tau s +1}$$

### Respuesta de un Sistema de primer orden ante una entrada escalón

$$ Y(s) = \frac{AK}{s(\tau s+1)} $$

Aplicandofracciones parciales:

$$ Y(s)= \frac{C1}{s}+\frac{C2}{s+\frac{1}{\tau}}=\frac{AK}{s}-\frac{AK}{s+\frac{1}{\tau}} $$

Al aplicar la transformada inversa de laplace 

$$ L^{-1}{ Y(s) } = y(t)= AK(1-e^{-\frac{t}{\tau}}) $$

### Respuesta temporal 
![](/respuesta_temporal.jpg)

![](/asumiendo_valores.jpg)
![](/constante_tiempo.jpg)

>🔑En las anteriores imagenes podemos ver como es el comportamiento del sistema aplicandole un escalon y en que punto se comienza a estabilizar, segun algunos libros y convenciones la estabilizacion de sistema comienza en 4tau donde ya se ha obtenido un 98.2% de la respuesta

### ubicacion de polos 

$$ G(s)= \frac{K}{\tau s+1}  $$

![](/ubicacion_polos.jpg)

>🔑 Entre mas lejos este el polo del origen es mas rapido


## Respuesta a la rampa unitaria 

$$ $$ Y(s) = \frac{AK}{s^{2}(\tau s+1)} $$ $$

Al desarrollar fracciones parciales 

$$ Y(s)= AK(\frac{1}{s^{2}}-\frac{1 \tau}{s}+\frac{\tau^{2}}{\tau s +1}) $$

$$ L^{-1}{ Y(s) } = y(t)= AK(t-\tau +\tau e^{-\frac{t}{\tau}}) $$

![](/respuesta_rampa.jpg)
![](/analisis_dinamico.jpg)

>🔑 AK = pendiente que tendra la rampa

# Ejercicios 

### 📚 1 Ejercicio

$$ \frac{Y(s)}{U(s)} = \frac{5}{2s+10} $$

$$ \frac{Y(s)}{U(s)} = \frac{5}{2s+10} = \frac{\frac{5}{10}}{\frac{2s}{10}+\frac{10}{10}}= \frac{0.5}{0.2s+1}$$

$$ \tau= 0.2 $$
$$ K= 0.5 $$

### 📚 2 Ejercicio

$$ \frac{Y(s)}{U(s)} = \frac{1.5}{0.5s+3} $$
$$ \frac{Y(s)}{U(s)} = \frac{1.5}{0.5s+3} = \frac{\frac{1.5}{3}}{\frac{0.5s}{3}+\frac{3}{3}}= \frac{0.5}{0.1667s+1}$$

$$ \tau = 0.1667 $$
$$ K = 0.5 $$









# Sistemas de Segundo orden

## Ecuaciones diferenciales de Segundo orden 

La estructura general de una ecuación de segundo orden es:
$$y'(t)+a_{1}y'(t)+a_{0}y(t)=b_{0}u(t)$$

Hallando la función de transferencia tenemos:

Aplicando transformada de LaPlace:

$$s^2 Y(s)   a_1 s Y(s)   a_0 Y(s) = b_0 U(s)$$

Despejando salida / Entrada

$$\frac{Y(s)}{U(s)} = \frac{b_0}{s^2   a_1 s   a_0}$$

# Forma canónica de los sistemas de segundo orden

$$\frac{Y(s)}{U(s)} = \frac{b_0}{s^2   a_1 s   a_0}$$

Esta forma no permite identificar directamente los parámetros temporales del sistema

Para esto en control se prefiere la forma canónica

La forma canónica considera lo siguiente:

$$𝑎1 = 2𝜁𝜔𝑛 𝑎0 = 𝜔𝑛2 𝑦 𝑏0 = 𝐾 ∗ 𝜔𝑛2$$

### Por lo tanto:

![ecuacion](/ecuacion2.jpg)


# Respuesta de un Sistema de Segundo ordena un escalón

- Factorizando:

  $$G(s) = \frac{K \cdot \omega_n^2}{(s   \zeta \omega_n   \omega_n \sqrt{\zeta^2 - 1})(s   \zeta \omega_n - \omega_n \sqrt{\zeta^2 - 1})}$$

  Aplicando escalon:

  $$Y(s) = \frac{K \cdot \omega_n^2 \cdot A}{(s   \zeta \omega_n   \omega_n \sqrt{\zeta^2 - 1})(s   \zeta \omega_n - \omega_n \sqrt{\zeta^2 - 1}) \cdot s}$$

  - Si \zeta = 1

    ![escalon](/escalon1.jpg)

  - Si \zeta >  1
    
    ![escalon](/escalon2.jpg)
    
