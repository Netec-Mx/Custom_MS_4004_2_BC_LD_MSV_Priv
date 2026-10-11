# Laboratorio 6: Preparar y poner a prueba la conversación con el cliente

**Duración:** 20 min

## Descripción
Práctica 1: Los participantes solicitarán a Copilot preparar un breve speech ejecutivo para presentar la oportunidad seleccionada ante el cliente. La conversación deberá partir de la comprensión de sus necesidades y de la evidencia analizada antes de introducir la propuesta de valor.

Práctica 2: A partir de los resultados del caso, los participantes utilizarán Copilot en PowerPoint para generar una presentación ejecutiva breve que sintetice contexto del cliente, necesidad identificada, evidencia relevante, oportunidad propuesta, escenarios analizados y próximos pasos. Se revisará la estructura generada para asegurar que la presentación diferencie claramente hechos, hipótesis y supuestos.

Práctica 3: Los participantes solicitarán a Copilot asumir el rol de un directivo del cliente corporativo ficticio y presentar una evaluación de opción múltiple. Copilot cuestionará los supuestos, beneficios y viabilidad de la propuesta mediante preguntas con opciones (A, B, C, D). El participante responderá seleccionando la opción adecuada y Copilot entregará retroalimentación inmediata sobre cada elección.

## Pasos para ejecutar la práctica

1. **Redacción y guardado del Speech Ejecutivo:**
   * En Copilot Chat, envía la siguiente solicitud:
     ```text
     Redacta un speech comercial ejecutivo de 2 minutos para el Gerente de Relación con el cliente corporativo basándote en la oferta de valor desarrollada.
     
     El argumento debe iniciar demostrando la comprensión del contexto del sector, presentar la evidencia de sus datos internos y exponer la propuesta de valor de forma consultiva.
     ```
   * Exporta la respuesta a un documento de Word con el nombre: `Speech_Comercial_Cliente.docx`.

2. **Generación de la Presentación en PowerPoint:**
   * Abre **Microsoft PowerPoint** y activa Copilot.
   * Adjunta o vincula los archivos creados en los laboratorios anteriores (`Hallazgos_y_Oportunidades_Cliente.docx`, `Evaluacion_Escenarios_Oportunidad.xlsx` y `Speech_Comercial_Cliente.docx`) y envía la siguiente orden:
     ```text
     Crea una presentación ejecutiva de 5 diapositivas utilizando como fuente el contenido de los archivos adjuntos:
     - Diapositiva 1: Contexto y Desafíos del Sector
     - Diapositiva 2: Hallazgos de Desempeño y Evidencia
     - Diapositiva 3: Propuesta de Oportunidad Estratégica
     - Diapositiva 4: Evaluación de Escenarios e Impacto Estimado
     - Diapositiva 5: Próximos Pasos y Plan de Validaciones
     
     Asegúrate de que en cada diapositiva se diferencie explícitamente entre Hechos, Hipótesis y Supuestos.
     ```

3. **Simulación con Preguntas de Selección Múltiple:**
   * Abre Copilot Chat, adjunta el documento `Speech_Comercial_Cliente.docx` y ejecuta el siguiente prompt:
     ```text
     Con base en el documento adjunto Speech_Comercial_Cliente.docx, actúa como el CFO del cliente corporativo y evalúa mi propuesta comercial mediante una prueba rápida de opción múltiple.

     Reglas:
     1. Hazme 3 preguntas consecutivas de selección múltiple (A, B, C, D) sobre objeciones típicas: supuestos financieros, retorno de inversión y diferenciadores frente a la competencia.
     2. Presenta la primera pregunta y espera a que yo responda solo indicando la letra de la opción (ej. "A").
     3. Cuando responda, indícame inmediatamente si la opción elegida es correcta o incorrecta, explica brevemente por qué basándote en la evidencia del documento, y pasa a la siguiente pregunta.
     ```

## Resultado esperado
Un documento de Word llamado `Speech_Comercial_Cliente.docx`, una presentación de 5 diapositivas generada automáticamente en PowerPoint vinculando los archivos del caso y una evaluación dinámica de opción múltiple completada con retroalimentación inmediata en Copilot Chat.
