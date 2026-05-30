# Procesamiento de Datos y Segmentación de Clientes (Store 1)

Este proyecto corresponde a la segunda etapa del análisis de datos para la plataforma de comercio electrónico **Store 1**. El objetivo principal es normalizar, estructurar y analizar una base de datos cruda de usuarios para extraer perfiles clave de consumo que sirvan como base analítica para el lanzamiento de un nuevo **Programa de Fidelización de Clientes**.

---

## 🎯 ¿Qué se realizó? (Metodología y Pasos)

El desarrollo del proyecto se ejecutó en un entorno de **Jupyter Notebook** y contempló las siguientes fases de ingeniería y análisis de datos:

1. **Limpieza e Ingeniería de Características Individuales:** Desarrollo de algoritmos iniciales para corregir tipos de datos (casting de edad a entero), remoción de caracteres residuales (`_` y espacios) y segmentación de cadenas de texto (separación de nombre y apellido).
2. **Normalización y Estandarización de Variables:** Transformación iterativa de categorías de productos en mayúsculas a minúsculas uniformes para evitar duplicidades lógicas en agrupaciones posteriores.
3. **Automatización mediante Funciones Reutilizables:** Modularización de todo el proceso de ETL (Extracción, Transformación y Carga) en una función limpia llamada `clean_user()` aplicada de forma masiva a todo el dataset crudo (`users_raw`).
4. **Análisis Financiero Integrado:** Cálculo automatizado de los ingresos totales generados por la base de usuarios mediante estructuras de control y funciones de agregación.
5. **Segmentación y Perfilado Estructurado:** Implementación de filtros lógicos complejos para extraer audiencias específicas:
   - Usuarios jóvenes (menores de 30 años).
   - Clientes de alto valor (menores de 30 años con consumo superior a \$1,000).
   - Clientes con afinidades de compra específicas (categoría *clothes*).
6. **Desarrollo de Motores de Búsqueda Personalizados:** Creación de la función paramétrica `get_clients_by_category()` para extraer sublistas dinámicas con los KPIs clave por ID, edad y gasto acumulado según la categoría requerida por el negocio.

---

## 📈 Logros e Impacto

- **Estandarización de Datos:** Se transformó una base de datos cruda inconsistente en un dataset estructurado y limpio listo para modelos analíticos o de producción.
- **Eficiencia Operacional:** La creación de funciones reutilizables permite al equipo de datos automatizar la limpieza de nuevos registros de clientes en segundos en lugar de realizar tareas manuales repetitivas.
- **Sólida Base de Segmentación:** Se proporcionó al equipo de marketing una segmentación granular de clientes de alto valor y filtros por categorías específicas, optimizando la asignación de presupuestos publicitarios para el nuevo Programa de Fidelización.

---

## 🛠️ Habilidades Tecnológicas Utilizadas

- **Lenguaje principal:** Python 3
- **Entorno de desarrollo:** Jupyter Notebook / Git Bash
- **Estructuras de datos complejas:** Manejo avanzado de listas anidadas, diccionarios, sublistas e indexación múltiple.
- **Lógica de programación:** Bucles controlados (`for`), condicionales avanzados (`if` / `elif`), funciones personalizadas con retorno paramétrico y manejo de tipos de datos (*Type Casting*).
