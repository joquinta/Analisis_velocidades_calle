# ¿A qué velocidad pasan los autos por Avenida Andrés Bello?
Usé inteligencia artificial y visión por computador, con el objetivo de crear una solución rápida, escalable y basada en evidencia.

🎥 **Enfoque técnico**

El método planteado fue el siguiente:

Grabar un video desde el costado de la avenida.

Usar modelos como YOLO para reconocer vehículos en cada frame.

Medir el tiempo entre puntos de paso para estimar velocidades.


🔄 **Iteración con LLMs**

Me apoyé en LLMs avanzados:

🧠 GPT-4o

🧠 Claude 3.5 Sonnet

🧠 Gemini 1.5 + Flask local para pruebas

Les pedí sugerencias para adaptar el código y entendían la lógica, pero ninguno logró modificar internamente las funciones de YOLO de forma efectiva. 

💡 **Una solución más cercana**

En un foro encontré una idea interesante:

"No trates de estimar velocidad directamente con el modelo. Solo traza dos líneas y mide el tiempo que un objeto (vehículo) se demora en cruzar de una a la otra."

Sonaba simple, pero implementarlo implicaba:

  - Hacer tracking consistente de cada vehículo.

  - Medir frames entre los cruces.

  - Calibrar la distancia real entre líneas para convertir a km/h.

Probé este enfoque con los modelos anteriores, pero los resultados seguían siendo imprecisos.

🚀 **DeepSeek R1: el cambio de paradigma**

Finalmente probé con DeepSeek R1, un modelo de lenguaje open source creado en China que está sorprendiendo por su rendimiento (al nivel de GPT-4o) y un 98% más barato de utilizar.

🚴‍♂️ **Validación y resultados**

Para calibrar, pasé en bicicleta a velocidad conocida. Luego analicé una muestra de 115 vehículos (solo un sentido). Resultados:

Velocidad promedio: 32 km/h

Solo una moto superó los 60 km/h

El video fue grabado cerca de un semáforo y saliendo de una curva, por lo que en otras condiciones la velocidad podría ser mayor.

