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
