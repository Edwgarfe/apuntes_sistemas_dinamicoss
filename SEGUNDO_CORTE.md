# 1 CLASE
# Principio general de modelamiento

**Tasa de acumulación**  
*Masa o Energía*  
=  
**Flujo de**  
*Masa o Energía*  
**Entrada – Flujo de**  
*Masa o Energía*  
**Salida**

# Sistemas masa-resorte-amortiguador

**Fenómeno físico que modela el sistema:**

- **Fₑ = k₂ × x**  → *Ley de Hooke* (resorte derecho)
- **Fₐ = k₁ × vₘ**  → *Fricción viscosa* (amortiguador izquierdo)
- **F = m × a**     → *Leyes de Newton*

# Sistemas masa-resorte-amortiguador

## Diagrama de cuerpo libre

## Ecuaciones del sistema masa-resorte-amortiguador

u - F_R - F_F = m * a

F_R = k₂ * y(t)

u(t) - k₂ * y(t) - F_F = m * a

F_F = k₁ * dy(t)/dt

u(t) - k₂ * y(t) - k₁ * dy(t)/dt = m * a

a = d²y(t)/dt²

u(t) - k₂ * y(t) - k₁ * dy(t)/dt = m * d²y(t)/dt²

# Ejemplo
## Sistema masa-resorte-amortiguador (suspensión de automóvil)

Este sistema modela una suspensión de auto con dos masas:  
- `M`: masa de la carrocería (superior)  
- `m`: masa de la rueda (inferior)

Conectadas por resortes y amortiguadores:  
- `k₁`, `c₁`: suspensión (entre la carrocería y la rueda)  
- `k₂`, `c₂`: neumático (entre la rueda y el suelo)  

## Variables:
- `y(t)`: desplazamiento vertical de la carrocería  
- `x(t)`: desplazamiento vertical de la rueda  
- `r(t)`: desplazamiento del terreno (entrada del sistema)

---

## Ecuaciones

```text
1.  M * d²y(t)/dt² = -k₁ * (y(t) - x(t)) - c₁ * (dy(t)/dt - dx(t)/dt)

2.  m * d²x(t)/dt² =  k₁ * (y(t) - x(t)) + c₁ * (dy(t)/dt - dx(t)/dt)
                     - k₂ * (x(t) - r(t)) - c₂ * (dx(t)/dt - dr(t)/dt)






































































































# 2 CLASE














































































# 3 CLASE

