# sprint7-final-project
# Análisis de Clientes y Uso de Servicios de Telecomunicaciones

## Objetivo del Proyecto

El objetivo de este proyecto es analizar el comportamiento de uso de clientes de una empresa de telecomunicaciones durante 2024, identificando patrones de consumo relacionados con llamadas, mensajes y tipo de plan contratado.

A través del análisis exploratorio y segmentación de usuarios, se busca comprender:
- diferencias de comportamiento entre planes,
- niveles de uso de los clientes,
- posibles patrones en consumo de servicios,
- distribución demográfica de los usuarios.

---

## Datasets Utilizados

### users.csv
Contiene información demográfica y de suscripción de los usuarios:
- `user_id`
- `age`
- `city`
- `plan`
- `reg_date`

### usage.csv
Contiene el historial de uso de servicios:
- `user_id`
- `type`
- `duration`
- `date`

---

## Etapas del Análisis

### 1. Limpieza y Preparación de Datos
- Conversión de fechas a formato datetime.
- Reemplazo de valores sentinel.
- Tratamiento de valores nulos.
- Validación de fechas futuras.

### 2. Exploración de Datos
- Revisión de columnas categóricas.
- Estadísticas descriptivas.
- Distribución de planes.
- Identificación de patrones de uso.

### 3. Ingeniería de Variables
- Creación de métricas agregadas por usuario:
  - cantidad de mensajes,
  - cantidad de llamadas,
  - minutos totales de llamadas.
- Segmentación de usuarios según nivel de uso.

### 4. Visualización
- Histogramas por tipo de plan.
- Distribuciones de edad.
- Comparación de consumo entre segmentos.

### 5. Segmentación de Clientes
Clasificación de usuarios en:
- Bajo uso
- Uso medio
- Alto uso

---

## Tecnologías Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

## Cómo Ejecutar el Proyecto

### Opción 1: Google Colab
1. Abrir el notebook `.ipynb` en Google Colab.
2. Subir los archivos `users.csv` y `usage.csv`.
3. Ejecutar las celdas en orden.

### Opción 2: Jupyter Notebook
1. Clonar el repositorio:
```bash
git clone <url-del-repositorio>
```

2. Instalar dependencias:
```bash
pip install pandas numpy matplotlib seaborn
```

3. Ejecutar Jupyter Notebook:
```bash
jupyter notebook
```

4. Abrir el archivo `.ipynb`.

---

## Guía de Reproducción

1. Descargar los datasets.
2. Ejecutar la sección de limpieza de datos.
3. Generar la tabla agregada de uso por usuario.
4. Combinar tablas.
5. Ejecutar análisis estadístico.
6. Generar visualizaciones.
7. Analizar segmentación de clientes.

---

## Resultados Esperados

El análisis permite:
- identificar diferencias entre planes,
- detectar usuarios de alto consumo,
- comprender patrones de comportamiento,
- apoyar futuras decisiones de negocio y segmentación comercial.
