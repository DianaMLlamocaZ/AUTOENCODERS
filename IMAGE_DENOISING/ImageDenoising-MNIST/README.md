# DESCRIPCIÓN:
En este proyecto, creé un autoencoder convolucional para eliminar el ruido gaussiano añadido a las imágenes del dataset MNIST.

# APLICACIÓN:
Denoising Images en el dataset MNIST.

# RESULTADOS:
- El autoencoder convolucional, incluso con pocas capas convolucionales, pudo eliminar decentemente el ruido presente en las imágenes

# CONCLUSIONES:
1) El performance del modelo es aceptable, ya que pudo remover el ruido gaussiano presente en cada una de las imágenes.

----

# MEJORAS: 
Probar con diferentes cantidades de filtros, así como aumentar el tamaño de las capas convolucionales, podría hacer que el modelo tenga un mejor performance
Sin embargo, añadir demasiadas capas podría generar overfitting. Por lo que es recomendable hacer fine-tunning con diferentes hiperparámetros y verificando siempre el performance.
