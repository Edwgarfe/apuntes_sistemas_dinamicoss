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

$$ q_{i} = A_{1}R_{1}\frac{dq_{1}}{dt}+q_{1}




































































































































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
