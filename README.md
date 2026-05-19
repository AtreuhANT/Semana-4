# Semana-8

1 

Interpolación Lineal Simple (Para comparación)

Antes de construir el spline, calcularemos los valores mediante interpolación lineal simple para tener una base de comparación. La ecuación de la recta entre dos puntos 
$(t_0, V_0)$ y $(t_1, V_1)$ es:

$$V_L(t) = V_0 + \frac{V_1 - V_0}{t_1 - t_0}(t - t_0)$$

Cálculo para $t = 4.3$ ms:

Los datos más cercanos de la tabla: $(4.0, 1.3011)$ y $(4.5, 1.2574)$.

  $$V_L(4.3) = 1.3011 + \frac{1.2574 - 1.3011}{4.5 - 4.0}(4.3 - 4.0)$$
  
  $$V_L(4.3) = 1.3011 + \frac{-0.0437}{0.5}(0.3) = 1.3011 - 0.02622 = 1.27488$$
  
  Cálculo para $t = 8.7$ ms:
  
Usamos los puntos: $(8.5, -0.3142)$ y $(9.0, -0.3148)$.

  $$V_L(8.7) = -0.3142 + \frac{-0.3148 - (-0.3142)}{9.0 - 8.5}(8.7 - 8.5)$$
  
  $$V_L(8.7) = -0.3142 + \frac{-0.0006}{0.5}(0.2) = -0.3142 - 0.00024 = -0.31444$$
