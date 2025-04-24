# DESCRIPCIÓN:
En este proyecto, creé un autoencoder convolucional para eliminar el ruido gaussiano presente en las tomografías computarizadas de pacientes con Covid 19.

Con el objetivo de entender el propósito del denoising autoencoder, utilicé enfoques tradicionales para remover el ruido, como el Gaussian Blur y Median Blur con la finalidad de comparar estos resultados con el modelo entrenado.

# APLICACIÓN:
Denoising Images en tomografías computarizadas de pacientes con Covid 19 utilizando un denoising autoencoder convolucional.

# RESULTADOS:
Para obtener los resultados, utilicé dos métricas:
* PSNR: De la fórmula del PSNR, se intuye que mientras más alto sea el valor PSNR, más parecida es la imagen reconstruida a la imagen original, debido a que el MSE (factor dividendo en la fórmula) deberá ser menor.
* SSIM: Mientras más cercano sea el valor resultado a 1, la imagen reconstruida es más 'similar' a la imagen original.

----

Los valores a continuación representan la media de los valores PNSR en las imágenes de test (sin ruido), sobre las imágenes originadas (reconstruidas) por el autoencoder al compararlas:

### PSNR: IMÁGENES REALES | IMÁGENES DEL AUTOENCODER
* Media de la métrica PSNR en las imágenes de test: 27.053668975830078

### PSNR: IMÁGENES REALES | IMÁGENES APLICANDO MEDIAN BLUR
* Media de la métrica PSNR en las imágenes de test: 12.511493682861328

# CONCLUSIONES:
-  

