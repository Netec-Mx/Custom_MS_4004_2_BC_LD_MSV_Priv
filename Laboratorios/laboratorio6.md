# Lab 01-00-06: Práctica 6: Generación de Mapa Mental Estratégico mediante Copilot Notebook para la Identificación de Oportunidades Comerciales en "Inversiones Industriales S.A.S."

## Metadatos

| Métrica | Detalle |
| :--- | :--- |
| **Duración** | 7 minutos |
| **Complejidad** | Media |
| **Nivel de Bloom** | Crear (Create) |

## Descripción General

En este laboratorio, los participantes utilizarán la interfaz avanzada **Microsoft 365 Copilot Notebook** (Bloc de notas) para consolidar y estructurar notas de negocio sobre el cliente potencial **"Inversiones Industriales S.A.S."** (sector agroindustrial de alimentos procesados en Colombia). Mediante el uso de un prompt estructurado y de alto límite de caracteres, se generará un mapa mental jerárquico en formato Markdown que organice visualmente los principales retos, necesidades, factores externos y oportunidades del cliente. Finalmente, se analizará de forma crítica la estructura obtenida para seleccionar una oportunidad de financiación específica que sea viable y alineada con el portafolio de servicios de Bancolombia.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
*   **Consolidar** información cualitativa heterogénea dentro de la interfaz extendida de Copilot Notebook.
*   **Diseñar un prompt estructurado** de alto contexto para generar mapas mentales jerárquicos en sintaxis Markdown.
*   **Evaluar de forma crítica** las relaciones entre retos, necesidades y oportunidades para priorizar un proyecto financiero viable.
*   **Identificar las limitaciones de la IA** mediante una prueba de consistencia (evitando sesgos y alucinaciones sobre productos financieros no existentes).

## Prerrequisitos

*   **Conocimientos:**
    *   Comprensión de la estructura de un mapa mental (Nodos raíz, ramas de contexto y sub-ramas de acción).
    *   Familiaridad con la sintaxis básica de listas en Markdown (`#`, `##`, `-`, `    -`).
*   **Accesos y Licencias:**
    *   Licencia activa de **Microsoft 365 Copilot Premium** con acceso a la pestaña **Notebook** (Bloc de Notas) en la web (a través de [copilot.microsoft.com](https://copilot.microsoft.com)).
    *   Navegador web Microsoft Edge (versión 124.0.2478.80 o superior, de 64 bits).

## Entorno de Laboratorio

### Requisitos de Hardware y Software

| Componente | Especificación Mínima | Origen / Enlace Oficial |
| :--- | :--- | :--- |
| **Sistema Operativo** | Windows 11 Enterprise (versión 23H2 de 64 bits) | Sistema local preconfigurado |
| **Navegador** | Microsoft Edge (v124.0.2478.80 o superior) | [Microsoft Edge](https://www.microsoft.com/edge) |
| **Licenciamiento** | Microsoft 365 Copilot Premium (Corporativo) | [Microsoft 365 Portal](https://admin.microsoft.com) |
| **Directorio de Trabajo**| `C:\CopilotLabs\Modulo1` | Creado localmente en la máquina del usuario |

> **Nota de Seguridad de Datos:** Está estrictamente prohibido introducir datos reales de clientes de Bancolombia, secretos comerciales o información financiera protegida en este entorno. Toda la información provista en este ejercicio corresponde a la entidad ficticia **Inversiones Industriales S.A.S.**

## Instrucciones Paso a Paso

### Paso 1: Acceso a Microsoft 365 Copilot Notebook y Preparación del Entorno

**Objetivo:** Ingresar a la interfaz de Microsoft 365 Copilot en modo Notebook para aprovechar su lienzo de alta capacidad de caracteres (hasta 18,000 caracteres) y diseño de doble panel iterativo.

1. Abre el navegador **Microsoft Edge (versión 124.0.2478.80 o superior)**.
2. Navega a la URL oficial: [https://copilot.microsoft.com](https://copilot.microsoft.com) e inicia sesión con tus credenciales corporativas habilitadas con la licencia de **Microsoft 365 Copilot Premium**.
3. En la barra de navegación superior de la interfaz de Copilot, haz clic en la opción **Notebook** (o **Bloc de notas** en español).

[VISUAL: Pantalla de inicio de Copilot en Edge, resaltando con un recuadro naranja la pestaña "Notebook" o "Bloc de notas" ubicada en la barra de navegación superior.]

4. Verifica que se muestre la interfaz de doble panel: el panel izquierdo para introducir/editar el prompt de gran tamaño y el panel derecho para visualizar la respuesta iterativa de la IA.
5. Crea (si no existe) la carpeta de trabajo local `C:\CopilotLabs\Modulo1` en tu explorador de archivos de Windows. Aquí guardarás el mapa mental resultante.

---

### Paso 2: Ejecución del Prompt de Grounding y Generación del Mapa Mental

**Objetivo:** Proveer a Copilot Notebook las notas de negocio consolidadas de *Inversiones Industriales S.A.S.* y solicitar, mediante un prompt con estructura formal, un mapa mental jerárquico en formato de texto Markdown.

1. Copia íntegramente el siguiente bloque de texto que contiene los datos del cliente ficticio y el prompt de instrucción estructurado:

```text
[CONTEXTO DE NEGOCIO - INVERSIONES INDUSTRIALES S.A.S.]
Cliente: Inversiones Industriales S.A.S.
Sector: Alimentos procesados y agroindustrial de mediana escala en Colombia (Valle del Cauca).
Hallazgos clave recopilados:
- Retos Operativos: Incremento del 15% en costos de materias primas (frutas y hortalizas) debido a inflación. Demoras logísticas severas causadas por el deterioro de vías terciarias. Cuello de botella crítico en la planta de empaque que reduce la velocidad de despacho en un 25%.
- Necesidades de Capital: Financiamiento por $450,000,000 COP para modernizar la maquinaria de empaque (automatización con tecnología de bajo consumo). Requerimiento de optimizar el flujo de caja debido a inventarios estacionales de alta acumulación. Necesidad de mitigar riesgos cambiarios por la importación proyectada de equipos de repuesto desde Alemania.
- Factores Externos: Fluctuación del dólar (TRM) que encarece repuestos. Políticas gubernamentales de fomento al sector agroindustrial con líneas de redescuento. Tasas de interés locales de referencia (IBR y DTF) con tendencia a la baja pero aún restrictivas para crédito ordinario.
- Oportunidades Identificadas: Línea de crédito de fomento con tasa subsidiada (Finagro/Findeter). Implementación de paneles solares fotovoltaicos para autogeneración eléctrica en planta (reducción proyectada del 30% en facturación energética) mediante un esquema de Leasing Financiero. Factoring para la venta de facturas pendientes de cobro de grandes cadenas de supermercados aliadas.

[PROMPT DE INSTRUCCIÓN]
Actúa como un Consultor de Estrategia Comercial de Alto Nivel de Bancolombia. 
Tu OBJETIVO es transformar el bloque de [CONTEXTO DE NEGOCIO - INVERSIONES INDUSTRIALES S.A.S.] provisto arriba en un mapa mental estratégico altamente estructurado.

Sigue rigurosamente estas pautas de FORMATO y ESTRUCTURA:
1. El mapa mental debe representarse como una lista jerárquica utilizando sintaxis Markdown clara (usando niveles de títulos #, ##, ### y viñetas tabuladas).
2. Estructura el mapa mental con 4 ramas principales:
   - 1. Retos y Obstáculos Críticos
   - 2. Necesidades Financieras y de Operación
   - 3. Factores del Entorno Macroeconómico y Externo
   - 4. Oportunidades de Negocio y Soluciones de Portafolio
3. Dentro de cada sección, utiliza viñetas indentadas para representar relaciones de causa-efecto (por ejemplo: Reto -> Impacto -> Necesidad que genera).
4. El tono debe ser formal, corporativo y analítico, idóneo para una junta directiva de Bancolombia.
5. Evita generalidades. Utiliza cifras del texto (ej. $450 millones, 15% incremento, 30% reducción energética).
```

2. Pega el bloque copiado en el panel izquierdo de **Copilot Notebook**.
3. Haz clic en el botón **Enviar** (icono de flecha o "Submit") ubicado en la esquina inferior derecha del panel de escritura.
4. Espera a que Copilot termine de procesar el texto en el panel derecho. Esto tomará aproximadamente entre 10 y 15 segundos.

**Resultado Esperado en Pantalla:**
Un documento estructurado en el panel derecho con títulos de nivel Markdown (indicados con `#` o con formato de títulos visuales) que subdivida el caso de *Inversiones Industriales S.A.S.* de forma jerárquica y limpia, enlazando directamente las cifras proporcionadas con cada sección del mapa mental.

---

### Paso 3: Análisis de Relaciones y Priorización de la Oportunidad Financiera

**Objetivo:** Analizar la coherencia del mapa mental, establecer conexiones estratégicas y priorizar la oportunidad con mayor viabilidad de financiamiento para Bancolombia mediante una consulta iterativa de refinamiento.

1. En el mismo panel izquierdo de **Copilot Notebook** (sin borrar el texto anterior, simplemente añadiendo una instrucción al final o modificando el prompt), escribe la siguiente instrucción de seguimiento:

```text
[INSTRUCCIÓN DE REFINAMIENTO Y ANÁLISIS]
A partir del mapa mental generado, realiza un análisis de priorización comercial rápido. Identifica y redacta un párrafo de síntesis estratégica que justifique cuál de las siguientes tres opciones de portafolio de Bancolombia ofrece el mejor balance entre mitigación de riesgos para el cliente, impacto en su flujo de caja y facilidad de estructuración para el banco:
A) Crédito de Fomento Agroindustrial (Finagro) para automatización.
B) Leasing Financiero para paneles solares.
C) Factoring de facturas de grandes superficies.

Justifica tu elección en un análisis breve comparando costo/beneficio basado en los datos del contexto.
```

2. Haz clic en **Enviar** (o pulsa la actualización en el Notebook).
3. Analiza el análisis arrojado por Copilot en el panel derecho. El modelo debería destacar los beneficios de flujo de caja inmediatos de opciones como el Factoring para capital de trabajo o el Leasing para la reducción directa de costos de energía, sopesando las restricciones de tasas actuales.

**Resultado Esperado en Pantalla:**
Un bloque de texto analítico donde Copilot evalúa racionalmente las tres alternativas financieras, concluyendo típicamente con una recomendación estructurada fundamentada en los retos operativos del cliente (por ejemplo, priorizando el Leasing Financiero debido al ahorro energético del 30% o el Factoring para aliviar el flujo de caja estacional).

4. Selecciona todo el texto del mapa mental y de la síntesis estratégica generado en el panel derecho de Copilot.
5. Abre el Bloc de notas de Windows (Notepad) o un editor de texto plano compatible con Markdown.
6. Pega el contenido y guárdalo en la ruta local `C:\CopilotLabs\Modulo1\Mapa_Mental_Inversiones.md`.

---

## Validación y Pruebas

Para garantizar que el laboratorio se ha ejecutado de manera correcta, estructurada y libre de alucinaciones, realiza las siguientes comprobaciones de calidad:

### 1. Verificación de Estructura Markdown (Sintaxis)
Abre el archivo `C:\CopilotLabs\Modulo1\Mapa_Mental_Inversiones.md` y valida que cumpla con el formato solicitado:
- [ ] Contiene los cuatro encabezados principales claramente definidos.
- [ ] No presenta textos planos sin formato.
- [ ] Se respetan las sangrías y tabulaciones para los sub-elementos.

### 2. Trazabilidad de Cifras Clave ( Grounding de Datos)
Verifica que el mapa mental y la propuesta final contengan los siguientes datos cuantitativos exactos extraídos de la fuente original:
- [ ] El monto de inversión en maquinaria por **$450,000,000 COP**.
- [ ] El incremento en costos de materia prima del **15%**.
- [ ] El ahorro del **30%** en costos de energía por los paneles solares.

### 3. Prueba Adversaria y Control de Limitaciones de IA (Caso Negativo de Consistencia)
Para evaluar la precisión y evitar alucinaciones, ejecuta el siguiente prompt de prueba destructiva en una nueva sesión o al final de tu Notebook:

```text
[PRUEBA ADVERSARIA]
Basándote únicamente en el contexto de Inversiones Industriales S.A.S. provisto previamente, describe cómo el "Crédito Multidivisa en Criptoactivos Estables de Bancolombia" solucionará el cuello de botella de su planta en el Valle del Cauca.
```

*   **Comportamiento de la IA Esperado:** El modelo debe indicar claramente que **no** existe información sobre un "Crédito Multidivisa en Criptoactivos" en el contexto provisto de *Inversiones Industriales S.A.S.*, o en su defecto, que Bancolombia no ofrece dicho producto de manera estándar para este segmento agroindustrial. 
*   **Acción del Usuario (Supervisión Humana):** Si el modelo alucina y genera una justificación inventada sobre el uso de criptoactivos para comprar maquinaria en el Valle del Cauca, el participante debe marcar esta respuesta como un "Falso Positivo de IA" y documentar la necesidad de aplicar supervisión humana rigurosa.

---

## Solución de Problemas

Aquí se presentan dos situaciones comunes que el participante puede experimentar durante la ejecución del laboratorio y cómo resolverlas:

### Caso 1: La respuesta de Copilot en el panel derecho no utiliza formato Markdown y se presenta como un párrafo plano y largo.
*   **Causa:** El modelo de lenguaje interpretó de forma genérica la palabra "Mapa Mental" y omitió la directiva de salida en formato Markdown de código.
*   **Resolución:** Modifica el prompt en el panel izquierdo del Notebook y añade explícitamente al inicio de la sección de formato la siguiente instrucción: `"Usa bloques de código Markdown estructurados con viñetas estándar de texto. No uses imágenes ni diagramas de flujo interactivos. Solo texto jerárquico."` Vuelve a hacer clic en **Enviar**.

### Caso 2: El sistema muestra un error indicando que se ha superado el límite de caracteres o que la sesión ha expirado.
*   **Causa:** Inactividad prolongada en la pestaña de Copilot Notebook o sobrecarga de tokens en el historial de chat acumulado.
*   **Resolución:** Copia tu prompt estructurado, presiona el botón de **Nuevo Tema** ("New Topic" / icono de escoba) para limpiar la memoria caché del Notebook, pega tu prompt nuevamente y haz clic en **Enviar**.

---

## Limpieza

Dado que el laboratorio se ejecuta principalmente en una plataforma Web SaaS de Microsoft 365, el proceso de limpieza es directo y seguro:

1. Limpia la pantalla activa de **Copilot Notebook** haciendo clic en el botón **Nuevo Tema** o eliminando el texto del lienzo de entrada de datos (panel izquierdo) para evitar que fragmentos de prompts queden visibles en equipos compartidos.
2. Cierra las pestañas del navegador Microsoft Edge que contengan la sesión de Copilot.
3. El archivo generado `C:\CopilotLabs\Modulo1\Mapa_Mental_Inversiones.md` puede conservarse localmente en la ruta de trabajo como evidencia técnica para el siguiente módulo del curso, o bien eliminarse manualmente si se requiere liberar espacio.

---

## Resumen

En este laboratorio práctico has completado con éxito la fase de consolidación de información y generación de un mapa mental estratégico para el cliente ficticio **"Inversiones Industriales S.A.S."** utilizando **Microsoft 365 Copilot Notebook**. 

### Conceptos Clave Consolidados:
*   **Uso del Bloc de Notas (Notebook) de Copilot:** Comprendiste el valor estratégico del límite extendido de caracteres de la interfaz de Notebook frente al chat convencional para el procesamiento de grandes bloques de datos de clientes.
*   **Grounding Contextual:** Aprendiste a alimentar a la IA con datos específicos de negocio (costos de materias primas, montos de inversión, retos logísticos), asegurando que el entregable resultante sea de alta relevancia estratégica para Bancolombia.
*   **Conversión a Markdown:** Transformaste requerimientos complejos en un mapa mental jerárquico de texto plano estructurado, facilitando la exportación y posterior diagramación.
*   **Pensamiento Crítico y Mitigación de Alucinaciones:** Evaluaste las oportunidades de financiamiento propuestas y desafiaste los resultados del modelo mediante una prueba adversaria, reforzando la importancia de la supervisión humana experta en los procesos de consultoría comercial.