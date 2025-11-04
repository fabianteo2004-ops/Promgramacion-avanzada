# Programacion avanzada
Este repositorio pertenece a Fabian Teodor de Ingeniería Telemática

Las preguntas que le hice a google gemini en esta practica fueron:
-¿Qué comando de NumPy uso para crear una matriz de ceros?
    Debes usar la función numpy.zeros(). Asegúrate de pasar la tupla con las dimensiones (nFilas, nColumnas) y especificar el tipo de dato como dtype=float para cumplir con los requisitos.
-¿Cómo verifico en el método Existe() si la matriz ya fue inicializada?
    Puedes comprobar si el atributo self.Matriz es None. La condición sería: return self.Matriz is not None and self._m_nFilas > 0.
-Al sumar o restar, ¿cómo compruebo que las dimensiones son iguales?
    Compara directamente los atributos de dimensión de ambos objetos. El if de validación sería: if self._m_nFilas != otra_matriz._m_nFilas or self._m_nColumnas != otra_matriz._m_nColumnas:
-¿Cómo garantizo que las funciones leer_int y leer_float manejen errores?
    Implementa un bucle while True con un bloque try...except ValueError. Si el intento de conversión (int() o float()) falla, el except captura el error, imprime un mensaje y el bucle repite la solicitud.
-En Introducir, ¿cómo recorro la matriz para pedir los datos?
    Necesitas dos bucles for anidados: uno para las filas (range(self._m_nFilas)) y otro para las columnas (range(self._m_nColumnas)). Usa la indexación de NumPy self.Matriz[i, j] = valor.
-¿Cómo puedo hacer que la entrada de datos en Introducir() funcione para matrices 1D y 2D sin cambiar el código?
    Usa el acceso indexado de NumPy para ambos casos. NumPy trata los vectores (1D) como matrices 1×N. El bucle anidado for i in range(self._m_nFilas): for j in range(self._m_nColumnas): funcionará automáticamente: si hay 1 fila, el bucle i solo se ejecuta una vez, y el bucle j cubre todos los elementos.
Son las preguntas que le hice a chatgpt de forma resumida
