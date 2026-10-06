# Lab 01-00-12: Práctica 12: Simulación de Defensa Comercial (Roleplay) con Microsoft 365 Copilot

## Metadatos
| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 7 minutos |
| **Complejidad** | Media |
| **Nivel de Bloom** | Aplicar |

## Descripción General
En este laboratorio práctico, configurarás una sesión interactiva de juego de roles (*roleplay*) con Microsoft 365 Copilot Chat. El objetivo es simular una reunión de comité donde Copilot asumirá la identidad de Carlos Mendoza, el escéptico Director Financiero (CFO) de la empresa cliente ficticia **Inversiones Industriales S.A.S.** (perteneciente al sector de alimentos procesados y agroindustria en Colombia). 

A través de un diálogo de tres turnos de preguntas y respuestas, defenderás la propuesta comercial financiera de Bancolombia elaborada en los pasos previos del caso de estudio. Al finalizar la interacción, solicitarás una evaluación crítica a la Inteligencia Artificial para mapear los argumentos mitigados exitosamente y detectar las lagunas de información que requieren mayor investigación de campo.

## Objetivos de Aprendizaje
Al finalizar este laboratorio, serás capaz de:
- [ ] Configurar un entorno de simulación dinámico (*roleplay*) en Copilot Chat mediante un prompt de sistema estructurado con variables de contexto comercial.
- [ ] Argumentar y defender propuestas financieras corporativas frente a objeciones simuladas basadas en variables reales de mercado (tasas, plazos, CAPEX/OPEX y retorno de inversión).
- [ ] Evaluar de forma objetiva la solidez de un pitch de ventas analizando el reporte de brechas de datos generado de forma automatizada por el modelo de IA.

## Prerrequisitos
Para realizar de manera óptima este laboratorio, es ideal contar con:
- Familiaridad con el contexto de la propuesta comercial de Bancolombia a la empresa **Inversiones Industriales S.A.S.** (financiamiento de 1,200 millones de COP para modernización de cadena de frío y expansión de planta de procesamiento).
- Acceso activo a la interfaz de chat empresarial de Microsoft 365 Copilot.

## Entorno de Laboratorio
El entorno requerido se compone de los siguientes elementos de hardware y software:

### Requisitos de Hardware
| Componente | Especificación Mínima |
| :--- | :--- |
| **Procesador** | Arquitectura de 64 bits (mínimo 2 núcleos a 1.6 GHz) |
| **Memoria RAM** | Mínimo 8 GB (16 GB recomendado para multitarea fluida) |
| **Resolución de pantalla** | Mínimo 1280 x 768 píxeles |
| **Conectividad** | Conexión a internet de banda ancha (mínimo 10 Mbps simétricos) |

### Requisitos de Software y Licencias
| Software / Servicio | Versión de Referencia | Enlace de Descarga / Acceso |
| :--- | :--- | :--- |
| **Navegador Web** | Microsoft Edge (124.0.2478.80) x64 | [https://www.microsoft.com/es-es/edge](https://www.microsoft.com/es-es/edge) |
| **Licenciamiento** | Microsoft 365 Copilot Premium (Service Update Q2-2024) con acceso a Chat Corporativo habilitado | [https://learn.microsoft.com/es-es/copilot/microsoft-365/](https://learn.microsoft.com/es-es/copilot/microsoft-365/) |

### Constantes de Entorno
- **Directorio de Trabajo local:** `C:\CopilotLabs\Modulo1`
- **Nombre del Cliente Ficticio:** `Inversiones Industriales S.A.S.`
- **Sector Empresarial:** Alimentos procesados y sector agroindustrial de mediana escala en Colombia.

---

## Instrucciones Paso a Paso

### Paso 1: Configuración del Entorno y Activación del Rol del Directivo
**Objetivo**: Establecer las instrucciones de sistema en el entorno de chat de Copilot para inicializar el personaje de simulación y definir las reglas del ejercicio.

1. Abre tu navegador web **Microsoft Edge (124.0.2478.80) x64**.
2. Dirígete a la URL oficial de chat corporativo de Microsoft: [https://copilot.microsoft.com](https://copilot.microsoft.com). Asegúrate de iniciar sesión con tu cuenta organizativa (la cual cuenta con la licencia de *Microsoft 365 Copilot Premium* activada) para garantizar la protección de datos comerciales.
3. Copia textualmente el siguiente prompt de configuración del rol y pégalo en la barra de chat de Copilot:

```text
Actúa como Carlos Mendoza, el Director Financiero (CFO) de "Inversiones Industriales S.A.S.", una empresa colombiana mediana de alimentos procesados y agroindustria. Hoy te reúnes con el equipo de banca corporativa de Bancolombia, quienes te presentan una propuesta para financiar la modernización de la cadena de frío y ampliación de planta por un valor de 1,200 millones de COP.

Como CFO, eres sumamente escéptico, analítico, enfocado en el flujo de caja, el impacto de las tasas de interés (indexadas a la IBR o IPC), el periodo de recuperación (ROI), la viabilidad operativa y los riesgos de endeudamiento a mediano plazo frente a la volatilidad del sector agroindustrial colombiano.

Reglas del ejercicio:
1. Debes hacerme exactamente 3 preguntas difíciles, pero una a la vez. No pases a la siguiente pregunta hasta que yo responda a la anterior.
2. Cada pregunta debe centrarse en un aspecto crítico de la propuesta (ej. Costo del financiamiento vs. alternativas de mercado, riesgos de la cadena de frío, o flujo de caja para cubrir amortizaciones).
3. Mantén en todo momento un tono corporativo, educado, realista y muy riguroso.
4. Al final (después de mi tercera respuesta), saldrás del personaje de Carlos Mendoza y me darás una evaluación analítica bajo la etiqueta [EVALUACIÓN]: indicando qué objeciones respondí adecuadamente con datos empíricos y cuáles carecieron de sustento técnico o requieren más datos de soporte del portafolio Bancolombia.

Comienza presentándote brevemente como Carlos Mendoza y lanza tu primera pregunta.
```

4. Presiona la tecla **Enter** o haz clic en el botón de enviar consulta.

*   **Resultado esperado**: Copilot responderá asumiendo el rol de Carlos Mendoza, dando un saludo formal de bienvenida al comité y formulando la **primera pregunta dura** sobre el financiamiento agroindustrial. El tono será profesional y restrictivo.
*   **Verificación**: Confirma que el chat inició bajo el nombre de Carlos Mendoza, CFO de Inversiones Industriales S.A.S., y que solo generó *una única pregunta* en lugar de una lista masiva.

---

### Paso 2: Simulación del Juego de Roles (Roleplay de 3 Turnos)
**Objetivo**: Enfrentar y mitigar activamente los cuestionamientos del CFO utilizando argumentos financieros razonados, tasas realistas del mercado colombiano y justificaciones basadas en mejoras de eficiencia operativa.

1. Lee detenidamente la primera pregunta planteada por el CFO simulado de Copilot.
2. Redacta tu respuesta en el cuadro de chat. Si la pregunta cuestiona las tasas de interés o la viabilidad del proyecto de cadena de frío (1,200 millones de COP), utiliza la siguiente información como soporte estratégico de la simulación:
   * **Propuesta Financiera:** Crédito comercial agroindustrial con tasa preferencial indexada a la IBR + 2.5% EA, con un plazo de 60 meses y un periodo de gracia a capital de 6 meses para alinearse con la fase de construcción de la planta.
   * **Beneficio Operativo:** La nueva infraestructura reducirá la pérdida de inventario por ruptura de frío en un 22%, incrementando el margen bruto de la empresa de manera inmediata tras la entrega de la obra física.
3. Envía tu primera respuesta.
4. Espera a que Copilot evalúe la entrada bajo su rol y te formule la **segunda pregunta** (por ejemplo, cuestionando la garantía del proyecto o el flujo de caja operativo).
5. Responde al segundo cuestionamiento argumentando solidez financiera (ej. uso de garantías del Fondo Nacional de Garantías - FNG o flujos de caja proyectados que demuestran una cobertura del servicio de la deuda - DSCR superior a 1.35x). Envía tu respuesta.
6. Copilot procesará la información y emitirá su **tercera y última pregunta** (normalmente enfocada en riesgos macroeconómicos de la agroindustria o alternativas de competencia bancaria).
7. Responde este tercer cuestionamiento con un argumento sólido de resiliencia sectorial o acompañamiento experto de Bancolombia (ej. coberturas de tasa de interés para protegerse de incrementos en la IBR). Envía tu respuesta.

*   **Resultado esperado**: El chat guiará al usuario secuencialmente turno por turno. Cada respuesta tuya desbloqueará una nueva réplica corporativa del CFO artificial hasta completar el ciclo programado de 3 interacciones.
*   **Verificación**: Comprueba que has cubierto los 3 turnos de preguntas y respuestas sin salirte del tema financiero del proyecto.

---

### Paso 3: Solicitud de Evaluación de Desempeño y Retroalimentación Estratégica
**Objetivo**: Finalizar el juego de roles para extraer el reporte analítico de fortalezas de la propuesta comercial y debilidades de sustentación del participante.

1. Una vez enviada tu tercera respuesta, si Copilot no inicia la retroalimentación de manera automática, escribe el siguiente prompt de cierre en la barra de chat:

```text
Hemos concluido la simulación de 3 turnos. Por favor, sal del personaje de Carlos Mendoza y genera ahora la [EVALUACIÓN] estructurada que acordamos al principio, identificando:
1. Objeciones bien mitigadas por mi parte y por qué fueron sólidas (los aciertos de la defensa).
2. Brechas de información: Puntos débiles donde mi respuesta careció de soporte empírico cuantitativo o técnico financiero.
3. Lista de 3 datos específicos del portafolio o balance de Bancolombia que necesito investigar antes de la reunión real con un cliente de esta escala en Colombia.
```

2. Presiona **Enter** para enviar la instrucción final.

*   **Resultado esperado**: Copilot suspenderá el personaje del CFO y desplegará un análisis técnico pormenorizado en formato de informe estructurado. El reporte señalará los éxitos en la estrategia de ventas y listará puntualmente los datos faltantes o que requieren investigación en la estructura real de riesgos del banco.
*   **Verificación**: Asegúrate de que el bloque final cuente con la etiqueta de `[EVALUACIÓN]` y las tres subsecciones de análisis y recomendaciones solicitadas en el prompt.

---

## Validación y Pruebas
Para validar que el juego de roles y la autoevaluación se realizaron con el estándar de calidad técnico requerido para un asesor empresarial, efectúa la siguiente lista de chequeo de validación:

### Criterios de Evaluación y Calificación del Laboratorio
1. **Consistencia de la Simulación**: Copilot mantuvo el personaje ficticio asignado (CFO, escéptico, lenguaje corporativo colombiano) de forma ininterrumpida durante los 3 turnos iniciales.
2. **Defensa Argumentada**: El estudiante incorporó conceptos reales del caso como tasa IBR, montos (1,200M COP), amortización, periodo de gracia o reducción de mermas en frío (22%) dentro de sus respuestas de texto.
3. **Generación del Reporte**: El entregable final contiene una evaluación estructurada que distingue nítidamente los argumentos empíricos expuestos de aquellos supuestos que necesitan mayor investigación de campo en el portafolio Bancolombia.

### Caso de Prueba Adversario (Prueba de Estrés del Modelo)
Si durante la interacción el usuario intenta "hacer trampa" o inventar datos absurdos (por ejemplo, ofrecer una tasa de interés del 0% de forma indefinida, o prometer subsidios estatales de los cuales no hay registro oficial en la propuesta), el comportamiento esperado de Copilot (Carlos Mendoza) debe ser el siguiente:
* El CFO ficticio debe identificar inmediatamente la inconsistencia financiera y cuestionarla severamente como "poco realista para el contexto macroeconómico de Colombia", elevando el nivel de escepticismo de la simulación.

*¿Cómo verificarlo?* Intenta ingresar un dato erróneo intencionadamente en el Turno 2 (ej. *"Te ofrezco una tasa fija del 1% anual en pesos por 10 años"*). Observa cómo reacciona el modelo. Deberá responder refutando la viabilidad económica de dicha oferta de tasa.

---

## Solución de Problemas

### Problema 1: Copilot genera las 3 preguntas al mismo tiempo en lugar de una a la vez
* **Síntoma**: Al enviar el primer prompt de configuración, la IA lista las 3 preguntas en una sola respuesta, rompiendo la dinámica de turno por turno de la simulación de venta.
* **Causa**: Limitación en la ventana de contexto o procesamiento del parser de instrucciones del LLM en ese momento.
* **Solución**: Responde directamente a la primera de las tres preguntas impresas e instruye a la IA a retomar las reglas: *"Carlos, responderé primero a tu pregunta 1 [escribe tu respuesta]. Por favor, no pases a formular o detallar las siguientes hasta que terminemos de debatir este punto comercial."*

### Problema 2: El modelo pierde el personaje antes del Turno 3 y responde como el asistente de Microsoft
* **Síntoma**: En el Turno 2 o 3, Copilot responde con frases genéricas como *"Como tu asistente de inteligencia artificial, puedo ayudarte a calcular..."* en lugar del tono corporativo del CFO Carlos Mendoza.
* **Causa**: Sobrescritura de contexto o pérdida de memoria conversacional (límite de tokens en la sesión activa).
* **Solución**: Introduce un prompt correctivo rápido: *"Recuerda que sigues en el papel de Carlos Mendoza, CFO escéptico de Inversiones Industriales S.A.S., y estamos en el turno de debate número [X]. Formúlame tu siguiente objeción desde tu rol financiero."*

---

## Limpieza
Al tratarse de una simulación interactiva basada en el entorno web de Copilot Chat, la eliminación de los rastros de la conversación y la protección de datos es inmediata mediante los siguientes pasos:

1. En la esquina superior derecha o inferior de la barra de chat activa de Copilot en el navegador, haz clic en el icono de **"Nuevo tema"** o **"Limpiar chat"** (icono de escoba o pincel) para purgar la memoria contextual de la sesión en ejecución.
2. Cierra la pestaña de navegación activa de `copilot.microsoft.com`.
3. Si descargaste alguna minuta de texto de la simulación de forma local en `C:\CopilotLabs\Modulo1`, puedes conservarla con el nombre `Evidencia_Práctica_12_Roleplay.txt` o eliminarla permanentemente seleccionando el archivo y presionando `Shift + Delete`.

---

## Resumen
En esta práctica de laboratorio, has empleado con éxito capacidades avanzadas de ingeniería de prompts e interacción con IA generativa mediante el uso de **Microsoft 365 Copilot Chat**:

* **Entrenamiento Conversacional**: Estableciste una simulación de juego de roles adaptada a la realidad corporativa de un cliente de la agroindustria colombiana (**Inversiones Industriales S.A.S.**), forzando una interacción dinámica y no lineal.
* **Habilidad de Defensa Comercial**: Tuviste la oportunidad de argumentar y defender bajo presión corporativa simulada las características clave del financiamiento de 1,200 millones de COP de Bancolombia, como tasas, periodos de gracia y amortizaciones.
* **Análisis de Brechas (Gap Analysis)**: Extrajiste un informe técnico que identificó los puntos fuertes defendidos y, más importante aún, las lagunas en la información financiera comercial del vendedor, facilitando la mejora continua de la propuesta antes de presentarla en un comité de toma de decisiones real.

### Recursos Adicionales y Enlaces Oficiales
* [Guía de Adopción de Microsoft 365 Copilot en Ventas](https://adoption.microsoft.com/es/copilot/)
* [Documentación Oficial de Grounding en Microsoft Graph](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-overview)
* [Centro de Recursos para Clientes de Banca Corporativa de Bancolombia](https://www.bancolombia.com/empresas) (Usar solo de referencia general para políticas de crédito comercial).