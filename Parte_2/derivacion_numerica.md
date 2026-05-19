Parte 2: Derivación numérica por diferencias centradas
Para evaluar la dinámica del biosensor, utilizamos la fórmula de diferencias finitas centradas de primer orden. 
Esta aproximación tiene un error de truncamiento del orden de O(h²), lo que la hace más precisa que las diferencias 
hacia adelante o hacia atrás.
La fórmula que utilizaremos es:

V'(t) ≈ [ V(t+h) - V(t-h) ] / 2h
