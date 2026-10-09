# Laboratorio 6: Preparar y poner a prueba la conversación con el cliente

**Duración:** 20 min

## Descripción
Práctica 1 (5 min): Los participantes solicitarán a Copilot preparar un breve speech ejecutivo para presentar la oportunidad seleccionada ante el cliente. La conversación deberá partir de la comprensión de sus necesidades y de la evidencia analizada antes de introducir la propuesta de valor.

Práctica 2 (8 min): A partir de los resultados del caso, los participantes utilizarán Copilot en PowerPoint para generar una presentación ejecutiva breve que sintetice contexto del cliente, necesidad identificada, evidencia relevante, oportunidad propuesta, escenarios analizados y próximos pasos. Se revisará la estructura generada para asegurar que la presentación diferencie claramente hechos, hipótesis y supuestos.

Práctica 3 (7 min): Los participantes solicitarán a Copilot asumir el rol de un directivo del cliente corporativo ficticio. Durante un breve juego de roles, Copilot cuestionará los supuestos, beneficios, diferenciadores y viabilidad de la propuesta. El participante responderá utilizando la evidencia obtenida durante el caso y, al finalizar, Copilot identificará las preguntas que fueron respondidas adecuadamente y aquellas para las que todavía sería necesario obtener información adicional.

## Pasos para ejecutar la práctica

1. **Redacción del Speech Ejecutivo (5 min):**
   * En Copilot Chat, envía la siguiente solicitud para preparar el guion de la reunión:
     ```text
     Redacta un speech comercial ejecutivo de 2 minutos para el Gerente de Relación con el cliente corporativo.
     
     El argumento debe iniciar demostrando la comprensión del contexto y tendencias de su mercado, presentar la evidencia de sus datos internos y cerrar exponiendo la propuesta de valor de forma consultiva antes de sugerir cualquier solución financiera.
     ```

2. **Generación de la Presentación en PowerPoint (8 min):**
   * Abre **Microsoft PowerPoint** y activa Copilot.
   * Envía la siguiente orden para estructurar la presentación:
     ```text
     Crea una presentación ejecutiva de 5 diapositivas basada en el siguiente resumen del cliente [Pega el contexto y la propuesta de valor]:
     - Diapositiva 1: Contexto y Desafíos del Sector
     - Diapositiva 2: Hallazgos de Desempeño y Evidencia
     - Diapositiva 3: Propuesta de Oportunidad Estratégica
     - Diapositiva 4: Evaluación de Escenarios e Impacto Estimado
     - Diapositiva 5: Próximos Pasos y Plan de Validaciones
     
     Asegúrate de que el texto de cada diapositiva diferencie explícitamente entre Hechos, Hipótesis y Supuestos.
     ```

3. **Simulación y Juego de Roles con el Cliente (7 min):**
   * Regresa a Copilot Chat y ejecuta el siguiente prompt para iniciar la simulación interactiva:
     ```text
     Asume el rol del Director Financiero (CFO) del cliente corporativo ficticio. Tu objetivo es cuestionar mi propuesta comercial de forma crítica y exigente.
     
     Reglas de la simulación:
     1. Hazme 3 preguntas desafiantes sobre los supuestos financieros, el retorno esperado y por qué esta solución es superior a la competencia.
     2. Espérame a que responda una pregunta antes de hacer la siguiente.
     3. Al finalizar mis respuestas, evalúa mi desempeño indicando qué puntos argumenté adecuadamente con evidencia y en cuáles cometí el error de presentar supuestos como hechos comprobados.
     
     Empieza saludando y haciéndome la primera pregunta crítica.
     ```

## Resultado esperado
Un guion de apertura comercial enfocado en necesidades, una presentación estructurada de 5 diapositivas en Microsoft PowerPoint especificando hechos e hipótesis, y la simulación interactiva completada recibiendo retroalimentación sobre la calidad de la defensa comercial.
