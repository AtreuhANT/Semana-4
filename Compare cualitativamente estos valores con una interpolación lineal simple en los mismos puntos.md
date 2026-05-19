3. Comparación Cualitativa de los Métodos
   
Al comparar los resultados de la interpolación lineal simple con el comportamiento del spline cúbico 
natural, podemos concluir lo siguiente desde la perspectiva del análisis de circuitos y procesamiento de señales: 

Falta de dinámica en la interpolación lineal: 

El método lineal asume que la tasa de cambio de voltaje entre dos puntos de muestreo (cada 0.5 ms)
es perfectamente constante. Esto genera "esquinas" o picos artificiales en la señal ($C^0$ continuidad). Desde el punto de vista eléctrico, esto implicaría 
que la corriente en el sensor piezoeléctrico cambia de forma instantánea de un valor a otro, lo cual es físicamente irrealizable debido a las capacitancias 
parásitas e inercias mecánicas del tejido biológico.  

Representación física fidedigna en el spline: 

El spline cúbico natural fuerza a que la señal, su primera
derivada (tasa de cambio) y su segunda derivada sean continuas a lo largo de todo el espectro temporal. Dado que el voltaje proviene de la deformación 
mecánica de un tejido biológico impulsado por el flujo sanguíneo y la actividad muscular, las transiciones físicas deben ser suaves. El spline capturará de 
manera mucho más precisa la aceleración y desaceleración real de la micro vibración en $t=4.3$ y $t=8.7$ ms , absorbiendo las curvaturas sutiles que la 
recta pasa por alto.
