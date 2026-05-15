# sprint7-final-project
# 📊 Análisis de Clientes y Consumo de Servicios – ConnectaTel

## 📌 Objetivo del Proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica, utilizando información registrada hasta el año 2024.

A través de técnicas de limpieza, exploración y visualización de datos, el proyecto busca:

* identificar patrones de consumo de llamadas y mensajes,
* analizar diferencias entre tipos de planes,
* detectar problemas de calidad de datos,
* segmentar usuarios según su nivel de uso,
* generar insights sobre el comportamiento histórico de los clientes.

---

# 🗂️ Datasets Utilizados

El proyecto utiliza tres datasets principales:

## 1. `users.csv`

Contiene información demográfica y de suscripción de los usuarios.

### Variables principales:

* `user_id`
* `age`
* `city`
* `plan`
* `reg_date`

---

## 2. `usage.csv`

Contiene el historial de uso de servicios por usuario.

### Variables principales:

* `user_id`
* `type`
* `duration`
* `length`
* `date`

---

## 3. `plans.csv`

Contiene información sobre los planes disponibles.

### Variables principales:

* precio mensual
* minutos incluidos
* GB incluidos
* costos por excedente

---

# 🔎 Etapas del Análisis

## 1. Carga y Exploración de Datos

* Importación de librerías.
* Carga de datasets.
* Revisión inicial con `.head()`, `.info()` y `.shape()`.
* Identificación de tipos de datos y estructura.

---

## 2. Identificación de Problemas de Calidad

* Detección de valores nulos.
* Identificación de sentinels.
* Revisión de valores inválidos.
* Exploración de columnas categóricas y numéricas.

---

## 3. Limpieza de Datos

* Conversión de fechas a formato `datetime`.
* Reemplazo de sentinels:

  * `-999` en edad.
  * `?` en ciudad.
* Corrección de fechas futuras.
* Tratamiento de valores nulos.

---

## 4. Ingeniería de Variables

Se construyó una tabla agregada por usuario para resumir el comportamiento histórico.

### Métricas generadas:

* cantidad de mensajes,
* cantidad de llamadas,
* minutos totales de llamadas.

También se combinaron datasets usando `merge()`.

---

## 5. Análisis Estadístico

* Resumen estadístico de variables numéricas.
* Distribución porcentual de planes.
* Identificación de rangos y posibles valores extremos.

---

## 6. Visualización de Datos

Se realizaron histogramas y gráficos comparativos para:

* edad,
* cantidad de mensajes,
* cantidad de llamadas,
* minutos de llamadas.

Los gráficos utilizaron `hue='plan'` para comparar usuarios Básico y Premium.

---

## 7. Segmentación de Clientes

Los usuarios fueron clasificados según su nivel de uso:

| Segmento  | Condición                     |
| --------- | ----------------------------- |
| Bajo uso  | llamadas < 5 y mensajes < 5   |
| Uso medio | llamadas < 10 y mensajes < 10 |
| Alto uso  | resto de usuarios             |

---

# 🛠️ Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* Google Colab

---

# ▶️ Cómo Ejecutar el Proyecto

## Opción 1: Google Colab

1. Abrir el notebook `.ipynb` en Google Colab.
2. Subir los archivos CSV necesarios.
3. Ejecutar las celdas en orden.

---

## Opción 2: Jupyter Notebook Local

### 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPOSITORIO>
```

### 2. Instalar dependencias

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Ejecutar Jupyter Notebook

```bash
jupyter notebook
```

### 4. Abrir el notebook del proyecto

Abrir el archivo:

```bash
S7 Version-Estudiante-Project-ConnectaTel.ipynb
```

---

# 🔁 Guía de Reproducción

Para reproducir el análisis:

1. Descargar o clonar el repositorio.
2. Colocar los datasets en la misma carpeta del notebook.
3. Ejecutar el notebook desde el inicio.
4. Revisar las etapas de:

   * limpieza,
   * transformación,
   * agregación,
   * visualización,
   * segmentación.
5. Interpretar los insights generados.

---

# 📈 Resultados Esperados

El proyecto permite:

* comprender el comportamiento de consumo de los usuarios,
* identificar diferencias entre planes,
* detectar usuarios de alto consumo,
* apoyar procesos de segmentación y toma de decisiones comerciales.

---

# 👨‍💻 Autor

Proyecto desarrollado como parte de un proceso de formación en análisis de datos utilizando Python y herramientas de visualización.

