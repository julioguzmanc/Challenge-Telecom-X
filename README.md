# Challenge-Telecom-X

# Análisis de Churn - TelecomX (Versión Reducida)

Este repositorio contiene el análisis exploratorio de una versión reducida del dataset **TelecomX**, con 250 registros.  
El objetivo principal es preparar los datos para analizar la **evasión de clientes** (Churn).

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
   ```python
   df = pd.read_csv("telecomX_normalized.csv")
