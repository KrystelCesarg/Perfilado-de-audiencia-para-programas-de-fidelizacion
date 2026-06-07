# Limpieza de Datos y Segmentación en Store 1 🚀

Trabajé simulando el rol de una analista de datos júnior para **Store 1**, una tienda de comercio electrónico que esta preparando el lanzamiento de su nuevo **Programa de Fidelización de Clientes**. 

El objetivo principal es normalizar, estructurar la información y segmentar a los clientes para que el equipo de marketing pueda armar campañas publicitarias bien dirigidas y personalizadas.

---

## 🎯 ¿Qué se realizó? (Metodología y Pasos)

El desarrollo del proyecto se ejecutó en un entorno de **Jupyter Notebook** y contempló las siguientes fases de ingeniería y análisis de datos:

1. **Limpieza e Ingeniería de Características Individuales:** Desarrollo de algoritmos iniciales para corregir tipos de datos (casting de edad a entero), remoción de caracteres residuales (`_` y espacios) y segmentación de cadenas de texto (separación de nombre y apellido); ejecutandolo en un solo registro de cliente para asegurar el funcionamiento.
2. **Normalización y estandarización de categorías:** Por medio de un bulce se realiza la transformación de categorías de productos pasándolas de mayúsculas a minúsculas uniformes para evitar duplicidades lógicas en agrupaciones posteriores.
3. **Automatización mediante Funciones Reutilizables:** Modularización de todo el proceso de ETL (Extracción, Transformación y Carga) en una función limpia llamada `clean_user()` aplicada de forma masiva a todo el dataset crudo (`users_raw`).
4. **Análisis Financiero Integrado:** Cálculo automatizado de los ingresos totales generados por la base de usuarios mediante estructuras de control y funciones de agregación.
5. **Segmentación y Perfilado Estructurado:** Implementación de filtros lógicos complejos para extraer audiencias específicas:
   - Usuarios jóvenes (menores de 30 años).
   - Clientes de alto valor (menores de 30 años con consumo superior a \$1,000).
   - Clientes con afinidades de compra específicas (categoría *clothes*).
8. **Desarrollo de Motores de Búsqueda Personalizados:** Creación de una función llamada `get_clients_by_category()`. De esta forma, si el negocio solicita el día de mañana: *"Necesito la lista de clientes que compran cosas para el hogar (home)"*, la función extrae automáticamente una sublista limpia con los KPIs clave por ID, nombre, edad y gasto total de esos clientes específicos.

---

## 📈 Logros e Impacto

- **Estandarización de Datos:** Se transformó una base de datos cruda inconsistente en un dataset estructurado y limpio listo para modelos analíticos o de producción.
- **Eficiencia Operacional:** La creación de funciones reutilizables permite al equipo de datos automatizar la limpieza de nuevos registros de clientes en segundos en lugar de realizar tareas manuales repetitivas.
- **Sólida Base de Segmentación:** Se proporcionó al equipo de marketing una segmentación granular de clientes de alto valor y filtros por categorías específicas, optimizando la asignación de presupuestos publicitarios para el nuevo Programa de Fidelización.

## 🧠 Los retos que me encontré en el camino

- **Estructuras complejas:** Trabajar con listas metidas dentro de otras listas (datos anidados) fue confuso al principio. Tuve que dominar muy bien el tema de los índices múltiples para no romper el código al intentar acceder, por ejemplo, sólo a la primera parte del nombre de un usuario.
- **Cambiar el chip a código reutilizable:** Al principio uno resuelve los problemas de forma lineal (paso 1, paso 2...), pero el verdadero reto fue abstraer eso y construir funciones modulares. Tenía que asegurarme de que si entraban 10,000 usuarios nuevos mañana, mis funciones los limpiaran sin pestañear.
- **Detalles invisibles en el texto:** Descubrí que un simple espacio de más o una mayúscula mal puesta hacían que mis filtros lógicos ignoraran a ciertos usuarios. Me obligó a ser extremadamente minuciosa con la estandarización del texto.

---

## 💡 Aprendizajes Clave

- **La importancia de la limpieza de datos (Data Cleaning):** Comprendí de manera práctica que el análisis de datos estratégico y los algoritmos comerciales dependen al 100% de la calidad y consistencia del formato inicial de los datos ya que por más buena que sea una estrategia de marketing, si tus datos base están duplicados o mal formateados, las decisiones van a fallar.
- **Pensamiento Modular y Automatización:** Aprendí a no escribir código para resolver el problema "de hoy", sino a diseñar herramientas (funciones) que automaticen el trabajo del futuro.
- **Conectar el código con el negocio:** Lo más valioso fue entender cómo traducir líneas de código y filtros lógicos en métricas de valor real para una empresa (como identificar clientes de alto valor o calcular ingresos totales para optimizar presupuestos de marketing).

---

## 🛠️ Habilidades Tecnológicas Utilizadas

- **Lenguaje:** Python 3 (Bucles `for`, condicionales `if/elif`, funciones personalizadas, Type Casting).
- **Entorno:** Jupyter Notebook y Git Bash para el control de versiones.
- **Habilidades clave:** Ingeniería de datos básica (ETL), lógica de programación, indexación multidimensional y segmentación de clientes.


