# Taller 1 – Introducción a Data Science
## Modelos de Regresión y Clasificación para la Predicción de Ratings de Bebidas Alcohólicas

### Descripción
En este taller, los estudiantes aplicarán sus conocimientos de Web Scraping, Análisis Exploratorio de Datos, Visualización, y Modelos de Regresión para predecir el rating de bebidas alcohólicas. Además, se incorporarán modelos de clasificación para determinar si el rating es positivo, negativo o neutral. Los datos serán obtenidos del sitio web [disaller.com](https://disaller.com/).

### Objetivos
1. Familiarizarse con las técnicas de Web Scraping para obtener datos de un sitio web.
2. Aplicar técnicas de exploración de datos y visualización sobre el conjunto de datos obtenido.
3. Modelar el rating de bebidas alcohólicas utilizando la información obtenida mediante Regresión Lineal.
4. Modelar y entrenar modelos de clasificación binaria y multiclase.
5. Utilizar métricas como accuracy, precision, recall y F1 para evaluar la clasificación, y MSE para la regresión.
6. Utilizar técnicas de cross-validation y optimización de hiperparámetros para mejorar el rendimiento de los modelos construidos.

### Entregables
- Un cuaderno interactivo Jupyter Notebook con todo el código fuente, resultados y análisis.
- El cuaderno debe utilizar apropiadamente celdas de markdown y de código.

### Fecha de Entrega
- **Fecha límite:** 26 de octubre del 2024 a las 23:59, usando la tarea “Entrega Taller-1” del campus virtual.

### Adquisición de Datos
Para este taller nos centraremos en Tequila/Mezcal. La pregunta principal es: “¿Existen atributos en los Tequilas o mezcales que sirvan para predecir si uno de ellos es bueno (según los ratings de los expertos)?”

Los datos se obtendrán mediante Web Scraping desde la siguiente URL: [https://distiller.com/](https://distiller.com/), específicamente en la sección de tequila/mezcal. Usaremos Selenium para realizar el scraping y BeautifulSoup para procesar los datos extraídos.

El proceso de extracción incluirá la recopilación de información de las siguientes columnas:
- `Name`, `Type`, `Cask`, `Location`, `Age`, `ABV %`, `Cost`, `Badge`, `# Ratings`, `Community Rating`, `Flavor Summary`, `Expert`, `Expert Score`, `Smoky`, `Earthy`, `Spicy`, `Herbal`, `Oily`, `Bitter`, `Rich`, `Sweet`, `Mineral`, `Salty`, `Umami`, `Tart`, `Fruity`, `Floral`, `Review`.

### Consideraciones de Implementación
Para realizar el scraping, se utilizará **Selenium** con **Chromium**. Aquí hay un ejemplo de código inicial para la configuración de Selenium:

```python
from selenium import webdriver
from selenium.webdriver.chrome.options import Options

options = Options()
options.add_argument("--headless=new")
driver = webdriver.Chrome(options=options)

# Código de extracción con BeautifulSoup.
driver.quit()
```

### Requerimientos Mínimos

1. **Web Scraping** [20 puntos]  
   - Utilizar técnicas de Web Scraping para extraer información de al menos 500 bebidas alcohólicas del sitio web.  
   - Almacenar los datos obtenidos en un DataFrame de Pandas.  

2. **Preprocesamiento de Datos** [20 puntos]  
   - Realizar una exploración inicial de los datos, utilizando estadísticas básicas y visualización.  
   - Aplicar técnicas de preprocesamiento y dividir los datos en conjuntos de entrenamiento y prueba (80/20 o 70/30).  

3. **Regresión Lineal** [20 puntos]  
   - Entrenar un modelo de Regresión Lineal para predecir el rating de las bebidas.  
   - Evaluar el modelo utilizando el MSE y el coeficiente de determinación (R²).  

4. **Clasificación** [15 puntos]  
   - Clasificar los ratings en tres categorías: positivo, neutral y negativo.  
   - Entrenar modelos de clasificación binaria y multiclase.  
   - Evaluar el rendimiento utilizando métricas de clasificación y matrices de confusión.  

5. **Optimización de Hiperparámetros** [15 puntos]  
   - Aplicar técnicas de optimización como Grid Search o Random Search para mejorar el rendimiento de los modelos de Regresión Lineal (LASSO y Ridge).  

6. **Conclusiones** [10 puntos]  
   - Presentar conclusiones relevantes sobre el análisis realizado y las ventajas/desventajas de los modelos utilizados.  

7. **Créditos Extra**  
   - Regresión kNN [10 puntos]  
   - Regresión No Lineal [10 puntos]  

### Consideraciones de Evaluación y Administrativas  
   - El taller puede realizarse en grupos de 1, 2 o 3 estudiantes, con la misma evaluación independientemente del tamaño del grupo.  
   - La evaluación se realizará hasta el primer error encontrado. Se espera que el cuaderno sea ejecutable de principio a fin.  
   - Las entregas atrasadas serán manejadas según la política del curso.  

### Dependencias  
   - Python 3.x  

   Librerías:  
   - pandas  
   - numpy  
   - matplotlib  
   - seaborn  
   - scikit-learn  
   - selenium  
   - beautifulsoup4  
   - jupyter  

### Instrucciones para Ejecutar el Proyecto  

1. Clonar este repositorio:  
   ```bash
   git clone https://github.com/Eltosergi/Taller1-IntrodataScience.git           
   ```
2. Instalar las dependencias:  
   ```bash
   pip install -r requirements.txt        
   ```
3. Instalar las dependencias:  
   ```bash
   jupyter notebook     
   ```