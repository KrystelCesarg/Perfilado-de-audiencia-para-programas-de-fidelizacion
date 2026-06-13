# Segmentación Avanzada de Usuarios para el Lanzamiento del Programa de Fidelización

## 🎯 Problema de Negocio
El equipo de marketing está preparando el lanzamiento de un nuevo Programa de Fidelización de Clientes. Sin embargo, la base de datos cruda presentaba inconsistencias, duplicados y formatos no estandarizados que impedían ejecutar campañas dirigidas de manera eficiente. El objetivo del proyecto fue normalizar la información histórica y segmentar a la audiencia para optimizar la asignación del presupuesto publicitario y personalizar la comunicación.

## 📊 Conjunto de Datos
El análisis se realizó sobre el conjunto de datos crudo de usuarios (`users_raw`), el cual contiene las siguientes variables:
* **Demográficas:** Edad y nombres completos (cadenas de texto anidadas).
* **De Comportamiento:** Categorías de productos comprados (ej. ropa, hogar) y gasto total individual.

## 🔍 Ingeniería de Datos y Análisis
1. **Pipeline de Limpieza:** Estandarización de formatos de texto, corrección de tipos de datos (conversión de edad a entero) y eliminación de ruido en cadenas (caracteres `_` y espacios en blanco).
2. **Automatización ETL Modular:** Creación de una función reutilizable llamada `clean_user()` para procesar de forma masiva y automática nuevos registros de clientes.
3. **Análisis Financiero Integrado:** Implementación de estructuras de control para calcular automáticamente los ingresos totales generados por la base de datos activa.
4. **Segmentación Predictiva:** Aplicación de filtros lógicos complejos para aislar audiencias estratégicas:
   * Usuarios jóvenes (menores de 30 años).
   * Clientes de alto valor (menores de 30 años con consumo superior a $1,000).
   * Afinidades específicas por categoría (compradores de la categoría *clothes*).
5. **Motor de Búsqueda Personalizado:** Desarrollo de la función parametrizada `get_clients_by_category()` para extraer dinámicamente listas de clientes con sus KPIs clave (ID, nombre, edad, gasto) según las necesidades inmediatas del negocio.

## 💡 Hallazgos Clave
* **Consistencia de Información:** Se transformó una base de datos inconsistente y desestructurada en un dataset limpio y listo para producción o modelos analíticos.
* **Eficiencia Operacional:** La automatización mediante funciones modulares redujo el tiempo de preparación de datos de horas de trabajo manual a solo unos segundos.
* **Mitigación de Riesgo de Negocio:** La segmentación granular evita el desperdicio de presupuesto en campañas masivas no dirigidas, asegurando un impacto directo en los clientes de alto valor.

## 🚀 Recomendaciones Estratégicas (Enfoque de Analítica de Personas y Negocio)
* **Automatización del Flujo de Retención:** Integrar la función `clean_user()` en un pipeline semanal automatizado para etiquetar y dar la bienvenida a nuevos miembros del programa de fidelización de forma inmediata.
* **Incentivos Dirigidos a Clientes Clave:** Lanzar un programa de referidos exclusivo para el segmento de alto valor identificado (menores de 30 años con gasto > $1k) para reducir los costos de adquisición de clientes mediante sus embajadores más activos.

## 🛠️ Herramientas y Tecnologías
* **Lenguaje:** Python 3 (Bucles, condicionales, funciones personalizadas, conversión de tipos de datos).
* **Entorno:** Jupyter Notebook.
* **Habilidades Clave:** Ingeniería de datos básica (ETL), indexación multidimensional e implementación de lógica de negocio.
