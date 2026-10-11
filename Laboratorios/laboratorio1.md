# Laboratorio 1: Convertir información en preguntas de negocio

**Duración:** 6 min

## Descripción
Los participantes conocerán el caso del cliente corporativo ficticio y transformarán una solicitud genérica como “identifica oportunidades para este cliente” en instrucciones diferenciadas para investigar su entorno y analizar posteriormente sus datos. Definirán qué información necesitan conocer, qué evidencia esperan obtener y qué aspectos no deben asumirse sin información suficiente.

## Pasos para ejecutar la práctica

1. **Evaluación de solicitud genérica inicial:**
   * Abre Microsoft 365 Copilot Chat.
   * Copia, pega y envía la siguiente solicitud genérica:
     ```text
     Identifica oportunidades de negocio para nuestro cliente corporativo.
     ```
   * Observa la respuesta superficial entregada por Copilot.

2. **Transformación en instrucción para investigación de entorno (Agente / Prompt especializado):**
   * Copia, pega y envía la siguiente instrucción estructurada bajo la fórmula Contexto + Objetivo + Origen + Expectativas:
     ```text
     Actúa como un Especialista en Inteligencia Comercial e Investigación de Mercados.
     
     Contexto: Un cliente corporativo del sector industrial/comercial se encuentra en proceso de expansión y transformación de su negocio.
     Objetivo: Diseñar una orden de investigación para explorar su entorno externo sin asumir hechos no comprobados.
     Origen: Información pública del sector y macrotendencias de mercado.
     Expectativas: Entrega un marco de investigación con:
     1. Los 4 aspectos clave del entorno del sector que debemos conocer.
     2. La evidencia objetiva y fuentes públicas que esperamos obtener.
     3. Tres supuestos del cliente que NO debemos asumir sin antes investigar.
     ```

3. **Transformación en instrucción para análisis de datos internos del cliente:**
   * Copia, pega y envía la siguiente instrucción para orientar el análisis de datos cuantitativos:
     ```text
     Actúa como un Analista Senior de Datos de Negocio.
     
     Contexto: Contamos con registros históricos de ventas, distribución por regiones, margen por línea de producto y comportamiento transaccional de un cliente corporativo.
     Objetivo: Formular las preguntas analíticas clave para descubrir patrones de crecimiento o fricción operativa.
     Origen: Datos transaccionales e históricos del cliente.
     Expectativas: Detalla:
     1. Cinco preguntas analíticas cuantitativas específicas.
     2. Variables requeridas para responder cada pregunta.
     3. El hallazgo de negocio que se espera descubrir con cada análisis.
     ```

## Resultado esperado
Dos instrucciones de alto nivel ejecutivo claramente diferenciadas: una estructurada para investigar el entorno externo del cliente mediante evidencia pública y otra diseñada para analizar cuantitativamente sus datos transaccionales, evitando asumir supuestos sin fundamento.
