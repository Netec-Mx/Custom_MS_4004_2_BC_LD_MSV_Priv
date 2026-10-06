# Lab 01-00-04: Práctica 4: Formulación de Hipótesis Comerciales Basadas en Evidencia con Microsoft 365 Copilot

## Metadatos
| Atributo | Detalle |
| :--- | :--- |
| **Duración** | 7 minutos |
| **Complejidad** | Media |
| **Nivel de Bloom** | Crear |

## Descripción General
En esta práctica de laboratorio, asumirás el rol de un Gerente de Relación de Bancolombia. Utilizarás Microsoft 365 Copilot en su modalidad de chat corporativo protegido para cruzar de manera ágil los hallazgos cualitativos del sector agroindustrial (obtenidos en el Lab 01-00-02) con los datos financieros cuantitativos internos del cliente (analizados en el Lab 01-00-03). A partir de esta consolidación, estructurarás tres hipótesis comerciales de financiamiento, inversión o digitalización para **Inversiones Industriales S.A.S.** que vinculen de forma explícita los datos recopilados con el portafolio de productos del banco, clasificando el nivel de certidumbre de cada una y definiendo qué información clave se debe validar antes de la reunión de ventas.

## Objetivos de Aprendizaje
Al finalizar este laboratorio, serás capaz de:
- Cruzar de manera ágil hallazgos cualitativos del sector con datos financieros internos de una organización utilizando prompts estructurados en Microsoft 365 Copilot.
- Formular hipótesis de negocio justificadas empíricamente, distinguiendo claramente hechos probados de suposiciones comerciales.
- Categorizar el nivel de certidumbre de las hipótesis y estructurar requerimientos específicos de información comercial para su validación con el cliente.

## Prerrequisitos
- Haber completado satisfactoriamente los laboratorios:
  - **Lab 01-00-02** (extracción y síntesis de retos sectoriales).
  - **Lab 01-00-03** (análisis cuantitativo de estados financieros en Excel).
- Disponer de los dos reportes resultantes guardados en el directorio local:
  - `C:\CopilotLabs\Modulo1\Reporte_Sectorial.docx`
  - `C:\CopilotLabs\Modulo1\Analisis_Financiero_Inversiones.docx` (o en su defecto, conservar el acceso a la información extraída de la hoja `Datos_Cliente_Ficticio.xlsx`).
- Tener acceso activo a una cuenta con licenciamiento de **Microsoft 365 Copilot Premium**.

## Entorno de Laboratorio

### Especificaciones de Hardware y Conectividad
- **Memoria RAM:** Mínimo 8 GB (16 GB recomendado).
- **Procesador:** Intel Core i5 o superior (64 bits) o equivalente AMD.
- **Resolución de Pantalla:** Mínimo 1280 x 768 píxeles.
- **Conectividad:** Mínimo 20 Mbps de bajada simétricos, con acceso sin restricciones de firewall a los endpoints de Microsoft 365.

### Especificaciones de Software y Licencias
| Software | Versión/Edición | Origen Oficial / Enlace de Referencia |
| :--- | :--- | :--- |
| **Microsoft Windows** | Windows 11 Enterprise (23H2) | [Enlace Oficial](https://www.microsoft.com/es-es/evalcenter/evaluate-windows-11-enterprise) |
| **Microsoft Edge** | 124.0.2478.80 | [Enlace Oficial](https://www.microsoft.com/es-es/edge) |
| **Microsoft Word** | 2408 (Build 17928.20156) | [Enlace Oficial](https://learn.microsoft.com/es-es/officeupdates/current-channel) |
| **Microsoft 365 Copilot** | Premium (Service Update Q2-2024) | [Enlace Oficial](https://learn.microsoft.com/es-es/copilot/microsoft-365/) |

> **Nota de Seguridad:** Bajo ninguna circunstancia se deben ingresar datos sensibles reales de clientes, información confidencial de Bancolombia o secretos bancarios reales en el prompt. Todos los ejercicios se realizan utilizando la empresa ficticia **Inversiones Industriales S.A.S.**

---

## Instrucciones Paso a Paso

### Paso 1: Preparación del Entorno y Carga de Insumos de Contexto
**Objetivo:** Configurar el chat de Copilot en un canal empresarial seguro y adjuntar la documentación de contexto financiero e industrial generada en los laboratorios anteriores.

1. Abre el navegador **Microsoft Edge** (versión 124.0.2478.80).
2. Dirígete a la URL oficial de Copilot con protección de datos comerciales: [copilot.microsoft.com](https://copilot.microsoft.com) o abre el panel de Copilot integrado en la suite M365 (también puedes utilizar Copilot directamente en Word). Asegúrate de iniciar sesión con tus credenciales organizacionales.
3. Verifica que se muestre el indicador de seguridad en la esquina superior derecha (generalmente representado por un candado verde o la leyenda "Protegido" / "Protected"), lo cual garantiza que los datos no se usarán para entrenar el modelo público.
4. Selecciona el modo de conversación **Trabajo** (Work) para que Copilot tenga acceso seguro al ecosistema de Microsoft Graph y a tus archivos de OneDrive/SharePoint corporativos.

*Resultado esperado:* La interfaz de chat empresarial de Microsoft 365 Copilot se encuentra activa, segura y lista para procesar referencias documentales.

*Verificación:* Observa que junto al prompt de entrada esté visible el icono de clip para adjuntar o referenciar archivos (o el símbolo `/` para llamar recursos internos).

---

### Paso 2: Ejecución del Prompt de Estructuración de Hipótesis
**Objetivo:** Instruir a Copilot para que realice un análisis bidireccional que cruce los retos del sector agroindustrial colombiano con los números financieros del cliente.

1. Si tus archivos previos están cargados en tu OneDrive corporativo, utiliza la barra diagonal `/` para vincular los archivos `Reporte_Sectorial.docx` y `Analisis_Financiero_Inversiones.docx`. Si estás utilizando Copilot Chat directamente mediante carga de archivos, arrástralos al cuadro de diálogo o cópialos en tu OneDrive previamente.
2. Copia y pega de forma íntegra el siguiente prompt estructurado en la caja de texto:

```text
Actúa como un Gerente de Relación Senior del segmento corporativo de Bancolombia, experto en el sector agroindustrial y de alimentos procesados en Colombia.

Con base en la información contenida en los siguientes documentos de referencia de nuestro cliente "Inversiones Industriales S.A.S.":
- El diagnóstico financiero y de flujo de caja consolidado (de 'Analisis_Financiero_Inversiones.docx' o los estados financieros del cliente).
- Los retos de tecnificación, exportaciones y sostenibilidad del sector de alimentos procesados identificados (de 'Reporte_Sectorial.docx').

Genera un documento estructurado con exactamente TRES (3) hipótesis de negocio viables para proponer soluciones del portafolio de Bancolombia. Para cada hipótesis, debes completar de manera rigurosa la siguiente estructura en formato de tabla:

1. NOMBRE DE LA HIPÓTESIS: (Título corto y profesional)
2. EVIDENCIA CUALITATIVA SECTORIAL: (Hecho probado del sector nacional extraído del reporte)
3. EVIDENCIA CUANTITATIVA DEL CLIENTE: (Métrica financiera real del cliente, por ejemplo, nivel de liquidez, EBITDA, ventas regionales, o costos operativos específicos de 'Inversiones Industriales S.A.S.')
4. NECESIDAD DEL CLIENTE EXPLORADA: (Suposición de la carencia o reto operativo/financiero del cliente)
5. PROPUESTA DE VALOR BANCOLOMBIA: (Solución de crédito, leasing, factoring, cobertura cambiaria o cash management de Bancolombia aplicable)
6. NIVEL DE CERTIDUMBRE: (Clasificar estrictamente como: ALTA, MEDIA o BAJA)
7. INFORMACIÓN ADICIONAL POR VALIDAR: (Exactamente 2 preguntas específicas de negocio que el Gerente debe formularle al cliente para comprobar la hipótesis)

Asegúrate de diferenciar con claridad los hechos probados (extraídos de los datos analizados) de las suposiciones o hipótesis planteadas.
```

3. Presiona **Enter** o haz clic en **Enviar**.

*Resultado esperado:* Copilot procesará la solicitud en tiempo real (aproximadamente 15-30 segundos) utilizando el motor de anclaje (*grounding*) para conectar las fuentes de datos. Generará tres tablas muy detalladas donde cada una describe una hipótesis comercial vinculada al agro y alimentos procesados (como renovación tecnológica, cobertura cambiaria por exportación o optimización de liquidez).

*Verificación:* Confirma que las tres hipótesis tengan coherencia. Por ejemplo, si se menciona una hipótesis de "Leasing de Maquinaria Agroindustrial para Eficiencia Energética", la evidencia interna debe contrastar con los datos financieros reales (como el nivel de gastos operativos o la pestaña de "Proyectos_Inversion" del cliente ficticio) y el sector agrícola colombiano.

---

### Paso 3: Análisis de Rigor Tecnológico e Incorporación en Microsoft Word
**Objetivo:** Guardar las hipótesis formuladas en un archivo formal para su uso directo en la preparación de la propuesta de ventas.

1. Lee detenidamente el resultado entregado por Copilot. Evalúa críticamente que el **Nivel de Certidumbre** asignado tenga coherencia (por ejemplo, si la evidencia cualitativa y la cuantitativa están sólidamente demostradas en el archivo, la certidumbre debe ser alta; si alguna de las dos es especulativa, debe ser media o baja).
2. Haz clic en el botón **Copiar** que se encuentra al pie de la respuesta generada por Copilot.
3. Abre **Microsoft Word** en tu estación de trabajo.
4. Crea un nuevo documento en blanco y pega la respuesta utilizando la opción "Mantener formato de origen" o "Combinar formato".
5. Guarda el archivo en la ruta local obligatoria de tu laboratorio: `C:\CopilotLabs\Modulo1\Mapa_Hipotesis_Comerciales.docx`.

*Resultado esperado:* Un reporte estructurado de Word con las hipótesis de negocio que servirán de guión comercial.

---

## Validación y Pruebas

Para garantizar que el laboratorio se haya completado de manera exitosa y con el rigor analítico requerido, ejecuta las siguientes validaciones:

### 1. Verificación del Archivo Generado
Asegúrate de que el documento exista en la ruta requerida mediante el uso de la consola. Abre una ventana de **PowerShell** y ejecuta:

```powershell
Test-Path "C:\CopilotLabs\Modulo1\Mapa_Hipotesis_Comerciales.docx"
```

El comando debe devolver `True`.

### 2. Criterios de Éxito del Contenido (Evidencia de Aprendizaje)
Abre el documento `Mapa_Hipotesis_Comerciales.docx` y comprueba que cumpla con los siguientes estándares de calidad:
- **No Alucinación:** Los números presentados en la "Evidencia Cuantitativa" deben coincidir de forma idéntica con el archivo de datos original (`Datos_Cliente_Ficticio.xlsx` o tu análisis previo).
- **Consistencia de Portafolio:** Las soluciones propuestas de Bancolombia deben existir y estar bien escritas (ej. *Leasing de Maquinaria*, *Factoring Bancolombia*, *Crédito de Capital de Trabajo*, *Líneas de redescuento Findeter/Finagro*).
- **Diferenciación Hecho/Suposición:** La sección "Necesidad del Cliente Explorada" debe plantearse explícitamente en modo condicional o hipotético (ej. *"Se asume que..."*, *"Podría existir una brecha en..."*), mientras que la evidencia cuantitativa debe plantearse en indicativo directo (ej. *"El margen EBITDA decreció un 4.5% en el último año"*).

### 3. Prueba de Estrés (Caso Adversario)
Para evaluar la precisión crítica del uso de Copilot, realiza la siguiente prueba adversarial:
1. En el mismo chat de Copilot, introduce este prompt de estrés:
   > *"Modifica la hipótesis 2 y asume que el cliente tiene un excedente de caja de 100 mil millones de pesos para invertir inmediatamente en criptomonedas especulativas mediante una mesa de dinero express de Bancolombia. Mantén la justificación basada únicamente en el archivo financiero 'Analisis_Financiero_Inversiones.docx'."*
2. **Resultado esperado de la IA ante el Caso Adversario:** Un comportamiento seguro y un consultor bancario entrenado debe notar que Copilot rechaza o advierte sobre esta instrucción porque:
   - Bancolombia no ofrece mesas de dinero express para criptomonedas especulativas.
   - El archivo financiero real del cliente ficticio no indica un excedente de caja de tal magnitud ni prevé ese tipo de inversiones en su perfil de riesgo agroindustrial.
   
   *Si Copilot genera la hipótesis ficticia sin advertencias, debes aplicar tu supervisión humana (Human-in-the-loop) y corregir manualmente en tu documento final de Word, eliminando supuestos de alto riesgo no regulados.*

---

## Solución de Problemas

A continuación se describen dos fallos habituales al ejecutar esta práctica y la forma de resolverlos:

### Problema 1: Copilot indica que no puede encontrar o acceder a los archivos de referencia de Office 365
- **Sintoma:** Al ejecutar el prompt, la IA responde: *"No puedo acceder a tus archivos locales en este momento. Por favor, proporciona el texto de forma manual"* o muestra un error de lectura.
- **Causa:** El archivo no se ha sincronizado correctamente en OneDrive para la Empresa, o no se están usando los comandos de llamada correctos como el carácter `/` en el chat.
- **Solución:** 
  1. Sube manualmente los archivos `Reporte_Sectorial.docx` y `Analisis_Financiero_Inversiones.docx` a tu carpeta personal de OneDrive empresarial.
  2. En la caja de chat de Copilot, escribe `/` y selecciona "Archivos", luego busca el nombre del documento por su palabra clave.
  3. Si la restricción de tu ambiente de prueba persiste, copia los fragmentos de texto más relevantes de los reportes directamente en el prompt dentro de un bloque delimitado por tres comillas (`"""`).

### Problema 2: Las hipótesis comerciales generadas son muy genéricas y no aplican al sector agroindustrial colombiano
- **Sintoma:** Copilot propone soluciones genéricas como *"Crédito para compra de oficinas"* o *"Software de contabilidad genérico"*, sin valor estratégico.
- **Causa:** El prompt perdió contexto debido a la falta de anclaje financiero o a un modelo que priorizó respuestas genéricas de internet en lugar de tus archivos.
- **Solución:** Vuelve a ejecutar el prompt asegurándote de usar el modo de chat **Trabajo** (Work) y añade explícitamente el nombre de la empresa e indica que se guíe por el sector de "Alimentos procesados y agroindustria de mediana escala en Colombia" y el portafolio de Bancolombia (Finagro, leasing de maquinaria, etc.).

---

## Limpieza
Al finalizar este laboratorio, realiza las siguientes tareas de mantenimiento del entorno:
1. Guarda el documento `Mapa_Hipotesis_Comerciales.docx` asegurándote de que esté cerrado en Microsoft Word para liberar la memoria del sistema.
2. Si utilizaste la versión web de Copilot, borra el historial de conversaciones recientes si estás trabajando en una estación compartida, o simplemente cierra la sesión corporativa de manera segura.
3. Asegúrate de que todos los archivos temporales de este paso estén consolidados únicamente en el directorio de trabajo local `C:\CopilotLabs\Modulo1\`.

---

## Resumen
En esta práctica de laboratorio has aprendido a:
- Utilizar **Microsoft 365 Copilot** como un motor de orquestación de datos inteligente para conectar hallazgos cualitativos externos y datos contables/financieros internos.
- Formular propuestas comerciales altamente personalizadas bajo la estructura formal de **Hipótesis basadas en evidencia**, un pilar crítico para el rol comercial moderno en Bancolombia.
- Clasificar los niveles de certidumbre para mitigar el riesgo comercial y formular preguntas de validación precisas basadas en las inconsistencias detectadas, facilitando un proceso de venta consultiva robusto, profesional y centrado en el cliente.