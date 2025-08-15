# Challenge-Telecom-X

# Análisis de Churn - TelecomX 

Este proyecto se centra en el análisis de datos de clientes de una empresa de telecomunicaciones con el objetivo de comprender y predecir la evasión de clientes (Churn). El conjunto de datos, proporciona información detallada sobre los servicios, contratos y comportamiento de los clientes. El objetivo principal es identificar los factores clave que influyen en la decisión de un cliente de dejar la compañía.

---

## 📂 Contenido

- `telecomX_data = pd.read_json('https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json')
- `notebook.ipynb`: Script/Jupyter Notebook con el proceso de carga, limpieza y expansión de datos.
- `README.md`: Este archivo de documentación.

---

## 🔍 Descripción del Dataset

La versión reducida contiene inicialmente **6 columnas**:

| Columna     | Descripción |
|-------------|-------------|
| `customerID` | ID único del cliente |
| `Churn` | Si el cliente dejó la empresa (`Yes`/`No`) |
| `customer` | Datos personales (JSON anidado) |
| `phone` | Información de servicio telefónico (JSON anidado) |
| `internet` | Información de servicio de internet (JSON anidado) |
| `account` | Información contractual y pagos (JSON anidado) |

Los campos anidados incluyen información como género, edad, tipo de contrato, servicios adicionales y montos facturados.

---

## 🛠 Proceso de Limpieza y Transformación

1. **Carga del Dataset**
   
La etapa inicial del proyecto se centró en la preparación de los datos. Los pasos clave incluyeron:

Importación y desanidado: Se cargó el archivo telecomX_data ('https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json') y se desanidaron las columnas anidadas para crear una estructura más manejable. El resultado es un DataFrame que se carga de la siguiente manera:

   ```python
   df = pd.read_csv("telecomX_normalized.csv")
   ```
2. **Carga del Dataset**

Conversión de tipos de datos: Se convirtieron los tipos de datos de las columnas para optimizar el análisis. Las columnas numéricas como tenure, Monthly y Total se convirtieron a float. Las columnas como Churn, Partner y SeniorCitizen se transformaron a tipo booleano (True/False), mientras que el resto de variables categóricas se asignaron al tipo category.

Manejo de valores nulos: Se identificaron y trataron los valores nulos, en particular en la columna Total, asegurando la integridad del conjunto de datos.

## 📊 Análisis Exploratorio de Datos ETL (Extract, Transform, Load)

Durante el ETL, se realizaron diversas visualizaciones para entender la distribución de las variables y su relación con la evasión de clientes. Los hallazgos clave incluyen:

Distribución de Churn: El porcentaje de clientes que evaden la empresa se comparó con el de aquellos que permanecen, proporcionando una visión inicial de la magnitud del problema.

Antigüedad (tenure): Se observó que los clientes con menor antigüedad tienden a tener una tasa de evasión significativamente más alta.

Tipo de Contrato: Los clientes con contratos de mes a mes mostraron una tasa de evasión mucho mayor en comparación con aquellos con contratos de uno o dos años.

Servicios Adicionales: La tasa de evasión disminuye a medida que los clientes contratan más servicios adicionales, como seguridad en línea, soporte técnico y protección de dispositivos.

## 💡 Conclusiones e Insights

El análisis ha revelado que la evasión de clientes no es un fenómeno aleatorio, sino que está influenciada por un conjunto de factores interrelacionados:

La antigüedad es crucial: La mayoría de las deserciones ocurren en los primeros meses de servicio.

El contrato de mes a mes representa un alto riesgo: Este tipo de contrato ofrece a los clientes mayor flexibilidad, pero también un mayor riesgo de cambio de proveedor.

El paquete de servicios influye en la lealtad: La contratación de servicios adicionales sugiere un mayor compromiso y satisfacción, reduciendo la probabilidad de que el cliente se vaya.

## 📝 Recomendaciones

Basado en los hallazgos, se sugieren las siguientes estrategias para mitigar la evasión de clientes:

Programas de retención temprana: Implementar ofertas o beneficios especiales para los clientes durante sus primeros meses de servicio para incentivarlos a permanecer.

Incentivar contratos a largo plazo: Ofrecer descuentos o promociones atractivas a los clientes con contratos de mes a mes para motivarlos a cambiarse a contratos de uno o dos años.

Promover servicios de valor añadido: Resaltar los beneficios de servicios como soporte técnico, seguridad en línea y protección de dispositivos para aumentar el compromiso del cliente y la percepción de valor de los servicios de la empresa.
