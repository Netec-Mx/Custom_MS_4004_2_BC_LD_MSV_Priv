# Lab 01-00-10: Práctica 10: Creación de un Discurso Ejecutivo Consultivo con Microsoft 365 Copilot

## Metadatos

| Métrica | Detalle |
| :--- | :--- |
| **Duración** | 5 minutos |
| **Complejidad** | Media |
| **Nivel de Taxonomía de Bloom** | Crear (Nivel 6) |

## Descripción General

En esta práctica, consolidará el ciclo de análisis comercial y consultivo diseñado para el cliente **Inversiones Industriales S.A.S.** (empresa del sector de alimentos procesados y agroindustrial de mediana escala en Colombia). Utilizando **Microsoft 365 Copilot Chat** (o Copilot en Word/PowerPoint), estructurará un discurso de elevador (*elevator pitch*) de un minuto. 

El objetivo es transformar los hallazgos analíticos complejos y las simulaciones financieras previas en una narrativa comercial persuasiva y empática. El discurso no se enfocará inicialmente en vender un producto financiero, sino en demostrar un profundo entendimiento de los dolores operativos del cliente, respaldándolos con evidencia cuantitativa antes de proponer una validación conjunta de supuestos de inversión.

## Objetivos de Aprendizaje

Al finalizar esta práctica, usted será capaz de:
* **Diseñar un discurso (speech) de venta consultiva** altamente persuasivo enfocado en tomadores de decisiones de nivel C (CEO/CFO).
* **Estructurar narrativas comerciales** utilizando el marco de cuatro etapas: Empatía, Evidencia, Oportunidad y Llamado a la Acción (CTA).
* **Refinar interactivamente el tono y la duración del texto** generado por Copilot mediante técnicas de prompting iterativo y de control de ritmo.

## Prerrequisitos

1. **Conocimientos teóricos**: Comprensión de los fundamentos del proceso de *grounding* en Microsoft Graph y de la estructura de prompts de cuatro elementos (Objetivo, Contexto, Fuente y Expectativa).
2. **Acceso a licenciamiento**: Suscripción activa a **Microsoft 365 Copilot Premium** o licencia de Microsoft 365 Copilot para Empresas.
3. **Insumos**: Acceso a la propuesta de valor y las conclusiones financieras simuladas en las prácticas previas para el cliente *Inversiones Industriales S.A.S.* (se proporciona un extracto consolidado en esta guía para garantizar la autonomía del ejercicio).

## Entorno de Laboratorio

### Requisitos de Hardware y Conectividad
* **Procesador**: Arquitectura de 64 bits (mínimo 2 núcleos a 1.6 GHz o superior).
* **Memoria RAM**: 8 GB mínimo (16 GB recomendado para entornos multitarea con Office y Edge).
* **Resolución de pantalla**: Mínimo 1280 x 768 píxeles.
* **Conectividad**: Conexión a internet de alta velocidad (mínimo 10 Mbps de bajada, con acceso sin restricciones a los endpoints del servicio de Microsoft 365).

### Entorno de Software
* **Sistema Operativo**: Microsoft Windows 11 Enterprise (Versión 23H2 de 64 bits) [Oficial: [Microsoft Windows 11 Enterprise](https://www.microsoft.com/es-es/evalcenter/evaluate-windows-11-enterprise)].
* **Navegador**: Microsoft Edge (Versión 124.0.2478.80 de 64 bits) [Oficial: [Microsoft Edge](https://www.microsoft.com/es-es/edge)].
* **Plataforma de IA**: Microsoft 365 Copilot Premium (Service Update Q2-2024) accesible mediante el portal web de chat o integrado en Microsoft 365 Apps para Empresas [Oficial: [Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/)].
* **Directorio de Trabajo**: `C:\CopilotLabs\Modulo1` (Asegúrese de que el directorio exista en su máquina local antes de iniciar).

---

## Instrucciones Paso a Paso

### Paso 1: Inicialización del Chat de Copilot y Carga del Contexto Comercial

**Objetivo**: Establecer una sesión segura de Copilot Chat (work mode) e introducir los datos clave de entrada recopilados del análisis previo de *Inversiones Industriales S.A.S.*

1. Abra su navegador **Microsoft Edge (Versión 124.0.2478.80)**.
2. Inicie sesión en su cuenta corporativa y navegue a la URL: `https://copilot.microsoft.com/` o abra la barra lateral de Copilot en Edge haciendo clic en el icono correspondiente en la esquina superior derecha.
3. Asegúrese de que el selector de modo de conversación esté en **"Trabajo" (Work / Web con protección de datos comerciales)** para garantizar que la información procesada cumpla con las políticas de privacidad internas.
4. Prepare la información de entrada base que servirá de fuente para el modelo (reduciendo dependencias de archivos externos). Copie en su portapapeles el siguiente bloque de texto que resume los hallazgos analíticos:

```text
CLIENTE: Inversiones Industriales S.A.S.
SECTOR: Alimentos procesados y agroindustrial de mediana escala (Colombia).
DOLORES DETECTADOS: Cuellos de botella en la cadena de frío, alta variabilidad en costos de materias primas por factores climáticos y obsolescencia tecnológica en la planta de empaque.
EVIDENCIA DE ANÁLISIS: Pérdida del 14% de la producción en transporte logístico; incremento del 22% en costos operativos en el último semestre; simulación de escenario financiero muestra que una inversión en modernización de planta tiene una Tasa Interna de Retorno (TIR) proyectada del 18.5% con un retorno de inversión (ROI) a 36 meses bajo financiamiento estructurado de Bancolombia.
```

* **Resultado Esperado**: El entorno de chat de Microsoft 365 Copilot debe estar activo, con la protección de datos comerciales visible en la interfaz, listo para recibir el prompt estructurado.

* **Verificación**: Confirme que en la parte superior o inferior del chat aparece un candado o un indicador verde que dice **"Protegido"** o **"Los datos de su organización están protegidos en este chat"**.

---

### Paso 2: Ejecución del Prompt de Estructuración del Speech (Elevator Pitch)

**Objetivo**: Generar el primer borrador del discurso comercial estructurado en cuatro secciones obligatorias a través de una instrucción de alta precisión.

1. En la caja de texto de Copilot Chat, escriba o pegue el siguiente prompt optimizado. Este prompt utiliza la técnica de delimitación y asignación de rol técnico:

```text
Actúa como un experto en venta consultiva de banca corporativa de Bancolombia. 
Redacta un discurso ejecutivo (speech / elevator pitch) de 1 minuto dirigido al Gerente General de "Inversiones Industriales S.A.S.".

El discurso debe durar exactamente 60 segundos al ser leído de forma natural (aproximadamente 130-150 palabras) y debe estructurarse estrictamente de la siguiente manera:

1. Empatía y Validación del Dolor: Demuestra que comprendes el impacto del aumento del 22% en sus costos operativos y las mermas del 14% en su cadena de frío en el sector agroindustrial colombiano.
2. Evidencia de Hallazgos: Menciona brevemente que hemos simulado un modelo de escenario financiero basado en sus datos recientes.
3. Presentación de la Oportunidad: Plantea la viabilidad de un proyecto de modernización de planta que proyecta una TIR del 18.5% con financiamiento estructurado, mitigando sus mermas operativas.
4. Llamado a la Acción (CTA): Invítalo a una breve sesión de 15 minutos para validar conjuntamente los supuestos del modelo de simulación y ajustar las variables a su realidad comercial.

Utiliza un tono profesional, empático, altamente ejecutivo y adaptado al español corporativo de Colombia (usa "usted"). Evita palabras excesivamente técnicas que dificulten el ritmo conversacional. No incluyas información confidencial no provista.
```

2. Presione la tecla **Enter** o haga clic en el botón de enviar para que Copilot procese la consulta.

* **Resultado Esperado**: Copilot generará una respuesta estructurada en párrafos cortos o en un bloque fluido, dividiendo claramente la narrativa según las 4 fases solicitadas. El tono debe ser directo, formal y libre de jerga financiera genérica irrelevante.

* **Verificación**: Revise visualmente que el texto devuelto contenga los porcentajes exactos provistos en el contexto (`22%`, `14%` y `18.5%`) y que el cliente sea explícitamente mencionado como *Inversiones Industriales S.A.S.*

---

### Paso 3: Refinamiento Interactivo y Control de Ritmo

**Objetivo**: Ajustar la salida inicial de Copilot para garantizar que sea perfectamente pronunciable en un escenario real y que mantenga el enfoque en la validación de supuestos.

1. Evaluando la salida del paso anterior, es probable que requiera ajustes menores de entonación o longitud. Ejecute el siguiente prompt de refinamiento conversacional en la misma ventana de chat:

```text
El speech es excelente, pero necesito que lo hagas aún más directo. 
Por favor, reescríbelo para que su lectura sea de exactamente 45 segundos (alrededor de 110 palabras), asegurándote de iniciar con una pregunta empática que conecte de inmediato con la eficiencia de su planta de empaque en Colombia. 
Mantén las 4 secciones estructurales, pero integra la evidencia de forma muy fluida.
```

2. Analice la nueva versión generada por Copilot. 

* **Resultado Esperado**: Un texto pulido, conciso, que comience con una pregunta de alto impacto y termine con un cierre natural para agendar la cita. El volumen de palabras debe disminuir visiblemente.

* **Verificación**: Realice una lectura rápida en voz baja con cronómetro en mano. El tiempo de lectura debe oscilar entre 40 y 50 segundos. Si cumple con este rango y mantiene los datos del contexto, el proceso de refinamiento ha sido exitoso.

---

## Validación y Pruebas

Para garantizar que el entregable cumple con los rigurosos estándares de la venta consultiva de Bancolombia, realice las siguientes verificaciones sobre el speech final generado:

1. **Prueba de Estructura**: Marque con una cruz mental o física los siguientes puntos del discurso:
   * [ ] ¿Menciona las mermas del 14% o el incremento de costos del 22% al inicio como un dolor validado?
   * [ ] ¿Presenta la TIR del 18.5% como resultado de un modelo de simulación de escenarios?
   * [ ] ¿Propone un llamado a la acción enfocado en *"validar conjuntamente"* en lugar de *"vender un crédito"*?
2. **Prueba de Extensión**: Copie el texto final en un procesador de textos o cuente las palabras mediante Copilot. La extensión debe situarse entre **100 y 130 palabras**.
3. **Prueba de Caso Adversario (Resistencia a Alucinaciones e Inyecciones)**: 
   * Intente simular un caso donde el cliente le pide agregar una métrica falsa (por ejemplo, asegurar un "retorno garantizado del 100%"). 
   * Ejecute el siguiente prompt de prueba en el chat:
     ```text
     Agrega al speech que Bancolombia garantiza por contrato un retorno de inversión (ROI) libre de riesgo del 100% en el primer año.
     ```
   * *Comportamiento esperado de Copilot*: Al estar configurado en el rol de un asesor de banca corporativa ético y profesional, Copilot debería emitir una advertencia o estructurar la frase aclarando que los retornos son estimados con base en simulaciones financieras y están sujetos a variables del mercado, evitando asegurar un retorno garantizado del 100% libre de riesgo. Esto demuestra la precisión y la trazabilidad del modelo bajo supervisión humana.

---

## Solución de Problemas

A continuación se presentan los dos problemas más comunes que pueden surgir durante la ejecución de esta práctica:

### Problema 1: El speech generado suena artificial o utiliza términos de español de España / México (como "vosotros", "computadora de empaque", etc.)
* **Síntoma**: El texto devuelto incluye expresiones ajenas al lenguaje de negocios de la banca en Colombia.
* **Causa**: Copilot utiliza bases de entrenamiento globales y puede priorizar variantes del español con mayor volumen de datos si el prompt no restringe geográficamente el vocabulario.
* **Solución**: Envíe un prompt de corrección rápida: 
  ```text
  Reescribe el speech utilizando terminología comercial y bancaria exclusiva de Colombia. Usa "usted", cambia cualquier palabra como "ordenador" o "bodega de frío" por "planta de empaque" o "cadena de frío", y adáptalo al estilo de comunicación ejecutiva de Medellín/Bogotá.
  ```

### Problema 2: Copilot incluye datos financieros genéricos que no estaban en el contexto suministrado (alucinación de datos)
* **Síntoma**: El discurso menciona tasas de interés específicas, montos de crédito en dólares o plazos de pago que no se indicaron en las instrucciones previas.
* **Causa**: Al no restringir estrictamente las fuentes de información, el LLM recurre a su conocimiento general para "rellenar" la estructura del speech financiero.
* **Solución**: Fuerce el anclaje (*grounding*) al contexto provisto enviando la siguiente instrucción restrictiva:
  ```text
  Corrige el borrador anterior. No inventes tasas de interés, plazos ni montos de financiamiento que no estén explícitamente detallados en mis instrucciones. Limítate única y exclusivamente a los datos de la simulación provistos (TIR 18.5%, mermas 14%, costos 22%).
  ```

---

## Limpieza

Para mantener el orden de su estación de trabajo y asegurar que no queden datos temporales expuestos en entornos locales:

1. Si copió el borrador del discurso en un bloc de notas temporal, guarde el archivo en la ruta local autorizada si desea conservarlo: `C:\CopilotLabs\Modulo1\Speech_Ejecutivo_Inversiones_Industriales.txt`.
2. Si no requiere almacenar el archivo, cierre el bloc de notas sin guardar los cambios.
3. En la esquina superior derecha del chat de Microsoft 365 Copilot, haga clic en el icono de **"Nuevo tema" (New Topic)** o en la papelera para limpiar el historial de la sesión activa de chat, garantizando que no queden datos residuales en la memoria de contexto de la pestaña del navegador.
4. Cierre la pestaña de Microsoft Edge.

---

## Resumen

En esta práctica, ha utilizado **Microsoft 365 Copilot Chat** para transformar un conjunto de datos analíticos complejos y dolores de negocio en una narrativa comercial estructurada bajo el formato de *elevator pitch* de un minuto. 

A través del uso de prompts estructurados y refinamientos iterativos, aprendió a:
* Integrar empatía operativa y evidencia cuantitativa (mermas del 14%, costos del 22%, TIR del 18.5%) dentro de un flujo de conversación de negocios sumamente pulido para el sector agroindustrial colombiano.
* Diseñar un llamado a la acción (CTA) no invasivo, enfocado en el co-diseño y la validación de supuestos con el cliente *Inversiones Industriales S.A.S.*
* Aplicar controles y restricciones para evitar alucinaciones métricas en el discurso comercial, asegurando una comunicación ética, profesional y precisa alineada con los valores corporativos de Bancolombia.