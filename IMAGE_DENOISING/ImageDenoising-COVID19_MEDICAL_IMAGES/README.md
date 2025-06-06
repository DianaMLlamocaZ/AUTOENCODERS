# DESCRIPCIÓN:
En este proyecto, creé un autoencoder convolucional para eliminar el ruido gaussiano (media=0, std=1) presente en las tomografías computarizadas de pacientes con Covid 19.

Con el objetivo de entender el propósito del denoising autoencoder, utilicé enfoques tradicionales para remover el ruido, como el Gaussian Blur y Median Blur con la finalidad de comparar estos resultados con el modelo entrenado.

----

# APLICACIÓN:
Denoising Images en tomografías computarizadas de pacientes con Covid 19 utilizando un denoising autoencoder convolucional.

----

# RESULTADOS NUMÉRICOS:
Para obtener los resultados, utilicé dos métricas:
* **PSNR**: De la fórmula del PSNR, se intuye que *mientras más alto sea el valor PSNR, más parecida es la imagen reconstruida a la imagen original*, debido a que el MSE (factor dividendo en la fórmula) deberá ser menor.
* **SSIM**: Mientras *más cercano sea el valor resultado a 1, la imagen reconstruida es más 'similar' a la imagen original*.

====

Los valores a continuación representan la media de los valores PNSR en las imágenes de test (sin ruido), sobre las imágenes originadas (reconstruidas), ya sea por el autoencoder o los enfoques tradicionales al compararlas:

#### PSNR: IMÁGENES REALES | IMÁGENES DEL AUTOENCODER
* Media de la métrica PSNR en las imágenes de test: 27.053668975830078

#### PSNR: IMÁGENES REALES | IMÁGENES APLICANDO MEDIAN BLUR
* Media de la métrica PSNR en las imágenes de test: 12.511493682861328

#### PSNR: IMÁGENES REALES | IMÁGENES APLICANDO GAUSSIAN BLUR
* Media de la métrica PSNR en las imágenes de test: 12.655463218688965

====

Los valores a continuación representan la media de los valores SSIM en las imágenes de test (sin ruido), sobre las imágenes originadas (reconstruidas), ya sea por el autoencoder o los enfoques tradicionales al compararlas:

#### SSIM: IMÁGENES REALES | IMÁGENES DEL AUTOENCODER
* Media de la métrica PSNR en las imágenes de test: 0.7886712573222626

#### SSIM: IMÁGENES REALES | IMÁGENES APLICANDO MEDIAN BLUR
* Media de la métrica PSNR en las imágenes de test: 0.6465682907408488

#### SSIM: IMÁGENES REALES | IMÁGENES APLICANDO MEDIAN BLUR
* Media de la métrica PSNR en las imágenes de test: 0.6412973922621209

====

Así, numéricamente, las métricas sugieren que las imágenes reconstruidas por el autoencoder presentan menos ruido que las imágenes generadas al utilizarse los enfoques tradicionales. Por lo tanto, el autoencoder realizó un mejor 'denoising' en las imágenes que los otros approaches.

----

# RESULTADOS VISUALES:
* Fila 1: Imágenes con ruido
* Fila 2: Imágenes sin ruido
* Fila 3: Imágenes donde aplico el autoencoder para remover el ruido
* Fila 4: Imágenes donde aplico el kernel GaussianBlur para remover el ruido
* Fila 5: Imágenes donde aplico el kernel MedianBlur para remover el ruido

![ResultadoFinal](./IMÁGENES/ImagenAE.JPG)

====

Visualmente, se corrobora lo anterior: las imágenes reconstruidas por el autoencoder presentan menos ruido que las imágenes generadas al utilizarse los enfoques Gaussian Blur y Median Blur.

----

# CONCLUSIONES:
- El autoencoder presentó un mejor performance al realizar el denoising, a las imágenes con ruido, que los otros enfoques.

