# Descripción del Dataset: `Casa_toluca.csv`

El archivo **`Casa_toluca.csv`** contiene un conjunto de datos del mercado inmobiliario enfocado en la venta de viviendas en Toluca de Lerdo, Estado de México, y sus áreas circundantes. A continuación se detallan la estructura, los campos y las principales estadísticas descriptivas de los datos.

---

## 1. Resumen General

* **Total de registros:** 2,004 propiedades.
* **Total de columnas:** 8 variables.
* **Cobertura geográfica:** Casas en venta en Toluca De Lerdo y zonas aledañas.

---

## 2. Estructura de las Columnas

| Nombre de Columna | Tipo de Dato | Valores Nulos | Descripción |
| :--- | :--- | :--- | :--- |
| `Unnamed: 0.2` | Entero | 0 | Índice autonumérico de la fila. |
| `Unnamed: 0` | Entero | 0 | Índice secundario de origen. |
| `Unnamed: 0.1` | Entero | 0 | Índice terciario de origen. |
| `Ubicación` | Texto (`string`) | 0 | Dirección o zona del inmueble ofertado. |
| `Area` | Numérico (`float`) | 283 | Superficie construida o de terreno (en $m^2$). |
| `Baños` | Numérico (`float`) | 54 | Número de baños disponibles en la propiedad. |
| `Habitaciones` | Numérico (`float`) | 73 | Número de recámaras/dormitorios. |
| `Precio` | Numérico (`float`) | 5 | Precio publicado del inmueble. |

---

## 3. Estadísticas Descriptivas Principales

| Métrica | Área ($m^2$) | Baños | Habitaciones | Precio |
| :--- | :--- | :--- | :--- | :--- |
| **Conteo** | 1,721 | 1,950 | 1,931 | 1,999 |
| **Promedio (Media)** | ~229.53 | ~2.50 | ~3.31 | ~169,047.20 |
| **Mediana (50%)** | 165.00 | 2.00 | 3.00 | 90,750.00 |
| **Mínimo** | 10.00 | 1.00 | 1.00 | 10,653.05 |
| **Máximo** | 11,111.00 | 124.00 | 40.00 | 10,000,000.00 |

---

## 4. Observaciones para Limpieza de Datos

1. **Columnas Redundantes:** Las columnas `Unnamed: 0.2`, `Unnamed: 0` y `Unnamed: 0.1` actúan únicamente como índices repetidos de captura y pueden ser eliminadas en el preprocesamiento.
2. **Valores Faltantes:** Hay 283 registros sin datos de `Area`, 73 sin `Habitaciones`, 54 sin `Baños` y 5 sin `Precio`.
3. **Valores Atípicos (Outliers):**
   * Existen valores extremos en `Habitaciones` (hasta 40) y `Baños` (hasta 124) que sugieren datos atípicos o propiedades comerciales/terrenos mal etiquetados.
   * La variable `Area` presenta un valor máximo de 11,111 $m^2$.
