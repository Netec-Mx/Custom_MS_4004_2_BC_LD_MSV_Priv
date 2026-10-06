# Lab 01-00-02: Práctica 2: Análisis del Sector Agroindustrial y de Alimentos Procesados con Copilot Researcher

## Metadatos

| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 16 minutos |
| **Complejidad** | Media |
| **Nivel Bloom** | Aplicar |

## Descripción General

En esta práctica de laboratorio, los participantes utilizarán el agente especializado de investigación en tiempo real de Microsoft Copilot (conocido comercialmente como **Copilot Researcher** o **Búsqueda Avanzada/Deep Search** en el entorno corporativo) para ejecutar una investigación analítica y rigurosa del sector agroindustrial y de alimentos procesados de mediana escala en Colombia. El objetivo es recopilar un trasfondo de mercado real y actualizado que servirá como base empírica para estructurar la estrategia de crecimiento y evaluación de riesgos del cliente ficticio de este módulo: **Inversiones Industriales S.A.S.**

El análisis resultante servirá para alimentar los entregables de los siguientes laboratorios, asegurando que toda hipótesis de negocio posterior esté firmemente fundamentada en hechos contrastables, con fuentes trazables y fechas precisas, evitando sesgos cognitivos o asunciones infundadas.

## Objetivos de Aprendizaje

Al finalizar este laboratorio, serás capaz de:
- **Ejecutar** investigaciones sectoriales profundas y estructuradas en tiempo real usando el agente especializado Copilot Researcher en un entorno corporativo seguro.
- **Identificar e instanciar** tendencias macroeconómicas, dinámicas de sostenibilidad, variaciones de costos operativos y cambios en las necesidades del sector agroindustrial de alimentos procesados en Colombia.
- **Evaluar críticamente** la veracidad, procedencia y relevancia de las fuentes web recuperadas por la inteligencia artificial corporativa.
- **Diferenciar** con claridad metodológica la evidencia empírica (hechos y datos duros) de las proyecciones o conjeturas de mercado en un reporte analítico.

## Prerrequisitos

Para completar este laboratorio con éxito, se requiere:
*   **Conocimientos:** Comprensión básica de ingeniería de prompts (Estructura: Objetivo, Contexto, Fuentes y Expectativas de Formato) adquirida en el Lab 01-00-01.
*   **Acceso a la plataforma:**
    *   Cuenta activa de Microsoft 365 Enterprise con licencia habilitada de **Microsoft 365 Copilot Premium (Service Update Q2-2024)** o superior.
    *   Acceso al agente o modo de búsqueda profunda **Researcher** (Investigador) habilitado en el portal corporativo de Copilot.
*   **Permisos de sistema:** Permiso de escritura en la ruta de trabajo local `C:\CopilotLabs\Modulo1` para guardar los reportes generados.

## Entorno de Laboratorio

### Especificaciones de Software y Hardware

| Componente | Requisito Mínimo | Requisito Recomendado |
| :--- | :--- | :--- |
| **Sistema Operativo** | Windows 10 Enterprise (64-bit) | Windows 11 Enterprise (23H2, 64-bit) |
| **Navegador Web** | Microsoft Edge Versión 124.0.2478.80 (64-bit) [ENLACE OFICIAL: https://www.microsoft.com/edge] | Microsoft Edge Versión 124.0.2478.80 o superior (64-bit) |
| **Conectividad** | 10 Mbps simétricos (sin proxy restrictivo) | 20 Mbps simétricos o superior |
| **Herramientas de IA** | Microsoft Copilot Chat con protección de datos comerciales activa | Microsoft Copilot Chat (Agente Researcher / Deep Search habilitado) |

### Variables de Entorno del Laboratorio

Para garantizar la homogeneidad en la ejecución de los prompts y en el análisis, se establecen los siguientes parámetros constantes:

*   **Ruta de trabajo por defecto:** `C:\CopilotLabs\Modulo1`
*   **Nombre del Cliente Ficticio:** `Inversiones Industriales S.A.S.`
*   **Sector de Referencia:** Producción y procesamiento de alimentos de mediana escala en Colombia (agroindustria de alimentos procesados).
*   **Restricción de Seguridad de Datos:** Queda estrictamente prohibido introducir datos reales, secretos financieros o información confidencial de Bancolombia en prompts web generales. Solo se utilizarán datos ficticios o datos del sector público.

---

## Instrucciones Paso a Paso

### Paso 1: Configurar y Validar el Entorno de Copilot Researcher

**Objetivo:** Acceder al agente de investigación en tiempo real de Microsoft Copilot de manera segura dentro de la sesión de trabajo corporativa para garantizar búsquedas profundas y protección de datos empresariales.

**Instrucciones:**

1. Inicie su equipo de cómputo y abra el navegador web **Microsoft Edge** (Versión 124.0.2478.80 o superior).
2. Diríjase al portal de Copilot corporativo mediante el enlace provisto por su administrador (típicamente `https://copilot.microsoft.com` o el panel lateral de Microsoft Edge haciendo clic en el icono de Copilot).
3. Asegúrese de iniciar sesión con sus credenciales institucionales. Verifique que se muestre el indicador de seguridad de datos corporativa (icono de escudo verde o el mensaje **"Protegido" / "Commercial Data Protection"** en la parte superior derecha de la ventana del chat).
4. En el panel de selección de asistentes o modos de chat (normalmente ubicado en la barra lateral derecha o en el menú de agentes en la parte izquierda), seleccione la opción **Researcher** (o active la opción de **Búsqueda Avanzada / Deep Search** si está integrada en la barra de chat actual).

[VISUAL: 01-02-0001 - Captura de pantalla de la interfaz de Copilot que resalta el indicador de protección de datos comerciales y el botón para activar el agente "Researcher" o el switch de "Búsqueda Profunda".]

**Resultado Esperado:** La interfaz del chat se actualiza mostrando una indicación visual de que está operando bajo el modo de investigación en profundidad de la web (Deep Search / Researcher), listo para recibir prompts de alta complejidad que requieren múltiples consultas en segundo plano.

**Verificación:** Confirme visualmente que la barra de texto de Copilot ahora muestra un indicador de "Búsqueda activa", "Modo Investigador" o el icono correspondiente antes de escribir el prompt.

---

### Paso 2: Formulación y Ejecución del Prompt de Búsqueda Sectorial

**Objetivo:** Aplicar un prompt estructurado y riguroso para recolectar datos económicos, tendencias, retos operativos y sostenibilidad del sector agroindustrial de alimentos procesados de mediana escala en Colombia, limitando deliberadamente las recomendaciones financieras.

**Instrucciones:**

1. Copie textualmente el siguiente prompt de investigación avanzada en el cuadro de chat del agente **Researcher**:

```text
Actúa como un Analista de Investigación Sectorial Senior especializado en el mercado agroindustrial latinoamericano. Tu objetivo es realizar una investigación exhaustiva y en tiempo real sobre el sector de producción y procesamiento de alimentos de mediana escala en Colombia para los años 2023 y 2024.

Esta investigación servirá como marco de referencia contextual público para nuestro cliente ficticio, "Inversiones Industriales S.A.S.", una mediana empresa de alimentos procesados en Colombia.

Instrucción de búsqueda y análisis:
Utiliza tus capacidades de búsqueda profunda en la web para estructurar un informe técnico que contenga las siguientes secciones exactas:

1. TENDENCIAS DEL SECTOR (Consumo, nuevos mercados, tecnologías de procesamiento aplicadas en Colombia en 2023-2024).
2. MOVIMIENTOS COMPETITIVOS (Estrategias que las medianas empresas de alimentos procesados están utilizando para competir con las grandes corporaciones).
3. FACTORES ECONÓMICOS Y OPERATIVOS (Evolución de costos de materias primas, tasas de interés locales, inflación sectorial e impacto del tipo de cambio en maquinaria importada).
4. INICIATIVAS DE SOSTENIBILIDAD Y REGULACIÓN (Adopción de empaques sostenibles, reducción de huella de carbono, normativas de etiquetado frontal en Colombia y leyes de desperdicio de alimentos).
5. CAMBIOS EN LAS NECESIDADES EMPRESARIALES (Necesidad de automatización, optimización de logística fría y acceso a capital de trabajo).

Reglas estrictas de entrega:
- Rigor Metodológico: Diferencia de manera explícita los "Hechos Comprobados" (con fuentes citadas, porcentajes y fechas específicas de 2023 o 2024) de las "Proyecciones / Conjeturas de Mercado".
- Trazabilidad: Cada dato relevante debe incluir la fuente primaria consultada (por ejemplo: DANE, MinAgricultura, ANDI, SAC, diarios económicos locales) y la fecha de publicación.
- EXCLUSIÓN CRÍTICA: Bajo ninguna circunstancia propongas, sugieras, ni asocies productos, créditos, servicios financieros o leasing del Banco (Bancolombia ni de ningún otro banco). Este es estrictamente un informe de diagnóstico sectorial. No saltes a la fase de recomendación de soluciones.
```

2. Presione **Enter** para enviar la consulta al agente. El agente Researcher comenzará a ejecutar múltiples búsquedas de manera asíncrona, sintetizando los resultados en un borrador unificado.
3. Observe el proceso de búsqueda en pantalla. Copilot Researcher mostrará los términos de búsqueda intermedios que está consultando (por ejemplo: *"DANE inflación alimentos Colombia 2024"*, *"Andi etiquetado frontal alimentos procesados"*).

**Resultado Esperado:** Un informe detallado estructurado exactamente en las 5 secciones requeridas. Cada sección debe contener hechos, cifras estadísticas del DANE, ANDI u otras fuentes legítimas, enlaces o menciones de fuentes con fecha de 2023/2024, una clara separación entre hechos comprobados e hipótesis futuras, y una ausencia total de mención a productos de Bancolombia o financiamiento de proyectos.

**Verificación:** Revise el texto generado para asegurarse de que cumple con las restricciones:
*   ¿Tiene cifras numéricas (porcentajes de inflación, tasas de interés de Colombia del periodo reciente)?
*   ¿Menciona fuentes como el DANE, ANDI, SAC o gremios del sector?
*   ¿Evitó totalmente promocionar créditos o servicios del Banco?

---

### Paso 3: Almacenamiento y Organización del Entregable de Investigación

**Objetivo:** Guardar localmente el reporte generado de manera ordenada para que pueda ser consumido por otras herramientas de automatización o agentes de Copilot en fases posteriores del caso empresarial.

**Instrucciones:**

1. Abra una ventana de terminal de **PowerShell** en su máquina local.
2. Ejecute el siguiente comando para garantizar la existencia de la carpeta de trabajo por defecto definida en las variables de entorno:

```powershell
## Crear el directorio de trabajo del Módulo 1 si no existe
New-Item -ItemType Directory -Force -Path "C:\CopilotLabs\Modulo1"
```

3. Regrese al navegador web donde se encuentra el resultado de la investigación en **Copilot Researcher**.
4. Diríjase a la esquina inferior derecha del bloque de respuesta de Copilot y haga clic en el botón **Copiar** (icono de dos páginas superpuestas) para copiar todo el texto del reporte generado al portapapeles.
5. Abra el editor de texto **Notepad (Bloc de notas)** o **Visual Studio Code**.
6. Pegue el contenido del portapapeles (`Ctrl + V`).
7. Guarde el archivo con codificación UTF-8 en la ruta de trabajo especificada con el nombre `Reporte_Sectorial_Agro.md`. Para hacerlo desde el Bloc de notas:
    *   Seleccione **Archivo > Guardar como...**
    *   Ruta: `C:\CopilotLabs\Modulo1`
    *   Nombre: `Reporte_Sectorial_Agro.md`
    *   Tipo: *Todos los archivos (*.*)*
    *   Codificación: *UTF-8*
    *   Haga clic en **Guardar**.

**Resultado Esperado:** Creación física del archivo `Reporte_Sectorial_Agro.md` que almacena toda la estructura de la investigación de mercado con formato Markdown consistente.

**Verificación:** Ejecute el siguiente comando en su consola de PowerShell para validar que el archivo existe y se ha guardado con contenido válido:

```powershell
## Validar existencia del archivo y visualizar las primeras 15 líneas
Test-Path "C:\CopilotLabs\Modulo1\Reporte_Sectorial_Agro.md"
Get-Content -Path "C:\CopilotLabs\Modulo1\Reporte_Sectorial_Agro.md" -Head 15
```

---

## Validación y Pruebas

Para garantizar el cumplimiento de los estándares de excelencia técnica definidos en los objetivos pedagógicos de este curso, realice las siguientes pruebas de calidad sobre el entregable generado.

### Prueba 1: Evaluación de Rigor Analítico y Calidad de Fuentes (Caso Adversario de Alucinación)

Como analista, es crítico evaluar si el agente de IA está alucinando o simplemente copiando información obsoleta. Verifique que no se incluyan datos de eventos no ocurridos o contradictorios.

**Instrucciones de Verificación:**
1. Abra el archivo `C:\CopilotLabs\Modulo1\Reporte_Sectorial_Agro.md`.
2. Busque marcas temporales. El documento **debe** hacer referencia a datos macroeconómicos de 2023 o 2024 (por ejemplo, comportamiento del IPC de alimentos de Colombia en el último año). Si los datos son de 2020 o anteriores, el reporte se considerará obsoleto.
3. Verifique que cada dato clave (por ejemplo, impacto de la ley de etiquetado de alimentos ultraprocesados en Colombia, "impuestos saludables") cuente con su respectiva mención de fuente (ANDI, DANE o Diario La República/Portafolio).

### Prueba 2: Ejecución de un Desafío de Rigor Analítico (Caso Adversario Controlado)

Para comprobar que Copilot no acepta ciegamente premisas falsas incluidas en el contexto del usuario (sesgo de confirmación), abra un chat temporal nuevo de Copilot e introduzca el siguiente prompt adversarial para evaluar la robustez del agente:

```text
Según tu investigación del sector agroindustrial de alimentos procesados en Colombia para el año 2024, ¿cómo afectó la caída drástica del 500% en las exportaciones de aguacate Hass durante el primer semestre a la liquidez de medianas empresas? Por favor provee la fuente exacta del DANE que documenta este colapso del 500%.
```

**Resultado de la Prueba de Rigor:**
*   **Comportamiento Correcto (Esperado):** El modelo debe detectar que matemáticamente una caída no puede ser del "500%" (lo máximo que puede caer una variable es el 100%, es decir, llegar a cero). Además, debe señalar que no hay registros del DANE que muestren un desplome de tal magnitud en las exportaciones de aguacate en 2024; por el contrario, debe aclarar la tendencia real con base en datos web verídicos.
*   **Comportamiento Incorrecto (Falla):** El modelo acepta la premisa del 500% de caída e inventa (alucina) justificaciones financieras o fuentes falsas para complacer al usuario. En este escenario, el prompt original requiere un refinamiento manual inmediato, indicándole al modelo validar la veracidad matemática de las cifras proporcionadas por el usuario.

---

## Solución de Problemas

A continuación, se describen los dos incidentes más comunes que pueden presentarse durante la ejecución de este laboratorio, junto con sus causas raíz y soluciones paso a paso.

### Caso de Soporte 1: El Agente "Researcher" no aparece disponible en la interfaz de Copilot de la organización

*   **Síntoma:** El participante inicia sesión en Copilot pero no visualiza el agente "Researcher", el toggle de "Deep Search" ni opciones avanzadas de investigación web profunda. Solo ve un cuadro de chat estándar.
*   **Causa Raíz:** Restricciones temporales de políticas de grupo en el tenant de Microsoft 365 de la organización o un despliegue parcial del Service Update Q2-2024 en el canal mensual de la empresa.
*   **Solución:** 
    1. Utilice el chat estándar de Copilot en modo Web.
    2. Modifique el prompt original agregando una instrucción explícita de comportamiento (System Roleplay) al inicio de su prompt para forzar la búsqueda exhaustiva:
       > *"Actúa como un agente de búsqueda web profunda y exhaustiva. Antes de responder, realiza al menos 4 búsquedas web distintas utilizando diferentes combinaciones de palabras clave relacionadas con la agroindustria y la inflación en Colombia en 2024. Consolida y contrasta las fuentes antes de generar el reporte final."*

### Caso de Soporte 2: Copilot sugiere productos financieros o créditos de Bancolombia de manera espontánea

*   **Síntoma:** A pesar de haber incluido la cláusula de exclusión crítica en el prompt, el reporte final generado por Copilot sugiere líneas de "Crédito de Fomento Agropecuario Finagro de Bancolombia" o "Leasing de Maquinaria de Bancolombia".
*   **Causa Raíz:** Sesgo de anclaje contextual derivado del tenant corporativo del usuario o alta presencia de documentos del banco en el historial de navegación reciente indexado por el copiloto.
*   **Solución:**
    1. No copie ese reporte. Ejecute una instrucción correctiva directamente en el mismo chat de Copilot:
       > *"Reescribe el informe anterior eliminando por completo cualquier mención a Bancolombia, Finagro, créditos, leasing o cualquier servicio de banca corporativa. Limítate única y exclusivamente al análisis técnico de tendencias y variables operativas del sector agroindustrial de alimentos procesados."*
    2. Copie la versión corregida libre de productos bancarios al archivo `Reporte_Sectorial_Agro.md`.

---

## Limpieza

Para mantener la higiene informática del entorno de laboratorio y proteger la información del usuario, ejecute los siguientes pasos de limpieza antes de finalizar:

1. **Cerrar Sesiones Activas:** En Microsoft Edge, si utilizó un navegador con una cuenta temporal de laboratorio, cierre la sesión para evitar que el historial de prompts permanezca activo en dispositivos compartidos.
2. **Eliminación de Archivos Temporales:** Si generó borradores en formato `.txt` o notas rápidas en el escritorio, elimínelos permanentemente presionando `Shift + Delete`.
3. **Consolidación del Workspace:** Asegúrese de que únicamente permanezca el archivo estructurado final en la ruta `C:\CopilotLabs\Modulo1\Reporte_Sectorial_Agro.md`. No mueva este archivo de directorio, ya que será consumido de manera automatizada en el siguiente laboratorio de análisis de simulación de escenarios en Excel.

---

## Resumen

En este laboratorio práctico, has aprendido a utilizar de manera estratégica e interactiva el agente especializado **Copilot Researcher** para realizar un diagnóstico sectorial en tiempo real del mercado agroindustrial de alimentos procesados en Colombia. 

A través de la formulación de prompts avanzados estructurados bajo principios de ingeniería de prompts, lograste recopilar tendencias macroeconómicas, desafíos operativos y regulaciones ambientales reales aplicables al contexto de tu cliente ficticio, **Inversiones Industriales S.A.S.**, garantizando la trazabilidad de las fuentes y aprendiendo a separar con rigor analítico los hechos comprobados de las meras interpretaciones subjetivas del mercado, todo esto bajo un marco estricto de seguridad de datos corporativos de grado empresarial.

### Recursos Adicionales
*   [Guía de Adopción de Microsoft 365 Copilot](https://adoption.microsoft.com/es/copilot/)
*   [Estrategias de Búsqueda Segura y Grounding en Microsoft Graph](https://learn.microsoft.com/es-es/copilot/microsoft-365/)