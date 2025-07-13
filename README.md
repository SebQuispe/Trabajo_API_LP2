# Trabajo_final_LP2

# 📊 Comparación de Precios de Celulares y Consolas  
### 🇵🇪 Tiendas en Perú vs 🌐 Tiendas Internacionales  
**Proyecto final - Curso de Lenguaje de programación II**

---

### 👥 Integrantes del equipo
- Alexander Villanueva — [alexvilla123]
- Sebastián Quispe — [SebQuispe]

---

### 🎯 Objetivo del proyecto
Comparar precios de **celulares** y **consolas de videojuegos** entre tiendas **locales del Perú** (como Hiraoka y Curacao) y **tiendas internacionales** mediante la API de Google Shopping.  
El proyecto busca identificar:
- ¿Qué marcas son más caras o baratas según el país?
- ¿Cuáles ofrecen mayores descuentos locales?
- ¿Existen diferencias de precios significativas?

---

### 🧩 Fuentes de datos utilizadas

1. **Scraping directo de Hiraoka (Perú)**  
   - Celulares y consolas extraídos de forma combinada.  
   - Archivos generados:  
     - `celulares_filtrados_por_marca.csv`  
     - `consolas_hiraoka.csv`

2. **Scraping directo de La Curacao (Perú)**  
   - Archivos por marca individual (Apple, Samsung, Motorola, Xiaomi, Honor para celulares; Sony, Nintendo, Microsoft, Asus para consolas).  
   - CSVs combinados en tiempo de ejecución.

3. **API de Google Shopping**  
   - Usando el endpoint `https://www.searchapi.io/api/v1/search`  
   - Productos extraídos con ubicación `California, United States`, para simular tiendas internacionales.  
   - Archivos:  
     - `celulares_google_shopping_api_actualizado.csv`  
     - `consolas_videojuegos_actualizado.csv`

---

### 🧪 Metodología

1. **Extracción de datos:**
   - Scraping con `requests` y `BeautifulSoup` para tiendas locales.
   - API externa gratuita para tiendas globales.

2. **Estructuración:**
   - Limpieza y normalización de columnas (marca, modelo, precio actual, precio anterior).
   - Fusión en un único `DataFrame` por categoría (celulares y consolas).

3. **Cálculos realizados:**
   - Precio promedio por marca y tienda.
   - Descuentos en soles y porcentaje (cuando hay precio anterior).
   - Diferencia de precio respecto al precio promedio internacional (API).

4. **Visualizaciones:**
   - Barras comparativas por marca.
   - Descuentos medios por tienda.

---

### 📌 Principales hallazgos

- En general, los precios de celulares en Perú son **más altos** que los observados en tiendas internacionales.
- Hiraoka ofrece mayores descuentos que Curacao, aunque sus precios base suelen ser más elevados.
- Para consolas, **Sony y Nintendo** muestran diferencias significativas entre países.
- En muchos casos, las tiendas internacionales no publican descuentos, pero sus precios son directamente más bajos.

---

### ⚙️ Tecnologías utilizadas

- Python (Pandas, Matplotlib, Seaborn)
- Web Scraping: `requests`, `BeautifulSoup`
- API REST: `searchapi.io`
- Git y GitHub (trabajo colaborativo)
- Jupyter Notebook / Py script

---

### 📢 Conclusión

Este proyecto permite comprender cómo varían los precios tecnológicos entre el mercado local y el global. Además, pone en práctica técnicas de extracción, estructuración y análisis de datos en escenarios reales y útiles para el consumidor.

