# Análisis de Sentimientos

## Descripción:
Implementación de 2 modelos de Inteligencia Artificial (MVS &amp; MLP) para clasificar tweets relacionados al Covid-19 en 5 diferentes tipos de sentimientos.


## Tabla de Contenidos 
- [Datos](#datos)
- [Metodología](#metodología)
- [Resultados](#resultados)

## Datos 
- El dataset utilizado contiene un registro de twitts del año 2020, los cuales están relacionados o hablan acerca del Covid.

![Dataset](Imágenes/Dataset.png)

## Metodología 

### 1. Limpieza de Datos 
- Se eliminó las columnas innecesarias, solo se utilizó la columna con el contenido del twitt y otra columna con la etiqueta que representa el tipo de sentimiento que da a entender el twitt.

### 2. Normalización de Datos 
- Se quitaron en los textos los "\n" (Saltos de líneas), "\r" (Retorno de Carro) y "\t" (Tabulaciones).
- Todas las palabras de convirtieron en minúsculas.
- También se filtraron las palabras que se utilizarían; se quitaron los signos de puntuación, palabras vacías, menciones, url, hashtags y dominios.
- Despues se convirtieron las palabras filtradas a su forma base.
- Al final se recontruyeron los textos con las palabras resultantes.
- Se normalizaron las etiquetas convirtiendolos a valores numéricos.

### 3. Bolsa de Palabras 
- Se convierte el texto en una matriz de características, donde cada elemento de la matriz representa la frecuencia de la palabra en el texto.
 
![Bolsa de Palabras](Imágenes/Bolsa_Palabras.png)

### 4. Implementar los Algoritmos
- Se implementaron 2 algoritmos distintos para ver cuál da mejores resultados:
  - Perceptrón Multi Capa (MLP)
  - Máquina de Vector de Soporte (SVM)

### 5. Entrenamiento del MLP 
- Se usaron los datos limpios para entrenar el algoritmo.
- Se utilizaron gráficas para ver exactitud y perdida del algoritmo.

### 6. Evaluación de los Modelos
- Se evaluó con las métricas de "accuracy", "precision", "recall" y "f1".
- También se usaron las matrices de confusión para ver los falsos positivos, etc.

## Resultados 
- Se pudo comparar ambos resultados de cada algoritmo con los mismos datos, lo cual el que dio mejores resultados fue el algoritmo MLP.
- Pero el algoritmo SVM no se alejó mucho de los resultados del otro algoritmo.
