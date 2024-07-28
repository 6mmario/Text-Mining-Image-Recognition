# Procesamiento de Imágenes con OpenCV
## Filtros Convolucionales
### Definición
- Técnicas utilizadas para aplicar diferentes tipos de efectos y transformaciones a las imágenes.
### Aplicaciones
- Suavizado de imágenes
- Realce de bordes
- Eliminación de ruido
### Tipos de Filtros
#### Filtro Promedio
- Utiliza un kernel de promedio para suavizar la imagen.
#### Filtro Gaussiano
- Utiliza una función gaussiana para suavizar la imagen y reducir el ruido.
#### Filtro Mediana
- Utiliza la mediana de los píxeles en la vecindad del kernel para reducir el ruido sal y pimienta.
#### Filtro Bilateral
- Suaviza la imagen mientras preserva los bordes.
### Implementación en OpenCV
- **cv2.filter2D()**
- **cv2.GaussianBlur()**
- **cv2.medianBlur()**
- **cv2.bilateralFilter()**
### Ejemplo
```python
import cv2
import numpy as np

imagen = cv2.imread('imagen.jpg')
kernel = np.ones((5,5),np.float32)/25
imagen_filtrada = cv2.filter2D(imagen, -1, kernel)
cv2.imshow('Imagen Filtrada', imagen_filtrada)
cv2.waitKey(0)
cv2.destroyAllWindows()
