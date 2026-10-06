# Lab 01-00-08: Práctica 8: Simulación Avanzada y Análisis de Sensibilidad con Copilot en Excel (Modo Edición)

## Metadatos

| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 8 minutos |
| **Complejidad** | Difícil (Hard) |
| **Nivel de Bloom** | Crear (Create) |

## Descripción General

En esta práctica de laboratorio, los participantes trabajarán sobre el modelo de simulación de escenarios estructurado previamente para el cliente **Inversiones Industriales S.A.S.** utilizando **Microsoft 365 Copilot en Excel** en su rol de asistente de cálculo y edición. El ejercicio consiste en guiar a Copilot para que incorpore de manera automática cálculos financieros clave (ingreso neto y margen de rentabilidad), genere una visualización gráfica de alto impacto que contraste los tres escenarios de negocio de la oportunidad y ejecute un análisis de sensibilidad guiado. Finalmente, se identificará qué variables comerciales y operativas (por ejemplo, el Costo de Adquisición de Clientes - CAC o la Tasa de Conversión) ejercen mayor influencia en la viabilidad financiera de la propuesta para Bancolombia.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
- **Utilizar Copilot en Excel (Modo Edición)** para estructurar e insertar de forma automatizada columnas calculadas complejas sin requerir formulación manual.
- **Generar y personalizar representaciones visuales de escenarios** mediante gráficos dinámicos sugeridos por Copilot para facilitar la toma de decisiones directivas.
- **Formular prompts de análisis de sensibilidad** que permitan evaluar el impacto de las variables críticas (CAC, tasa de conversión, inversiones) en la rentabilidad simulada del cliente.

## Prerrequisitos

Para completar este laboratorio con éxito, el participante requiere:
* **Conocimientos:** 
  * Entender la diferencia entre datos estructurados (tablas de Excel) y rangos normales.
  * Familiaridad básica con conceptos financieros como Ingresos, Costos de Adquisición (CAC), Márgenes Operativos y Escenarios (Pesimista, Base, Optimista).
  * Haber completado el Lab 01-00-07 y contar con el archivo base guardado en la ruta local correspondiente.
* **Accesos:**
  * Acceso a una cuenta corporativa o educativa de Microsoft 365 activa con licencia de **Microsoft 365 Copilot Premium** habilitada en aplicaciones de escritorio.
  * Conectividad web sin restricciones para el procesamiento de prompts de IA.

## Entorno de Laboratorio

### Requisitos de Hardware y Software

| Componente | Especificación Técnica Mínima |
| :--- | :--- |
| **Sistema Operativo** | Microsoft Windows 11 Enterprise (Versión 23H2 o superior) |
| **Procesador** | Arquitectura x64 a 1.6 GHz o superior (mínimo 2 núcleos) |
| **Memoria RAM** | Mínimo 8 GB (16 GB recomendado para el uso fluido de IA) |
| **Aplicación de Escritorio** | Microsoft Excel para Microsoft 365 (Canal Empresarial Mensual, Versión 2408, Build 17928.20156 o superior) |
| **Licenciamiento** | Licencia de Microsoft 365 Copilot habilitada en el cliente de escritorio |
| **Almacenamiento Local** | Directorio de trabajo local configurado en `C:\CopilotLabs\Modulo1` |

> **Nota de Seguridad de Datos:** Bajo ninguna circunstancia se deben ingresar datos financieros reales, secretos comerciales o información bancaria confidencial de clientes reales de Bancolombia en el motor de Copilot. Todas las cifras y nombres de clientes son ficticios.

---

## Instrucciones Paso a Paso

### Paso 1: Preparación del Entorno y Verificación del Archivo de Escenarios

**Objetivo:** Cargar el archivo de trabajo de la sesión anterior en un entorno seguro y sincronizado con OneDrive, garantizando que Copilot pueda acceder al modo Edición.

**Instrucciones:**

1. Abra el explorador de archivos de Windows y navegue hasta la ruta del laboratorio: `C:\CopilotLabs\Modulo1`.
2. Busque el archivo generado en la práctica anterior, titulado **`Analisis_Oportunidad_Bancolombia.xlsx`**.
3. Abra el archivo con la aplicación de escritorio de **Microsoft Excel** (edición de 64 bits).
4. **Verificación de Sincronización:** Asegúrese de que el botón de **Autoguardado** (ubicado en la esquina superior izquierda de la ventana de Excel) esté activo (`ON`). Esto es indispensable para habilitar todas las funcionalidades de interacción directa de Copilot en archivos almacenados en la nube (OneDrive/SharePoint).
5. Verifique que los datos se encuentran estructurados en una **Tabla de Excel** con nombre (por ejemplo, `TablaEscenarios`). Si solo se visualiza un rango normal, seleccione todos los datos (rango `A1:G4`) y presione `Ctrl + T` para convertirlo formalmente en una tabla.

[VISUAL: 01-01-0002 - Vista de la interfaz de Microsoft Excel en Windows 11 mostrando el botón de autoguardado en ON y el archivo cargado en OneDrive con la estructura de la TablaEscenarios.]

*   **Resultado Esperado:** El archivo de Excel se carga correctamente, la tabla de 3 escenarios se visualiza claramente y el botón de Copilot en la barra de herramientas de "Inicio" se encuentra habilitado y de color verde.
*   **Verificación:** Haga clic en cualquier celda dentro del rango de datos. Debería aparecer la pestaña flotante "Diseño de tabla", lo que confirma que el rango está estructurado adecuadamente.

---

### Paso 2: Cálculo de Métricas Financieras con Copilot (Modo Edición)

**Objetivo:** Instruir a Copilot para que calcule el Ingreso Neto y el Margen Operativo porcentual de cada escenario, inyectando fórmulas automatizadas dentro de la tabla.

**Instrucciones:**

1. Haga clic en el botón de **Copilot** en la pestaña *Inicio* de Excel para desplegar el panel de chat lateral derecho.
2. Una vez cargado el panel, utilizaremos el **Modo Edición** mediante prompts precisos de lenguaje natural. Copie y pegue exactamente la siguiente instrucción en el cuadro de chat:

   ```text
   Calcula una nueva columna llamada 'Ingreso Neto' restando el 'Costo Operativo (COP)' y el costo de adquisición total (que es 'Clientes Nuevos' multiplicado por 'Costo de Adquisición (CAC - COP)') del 'Ingreso Estimado (COP)'. Aplica formato de moneda COP.
   ```

3. Presione Enter. Espere a que Copilot procese la estructura de la tabla, formule la regla de cálculo utilizando la sintaxis de tablas de Excel y le muestre la propuesta en el panel lateral.
4. Revise la fórmula sugerida en la tarjeta de previsualización (debería asemejarse a `=[[Ingreso Estimado (COP)]]-[[Costo Operativo (COP)]]-([[Clientes Nuevos]]*[[Costo de Adquisición (CAC - COP)]])`). 
5. Haga clic en **Insertar columna** (Insert column) si la fórmula es correcta.
6. Ahora, genere el margen relativo de rentabilidad comercial. Ingrese el siguiente prompt en el chat de Copilot:

   ```text
   Calcula una nueva columna llamada 'Margen (%)' que sea igual al 'Ingreso Neto' dividido por el 'Ingreso Estimado (COP)'. Dale formato de porcentaje con 2 decimales.
   ```

7. Revise la propuesta de Copilot y presione **Insertar columna**.

*   **Resultado Esperado:** La tabla de Excel ahora cuenta con dos nuevas columnas calculadas de forma dinámica y uniforme para los escenarios Pesimista, Base y Optimista.
*   **Verificación:** Sitúese sobre la celda `H2` y luego sobre la `I2`. Compruebe en la barra de fórmulas que no se ingresaron valores planos o constantes, sino expresiones estructuradas del tipo `=[@[Ingreso Neto]]/[@[Ingreso Estimado (COP)]]`.

---

### Paso 3: Generación de la Visualización de Escenarios

**Objetivo:** Utilizar Copilot para construir una gráfica representativa que compare las tres proyecciones financieras estructuradas, optimizando la posterior toma de decisiones comercial.

**Instrucciones:**

1. Seleccione la tabla completa en su hoja de cálculo actual.
2. En el cuadro de texto del panel de Copilot en Excel, ingrese el siguiente prompt detallado de visualización:

   ```text
   Genera un gráfico de columnas agrupadas que compare el 'Ingreso Estimado (COP)' y el 'Ingreso Neto' para cada uno de los tres 'Escenario'. Pon el gráfico en una nueva hoja.
   ```

3. Presione Enter. Copilot procesará los datos específicos de la tabla y generará un gráfico conceptual en el panel de chat.
4. Haga clic sobre el botón **Agregar a una hoja nueva** (Add to a new sheet) que aparece sobre la sugerencia de gráfico del panel.

[VISUAL: 01-01-0003 - Interfaz de Copilot mostrando el gráfico de barras sugerido donde se comparan ingresos brutos frente a netos para los tres escenarios de Inversiones Industriales S.A.S.]

*   **Resultado Esperado:** Se creará una pestaña adicional en el libro de trabajo (por ejemplo, `Hoja2`) que contendrá el gráfico sugerido con títulos correctos, leyenda clara de colores y los nombres de los escenarios (Pesimista, Base, Optimista) en el eje horizontal.
*   **Verificación:** Confirme visualmente que la barra del escenario Optimista refleje un mayor nivel de Ingreso Neto que los escenarios Base y Pesimista, validando la lógica lógica y matemática de las proyecciones.

---

### Paso 4: Análisis de Sensibilidad y Variables Críticas

**Objetivo:** Evaluar cuantitativamente cuáles de las variables ingresadas presentan el mayor riesgo o la mayor oportunidad en el modelo financiero del cliente.

**Instrucciones:**

1. Vuelva a la pestaña original que contiene la tabla de datos principal.
2. En el chat de Copilot, introduzca el siguiente prompt estructurado enfocado en el rol analítico (análisis de sensibilidad comercial):

   ```text
   Analiza detalladamente los datos de la tabla de escenarios de Inversiones Industriales S.A.S. ¿Qué variable de entrada (Tasa de Conversión, CAC, Costo Operativo o Inversión Inicial) tiene la mayor influencia porcentual en el 'Margen (%)' cuando pasamos de un escenario Base a uno Pesimista? Identifica cuáles variables clave deberíamos validar prioritariamente con el cliente antes de la propuesta formal.
   ```

3. Evalúe detenidamente la respuesta redactada por Copilot en el chat.
4. Copie los puntos estratégicos devueltos por la IA y péguelos temporalmente en una celda en blanco debajo de su tabla (por ejemplo, en el rango `A7:D12`) para que queden guardados como comentarios estratégicos para la fase posterior de PowerPoint.
5. Guarde los cambios ejecutando el comando de guardado rápido (`Ctrl + G` o haga clic en el icono de guardar).

*   **Resultado Esperado:** Copilot devolverá un análisis de texto que identifica la variable con mayor sensibilidad (comúnmente la *Tasa de Conversión* o el *Costo de Adquisición - CAC* debido al peso directo que tiene sobre el volumen de clientes y el ingreso neto). El análisis debe indicar los puntos clave a mitigar.
*   **Verificación:** Compruebe que el texto explicativo de Copilot menciona explícitamente al cliente ficticio *Inversiones Industriales S.A.S.* y destaca el impacto de las variables de costos unitarios de adquisición frente a los ingresos estimados.

---

## Validación y Pruebas

Para garantizar que el modelo de escenarios y la visualización cumplen de manera estricta los criterios técnicos y comerciales requeridos para una posterior defensa ejecutiva ante los analistas del banco, ejecute las siguientes validaciones metodológicas:

### Criterios de Éxito Técnicos
1. **Fórmulas Dinámicas Integras:** Al posicionarse en las celdas de las columnas `Ingreso Neto` y `Margen (%)`, estas deben estar formuladas con la sintaxis `@` correspondiente a tablas inteligentes. No debe haber ningún cálculo con valores fijos escritos directamente a mano (*hardcoded*).
2. **Sincronización:** El libro debe reflejar las dos pestañas de trabajo: una con la tabla matriz de datos de simulación calculada y otra con el gráfico comparativo interactivo provisto por Copilot.

### Caso de Prueba Adversario: Prueba de Resistencia de Datos (Inyección de Error)
Para validar la robustez matemática del modelo de simulación de escenarios generado por Copilot ante información contradictoria o valores extremos de mercado:

1. Modifique temporalmente el valor de **Costo de Adquisición (CAC - COP)** para el *Escenario Pesimista* en su tabla, cambiándolo de la cifra original a un valor extremo: **`$5,000,000 COP`** por cliente.
2. Observe el comportamiento de la columna **Margen (%)**:
   * **Comportamiento Esperado:** El modelo debe recalcularse en tiempo real de manera automática. El Margen (%) del Escenario Pesimista debe desplomarse drásticamente y mostrarse en un valor fuertemente negativo (por ejemplo, menor al `-100%`).
   * **Acción Correctiva con Copilot:** Si las fórmulas estuvieran rotas o los valores fuesen planos, el cálculo no cambiaría. El cambio inmediato confirma que la arquitectura lógica inyectada por Copilot funciona perfectamente.
3. **Reversión del Cambio:** Presione `Ctrl + Z` para devolver el valor de CAC a su número original establecido en el laboratorio anterior para evitar distorsionar el análisis estratégico real de la entrega de propuesta.

---

## Solución de Problemas

A continuación se detallan dos situaciones técnicas comunes que se presentan durante la ejecución de tareas de Copilot en Excel, junto con sus causas raíz y formas de resolución inmediata:

### Problema 1: El panel lateral de Copilot aparece deshabilitado (gris) o se muestra un mensaje que indica que los archivos deben guardarse en la nube.
* **Síntoma:** El botón de Copilot en la pestaña "Inicio" no permite ser presionado, o el chat se abre indicando que solo trabaja con tablas almacenadas en OneDrive.
* **Causa:** El archivo de Excel se encuentra almacenado de forma local directa en la ruta `C:\CopilotLabs\Modulo1` pero no está vinculado activamente con una cuenta de almacenamiento en la nube activa de Microsoft 365 (OneDrive para la Empresa), lo que impide que el motor semántico de Microsoft Graph acceda al archivo para la edición compartida.
* **Solución:** 
  1. En Excel, vaya a **Archivo** > **Guardar como**.
  2. Seleccione su cuenta corporativa de **OneDrive - Bancolombia** (o equivalente de entrenamiento).
  3. Guarde el archivo en dicha ubicación virtual manteniendo el nombre `Analisis_Oportunidad_Bancolombia.xlsx`.
  4. Active la opción **Autoguardado** en la esquina superior izquierda. La funcionalidad de Copilot se activará de forma inmediata.

### Problema 2: Copilot devuelve un mensaje de error diciendo "No se pudo crear el gráfico con los datos actuales" o el gráfico generado aparece totalmente vacío.
* **Síntoma:** La ventana de chat arroja un aviso de fallo al intentar interpretar la tabla para renderizar la visualización de comparación de escenarios.
* **Causa:** La tabla activa tiene celdas con errores sintácticos (como `#¡DIV/0!`, `#¡VALOR!`) o el usuario no ha hecho foco (clic) dentro del cuerpo de la tabla para dar contexto de los datos antes de ejecutar el prompt.
* **Solución:**
  1. Revise que ninguna celda de la tabla contenga errores de cálculo.
  2. Haga clic en una celda central de la tabla (por ejemplo, la celda `B2`).
  3. Vuelva a redactar un prompt más explícito en el chat: `"Selecciona toda la TablaEscenarios y crea un gráfico de columnas agrupadas basado en las columnas Escenario, Ingreso Estimado (COP) e Ingreso Neto"`.

---

## Limpieza

Mantener su entorno de desarrollo organizado es crucial para evitar conflictos de almacenamiento en futuras prácticas. Ejecute las siguientes acciones de cierre:

1. Verifique que la hoja que contiene el gráfico comparativo esté correctamente guardada dentro del libro.
2. Presione `Ctrl + G` para asegurar el guardado de la última versión refinada de **`Analisis_Oportunidad_Bancolombia.xlsx`**.
3. Cierre completamente la aplicación de Microsoft Excel.
4. Conserve el archivo resultante de esta práctica de forma segura en `C:\CopilotLabs\Modulo1\Analisis_Oportunidad_Bancolombia.xlsx`. Este archivo consolidado será el insumo directo para la construcción de la presentación ejecutiva de alto impacto en el siguiente módulo.

---

## Resumen

En esta práctica de laboratorio, hemos transformado un conjunto de proyecciones planas en un modelo comercial interactivo, robusto y automatizado utilizando **Copilot en Excel (Modo Edición)** en solo 8 minutos.

### Puntos Clave Aprendidos:
- **Productividad a través del Modo Edición:** La capacidad de estructurar y formular cálculos dinámicos de columnas completas escribiendo instrucciones en lenguaje natural, agilizando el flujo tradicional de fórmulas de Excel.
- **Narrativa Visual Automatizada:** La generación asistida de un gráfico dinámico comparativo que clarifica la viabilidad comercial y facilita que un ejecutivo de cuenta de Bancolombia evalúe de un vistazo los riesgos de cada escenario.
- **Consultoría de Negocio con IA:** La utilización de prompts de sensibilidad para realizar análisis preliminares de riesgo de variables financieras complejas, sirviendo como insumo estratégico para la toma de decisiones basada en hipótesis comerciales válidas.