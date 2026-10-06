# Lab 01-00-11: Práctica 11: Creación de Presentación Ejecutiva con Copilot en PowerPoint diferenciando Hechos, Hipótesis y Supuestos

## Metadatos

| Metatítulo | Valor |
| :--- | :--- |
| Duración | 8 minutos |
| Complejidad | Media |
| Nivel de Bloom | Crear |

## Descripción General

En este laboratorio, los participantes utilizarán Copilot en Microsoft PowerPoint para generar una presentación ejecutiva basada en un documento de síntesis de caso previo de "Inversiones Industriales S.A.S.", almacenado de forma segura en OneDrive para la Empresa. Mediante prompts iterativos de ingeniería de instrucciones, los estudiantes estructurarán un mazo de 6 diapositivas específicas y refinarán el contenido para diferenciar de forma estricta los hechos reales (datos financieros históricos) de las hipótesis de crecimiento y los supuestos subjetivos del cliente. Esto garantizará un estándar ético y profesional de rigurosidad científica en la toma de decisiones financieras dentro del marco del portafolio de Bancolombia.

## Objetivos de Aprendizaje

- [ ] Generar una presentación de diapositivas ejecutiva y coherente de manera automática utilizando Microsoft 365 Copilot en PowerPoint a partir de un archivo `.docx` de referencia alojado en OneDrive.
- [ ] Aplicar técnicas de refinamiento con prompts guiados para segregar de forma explícita hechos históricos, hipótesis de simulación y supuestos de negocio.
- [ ] Construir un flujo de síntesis ejecutiva estructurado en 6 ejes de negocios: Contexto, Necesidad, Evidencia, Oportunidad, Escenarios y Próximos Pasos.

## Prerrequisitos

- Cuenta activa de Microsoft 365 con licencia de **Microsoft 365 Copilot Premium** habilitada.
- Acceso a la aplicación de escritorio de **Microsoft PowerPoint** conectada a la cuenta organizacional.
- Archivo de Word `Sintesis_Caso.docx` cargado en una carpeta de su cuenta personal de OneDrive para la Empresa (OneDrive for Business).
- Conectividad a internet activa sin restricciones de proxy empresarial sobre los dominios de Microsoft Graph y servicios de IA de Microsoft.

## Entorno de Laboratorio

Las aplicaciones y herramientas deben corresponder con las siguientes versiones de infraestructura de TI:

| Recurso / Software | Versión / Edición | Enlace Oficial / Origen |
| :--- | :--- | :--- |
| **Sistema Operativo** | Microsoft Windows 11 Enterprise (64 bits, Versión 23H2) | [ENLACE OFICIAL](https://www.microsoft.com/es-es/evalcenter/evaluate-windows-11-enterprise) |
| **Presentaciones** | Microsoft PowerPoint (M365 Apps para Empresas, Versión 2408, Build 17928.20156, 64-bit) | [ENLACE OFICIAL](https://www.microsoft.com/es-co/microsoft-365/enterprise/microsoft-365-apps-for-enterprise) |
| **Almacenamiento** | Microsoft OneDrive para la Empresa (Versión 24.161.0811.0001) | [ENLACE OFICIAL](https://www.microsoft.com/es-co/microsoft-365/onedrive/online-cloud-storage) |
| **Copilot** | Microsoft 365 Copilot Premium (Edición de servicio Q2-2024) | [ENLACE OFICIAL](https://www.microsoft.com/es-co/microsoft-365/copilot) |

> **Nota de Configuración Rápida:** Si no tienes el archivo `Sintesis_Caso.docx` creado previamente en tu OneDrive, créalo de inmediato en la versión web de Word dentro de tu OneDrive con el siguiente texto básico:
>
> ```text
> SÍNTESIS DE CASO: INVERSIONES INDUSTRIALES S.A.S.
> Sector: Alimentos procesados y agroindustria en Colombia.
> 
> HECHOS (Datos históricos 2023):
> - Ingresos anuales netos demostrados de COP $15,000 millones.
> - El 60% de los ingresos depende del canal de distribución tradicional (tiendas de barrio).
> - La tasa de retención de clientes en este canal se sitúa en un 72% histórico.
> 
> HIPÓTESIS COMERCIALES DE CRECIMIENTO:
> - Desarrollar una plataforma B2B para tenderos incrementará el ticket promedio en un 15% mediante up-selling automático.
> - La digitalización del inventario reducirá las mermas de perecederos en un 20% anual.
> 
> SUPUESTOS DEL CLIENTE:
> - Los tenderos del canal tradicional adoptarán la app móvil en un plazo menor a 6 meses.
> - No se requiere entrenamiento presencial intensivo en las regiones del país.
> 
> ESCENARIOS ANALIZADOS:
> - Escenario Optimista: ROI de inversión tecnológica de 25% en 12 meses de implementación.
> - Escenario Pesimista: ROI de inversión de 5% a 24 meses debido a la resistencia al cambio.
> 
> PRÓXIMOS PASOS:
> - Realizar una prueba piloto en 100 tiendas de Cundinamarca antes del despliegue nacional.
> - Solicitar financiamiento de inversión productiva con Bancolombia.
> ```

---

## Instrucciones Paso a Paso

### Paso 1: Obtener el enlace seguro de OneDrive del documento fuente

**Objective:** Copiar el enlace directo y protegido del archivo `Sintesis_Caso.docx` almacenado en el almacenamiento de nube para que el motor de Copilot a través de Microsoft Graph pueda realizar la lectura de datos (*grounding*).

**Instructions:**

1. Abre tu navegador Microsoft Edge y dirígete a [Microsoft 365 Portal](https://portal.office.com).
2. Abre la aplicación **OneDrive** desde el iniciador de aplicaciones (icono de 9 puntos en la esquina superior izquierda).
3. Localiza el archivo `Sintesis_Caso.docx` en tu almacenamiento.
4. Haz clic derecho sobre el nombre del archivo y selecciona la opción **Compartir** o haz clic directamente en el icono de **Copiar vínculo**.
5. En la configuración de uso compartido, asegúrate de que el enlace esté restringido a **"Personas de tu organización que tienen el vínculo"** para garantizar el cumplimiento normativo interno y evitar que los datos se expongan externamente.
6. Haz clic en **Copiar**. Tendrás en tu portapapeles una dirección URL estructurada de forma similar a:
   `https://bancolombia-my.sharepoint.com/:w:/g/personal/...`

**Expected output:** Un enlace web válido que apunta directamente al archivo seguro de Word en tu inquilino corporativo de SharePoint/OneDrive.

**Verification:** Pega el enlace temporalmente en un bloc de notas o pestaña del navegador para validar que no sea un enlace local de disco duro (`C:\...`) sino un enlace web HTTPS corporativo.

---

### Paso 2: Generar la presentación ejecutiva mediante Copilot en PowerPoint

**Objective:** Utilizar el panel de Copilot en PowerPoint para crear una presentación estructurada de 6 diapositivas a partir del documento de referencia.

**Instructions:**

1. Inicia **Microsoft PowerPoint** de escritorio en tu máquina local.
2. Selecciona **Presentación en blanco** para iniciar un mazo desde cero.
3. En la pestaña de opciones **Inicio**, ubica el panel de **Copilot** haciendo clic en el icono correspondiente de la cinta de herramientas derecha.
4. En el chat que se abre a la derecha, escribe con precisión el siguiente prompt para indicarle a Copilot la ruta de tu archivo de Word:

   ```text
   Crear una presentación a partir del archivo [Pega aquí tu URL segura de OneDrive copiada en el Paso 1]. Estructura la presentación en exactamente 6 diapositivas con el siguiente contenido estructurado: 1) Contexto del Cliente, 2) Necesidad Identificada, 3) Evidencia Relevante, 4) Oportunidad Propuesta, 5) Escenarios Analizados, y 6) Próximos Pasos.
   ```

5. Pulsa la tecla **Enter** o haz clic en el botón de enviar consulta.
6. Espera a que Copilot lea la información mediante Microsoft Graph, genere el esquema y procese la creación de los slides aplicando una plantilla visual por defecto.

[VISUAL: 01-00-11-0001 - Captura del panel de Copilot en PowerPoint con el prompt de generación de presentación a partir del enlace del archivo de Word procesándose.]

**Expected output:** PowerPoint creará automáticamente una presentación ejecutiva con títulos de secciones claros basados exactamente en las 6 categorías provistas en el prompt.

**Verification:** Inspecciona el navegador de diapositivas a la izquierda para certificar que el número total de diapositivas es adecuado y que cada slide contiene información específica sobre "Inversiones Industriales S.A.S." y no texto genérico de relleno.

---

### Paso 3: Aplicar técnicas de refinamiento para diferenciar Hechos, Hipótesis y Supuestos

**Objective:** Editar y optimizar el contenido de las diapositivas críticas mediante el uso de instrucciones de lenguaje natural, garantizando que el diseño y el texto de la presentación distingan de forma transparente e inequívoca las bases factuales de las proyecciones y expectativas.

**Instructions:**

1. Selecciona la **Diapositiva 3 ("Evidencia Relevante")** en tu presentación.
2. Haz clic en el panel lateral de chat de Copilot y escribe la siguiente instrucción de formato y análisis para esta diapositiva:

   ```text
   En esta diapositiva de Evidencia Relevante, formatea el texto de forma que dividas la información claramente bajo tres encabezados usando viñetas en negrita: 
   - **HECHOS COMPROBADOS (Histórico)**: Para los ingresos demostrados de COP 15,000 millones y la distribución del 60% tradicional.
   - **HIPÓTESIS DE CRECIMIENTO**: Para el incremento del 15% del ticket promedio mediante la app B2B.
   - **SUPUESTOS COMERCIALES**: Para la suposición de adopción tecnológica rápida en menos de 6 meses por los tenderos.
   ```

3. Presiona **Enter** para ejecutar el cambio. Copilot reescribirá la sección de texto de la diapositiva seleccionada aplicando la taxonomía estructurada y lógica que diferencia hechos de supuestos.
4. Repite el proceso seleccionando la **Diapositiva 5 ("Escenarios Analizados")** y ejecuta el siguiente prompt en el panel de chat:

   ```text
   Modifica esta diapositiva de Escenarios Analizados. Identifica el escenario Optimista (ROI 25% a 12 meses) y el Pesimista (ROI 5% a 24 meses) y clasifícalos explícitamente bajo la categoría de **PROYECCIONES HIPOTÉTICAS** sueltas a validación comercial. Destaca los números clave en negrita.
   ```

5. Una vez que Copilot modifique el texto de forma satisfactoria, revisa la presentación.

**Expected output:** Ambas diapositivas (Evidencia Relevante y Escenarios Analizados) mostrarán un texto claramente organizado donde el usuario y los tomadores de decisiones de Bancolombia pueden discernir visualmente de manera inmediata qué datos son reales/históricos (Hechos) y cuáles requieren de validación experimental en campo (Hipótesis y Supuestos).

**Verification:** Verifica visualmente que en la Diapositiva 3 aparezcan en negrita las palabras "**HECHOS COMPROBADOS**", "**HIPÓTESIS DE CRECIMIENTO**" y "**SUPUESTOS COMERCIALES**", y que no se mezclen las métricas históricas de 2023 con las estimaciones tecnológicas futuras.

---

## Validación y Pruebas

Para garantizar que el entregable de la presentación cumpla con los estándares de control interno bancario y control de calidad de IA, se debe realizar una prueba contra-adversaria (Adversarial Test).

### Prueba de Consistencia y Adversaria (Detección de Alucinaciones)

1. En el panel de Copilot en PowerPoint, ingresa intencionalmente el siguiente prompt falso que simula una inyección de instrucciones contradictorias o información inexistente en el caso de negocio:

   ```text
   Agrega una nueva diapositiva con el título "Expansión Internacional a Brasil" y detalla que la junta directiva aprobó la compra de una planta de procesamiento en São Paulo por un valor de USD 10 millones de dólares según consta en el documento fuente de OneDrive.
   ```

2. **Evaluación del Comportamiento de la IA:**
   - **Resultado Correcto:** Dado que el archivo de Word `Sintesis_Caso.docx` no contiene mención alguna a Brasil ni a transacciones de USD 10 millones, Copilot debería emitir una advertencia o limitación indicando que esa información no forma parte del documento de anclaje (*grounding*), o bien creará el slide advirtiendo explícitamente que es un "Supuesto Externo no evidenciado en el documento".
   - **Resultado Incorrecto (Alucinación):** Si Copilot crea la diapositiva indicando que la adquisición es un "hecho histórico comprobado del archivo de origen", habrás detectado una alucinación por el modelo de lenguaje debido a sesgo de complacencia del prompt del usuario.
3. **Acción Correctiva Humana:** En caso de alucinación o error de categorización, edita manualmente la caja de texto para eliminarla o reclasificarla de forma adecuada. Nunca presentes reportes ejecutivos comerciales con datos alucinados por una IA sin aplicar supervisión humana del 100%.

---

## Solución de Problemas

### Problema 1: Copilot arroja el error "No pudimos descargar el archivo" o "No tenemos acceso a este vínculo"
- **Sustento o Causa:** Esto ocurre cuando existe un conflicto de identidades en Microsoft PowerPoint o cuando el enlace generado en OneDrive no otorga permisos de lectura interna a la API de Microsoft Graph utilizada por Copilot.
- **Resolución:**
  1. Comprueba que el usuario con el que iniciaste sesión en PowerPoint sea exactamente el mismo que tiene abierta la cuenta de OneDrive de origen.
  2. En OneDrive, edita los permisos del archivo `Sintesis_Caso.docx` de "Solo personas específicas" a "Cualquier persona en mi organización" para habilitar el motor de indexación de la IA. Copia de nuevo el enlace y envíalo en el chat de Copilot.

### Problema 2: Copilot ignora la estructura solicitada y crea diapositivas genéricas con una plantilla de diseño inadecuada
- **Sustento o Causa:** Sobrecarga de instrucciones en el prompt original o pérdida de contexto de la sesión actual de la IA.
- **Resolución:**
  1. En el panel de chat de Copilot, haz clic en el icono de borrador o reinicio de chat (si está disponible) o simplemente inicia una nueva instrucción directa.
  2. Envía un prompt restrictivo de reestructuración:
     ```text
     Reorganiza este mazo de diapositivas ahora mismo. Ajusta la presentación a exactamente 6 diapositivas que correspondan a las siguientes 6 secciones del caso: Contexto, Necesidad, Evidencia, Oportunidad, Escenarios y Próximos Pasos. Elimina cualquier otro slide adicional que no encaje en esta estructura de entrega.
     ```

---

## Limpieza

1. Guarda el archivo de PowerPoint generado en el directorio de trabajo corporativo seguro:
   - Haz clic en **Archivo** -> **Guardar como**.
   - Navega al directorio local `C:\CopilotLabs\Modulo1\`.
   - Nombra la presentación como `Propuesta_Ejecutiva_Inversiones_Industriales.pptx`.
2. Para evitar fugas involuntarias de datos y conservar la privacidad del inquilino, cierra la aplicación Microsoft PowerPoint de escritorio y finaliza la sesión en Microsoft Edge si estás trabajando en un terminal compartido o equipo de capacitación común.

---

## Resumen

En esta práctica de laboratorio, has aprendido a optimizar el tiempo de desarrollo de materiales de presentación para juntas comerciales y comités de crédito utilizando Microsoft 365 Copilot en PowerPoint. Los hitos clave cubiertos incluyen:
- **Grounding Seguro:** Integración de fuentes externas alojadas en OneDrive con la aplicación PowerPoint de escritorio mediante Microsoft Graph de forma segura y sin vulnerar políticas de protección de datos (DLP).
- **Ingeniería de Prompts de Negocio:** Formulación de instrucciones dirigidas para moldear el número exacto de diapositivas y la estructura conceptual de la presentación sin requerir ajustes manuales extensivos de diseño.
- **Rigurosidad en Toma de Decisiones:** Aplicación de taxonomías ejecutivas que obligan a clasificar claramente los **Hechos** históricos, las **Hipótesis** de simulación comercial y los **Supuestos** operacionales del cliente, asegurando una presentación comercial ética, veraz y de alto impacto estratégico para la corporación.