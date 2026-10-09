# Laboratorio 3: Descubrir oportunidades potenciales mediante el agente Analista

**Duración:** 20 min

## Descripción
Práctica 1 (13 min): Los participantes analizarán un conjunto de datos completamente ficticios sobre el cliente corporativo del caso, relacionados con variables como evolución de ingresos, regiones, unidades de negocio, inversiones, crecimiento y otros indicadores relevantes. Utilizarán el agente Analista para identificar patrones, variaciones, relaciones entre variables y comportamientos que ameriten profundización. Solicitarán diferenciar los hallazgos sustentados por los datos de las hipótesis que requieren información adicional.

Práctica 2 (7 min): A partir de los hallazgos obtenidos, los participantes solicitarán a Copilot formular diferentes hipótesis de necesidades u oportunidades que podrían explorarse con el cliente. Cada hipótesis deberá vincularse con la evidencia que la origina, explicar qué necesidad podría existir y señalar qué información adicional debería validarse antes de convertirla en una propuesta comercial.

## Pasos para ejecutar la práctica

1. **Análisis de datos con el agente Analista (13 min):**
   * Selecciona el agente **Analista (Analyst)** en Microsoft 365 Copilot.
   * Adjunta o vincula el archivo con los datos ficticios del cliente (ingresos, regiones, unidades de negocio, inversiones) y envía el siguiente prompt:
     ```text
     Analiza el conjunto de datos adjunto del cliente corporativo ficticio sobre la evolución de sus ingresos, comportamiento regional, desempeño por unidad de negocio e inversiones de capital.
     
     Identifica:
     1. Patrones anómalos, variaciones significativas y relaciones entre variables de crecimiento.
     2. Un desglose en dos secciones estrictas:
        - HALLAZGOS SUSTENTADOS (hechos probados cuantitativamente por los datos).
        - HIPÓTESIS QUE REQUIEREN PROFUNDIZACIÓN (supuestos derivados del comportamiento de los datos).
     ```

2. **Formulación y vinculación de hipótesis de oportunidad (7 min):**
   * Copia el resultado del análisis anterior, regresa a Copilot Chat y envía el siguiente prompt:
     ```text
     Con base en los hallazgos de datos obtenidos por el Analista [Pega los hallazgos], formula 3 hipótesis de oportunidad de negocio estructuradas.
     
     Para cada hipótesis exige la siguiente estructura obligatoria:
     1. Evidencia origen (el dato numérico exacto que la respalda).
     2. Necesidad potencial del cliente (qué problema o reto operativo/financiero deduce).
     3. Información faltante (qué datos adicionales se deben validar obligatoriamente antes de estructurar una propuesta comercial).
     ```

## Resultado esperado
Un diagnóstico analítico dividiendo hechos cuantitativos e hipótesis, acompañado de una matriz de 3 oportunidades comerciales fundamentadas en la evidencia de datos e identificando las variables críticas a validar.
