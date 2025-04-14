## Principio general de modelamiento

El **principio general de modelamiento** es una regla fundamental utilizada para describir sistemas físicos. Aplica tanto para **masa** como para **energía** (o cualquier otra cantidad conservativa como carga, cantidad de movimiento, etc.)
- **Tasa de acumulación**: Cambio en el tiempo de la cantidad dentro del sistema (puede ser masa, energía, etc.)
- **Flujo de entrada**: Lo que entra al sistema
- **Flujo de salida**: Lo que sale del sistema

Este principio se usa para modelar:

- Sistemas térmicos (balance de energía)
- Dinámica de fluidos (balance de masa)
- Circuitos eléctricos (balance de carga o energía)
- Sistemas mecánicos (balance de momento o cantidad de movimiento)
## Sistemas Mecanicos
# Resorte

El resorte es un elemento mecánico fundamental en sistemas físicos. Se utiliza para modelar fuerzas restauradoras que dependen del desplazamiento.

# Modelo de resorte lineal (Ley de Hooke)

\[
F = k \cdot x = k(x_1 - x_2)
\]

Donde:
- `F` es la fuerza ejercida por el resorte,
- `k` es la constante del resorte (rigidez),
- `x` es el desplazamiento desde la posición de equilibrio,
- `x₁`, `x₂` son las posiciones de los extremos del resorte
Se asumen **resortes lineales**, es decir, la **fuerza externa aplicada y el desplazamiento están relacionados por una constante de proporcionalidad** (`k`)

La gráfica muestra la relación fuerza vs. desplazamiento para diferentes tipos de resortes:

- **Resorte lineal**: relación lineal (recta)
- **Resorte duro**: la rigidez aumenta con el desplazamiento
- **Resorte suave**: la rigidez disminuye con el desplazamiento
# Amortiguador

Un **amortiguador** es un elemento mecánico que modela una fuerza proporcional a la **velocidad relativa** entre dos cuerpos. Este comportamiento es típico en sistemas donde se presenta fricción viscosa
# Modelo de fricción viscosa (Amortiguador lineal)

\[
F = b \cdot \dot{x} = b(\dot{x}_1 - \dot{x}_2)
\]

Donde:
- `F` es la fuerza generada por el amortiguador.
- `b` es la **constante de fricción viscosa**.
- \(\dot{x}_1\) y \(\dot{x}_2\) son las velocidades de los extremos del amortiguador
# Comportamiento del amortiguador

- Es un **comportamiento lineal**.
- La fuerza disipa energía cinética.
- Se utiliza comúnmente para representar la **fricción entre una masa y una superficie**, o en sistemas de suspensión
## Tipos de fricción
## Fricción en seco

### Diagrama de fuerzas

En la imagen se muestra un bloque sobre una superficie plana, donde se ilustran las fuerzas involucradas en la fricción en seco:
- **mg**: peso del objeto (fuerza gravitacional)
- **N**: fuerza normal (perpendicular a la superficie)
- **F**: fuerza de fricción (se opone al movimiento)
- **Fuerza de tracción**: fuerza que intenta mover el objeto

También se muestra una gráfica que relaciona la fuerza de fricción con la velocidad:

- En reposo, la fricción es **estática**, que aumenta hasta un valor máximo.
- Una vez iniciado el movimiento, la fricción se convierte en **deslizante** (o cinética), que es menor y casi constante

Esto refleja que:
- La **fricción estática** impide que el cuerpo se mueva hasta que se supera su límite
- Al comenzar el movimiento, la **fricción deslizante** toma el control
### Fricción en seco
- Es aquella que se presenta cuando un cuerpo con una superficie no lubricada se desliza sobre otra superficie no lubricada.
  - **Fricción estática**
  - **Fricción por deslizamiento**
  - **Fricción por rodamiento**
  - 
## Fricción por rodamiento

La **fricción por rodamiento** ocurre cuando un cuerpo (como una rueda o cilindro) rueda sobre una superficie en lugar de deslizarse. Este tipo de fricción es mucho menor que la fricción por deslizamiento

- **mg**: peso del cuerpo (fuerza hacia abajo debido a la gravedad).
- **N**: fuerza normal ejercida por la superficie.
- **P**: fuerza aplicada para mover el cuerpo.
- **T₁ y T₂**: fuerzas de contacto en los extremos del área de contacto.
- **r**: radio del cuerpo que rueda.
- **h**: altura a la que se aplica la fuerza **P**.
## Sistemas masa-resorte-amortiguador
1. u - FR - FF = m * a
    Segunda Ley de Newton: la suma de fuerzas es igual a masa por aceleración.

2. FR = k2 * y(t)
    Fuerza del resorte (Ley de Hooke): proporcional al desplazamiento.

3. FF = k1 * dy(t)/dt
    Fuerza del amortiguador (fricción viscosa): proporcional a la velocidad.

4. u(t) - k2 * y(t) - FF = m * a
    Sustituyendo FR en la ecuación de Newton.

5. u(t) - k2 * y(t) - k1 * dy(t)/dt = m * a
    Sustituyendo FF también: ecuación dinámica completa.

6. a = d²y(t)/dt²
    Definición de aceleración como segunda derivada del desplazamiento.

7. u(t) - k2 * y(t) - k1 * dy(t)/dt = m * d²y(t)/dt²
    Forma final de la ecuación diferencial del sistema.
   
## Ejemplo:
Encontrar el modelo matemático que describe el sistema masa-resorte-amortiguador representado por la suspensión de un automóvil.

El sistema está compuesto por:
- Una masa `m` (la carrocería del automóvil).
- Un resorte de rigidez `k₂`.
- Un amortiguador de coeficiente `k₁`.
- Una entrada `u(t)` correspondiente al desplazamiento vertical del terreno o rueda.
- Una salida `y(t)` correspondiente al desplazamiento de la carrocería.

### Supuestos:
- Movimiento unidimensional (vertical)
- Comportamiento lineal de resortes y amortiguadores
- El resorte y amortiguador están conectados entre la masa y el terreno

Fuerza total sobre la masa:
m * d²y(t)/dt² = -k₂ * (y(t) - u(t)) - k₁ * (dy(t)/dt - du(t)/dt)
m * y''(t) + k₁ * (y'(t) - u'(t)) + k₂ * (y(t) - u(t)) = 0

 Donde:
 - `y''(t)` es la aceleración de la masa
 - `y'(t)` es la velocidad de la masa
 - `u(t)` es la entrada del sistema (irregularidad del terreno)
 - `k₁`, `k₂` son constantes positivas
 - Este modelo describe una suspensión pasiva
## Ejemplo 1: Control de temperatura de un horno
Modelar el comportamiento térmico de un horno eléctrico regulado por un termostato

## Supuestos:
- La temperatura interna del horno es `T(t)`.
- La entrada de calor está dada por la señal de control `u(t)`.
- Existe pérdida de calor hacia el ambiente a temperatura `T_amb`.

## Modelo:

Por el principio general de modelamiento (balance de energía):
C * dT(t)/dt = -k * (T(t) - T_amb) + u(t)

## Variables:
- `C`: Capacidad térmica del horno.
- `k`: Coeficiente de pérdida térmica.
- `u(t)`: Potencia de calefacción suministrada.
- `T(t)`: Temperatura interna del horno.
- `T_amb`: Temperatura ambiente (constante).

## Interpretación:
- El modelo describe cómo cambia la temperatura del horno en función de la energía suministrada y las pérdidas.
- Se puede usar para diseñar un controlador (ej. PID) que mantenga la temperatura deseada
## Ejemplo 2: Sistema masa-resorte-amortiguador vertical
Modelar el movimiento vertical de una masa suspendida por un resorte y amortiguador.

## Descripción:
- Una masa `m` cuelga de un resorte con constante `k` y amortiguador de constante `b`.
- La posición vertical de la masa es `y(t)` (medida hacia abajo desde la posición de equilibrio).
- Se considera la gravedad.

### Modelo dinámico (con fuerza neta):
m * d²y(t)/dt² = -k * y(t) - b * dy(t)/dt + m * g
m * y''(t) + b * y'(t) + k * y(t) = 0

# Sistemas Acoplados
# Ejemplos de Modelado Dinámico de Sistemas Físicos

##  Ejemplo 1: Control de temperatura de un horno

Modelar el comportamiento térmico de un horno eléctrico regulado por un termostato.

### Supuestos:
- La temperatura interna del horno es `T(t)`.
- La entrada de calor está dada por la señal de control `u(t)`.
- Existe pérdida de calor hacia el ambiente a temperatura `T_amb`.

### Modelo:

Por balance de energía:

```
C * dT(t)/dt = -k * (T(t) - T_amb) + u(t)
```

### Variables:
- `C`: Capacidad térmica del horno.
- `k`: Coeficiente de pérdida térmica.
- `u(t)`: Potencia de calefacción suministrada.
- `T(t)`: Temperatura interna del horno.
- `T_amb`: Temperatura ambiente (constante).

### Interpretación:
- El modelo describe cómo varía la temperatura interna en función del calor suministrado y las pérdidas.
- Se puede usar para diseñar un controlador (ej. PID) que mantenga la temperatura deseada.

---

## Ejemplo 2: Sistema masa-resorte-amortiguador vertical

Modelar el movimiento vertical de una masa suspendida por un resorte y un amortiguador.

### Descripción:
- Una masa `m` cuelga de un resorte con constante `k` y amortiguador de constante `b`.
- La posición vertical de la masa es `y(t)` (medida hacia abajo desde el equilibrio).
- Se considera el efecto de la gravedad.

### Modelo dinámico (segunda ley de Newton):

```
m * y''(t) + b * y'(t) + k * y(t) = 0
```

Donde:
- `y''(t)`: Aceleración de la masa.
- `y'(t)`: Velocidad de la masa.
- `y(t)`: Desplazamiento desde el equilibrio.

Este sistema se puede resolver numéricamente para simular su comportamiento o diseñar un sistema de control.

---

## Sistemas Acoplados
## Para la masa 1:
u - FR1 - FR2 - FF = m1 * a_m1
- La distancia de elongación del resorte 2 depende del movimiento de ambas masas.
- La velocidad del émbolo del amortiguador del resorte 2 depende del movimiento de ambas masas
u(t) - k1 * x1(t) - k2 * (x1(t) - x2(t)) - b * d/dt[x1(t) - x2(t)] = m1 * d²x1(t)/dt²

### Para la masa 2:
- La distancia de elongación del resorte 2 depende del movimiento de ambas masas.
- La velocidad del émbolo del amortiguador del resorte 2 depende del movimiento de ambas masas

k2 * (x1(t) - x2(t)) + b * d/dt[x1(t) - x2(t)] - k3 * x2(t) = m2 * d²x2(t)/dt²


## Modelo resultante (sistema acoplado completo)

u(t) - k1 * x1(t) - k2 * (x1(t) - x2(t)) - b * d/dt[x1(t) - x2(t)] = m1 * d²x1(t)/dt²

k2 * (x1(t) - x2(t)) + b * d/dt[x1(t) - x2(t)] - k3 * x2(t) = m2 * d²x2(t)/dt²

## Ejemplo

### Para la masa `m1`:
m1 * d²x1(t)/dt² = -k1 * x1(t) - b * dx1(t)/dt + k2 * (x2(t) - x1(t))
### Para la masa `m2`:
m2 * d²x2(t)/dt² = -k2 * (x2(t) - x1(t))
## Variables:
- `m1`, `m2`: masas.
- `k1`, `k2`: constantes de los resortes.
- `b`: constante del amortiguador.
- `x1(t)`, `x2(t)`: posiciones respecto al equilibrio.
- `dx1(t)/dt`, `dx2(t)/dt`: velocidades.
- `d²x1(t)/dt²`, `d²x2(t)/dt²`: aceleraciones.
# Ejemplo 1: Sistema de tanque con entrada y salida de fluido
- Un tanque tiene una entrada de flujo de agua `q_in(t)` y una salida proporcional a la altura del fluido.
- La altura del agua en el tanque es `h(t)`.
- La salida se modela como `q_out(t) = k * h(t)` donde `k` es una constante relacionada con el orificio de salida
A * dh(t)/dt = q_in(t) - k * h(t)
## Variables

- `A`: Área de la sección transversal del tanque.
- `h(t)`: Altura del agua en el tanque.
- `q_in(t)`: Flujo de entrada (puede ser constante o variable).
- `k`: Constante de flujo de salida.
- `q_out(t) = k * h(t)`: Flujo de salida

# Ejemplo 2: Péndulo simple
- Una masa `m` está colgada de un hilo de longitud `L`.
- La posición angular respecto a la vertical es `θ(t)`.
- Solo actúa la gravedad (no hay fricción ni resistencia del aire).
**Ecuación del movimiento (no lineal):**
m * L * d²θ(t)/dt² + m * g * sin(θ(t)) = 0
**Aproximación lineal (para pequeños ángulos):**
d²θ(t)/dt² + (g / L) * θ(t) = 0
## Variables

- `m`: Masa del cuerpo.
- `L`: Longitud del hilo.
- `g`: Aceleración de la gravedad.
- `θ(t)`: Ángulo con respecto a la vertical.
## Ejemplo 3: Sistema Rotacional con Torsión

Modelar un sistema rotacional que involucra un resorte de torsión y un amortiguador.

- `φ`: Ángulo de torsión (análogo al desplazamiento lineal).
- `dφ/dt`: Velocidad angular.
- `d²φ/dt²`: Aceleración angular.
- `J`: Momento de inercia (análogo a la masa).
- `T(t)`: Torque aplicado (análogo a la fuerza).
- `k`: Constante de torsión (análogo al resorte lineal).
- `b`: Coeficiente de fricción rotacional (análogo al amortiguador)

- Torque del resorte:  
  `F_R = k * φ`

- Torque del amortiguador:  
  `F_F = b * dφ/dt`

- Torque total aplicado:  
  `T = J * d²φ/dt²`

## Ejemplo: 
Desarrollar un modelo para describir la posición angular `θ(t)` de un sistema rotacional con eje rígido.

- `θ(t)`: Posición angular del eje (variable dependiente).
- `T(t)`: Torque aplicado (entrada).
- `J`: Momento de inercia del eje.
- `b`: Coeficiente de fricción rotacional.
  
T(t) - b * dθ(t)/dt = J * d²θ(t)/dt²
J * θ''(t) + b * θ'(t) = T(t)

## Ejemplo 1: Péndulo simple
Modelar el comportamiento dinámico de un péndulo simple oscilando sin fricción
- La masa se concentra en una esfera de masa `m`.
- La varilla es rígida, de longitud `L` y sin masa.
- No hay fricción (movimiento conservativo).
- El movimiento es angular, en un plano

### Variables:
- `θ(t)`: Ángulo medido desde la vertical (rad).
- `g`: Aceleración gravitacional.
- `L`: Longitud de la varilla.
- `m`: Masa puntual al final de la varilla.

### Modelo dinámico:

Aplicando las leyes del movimiento rotacional:
J * d²θ(t)/dt² + m * g * L * sin(θ(t)) = 0
Donde el momento de inercia del péndulo respecto al punto de suspensión es:
J = m * L²
Sustituyendo:
m * L² * d²θ(t)/dt² + m * g * L * sin(θ(t)) = 0
Dividiendo todo entre `m * L`:
L * d²θ(t)/dt² + g * sin(θ(t)) = 0
Cuando `θ(t)` es pequeño, `sin(θ) ≈ θ`:
d²θ(t)/dt² + (g / L) * θ(t) = 0

## Ejemplo 2: Sistema masa-resorte horizontal sin fricción

Modelar el movimiento de una masa unida a un resorte horizontal sobre una superficie sin fricción.
### Variables:
- `x(t)`: Desplazamiento de la masa desde su posición de equilibrio.
- `k`: Constante del resorte.
- `m`: Masa del objeto.

### Modelo dinámico:

Por la segunda ley de Newton:
F_resorte = -k * x(t) m * d²x(t)/dt² = -k * x(t)
O escrito como:
d²x(t)/dt² + (k / m) * x(t) = 0
La solución es una función seno/coseno:
x(t) = A * cos(ωt) + B * sin(ωt)
Donde `ω = sqrt(k/m)` es la frecuencia angular del sistema

## Definiciones

### Trabajo:
Es una medida de la realización del esfuerzo (fuerza).

\[ W = F \cdot x \quad \text{[N·m]} \]

Trabajo total realizado:
\[ \int_{0}^{x} kx \, dx = \frac{1}{2} kx^2 \]

• Energía: Capacidad para realizar trabajo.
Tipos de energía:
- Energía potencial
- Energía cinética

## Energía potencial

- En los sistemas mecánicos la energía potencial cambia de acuerdo a su posición (con respecto a una referencia).
- En los sistemas mecánicos los resortes y las masas almacenan energía potencial.
- La energía potencial es equivalente al trabajo realizado por la fuerza externa.

\[ U = \int_{x_0}^{x} mg \, dx = mgh \]

Donde:
- \( m \): masa
- \( g \): aceleración debida a la gravedad
- \( h \): altura desde una referencia
  
# Energía y Potencia en Sistemas Mecánicos

## Energía Cinética

- La energía cinética es debida a la velocidad.
- Solo los elementos de inercia pueden almacenar energía cinética.

$$
T = \frac{1}{2}mv^2 \quad \text{o} \quad T = \frac{1}{2}J\omega^2
$$

- El cambio en la energía cinética corresponde al trabajo realizado sobre una masa:

$$
\Delta T = \int_{t_1}^{t_2} \vec{F} \cdot \vec{v} \, dt = \frac{1}{2}mv_2^2 - \frac{1}{2}mv_1^2
$$

---

## Potencia

- La potencia es la realización de trabajo respecto al tiempo:

$$
P = \frac{dW}{dt}
$$

- Potencia media:

$$
\text{Potencia media} = \frac{\text{Trabajo realizado entre } (t_2 - t_1)}{t_2 - t_1}
$$

---

## Energía Potencial en un Resorte

- Trabajo neto hecho sobre el resorte cuando se comprime o estira:

$$
U = \int F \, dx = \int kx \, dx = \frac{1}{2}kx^2
$$

- Cambio general de energía:

$$
\Delta U = \frac{1}{2}kx_2^2 - \frac{1}{2}kx_1^2
$$

---

## Potencia en un Resorte

- Potencia requerida para estirar o comprimir un resorte:

$$
P = \frac{dW}{dt} = \frac{dF \cdot dx}{dt} = Fx = kx \cdot \dot{x}
$$

- Sabiendo que:

$$
\dot{U} = kx \cdot \dot{x}
$$

Entonces:

$$
P = \dot{U}
$$

---

## Potencia en una Masa

- Potencia para acelerar una masa en línea recta:

$$
P = \frac{dW}{dt} = F \cdot \dot{x} = m\ddot{x} \cdot \dot{x}
$$

- Sabiendo que:

$$
T = \frac{1}{2}m\dot{x}^2
$$

Entonces:

$$
P = \dot{T}
$$

---

## Energía Disipada en un Amortiguador

- Energía disipada corresponde al trabajo realizado por la fuerza de fricción viscosa:

$$
\Delta W = \int F \, dx = \int b\dot{x} \, dx = \int b\dot{x}^2 \, dt
$$

- **No importa el signo de la velocidad**, siempre se disipa energía.

---

## Potencia Disipada en Amortiguador

- Potencia disipada por fricción:

$$
P = F \cdot \dot{x} = b\dot{x} \cdot \dot{x} = b\dot{x}^2
$$

---
# Modelamiento de sistemas eléctricos

Los componentes fundamentales de los circuitos eléctricos, específicamente los sistemas RLC. Estos sistemas están compuestos por resistores, inductores y capacitores, que interactúan de acuerdo con las leyes de Kirchhoff. Veremos cómo modelar y analizar estos circuitos mediante ecuaciones diferenciales.

## 1. Circuitos RLC
El circuito RLC es un sistema compuesto por resistores, inductores y capacitores que se conectan de diversas maneras, permitiendo modelar fenómenos físicos como los osciladores eléctricos. La ley de Kirchhoff nos ayuda a analizar el comportamiento de estos circuitos.

 Definición: El circuito RLC es un tipo de circuito eléctrico que incluye un resistor (R), un inductor (L) y un capacitor (C) conectados en diversas configuraciones para analizar fenómenos de oscilación y energía en sistemas eléctricos.
## 1.1. Ley de Kirchhoff y la Ley de Ohm
Aplicamos la ley de Kirchhoff para los circuitos RLC, lo que nos permite escribir las ecuaciones diferenciales que modelan el comportamiento de la corriente y el voltaje en el sistema.
$$R=\frac{v(T)}{i(T)}$$
Ley de Ohm

## 2. Ecuaciones:
Corriente a través de un condensador:   $$I(T)= C \frac{DV(T)}{D T}$$

Voltaje a través de un inductor:  $V(T)=L\frac{DI(T)}{DT}$
## 3. Ejemplo de Análisis de un Circuito RLC
Veamos cómo se puede analizar un circuito RLC utilizando las ecuaciones derivadas de la ley de Kirchhoff.

Circuito de ejemplo:

Aplicando la ley de Kirchhoff de voltajes (LKT) al circuito que aparece en la figura, obtenemos una ecuación diferencial que describe la relación entre el voltaje y la corriente en el sistema:

Ecuación de Kirchhoff:  $U (T)+I(T)*R+L\frac{DI(T)}{DT}+C Y (T)=0$

## 4. Circuitos con Resistores Adicionales
En esta sección, analizaremos un circuito con dos resistores y un condensador. A continuación, se presenta el circuito:

 Definición: Un circuito compuesto por más de un resistor (como R1 y R2) y un condensador puede ser modelado usando las leyes de Kirchhoff para obtener la ecuación del sistema.
## 4.1. Aplicando Leyes de Kirchhoff (LKC)
Cuando tenemos resistores adicionales en el circuito, aplicamos la ley de Kirchhoff de corrientes para modelar el comportamiento del circuito:

$U (T)-2 \frac{DY(T)}{DT}-\frac{1}{0.5}Y(T)=0$

## 4. 4. Ejemplo: Aplicando Nodos
En este caso, utilizamos la ley de Kirchhoff de corrientes para aplicar el análisis de nodos en un circuito con diferentes componentes:

$U(T)-6\frac{DY(T)}{DT}-2Y(T)=0$

## 5. Ejercicios
 Ejercicio 1: Obtener el modelo para un circuito con resistores adicionales y un condensador.

Solución:
Utiliza las leyes de Kirchhoff para obtener la ecuación diferencial que describa el sistema. Aplica las ecuaciones obtenidas en la clase para resolver el sistema.

 Ejercicio 2:
Aplicar la ley de Kirchhoff para un circuito con dos resistores en serie y un condensador.

Solución:
Similar al ejercicio 1, pero con una configuración distinta de resistores.
## 6. Tablas y Figuras
Asegúrate de incluir tablas con los valores de los componentes (R1, R2, L, C) y cómo afectan al comportamiento del circuito.

![image](https://github.com/user-attachments/assets/1da26918-3653-42f3-abe3-adc0fe60e3dc)







