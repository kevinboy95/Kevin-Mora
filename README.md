import pandas as pd
import matplotlib.pyplot as plt

def calcular_distribucion(pregunta):
    frecuencias = encuestados[pregunta].value_counts().sort_index()
    return frecuencias

def calcular_medidas_distribucion(pregunta):
    medidas = {
        "Media": encuestados[pregunta].mean(),
        "Mediana": encuestados[pregunta].median(),
        "Moda": encuestados[pregunta].mode()[0],
        "Varianza": encuestados[pregunta].var(),
        "Desviación Estándar": encuestados[pregunta].std(),
        "Rango": encuestados[pregunta].max() - encuestados[pregunta].min()
    }
    return medidas

# Calcular la distribución de frecuencias y medidas de distribución para Pregunta 1
pregunta_1 = "Pregunta 1"
distribucion_pregunta_1 = calcular_distribucion(pregunta_1)
medidas_pregunta_1 = calcular_medidas_distribucion(pregunta_1)

# Crear un gráfico de barras apiladas
labels = distribucion_pregunta_1.index
data = [encuestados[encuestados[pregunta_1] == label][pregunta_1].count() for label in labels]

plt.bar(labels, data, label="Frecuencia", color='green')
plt.xlabel("Numero de respuestas")
plt.ylabel("Número de personas")
plt.title(f"Distribución de respuestas - {pregunta_1}")
plt.legend()
plt.show()

# Mostrar medidas de distribución para Pregunta 1
print(f"Medidas de distribución para {pregunta_1}:")
print(medidas_pregunta_1)
print("\n")

# Calcular la distribución de frecuencias y medidas de distribución para Pregunta 2
pregunta_2 = "Pregunta 2"
distribucion_pregunta_2 = calcular_distribucion(pregunta_2)
medidas_pregunta_2 = calcular_medidas_distribucion(pregunta_2)

# Crear un gráfico de barras apiladas
labels = distribucion_pregunta_2.index
data = [encuestados[encuestados[pregunta_2] == label][pregunta_2].count() for label in labels]

plt.bar(labels, data, label="Frecuencia", color='blue')
plt.xlabel("Numero de respuestas")
plt.ylabel("Número de personas")
plt.title(f"Distribución de respuestas - {pregunta_2}")
plt.legend()
plt.show()

# Mostrar medidas de distribución para Pregunta 2
print(f"Medidas de distribución para {pregunta_2}:")
print(medidas_pregunta_2)
print("\n")

# Calcular la distribución de frecuencias y medidas de distribución para Pregunta 3
pregunta_3 = "Pregunta 3"
distribucion_pregunta_3 = calcular_distribucion(pregunta_3)
medidas_pregunta_3 = calcular_medidas_distribucion(pregunta_3)

# Crear un gráfico de barras apiladas
labels = distribucion_pregunta_3.index
data = [encuestados[encuestados[pregunta_3] == label][pregunta_3].count() for label in labels]

plt.bar(labels, data, label="Frecuencia", color='purple')
plt.xlabel("Numero de respuestas")
plt.ylabel("Número de personas")
plt.title(f"Distribución de respuestas - {pregunta_3}")
plt.legend()
plt.show()

# Mostrar medidas de distribución para Pregunta 3
print(f"Medidas de distribución para {pregunta_3}:")
print(medidas_pregunta_3)
print("\n")

# Calcular la distribución de frecuencias y medidas de distribución para Pregunta 4
pregunta_4 = "Pregunta 4"
distribucion_pregunta_4 = calcular_distribucion(pregunta_4)
medidas_pregunta_4 = calcular_medidas_distribucion(pregunta_4)

# Crear un gráfico de barras apiladas
labels = distribucion_pregunta_4.index
data = [encuestados[encuestados[pregunta_4] == label][pregunta_4].count() for label in labels]

plt.bar(labels, data, label="Frecuencia", color='brown')
plt.xlabel("Numero de respuestas")
plt.ylabel("Número de personas")
plt.title(f"Distribución de respuestas - {pregunta_4}")
plt.legend()
plt.show()

# Mostrar medidas de distribución para Pregunta 4
print(f"Medidas de distribución para {pregunta_4}:")
print(medidas_pregunta_4)
print("\n")

# Calcular la distribución de frecuencias y medidas de distribución para Pregunta 5
pregunta_5 = "Pregunta 5"
distribucion_pregunta_5 = calcular_distribucion(pregunta_5)
medidas_pregunta_5 = calcular_medidas_distribucion(pregunta_5)

# Crear un gráfico de barras apiladas
labels = distribucion_pregunta_5.index
data = [encuestados[encuestados[pregunta_5] == label][pregunta_5].count() for label in labels]

plt.bar(labels, data, label="Frecuencia", color='orange')
plt.xlabel("Numero de respuestas")
plt.ylabel("Número de personas")
plt.title(f"Distribución de respuestas - {pregunta_5}")
plt.legend()
plt.show()

# Mostrar medidas de distribución para Pregunta 5
print(f"Medidas de distribución para {pregunta_5}:")
print(medidas_pregunta_5)
print("\n")

# Calcular la tasa de respuestas afirmativas para la Pregunta 3
respuestas_afirmativas = encuestados[pregunta_3].eq("Sí").sum()
tasa_afirmativa = respuestas_afirmativas / total_encuestas * 10

print(f"Tasa de respuestas afirmativas para la {pregunta_3}: {tasa_afirmativa:.3}")
