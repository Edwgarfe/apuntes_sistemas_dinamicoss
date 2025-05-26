# Ecuaciones Difereciales Parcial

## Constantes 
$$ r_{A} = 15cm $$
$$ r_{B} = 9cm $$
$$ r_{C} = 8cm $$

$$ A_{A} = \pi r_{A}^{2} = \pi (15 cm)^{2} = 225 \pi cm^{2}  $$
$$ A_{B} = \pi r_{A}^{2} = \pi (9 cm)^{2} = 81 \pi cm^{2}  $$
$$ A_{C} = \pi r_{A}^{2} = \pi (8 cm)^{2} = 64 \pi cm^{2}  $$

$$ R_{1} = 2cm $$
$$ R_{2} = 3cm $$
$$ R_{3} = 1cm $$
$$ R_{4} = 1cm $$

$$ K_{p} = 4 $$


## Flujos de salida 

$$ q_{i} = K_{p} * q_{4} $$

$$ q_{1} = \frac{h_{A}-h_{1}}{R_{1}} = \frac{h_{A}-h_{1}}  {2} $$

$$ q_{2} = \frac{h_{A}-h_{B}}{R_{2}} = \frac{h_{A}-h_{B}}{3} $$

$$ q_{3} = \frac{h_{B}}{R_{3}} = \frac{h_{B}}{1} $$

$$ q_{4} = \frac{h_{C}}{R_{4}} = \frac{h_{C}}{1} $$

## Intercambios de energia

### 1 Ecuación
$$ A_{A} \frac{dh_{A}}{dt} = q_{i} - q_{1} - q_{2} $$
> sustituyendo y despejando quedaria
> 
$$ \frac{dh_{A}}{dt} = \frac{4*h_{c} - \frac{h_{A}-h_{1}}  {2} -\frac{h_{A}-h_{B}}{3}}{225} $$

### 2 Ecuación
$$ A_{B} \frac{dh_{B}}{dt} = q_{1} + q_{2} - q_{3} $$
> Sustituyendo y despejando quedaria:

$$ \frac{dh_{B}}{dt} =\frac{ \frac{h_{A}-h_{1}}{2} + \frac{h_{A}-h_{B}}{3} - \frac{h_{B}}{1}} {81} $$

### 3 Ecuación
$$ A_{C} \frac{dh_{C}}{dt} = q_{3} - q_{4} $$
> Sustituyendo y despejando quedaria:

$$ \frac{dh_{C}}{dt} = \frac{\frac{h_{B}}{1} - h_{C}} {64} $$
