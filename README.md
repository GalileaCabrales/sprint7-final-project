# Sprint 7 Final Project - ConnectaTel Customer Behavior Analysis

## 📌 Descripción del proyecto

Como analista de datos, el objetivo de este proyecto es analizar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, utilizando información registrada hasta 2024.

A través del análisis exploratorio de datos (EDA), limpieza de datos, detección de anomalías y segmentación de usuarios, se buscó identificar patrones de consumo, perfiles de clientes y oportunidades de negocio para mejorar la oferta de planes y las estrategias de retención.

---

## 📂 Datasets utilizados

### plans.csv
Contiene información sobre los planes disponibles:

- Nombre del plan
- Precio mensual
- Minutos incluidos
- GB incluidos
- Costos por consumo adicional

### users.csv
Contiene información de los clientes:

- user_id
- Nombre y apellido
- Edad
- Ciudad
- Fecha de registro
- Plan contratado
- Fecha de cancelación (churn)

### usage.csv
Contiene el historial de uso de los servicios:

- user_id
- Tipo de uso (llamada o mensaje)
- Fecha del evento
- Duración de llamadas
- Longitud de mensajes

---

## 🔍 Etapas del análisis

### 1. Exploración inicial de datos
- Revisión de estructura y tipos de datos.
- Identificación de valores nulos.

### 2. Detección de valores inválidos y sentinels
- Identificación de edades inválidas (-999).
- Detección de ciudades registradas como "?" o vacías.
- Identificación de posibles valores sentinel en variables de uso (`duration = 120`, `length = 1490`).
- Detección de fechas fuera de rango.

### 3. Limpieza y transformación
- Conversión de fechas a formato datetime.
- Validación de variables numéricas y categóricas.
- Revisión de inconsistencias en los registros.

### 4. Construcción de métricas por usuario
- Cantidad total de mensajes.
- Cantidad total de llamadas.
- Minutos totales de llamada.

### 5. Análisis exploratorio de datos (EDA)
- Estadísticas descriptivas.
- Distribuciones mediante histogramas.
- Detección de outliers mediante boxplots.
- Análisis de comportamiento según el plan.

### 6. Segmentación de clientes
Segmentación por edad:
- Joven (< 30 años)
- Adulto (30-59 años)
- Adulto Mayor (60+ años)

Segmentación por nivel de uso:
- Bajo uso
- Uso medio
- Alto uso

### 7. Insights de negocio
- Identificación de segmentos valiosos.
- Patrones de consumo.
- Recomendaciones comerciales para ConnectaTel.

---

## 🛠 Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

## ▶️ Cómo ejecutar el proyecto

### Opción 1: Google Colab

1. Descarga el archivo `.ipynb`.
2. Abre Google Colab.
3. Selecciona **Archivo → Subir cuaderno**.
4. Carga el notebook.
5. Sube los archivos:
   - `plans.csv`
   - `users.csv`
   - `usage.csv`
6. Ejecuta las celdas de forma secuencial.

### Opción 2: Jupyter Notebook

1. Clona este repositorio.
2. Instala las dependencias necesarias:

```bash
pip install pandas numpy matplotlib seaborn
```

3. Abre el notebook:

```bash
jupyter notebook
```

4. Ejecuta todas las celdas.

---

## 🔄 Guía de reproducción

1. Cargar los datasets.
2. Explorar estructura y calidad de datos.
3. Identificar y documentar nulos, valores inválidos y sentinels.
4. Convertir variables de fecha.
5. Construir métricas agregadas por usuario.
6. Realizar análisis estadístico y visualizaciones.
7. Detectar outliers y evaluar su impacto.
8. Crear segmentos de clientes por edad y nivel de uso.
9. Generar insights y recomendaciones para el negocio.

---

## 📈 Principales hallazgos

- La mayoría de los clientes pertenece al segmento de edad adulto.
- El grupo más grande de usuarios corresponde al segmento de uso medio.
- Se detectaron valores inválidos y sentinels que podían afectar algunos análisis.
- Los usuarios de alto uso representan una oportunidad para estrategias de fidelización y planes premium.
- Los patrones de consumo presentan distribuciones sesgadas a la derecha, con una minoría de usuarios de consumo intensivo.

---
**Autor:** Gali  
**Proyecto:** Sprint 7 Final Project - Data Analysis Bootcamp
