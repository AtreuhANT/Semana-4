Código en Python para obtener la raíz exacta (Parte 3):


    def biseccion_spline(a, b, tol):
    # Verificamos que exista un cambio de signo en el intervalo
    if evaluar_spline(a) * evaluar_spline(b) >= 0:
        return None
    
    iteracion = 1
    # Ejecutamos el bucle hasta que el tamaño del intervalo sea menor a la tolerancia
    while (b - a) / 2.0 > tol:
        c = (a + b) / 2.0
        
        if evaluar_spline(c) == 0:
            break  # Encontramos la raíz exacta
        elif evaluar_spline(a) * evaluar_spline(c) < 0:
            b = c  # La raíz está en la mitad izquierda
        else:
            a = c  # La raíz está en la mitad derecha
            
        iteracion += 1
        
    raiz_estimada = (a + b) / 2.0
    return raiz_estimada, iteracion

    # Calculamos la raíz en el primer intervalo [7.0, 7.5] con tolerancia 1e-3 ms
    raiz, num_iters = biseccion_spline(7.0, 7.5, 0.001)

    print("\n--- Parte 3: Búsqueda de raíces ---")
    print(f"El circuito cambia de estado en t = {raiz:.4f} ms")
    print(f"Iteraciones computadas: {num_iters}")
