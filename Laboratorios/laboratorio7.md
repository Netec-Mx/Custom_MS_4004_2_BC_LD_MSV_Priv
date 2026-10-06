# Lab 01-00-07: Práctica 7: Construcción de Modelos de Simulación de Escenarios con Copilot en Excel (Modo Plan)

## Metadatos

| Característica | Detalle |
| :--- | :--- |
| **Duración** | 8 minutos |
| **Complejidad** | Difícil (Hard) |
| **Nivel de Bloom** | Crear (Create) |
| **Tecnologías** | Microsoft Excel, Microsoft 365 Copilot Premium (Modo Plan/Edición) |

## Descripción General

En este laboratorio, aplicarás habilidades analíticas avanzadas para evaluar la viabilidad de la oportunidad comercial seleccionada en la práctica anterior para **Inversiones Industriales S.A.S.** (sector de alimentos procesados y agroindustrial de mediana escala en Colombia). 

Abrirás un libro en blanco en Microsoft Excel, guardarás el archivo en OneDrive para habilitar las capacidades de Copilot y, utilizando exclusivamente lenguaje natural a través de la interfaz de Copilot (Modo Plan/Edición), estructurarás un modelo financiero de simulación de escenarios a 3 años. El modelo contendrá tres escenarios explícitos (conservador, base y expansivo) con supuestos y variables operativas ficticias pero realistas para el sector agroindustrial, permitiendo evaluar la oportunidad de manera rigurosa sin requerir la formulación manual de ecuaciones complejas.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
- **Habilitar y configurar** el entorno de Microsoft 365 Copilot en Microsoft Excel mediante el guardado en la nube corporativa (OneDrive/SharePoint).
- **Formular prompts estructurados** en el panel de Copilot utilizando el "Modo Plan" para esquematizar y diseñar una tabla de modelado financiero multidimensional.
- **Construir escenarios simulados** (conservador, base y expansivo) basados en variables clave como inversión inicial, ingresos proyectados, costos operativos y tasa de crecimiento.
- **Validar críticamente** los resultados y fórmulas generadas por Copilot en Excel, asegurando la trazabilidad matemática y lógica de los supuestos financieros.

## Prerrequisitos

Para completar con éxito este laboratorio, requieres:
- **Conocimientos teóricos**: Comprensión de los conceptos de modelado financiero básico (ingresos, costos de operación, flujo de caja neto, tasa de crecimiento y escenarios de sensibilidad).
- **Licenciamiento y Acceso**:
  - Cuenta corporativa activa de Microsoft 365 con licencia de **Microsoft 365 Copilot Premium**.
  - Acceso a **Microsoft OneDrive para la Empresa** sincronizado localmente o acceso directo a Excel Web.
- **Estado Inicial del Caso**: Haber seleccionado una oportunidad de negocio en la Práctica 6. Para este laboratorio de simulación, utilizaremos la oportunidad validada: *"Implementación de un deshidratador solar híbrido industrial para optimizar el procesamiento de frutas locales en Inversiones Industriales S.A.S."*

## Entorno de Laboratorio

### Requisitos de Hardware y Software

| Componente | Especificación Técnica Requerida |
| :--- | :--- |
| **Sistema Operativo** | Microsoft Windows 11 Enterprise (Versión 23H2 o superior) |
| **Aplicación de Escritorio** | Microsoft Excel para Empresas de 64 bits (Canal Mensual, Versión 2408 - Build 17928.20156 o superior) [VERSIÓN POR VALIDAR] o Excel en la Web. |
| **Navegador Web** | Microsoft Edge (Versión 124.0.2478.80 o superior) [VERSIÓN POR VALIDAR] |
| **Conectividad** | Conexión de banda ancha de mínimo 10 Mbps de bajada con acceso directo a endpoints oficiales de Microsoft 365. |
| **Directorio de Trabajo** | Localmente mapeado en `C:\CopilotLabs\Modulo1\` |

> **Nota Crítica de Configuración**: Microsoft 365 Copilot en Excel de escritorio requiere obligatoriamente que la función **Autoguardado (AutoSave)** esté activa. Esto solo es posible si el archivo se crea o se guarda directamente en una carpeta sincronizada con OneDrive para la Empresa o SharePoint Online.

## Instrucciones Paso a Paso

### Paso 1: Inicialización del Libro y Configuración de Guardado en la Nube

**Objetivo**: Crear un libro de Excel en blanco en el directorio local de trabajo y sincronizarlo con OneDrive para activar el panel interactivo de Copilot.

1. Abre la aplicación de escritorio de **Microsoft Excel** o accede a través de Office Portal (`office.com`) y selecciona Excel.
2. Crea un **Libro en blanco**.
3. Guarda inmediatamente el archivo con las siguientes especificaciones:
   - **Ruta local**: `C:\CopilotLabs\Modulo1\` (Asegúrate de que esta carpeta esté sincronizada con tu cuenta corporativa de OneDrive).
   - **Nombre del archivo**: `Evaluacion_Escenarios_Oportunidad.xlsx`
4. Confirma que la opción **Autoguardado** (ubicada en la esquina superior izquierda de la barra de título de Excel) esté en estado **Activado**.

[VISUAL: 01-00-07-001 - Captura de la barra superior de Excel mostrando el interruptor de 'Autoguardado' en ON y el archivo guardado con formato .xlsx en la cuenta corporativa de OneDrive].

5. En la pestaña de **Inicio (Home)** de la cinta de opciones, ubica el botón de **Copilot** en el extremo derecho de la barra y haz clic en él para abrir el panel lateral de chat de Copilot.

---

### Paso 2: Generación del Modelo de Supuestos Base con Copilot

**Objetivo**: Guiar a Copilot mediante un prompt estructurado para que actúe en Modo Plan y diseñe una tabla de supuestos financieros ficticios pero coherentes para el proyecto de deshidratador solar híbrido.

1. En el panel de Copilot que se muestra a la derecha de la pantalla, copia y pega con precisión el siguiente prompt estratégico diseñado para el sector agroindustrial colombiano:

```text
Actúa como un analista de planeación financiera experto. Diseña un plan y luego genera una estructura de datos en la hoja actual para evaluar la viabilidad de la oportunidad: "Implementación de un deshidratador solar híbrido industrial" para el cliente "Inversiones Industriales S.A.S." del sector de alimentos procesados. 

Necesito una estructura clara que contenga:
1. Una sección de "Variables de Entrada y Supuestos" en Pesos Colombianos (COP) que incluya: Inversión Inicial, Tasa de Descuento (WACC de 12%), y Costos de Operación Base anuales.
2. Tres escenarios explícitos: "Conservador", "Base" y "Expansivo".
3. Para cada escenario, proyecta a 3 años (Año 1, Año 2, Año 3) las siguientes variables ficticias pero coherentes para el mercado colombiano: Ingresos Proyectados, Costos Operativos y el Flujo de Caja Neto (calculado como Ingresos menos Costos Operativos).

Por favor, esquematiza primero tu plan de acción antes de insertar los datos.
```

2. Presiona **Enviar** (Enter).
3. **Analiza la interacción**: Copilot entrará en su "Modo Plan", sugiriéndote primero los pasos lógicos que tomará para construir el modelo (ej. crear la sección de parámetros, luego la matriz de escenarios y finalmente las fórmulas de flujo de caja).
4. Cuando Copilot presente la propuesta estructurada en el panel y te ofrezca la opción de aplicarla (generalmente a través de un botón como **Aplicar a una nueva hoja** o **Insertar tabla**), haz clic en el botón correspondiente para plasmar la estructura en la cuadrícula de Excel.

---

### Paso 3: Estructuración y Conversión de Datos a Formato de Tabla Oficial

**Objetivo**: Asegurar que los datos generados por Copilot cumplan con los requisitos técnicos de formato de Excel para permitir análisis avanzados de datos.

1. Si Copilot insertó la información como texto plano o rangos independientes, selecciona todo el rango de celdas generado por el modelo (por ejemplo, desde `A1` hasta `E15` o el rango donde se hayan ubicado los escenarios).
2. Ve a la pestaña de **Inicio** > **Dar formato como tabla** y selecciona cualquier estilo de tabla. Asegúrate de marcar la casilla *"La tabla tiene encabezados"*.
3. Si Copilot ya insertó el modelo estructurado en formato de Tabla de Excel nativa, valida que los nombres de las columnas sean claros (ej. `Escenario`, `Año 1`, `Año 2`, `Año 3`, `Métrica`).
4. Revisa que los valores financieros estén expresados correctamente. Para cumplir con el estándar corporativo, aplica formato de moneda COP a los campos de dinero:
   - Selecciona las celdas con montos numéricos.
   - Presiona `Ctrl + 1` (o clic derecho > **Formato de celdas**).
   - Selecciona **Moneda**, establece las posiciones decimales en `0` y el símbolo en `$` (Español - Colombia).

---

### Paso 4: Ajuste de Fórmulas Dinámicas mediante Copilot en Modo Edición

**Objetivo**: Asegurar la integridad matemática del modelo de simulación utilizando la capacidad de Copilot para automatizar la inserción de fórmulas sin intervención de programación manual.

1. En el panel de Copilot, escribe la siguiente instrucción para automatizar el cálculo del Flujo de Caja Neto de forma unificada:

```text
En la tabla de escenarios, calcula el "Flujo de Caja Neto" para cada uno de los tres escenarios (Conservador, Base y Expansivo) para los años 1, 2 y 3. Utiliza la fórmula lógica: Ingresos Proyectados menos Costos Operativos. Asegúrate de aplicar esta fórmula de forma consistente en toda la columna o celdas correspondientes.
```

2. Haz clic en **Enviar**.
3. Copilot analizará la estructura de la tabla y sugerirá una fórmula de Excel (por ejemplo, `=SUMA(...)` o restas directas de celdas como `=[@Ingresos]-[@Costos]`). 
4. Haz clic en el botón de **Aceptar** o **Insertar columna/fórmula** que proporciona el asistente en el panel lateral.
5. Valida visualmente en la cuadrícula de Excel que la operación matemática se haya propagado correctamente a lo largo de las filas correspondientes de cada escenario.

*Resultado esperado en pantalla:*
*Una hoja de cálculo estructurada con una sección clara de supuestos macroeconómicos de la empresa, seguida de una tabla unificada con 3 bloques de escenarios bien definidos (Conservador, Base, Expansivo) que proyectan los ingresos, costos operativos y el Flujo de Caja Neto resultante para un periodo de 3 años.*

---

## Validación y Pruebas

Para asegurar la precisión del modelo construido y la correcta interacción con la inteligencia artificial de Microsoft 365, realiza las siguientes comprobaciones de calidad en tu entorno local:

### 1. Validación de la Integridad del Archivo y Conexión
- Comprueba que el archivo `Evaluacion_Escenarios_Oportunidad.xlsx` se encuentra guardado en `C:\CopilotLabs\Modulo1\`.
- Verifica que el icono de la nube junto al nombre del archivo no presente errores de sincronización de OneDrive.

### 2. Prueba Matemática del Flujo de Caja Neto (Trazabilidad)
- Posiciónate en la celda correspondiente al **Año 1** bajo el **Escenario Base**.
- Realiza el cálculo manual de forma mental o rápida: si tus *Ingresos Proyectados* generados por Copilot son, por ejemplo, `COP 150.000.000` y tus *Costos Operativos* son `COP 90.000.000`, la celda de *Flujo de Caja Neto* debe mostrar exactamente `COP 60.000.000`.
- Verifica que la celda contenga una fórmula de Excel válida (por ejemplo, `=B10-B11` o referencias estructuradas de tabla `=[@[Ingresos Año 1]]-[@[Costos Año 1]]`) y no un valor estático escrito en formato de texto plano.

### 3. Prueba Adversaria de Consistencia de Datos (Control de Limitaciones de IA)
- **Desafío**: Cambia drásticamente el valor de la celda de *Costos Operativos* del *Escenario Base - Año 1* por un valor que exceda los ingresos (por ejemplo, si el ingreso es `150.000.000`, digita un costo de `200.000.000`).
- **Verificación esperada**: El *Flujo de Caja Neto* debe recalcularse de forma automática instantáneamente, mostrando un valor negativo en formato contable (ej. `($50.000.000)` o `-50.000.000`). Si el valor no cambia, la fórmula insertada por Copilot no es dinámica y requiere corrección manual. *Regresa el valor a su estado inicial antes de continuar.*

---

## Solución de Problemas

En caso de encontrar desviaciones operativas durante la ejecución de este laboratorio, revisa los siguientes diagnósticos resueltos paso a paso:

### Problema 1: El panel de Copilot se encuentra deshabilitado (gris/inactivo) en la barra de herramientas de Excel
- **Sintoma**: Abres el archivo de Excel pero el icono de Copilot en la esquina superior derecha no responde al hacer clic o se muestra descolorido y bloqueado.
- **Causa**: El libro actual no cumple con las políticas de almacenamiento en la nube requeridas por Microsoft 365 Copilot. Está guardado localmente (ej. directamente en el disco `C:\` sin sincronización activa de OneDrive) o el Autoguardado está desactivado.
- **Resolución**: 
  1. Haz clic en la opción **Archivo** > **Guardar una copia**.
  2. Selecciona obligatoriamente tu espacio corporativo de **OneDrive - Bancolombia** (o tu cuenta empresarial de M365).
  3. Asegúrate de guardar el archivo en la ruta local de tu equipo asociada a esa sincronización (`C:\CopilotLabs\Modulo1\`).
  4. Confirma que la esquina superior izquierda de Excel muestre el interruptor de **Autoguardado** encendido. El panel de Copilot se activará de forma automática en un lapso de 3 a 5 segundos.

### Problema 2: Copilot genera un mensaje de error indicando que "No se puede trabajar sobre un rango que no sea una tabla"
- **Sintoma**: Al enviar un prompt para calcular el flujo de caja o modificar escenarios, Copilot responde con la advertencia: *"Actualmente solo puedo ayudarte con datos que estén dentro de una Tabla de Excel."*
- **Causa**: Excel requiere que la estructura de datos sea declarada explícitamente como un objeto de tipo "Tabla" para que el modelo de lenguaje de Copilot identifique los límites del conjunto de datos mediante Microsoft Graph.
- **Resolución**:
  1. Selecciona todo el rango de celdas que contiene los escenarios financieros generados.
  2. Presiona el atajo de teclado `Ctrl + T` (o ve a la pestaña **Inicio** > **Dar formato como tabla**).
  3. En la ventana emergente que se abre, asegúrate de marcar la opción **La tabla tiene encabezados** y haz clic en **Aceptar**.
  4. Vuelve a escribir tu instrucción en el panel de Copilot y presiona Enviar. La IA procesará la orden sin inconvenientes.

---

## Limpieza

Al finalizar tus pruebas de validación, prepara tu estación de trabajo para los siguientes módulos del entrenamiento:

1. Asegúrate de restaurar cualquier cambio temporal o de prueba numérica realizado durante la sección de "Validación y Pruebas" para mantener los supuestos base limpios.
2. Guarda el libro presionando `Ctrl + G` o confirmando que el estado del archivo en la barra superior sea *"Guardado"*.
3. Cierra la aplicación de Microsoft Excel de forma segura.
4. No elimines la carpeta `C:\CopilotLabs\Modulo1\Evaluacion_Escenarios_Oportunidad.xlsx`, ya que este modelo de escenarios simulados servirá como insumo directo para estructurar la presentación de alto impacto que desarrollarás en los módulos de PowerPoint.

---

## Resumen

En esta práctica ágil de 8 minutos, has logrado:
- **Configurar un entorno colaborativo seguro** conectando tu almacenamiento corporativo de OneDrive con Microsoft Excel, habilitando con éxito las capacidades analíticas en la nube de Microsoft 365 Copilot Premium.
- **Implementar una sesión de trabajo con IA en Modo Plan**, aprendiendo a recibir un borrador de plan de acción de Copilot antes de inyectar datos en la cuadrícula de trabajo.
- **Modelar escenarios financieros de sensibilidad** (Conservador, Base y Expansivo) personalizados para el sector de alimentos procesados de Inversiones Industriales S.A.S. en Colombia, utilizando exclusivamente prompts estructurados en lenguaje natural.
- **Auditar la calidad del modelo de IA** comprobando el funcionamiento de las fórmulas lógicas aplicadas de forma unificada en el flujo de caja neto.