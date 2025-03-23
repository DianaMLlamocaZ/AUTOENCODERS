# DESCRIPCIÓN:
En este proyecto, creé un autoencoder simple basado en una capa completamente conectada para reducir la dimensionalidad de los datos manteniendo la información más relevante. Luego, usé dicha representación codificada para entrenar un modelo de clasificación (regresión logística) en el conjunto de datos MNIST.

# APLICACIÓN:
Reducción de la dimensionalidad y uso de la representación codificada para entrenar un modelo de clasificación.

# RESULTADOS:
Accuracy sin reducción de dimensionalidad: 92.56%

Accuracy con reducción de dimensionalidad: 89.87%

# CONCLUSIONES:
1) Al entrenar el modelo en la data sin reducir la dimensionalidad, el clasificador tardó más tiempo en entrenar, debido a la cantidad de dimensiones de cada representación para las imágenes.
2) El performance del clasificador que se entrenó con las features comprimidas presentó un accuracy menor (una reducción del 3%, aproximadamente), debido a que se redujo el espacio de características para las imágenes compactas. Sin embargo, el modelo presentaría una mejor generalización, ya que solo se extraen las características más importantes de las imágenes, que luego se usarán para entrenar el clasificador.
