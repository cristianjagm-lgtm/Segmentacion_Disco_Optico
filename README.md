# Segmentación de Disco Óptico mediante Redes Profundas (U-Net)

Este proyecto implementa una solución de aprendizaje profundo para la segmentación semántica del disco óptico en imágenes de retina. Desarrollado como parte del trabajo de ingeniería en la **Universidad Industrial de Santander (UIS)**.

##  Detalles de la Arquitectura
El modelo utiliza una arquitectura **U-Net** personalizada con:
* **Encoder/Decoder:** 4 bloques de contracción y 4 de expansión.
* **Regularización:** Capas de `BatchNormalization` y `Dropout` para estabilidad.
* **Optimización:** Pipeline de datos con `tf.data` (Prefetching y Autotune) para maximizar el uso de la GPU.
* **Data Augmentation:** Rotaciones y contrastes aleatorios integrados en el modelo.

##  Métricas de Evaluación
Para garantizar la precisión médica, el modelo se evalúa con:
* **Dice Coefficient & IoU:** Precisión del solapamiento de la segmentación.
* **Sensibilidad (Recall):** Capacidad de detección del disco óptico.
* **Especificidad:** Precisión en la identificación del fondo retiniano.

##  Instrucciones de Uso
1. Clone este repositorio.
2. Asegúrese de tener el dataset **ORIGA-light** organizado en las rutas especificadas en el notebook.
3. Ejecute `main.ipynb` en Google Colab o un entorno con soporte para GPU.

---
**Autor:** Cristian  
**Institución:** Universidad Industrial de Santander (UIS)  
**Año:** 2026