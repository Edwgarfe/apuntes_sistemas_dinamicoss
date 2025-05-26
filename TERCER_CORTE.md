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






