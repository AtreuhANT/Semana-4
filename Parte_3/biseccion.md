Parte 3: Búsqueda de raíces por bisección

1. Identificación de los cruces por cero
Un cruce por cero en un circuito electrónico de decisión ocurre cuando la señal de voltaje cambia de signo (es decir, la raíz de la función). Observando la tabla de calibración, esto sucede en dos intervalos distintos:

Primer cruce: Entre t = 7.0 ms (V = 0.1672 V) y t = 7.5 ms (V = -0.0186 V).

Segundo cruce: Entre t = 10.0 ms (V = -0.2100 V) y t = 10.5 ms (V = 0.0483 V).

2. Aplicación del método de bisección (Primer cruce)

Trabajaremos con el intervalo de la primera raíz: [7.0, 7.5].

Para evaluar el voltaje en los puntos medios con la máxima precisión requerida en ingeniería, nos apoyamos en la función del Spline Cúbico Natural que modela la señal (calculada en la Parte 1).

Iteración 1:

Límites iniciales: a = 7.0, b = 7.5

Cálculo del punto medio:

$$c_1 = \frac{7.0 + 7.5}{2} = 7.25\text{ ms}$$

Al evaluar la función de voltaje en este punto (V(7.25)), el resultado es positivo (aproximadamente 0.076 V según el spline).

Como V(7.0) es positivo y V(7.5) es negativo, el cambio de signo se concentra ahora entre 7.25 y 7.5.

Nuevo intervalo: [7.25, 7.5]

Iteración 2:

Nuevos límites: a = 7.25, b = 7.5

Cálculo del nuevo punto medio:$$c_2 = \frac{7.25 + 7.5}{2} = 7.375\text{ ms}$$

Al evaluar V(7.375), el voltaje sigue siendo positivo antes de caer por debajo de cero en 7.5.

Intervalo reducido reportado: [7.375, 7.5]

3. Estimación de la raíz con tolerancia
  
   Para garantizar que el error de estimación del tiempo de activación del circuito sea menor a 0.001 ms (tolerancia de 10^-3), podemos calcular teóricamente el número de iteraciones necesarias "n" con la fórmula del error máximo de bisección:

   $$n \ge \frac{\ln(b - a) - \ln(\text{tolerancia})}{\ln(2)}$$

   $$n \ge \frac{\ln(0.5) - \ln(0.001)}{\ln(2)} \approx 8.96$$

   Esto significa que el algoritmo requiere al menos 9 iteraciones para alcanzar la precisión solicitada de 10^-3 ms.
