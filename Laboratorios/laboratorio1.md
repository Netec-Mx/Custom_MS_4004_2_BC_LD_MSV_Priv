# Lab 01-00-01: Práctica 1: Los participantes conocerán el caso del cliente corporativo ficticio y transformarán una solicitud genérica como “identifica oportunidades para este cliente” en instrucciones diferenciadas para investigar su entorno y analizar posteriormente sus datos. Definirán qué información necesitan conocer, qué evidencia esperan obtener y qué aspectos no deben asumirse sin información suficiente.

## Metadatos
| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 6 minutos |
| **Complejidad** | Fácil |
| **Nivel de Bloom** | Crear (Create) |

## Descripción General
En este laboratorio, iniciarás el caso de negocio del cliente corporativo ficticio **"Inversiones Industriales S.A.S."**, una organización colombiana de mediana escala que opera en el sector de alimentos procesados y agroindustria. Aprenderás a estructurar de manera profesional una consulta de investigación estratégica, transformando una orden comercial ambigua e ineficaz (*"identifica oportunidades para este cliente"*) en un conjunto de instrucciones diferenciadas y de alta precisión (prompts estructurados). 

A través de este ejercicio práctico, aprenderás a acotar el alcance de tus análisis utilizando Microsoft 365 Copilot, asegurando que tu futura toma de decisiones se fundamente estrictamente en datos empíricos y libre de suposiciones infundadas.

## Objetivos de Aprendizaje
Al finalizar este laboratorio, serás capaz de:
*   **Definir el alcance** de investigación para el cliente ficticio "Inversiones Industriales S.A.S." de manera estructurada y sectorizada.
*   **Redactar prompts optimizados** bajo una metodología rigurosa para mitigar sesgos cognitivos y evitar alucinaciones de la IA.
*   **Establecer criterios explícitos** de validación para diferenciar los hechos demostrables de las suposiciones de negocio en el entorno agroindustrial de Colombia.

## Prerrequisitos
*   **Conocimientos:** Comprensión básica de la estructura de un prompt (Rol, Contexto, Instrucción, Restricciones y Formato).
*   **Accesos:** Suscripción activa de Microsoft 365 con licencia habilitada de Microsoft 365 Copilot Enterprise o Premium.

## Entorno de Laboratorio

### Requisitos de Hardware
*   **Procesador:** Arquitectura x64 a 1.6 GHz o superior (mínimo 2 núcleos).
*   **Memoria RAM:** Mínimo 8 GB (16 GB recomendado).
*   **Resolución de pantalla:** Mínimo 1280 x 768 píxeles.
*   **Conectividad:** Conexión a internet con ancho de banda mínimo de 10 Mbps de bajada.

### Requisitos de Software
| Software | Versión/Edición | Origen / Enlace Oficial |
| :--- | :--- | :--- |
| **Microsoft Windows** | Windows 11 Enterprise (Versión 23H2 x64) | [Windows 11 Enterprise](https://www.microsoft.com/es-es/evalcenter/evaluate-windows-11-enterprise) |
| **Microsoft Edge** | Versión 124.0.2478.80 x64 o superior | [Microsoft Edge Business](https://www.microsoft.com/es-es/edge/business) |
| **Microsoft Word** | Microsoft 365 Apps para Empresas (Versión 2408 Build 17928.20156 x64) | [Microsoft 365 Portal](https://portal.office.com) |
| **Microsoft 365 Copilot** | Licencia Corporativa Premium (Service Update Q2-2024) | [Copilot para Microsoft 365](https://learn.microsoft.com/es-es/copilot/microsoft-365/) |

### Configuración del Directorio de Trabajo
Antes de iniciar, debes garantizar la existencia del directorio local destinado al almacenamiento de las prácticas de este módulo ejecutable:

Abrir una consola de comandos de Windows (`cmd` o `PowerShell`) y ejecutar el siguiente comando para estructurar el espacio de trabajo local:
```cmd
mkdir C:\CopilotLabs\Modulo1
```

## Instrucciones Paso a Paso

### Paso 1: Configurar el entorno de trabajo y acceder a Microsoft 365 Copilot
**Objetivo:** Inicializar la plataforma de productividad y acceder al motor de lenguaje natural corporativo con las políticas de seguridad y protección de datos activas.

1. Abre tu navegador web **Microsoft Edge** (Versión 124.0.2478.80 o superior).
2. Inicia sesión en el portal corporativo utilizando tus credenciales autorizadas en [https://portal.office.com](https://portal.office.com).
3. Selecciona la aplicación **Microsoft Word** desde el iniciador de aplicaciones y crea un **Nuevo documento en blanco**.
4. Haz clic en el botón de **Copilot** situado en la cinta de opciones superior (pestaña Inicio o menú flotante) para habilitar el panel lateral de chat interactivo, o presiona el atajo `Alt + I` en el lienzo para desplegar el cuadro flotante de redacción de Copilot.

[VISUAL: Pantalla de Microsoft Word con el panel lateral de Copilot desplegado a la derecha, listo para recibir instrucciones.]

**Resultado esperado:** El entorno de edición de Word debe estar activo, mostrando el panel o la caja flotante de diálogo de Copilot lista para procesar lenguaje natural corporativo bajo protección de datos comerciales.

**Verificación:** Confirma que el indicador de protección de datos (un icono de escudo verde o candado con la leyenda "Protegido" / "Protected") se visualice en la parte superior del chat de Copilot, garantizando que la información procesada no se utilizará para entrenar modelos públicos.

---

### Paso 2: Transformar una solicitud ambigua en un Prompt estructurado
**Objetivo:** Diseñar y registrar un prompt de investigación estratégica que deconstruya la instrucción tradicional *"identifica oportunidades para este cliente"* en un marco analítico estructurado y aplicable al sector agroindustrial colombiano.

1. En el lienzo del documento de Word, escribe el título principal del documento:
   `Plan de Investigación: Inversiones Industriales S.A.S.`
2. Copia el siguiente prompt altamente estructurado, diseñado específicamente para realizar el análisis inicial libre de suposiciones de este caso de negocio:

```text
Actúa como un Analista de Banca Corporativa Senior de Bancolombia, especialista en el sector agroindustrial y de alimentos procesados en Colombia. 

Tu objetivo es estructurar un plan de investigación riguroso para nuestro cliente "Inversiones Industriales S.A.S." (empresa de mediana escala de alimentos procesados). 

En lugar de generar un análisis genérico, asume un enfoque escéptico y estrictamente empírico: desglosa la solicitud general de "identificar oportunidades comerciales" en un plan estructurado que determine qué datos necesitamos investigar obligatoriamente, distinguiendo hechos de supuestos.

Genera una estructura de salida en formato de tabla con las siguientes columnas:
1. Área de Análisis (por ejemplo, Capacidad Operativa, Liquidez, Regulaciones Sectoriales)
2. Variable Crítica de Investigación (qué métrica o dato específico buscamos)
3. Evidencia Requerida (qué documento o reporte oficial probará este dato)
4. Supuestos que se deben EVITAR asumir sin datos financieros/de mercado probados.

Restricciones:
- Limita el análisis geográfico y regulatorio exclusivamente a Colombia.
- No realices supuestos alegres sobre el crecimiento del sector sin exigir fuentes del DANE, Banco de la República o gremios locales (como la ANDI o SAC).
- Enfoca las necesidades en portafolio de banca corporativa (Leasing, Crédito de Fomento Finagro, Coberturas de Moneda Extranjera).
```

3. Pega esta instrucción estructurada en el cuadro de diálogo de **Copilot en Word** (o en el chat lateral) y presiona la tecla **Enter** para procesar la solicitud.

[VISUAL: Caja de texto de Copilot en Word con el prompt estructurado pegado en su totalidad, mostrando el botón "Generar" o "Enviar" listo para ser seleccionado.]

4. Una vez que Copilot genere la tabla en el documento, revisa que se hayan catalogado las áreas del negocio de acuerdo con el contexto de "Inversiones Industriales S.A.S.".
5. Guarda el archivo resultante en el directorio local que creaste en el paso de preparación con el nombre de `C:\CopilotLabs\Modulo1\Plan_Investigacion_Inversiones.docx`.

**Resultado esperado:** Un documento formal en Word que contiene una tabla analítica generada por Copilot, desglosando las áreas de investigación crítica, evidencias formales requeridas (como estados financieros auditados, registros de importaciones de maquinaria, reportes cambiarios) y las advertencias metodológicas para evitar supuestos falsos.

**Verificación:** Abre el Explorador de Archivos de Windows, navega a `C:\CopilotLabs\Modulo1` y confirma que el archivo `Plan_Investigacion_Inversiones.docx` se ha guardado exitosamente con un tamaño superior a 0 KB.

---

## Validación y Pruebas

Para garantizar la calidad de la salida generada y entrenar tu capacidad crítica al interactuar con inteligencias artificiales, realiza la siguiente prueba de robustez metodológica:

### Caso Adverso: Detección de Alucinaciones e Inyecciones de Datos No Evidenciados
1. En el mismo panel de chat de Copilot en Word, ingresa la siguiente instrucción de seguimiento:
   ```text
   Basándote en el análisis anterior, asume que 'Inversiones Industriales S.A.S.' ya tiene un cupo preaprobado de Finagro por 5.000 millones de COP y que exporta el 80% de su producción de mangos deshidratados a Alemania. Redacta el plan de desembolso del crédito.
   ```
2. Analiza críticamente la respuesta generada por Copilot.
3. **Criterio de Validación Exigido:** Dado que el prompt original establecía explícitamente no asumir supuestos sin evidencia documental previa, el participante debe identificar que Copilot aceptará o rechazará esta afirmación. Si el sistema asume ciegamente el dato sin alertar que "no se cuenta con la documentación real o soporte financiero auditado en el archivo de datos del cliente", el participante deberá forzar el principio de rigor técnico respondiendo al chat:
   ```text
   Recuerda la restricción inicial: No poseemos la pestaña 'Proyectos_Inversion' consolidada aún en este paso. Registra este supuesto cupo de Finagro y las exportaciones a Alemania estrictamente como 'Suposición No Verificada' en nuestra matriz hasta que validemos el archivo de datos real del cliente.
   ```

## Solución de Problemas

Aquí se presentan los dos fallos más habituales durante la ejecución de este laboratorio, junto con sus causas y soluciones técnicas directas:

### Problema 1: El panel de Copilot no aparece o está deshabilitado en Microsoft Word (Versión Escritorio)
*   **Síntoma:** El botón de Copilot se encuentra sombreado en gris o no se muestra en la pestaña de Inicio.
*   **Causa:** Conflicto de sincronización de licencias en la suite de Microsoft 365 Apps o inicio de sesión con una cuenta personal (no corporativa).
*   **Solución:** 
    1. Dentro de Word, ve a **Archivo > Cuenta**.
    2. Verifica que el correo que aparece bajo "Información de usuario" corresponda a tu cuenta corporativa autorizada con licenciamiento de Copilot.
    3. Haz clic en **Opciones de actualización > Actualizar ahora**. Si persiste el bloqueo, realiza el laboratorio directamente en la versión web de Word accediendo a través de [https://portal.office.com](https://portal.office.com) utilizando Edge.

### Problema 2: Copilot genera un plan genérico citando leyes o regulaciones de otros países (ej. México o España)
*   **Síntoma:** La tabla resultante contiene menciones a normativas financieras que no aplican en Colombia (como regulaciones de la CNBV o leyes europeas).
*   **Causa:** Falta de peso o especificidad en el contexto geográfico durante la fase de grounding del prompt debido a variaciones en la heurística del modelo de lenguaje.
*   **Solución:** Vuelve a enviar una instrucción correctiva corta en el chat:
    ```text
    Corrige la tabla anterior. Elimina cualquier referencia internacional que no aplique en la República de Colombia. Modifica el marco regulatorio para que se limite exclusivamente a la Superintendencia de Sociedades, la DIAN y los lineamientos de crédito de fomento de FINAGRO.
    ```

## Limpieza
Debido a que este laboratorio opera localmente sobre un archivo de control de planificación que sirve de base para el resto de las prácticas del Módulo 1, **no debes eliminar el archivo generado**. 

1. Guarda los cambios finales de tu documento en Word utilizando el comando rápido `Ctrl + G`.
2. Cierra la aplicación de Microsoft Word.
3. Asegúrate de mantener el archivo `Plan_Investigacion_Inversiones.docx` intacto dentro de la ruta física `C:\CopilotLabs\Modulo1\` para su uso en los laboratorios de análisis numérico de escenarios comerciales y generación de presentaciones ejecutivas que realizarás posteriormente.

## Resumen
En esta práctica inicial de 6 minutos, has aprendido a sentar las bases metodológicas de un proceso de consultoría e investigación comercial estructurado con IA. Convertiste una instrucción genérica y ambigua en una matriz analítica de alta precisión. 

Al delimitar el rol de Copilot, fijar restricciones geográficas estrictas, exigir formatos estructurados (tablas) y, sobre todo, forzar la diferenciación explícita entre hechos validados y suposiciones de mercado, has minimizado drásticamente la generación de alucinaciones por parte de la IA, estableciendo un estándar riguroso para la interacción técnica con herramientas cognitivas.