Parte 2: Derivación numérica por diferencias centradas.

Para evaluar la dinámica del biosensor, utilizamos la fórmula de diferencias finitas centradas de 
primer orden. Esta aproximación tiene un error de truncamiento de $\mathcal{O}(h^2)$, lo que la hace más precisa que las diferencias hacia adelante o hacia atrás.

La fórmula es:

$$V'(t) \approx \frac{V(t+h) - V(t-h)}{2h}$$

Donde el paso temporal es $h = 0.5\text{ ms}$ según los datos de calibración de la tabla.
Cálculos Numéricos1. 
Para $t = 4.0\text{ ms}$:

Tomamos los valores en $t = 4.5\text{ ms}$ y $t = 3.5\text{ ms}$.

$$V'(4.0) \approx \frac{V(4.5) - V(3.5)}{2(0.5)}$$

$$V'(4.0) \approx \frac{1.2574 - 1.6583}{1.0}$$

$$V'(4.0) \approx -0.4009\text{ V/ms}$$

2. Para $t = 8.0\text{ ms}$:

     Tomamos los valores en $t = 8.5\text{ ms}$ y $t = 7.5\text{ ms}$.

$$V'(8.0) \approx \frac{V(8.5) - V(7.5)}{2(0.5)}$$

$$V'(8.0) \approx \frac{-0.3142 - (-0.0186)}{1.0}$$

$$V'(8.0) \approx -0.2956\text{ V/ms}$$

3. Para $t = 12.0\text{ ms}$:
   
Tomamos los valores en $t = 12.5\text{ ms}$ y $t = 11.5\text{ ms}$.

  $$V'(12.0) \approx \frac{V(12.5) - V(11.5)}{2(0.5)}$$
    
   $$V'(12.0) \approx \frac{0.8982 - 0.5185}{1.0}$$
    
   $$V'(12.0) \approx 0.3797\text{ V/ms}$$

Interpretación Física del Signo (Dinámica del Biosensor)

En un sensor piezoeléctrico, la carga generada (y por ende el voltaje en sus terminales) es directamente proporcional a la deformación mecánica aplicada por el tejido biológico. 

La derivada del voltaje respecto al tiempo, $\frac{dV}{dt}$, representa la velocidad de deformación del tejido y es proporcional a la corriente en el circuito equivalente.

Derivada Negativa (En $t = 4.0\text{ ms}$ y $t = 8.0\text{ ms}$):

  El valor negativo indica que el voltaje está disminuyendo. Mecánicamente, esto significa que la presión sobre el cristal piezoeléctrico se está relajando (el tejido muscular se expande o la onda de flujo sanguíneo ha pasado su pico máximo). 
  Eléctricamente, el sensor está descargando su capacitancia, indicando que la corriente fluye en sentido inverso hacia el módulo     de   procesamiento. 

Derivada Positiva (En $t = 12.0\text{ ms}$):

El valor positivo indica que el voltaje está aumentando. En términos biomecánicos, el tejido está aplicando una fuerza de compresión creciente sobre el sensor en ese instante. Eléctricamente, el sensor actúa como una fuente activa inyectando corriente hacia el circuito electrónico.
      
