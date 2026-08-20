\# MTH-001

\# Metodología para el Desarrollo de Sistemas Expertos Basados en Conocimiento



\---



\## Información del Documento



| Campo | Valor |

|---|---|

| Código | MTH-001 |

| Nombre | Metodología para el Desarrollo de Sistemas Expertos Basados en Conocimiento |

| Tipo documental | Metodología |

| Versión | 0.1 |

| Estado | En desarrollo |

| Proyecto de origen | PrevInspect AI |

| Fecha | 2026-08-10 |



\---



\# Índice



1\. Propósito

2\. Alcance

3\. Fundamentos de la Metodología

4\. Principios Metodológicos

5\. Capas del Sistema

6\. Familias Documentales

7\. Sistema de Conocimiento

8\. Ciclo de Desarrollo

9\. Gobernanza y Trazabilidad

10\. Gestión de Decisiones Arquitectónicas

11\. Gestión de Continuidad

12\. Independencia Tecnológica

13\. Validación de la Metodología

14\. Aplicabilidad a Otros Dominios

15\. Limitaciones

16\. Referencias

17\. Historial de Cambios



\---



\# 1. Propósito



Establecer una metodología estructurada para el diseño, desarrollo, validación, evolución y mantenimiento de sistemas expertos basados en conocimiento, capaces de integrar conocimiento normativo, técnico, documental y experto de manera trazable y controlada.



La metodología busca asegurar que el conocimiento utilizado por el sistema pueda ser identificado, estructurado, relacionado con su fuente, validado, actualizado y utilizado para apoyar procesos de análisis y toma de decisiones.



Su desarrollo se origina en PrevInspect AI como caso de aplicación y validación, pero se plantea con un nivel de abstracción que permita evaluar posteriormente su aplicabilidad a otros dominios que requieran sistemas expertos basados en conocimiento.



\---



\# 2. Alcance



La presente metodología abarca el ciclo de vida del conocimiento utilizado en sistemas expertos basados en conocimiento, desde su identificación y adquisición hasta su utilización, mantenimiento, actualización y eventual retiro u obsolescencia.



Su alcance comprende:



\* la identificación de fuentes de conocimiento relevantes;

\* la adquisición y recopilación de conocimiento normativo, técnico, documental y experto;

\* la evaluación y clasificación de las fuentes de conocimiento;

\* la estructuración y representación del conocimiento para su utilización por el sistema;

\* la vinculación del conocimiento con sus fuentes y evidencias;

\* la definición y mantenimiento de relaciones entre conceptos, reglas, casos, documentos y demás componentes del sistema de conocimiento;

\* la validación del conocimiento antes y durante su utilización;

\* la trazabilidad de cambios, decisiones y versiones;

\* la actualización del conocimiento cuando cambien las fuentes, las condiciones del dominio o la evidencia disponible;

\* la identificación, control y retiro del conocimiento obsoleto, reemplazado o invalidado;

\* la evaluación continua del comportamiento del sistema y de la calidad del conocimiento utilizado.



La metodología considera la interacción entre conocimiento, arquitectura, procesos de desarrollo y mecanismos tecnológicos, manteniendo una separación conceptual que permita modificar la implementación tecnológica sin perder la estructura, procedencia y trazabilidad del conocimiento.



MTH-001 no determina por sí misma la validez jurídica, técnica o científica de una fuente, ni sustituye el juicio de especialistas competentes. Su función es establecer un proceso sistemático para incorporar, organizar, relacionar, validar, utilizar y mantener conocimiento dentro de un sistema experto.



Aunque PrevInspect AI constituye el caso inicial de aplicación y validación de esta metodología, su alcance conceptual no se limita al ámbito de la seguridad y salud en el trabajo. Su posible utilización en otros dominios deberá evaluarse considerando las características, fuentes, riesgos y requisitos de validación propios de cada contexto.





\---



\# 3. Fundamentos de la Metodología



La metodología se fundamenta en la integración de principios provenientes de distintas disciplinas relacionadas con la construcción, representación, gestión y gobernanza del conocimiento.



Sus principales fundamentos son:



\### 3.1 Sistemas expertos basados en conocimiento



Se adopta como base conceptual la separación tradicional entre conocimiento, hechos, reglas, mecanismos de inferencia, mecanismos de explicación e interacción con el usuario.



La metodología amplía esta perspectiva incorporando explícitamente la procedencia del conocimiento, sus evidencias, su estado de validación, su versionamiento y su ciclo de vida.



\### 3.2 Ingeniería del conocimiento



Se incorporan principios de ingeniería del conocimiento para identificar, adquirir, estructurar, representar, validar, mantener y utilizar conocimiento dentro de sistemas computacionales.



Estos procesos constituyen una base para transformar conocimiento proveniente de distintas fuentes en componentes utilizables por el sistema.



\### 3.3 Metodologías estructuradas para sistemas basados en conocimiento



La metodología reconoce antecedentes como CommonKADS, particularmente en la necesidad de separar y representar explícitamente distintos aspectos del problema, las tareas, los agentes, el conocimiento y el diseño del sistema.



No se adopta CommonKADS como metodología completa, sino como uno de los antecedentes conceptuales utilizados en la construcción del enfoque propuesto.



\### 3.4 Gestión del conocimiento



Se incorporan principios asociados al ciclo de vida del conocimiento, incluyendo su creación o adquisición, almacenamiento, mantenimiento, actualización, utilización y eventual retiro.



El conocimiento se considera un activo que debe permanecer gestionable independientemente de la tecnología que lo consuma.



\### 3.5 Gobernanza y trazabilidad



La metodología incorpora principios de gobernanza relacionados con trazabilidad, responsabilidad, documentación, validación, control de cambios, evaluación y supervisión.



Cada componente relevante del conocimiento deberá poder relacionarse, cuando corresponda, con su fuente, evidencia, versión y estado de validación.



\### 3.6 Integración metodológica



La metodología no plantea estos fundamentos como componentes aislados.



Su hipótesis de trabajo consiste en integrarlos dentro de una arquitectura en la que documentos, conocimiento estructurado, reglas, evidencias, mecanismos de inferencia e inteligencia artificial puedan relacionarse de manera gobernable y trazable.



En esta arquitectura se establece como principio fundamental:



\*\*La IA consume conocimiento; no lo reemplaza.\*\*



El conocimiento deberá poder existir, ser revisado, actualizado, auditado y preservado independientemente del modelo de inteligencia artificial utilizado.



La integración específica de estos componentes constituye una hipótesis metodológica en desarrollo y deberá ser contrastada con literatura especializada, metodologías existentes y estándares aplicables antes de atribuirle carácter original.



\---



\# 4. Principios Metodológicos



\### 4.1 Independencia del conocimiento respecto de la tecnología



El conocimiento gestionado por un sistema experto debe mantenerse conceptualmente independiente de las tecnologías utilizadas para almacenarlo, procesarlo, consultarlo o utilizarlo.



Los modelos de inteligencia artificial, motores de inferencia, bases de datos, lenguajes de programación y demás componentes tecnológicos constituyen mecanismos para utilizar el conocimiento, pero no deben convertirse en su única forma de existencia.



Esta separación busca permitir que el conocimiento pueda ser preservado, revisado, actualizado, validado, auditado y reutilizado aun cuando cambien las tecnologías que participan en el sistema.



Por lo tanto, la sustitución o evolución de un componente tecnológico no debería implicar la pérdida de la estructura, procedencia, evidencia, relaciones, versiones o estado de validación del conocimiento.



Este principio se resume en la siguiente formulación:



\*\*La tecnología puede cambiar; el conocimiento debe permanecer gobernable.\*\*



Este principio complementa la formulación establecida previamente:



\*\*La IA consume conocimiento; no lo reemplaza.\*\*



\### 4.2 Trazabilidad del conocimiento



Todo conocimiento incorporado o utilizado por el sistema deberá poder ser relacionado, cuando corresponda, con su origen, fuente, evidencia, versión y estado de validación.



La trazabilidad permite conocer de dónde proviene un elemento de conocimiento, qué antecedentes lo sustentan, qué transformaciones ha experimentado y bajo qué condiciones se encuentra vigente dentro del sistema.



Este principio busca evitar que reglas, criterios, conceptos, relaciones o recomendaciones permanezcan aislados de los antecedentes que permiten justificar su existencia y utilización.



La trazabilidad deberá mantenerse durante el ciclo de vida del conocimiento, incluyendo su incorporación, revisión, actualización, reemplazo, invalidación o retiro.



Cuando una decisión o resultado del sistema utilice conocimiento sujeto a requisitos normativos, técnicos, documentales o expertos, deberá ser posible identificar los elementos de conocimiento relevantes que participaron en dicho proceso y, cuando corresponda, sus fuentes y evidencias asociadas.



Este principio no establece todavía los mecanismos tecnológicos utilizados para implementar la trazabilidad. Estos deberán definirse en las capas y componentes correspondientes de la arquitectura.



\*\*El conocimiento utilizado por el sistema debe poder rastrearse hasta los antecedentes que sustentan su utilización.\*\*



\### 4.3 Validación del conocimiento



El conocimiento incorporado al sistema deberá someterse a mecanismos de validación acordes con su naturaleza, origen, nivel de riesgo y contexto de utilización.



La incorporación de una fuente, documento, norma, evidencia, certificado, criterio técnico o conocimiento experto no implica por sí misma que su contenido se encuentre validado para ser utilizado por el sistema.



La validación deberá permitir determinar, cuando corresponda, la pertinencia, consistencia, vigencia y suficiencia del conocimiento respecto del propósito para el cual será utilizado.



Los criterios y mecanismos de validación podrán variar según el tipo de conocimiento. El conocimiento normativo, técnico, documental, empírico o experto puede requerir fuentes, evidencias, responsables y procedimientos de validación diferentes.



El estado de validación deberá mantenerse asociado al conocimiento y formar parte de su trazabilidad durante su ciclo de vida.



La validación no deberá considerarse necesariamente permanente. Cuando una fuente, certificado, evidencia o documento posea vigencia temporal, se encuentre asociado a una partida, lote, versión o condición específica, o esté sujeto a revisión periódica, dichas condiciones deberán formar parte del control y estado de validación del conocimiento asociado.



Cuando cambien las fuentes, evidencias, condiciones del dominio, versiones documentales o antecedentes que sustentan un elemento de conocimiento, deberá evaluarse la necesidad de una nueva validación.



Este principio no supone que el sistema experto sustituya la competencia o responsabilidad de los especialistas encargados de determinar la validez jurídica, técnica, científica o profesional de una fuente o criterio.



\*\*Incorporar conocimiento no significa validarlo; su utilización requiere determinar previamente bajo qué condiciones puede considerarse válido.\*\*



\### 4.4 Vigencia y evolución del conocimiento



El conocimiento gestionado por el sistema deberá mantener información suficiente para determinar su estado de vigencia y reconstruir su evolución a lo largo del tiempo.



La incorporación de una nueva versión, modificación, sustitución, derogación o actualización de una fuente no deberá implicar necesariamente la eliminación del conocimiento anteriormente utilizado.



Cuando corresponda, el sistema deberá permitir distinguir entre conocimiento vigente, modificado, sustituido, derogado, obsoleto o sujeto a revisión, conservando las relaciones necesarias para identificar qué elemento lo reemplazó, modificó o dejó sin efecto.



Los mecanismos de evolución podrán variar según la naturaleza de la fuente. Entre otros casos, deberán considerarse:



\* disposiciones legales o reglamentarias que sean modificadas, derogadas total o parcialmente o sustituidas por otras;

\* normas técnicas que publiquen nuevas ediciones, versiones o modificaciones;

\* documentos controlados de sistemas de gestión que sean revisados y sustituidos, conservándose las versiones anteriores como documentación obsoleta cuando corresponda;

\* certificados, evidencias u otros antecedentes cuya validez dependa de fechas, períodos, partidas, lotes, versiones o condiciones determinadas.



La conservación histórica deberá permitir reconstruir qué conocimiento se encontraba vigente, validado y disponible para utilización en un momento determinado.



Cuando un elemento de conocimiento deje de estar vigente, su conservación histórica no deberá implicar que continúe habilitado para ser utilizado como conocimiento vigente por el sistema.



Los cambios relevantes deberán conservar trazabilidad suficiente para identificar, cuando corresponda, la versión anterior, la nueva versión, la naturaleza del cambio, su fecha, su fuente y las razones que justificaron la modificación de su estado.



Este principio permite que las decisiones o resultados históricos puedan interpretarse considerando el conocimiento que se encontraba disponible y vigente en el momento en que fueron producidos.



\*\*El conocimiento puede cambiar de estado o ser sustituido; su evolución y contexto histórico deben permanecer trazables.\*\*



\### 4.5 Inferencia sustentada en conocimiento



Las inferencias, conclusiones, glosas, recomendaciones, acciones o directrices generadas por un sistema experto deberán encontrarse sustentadas en conocimiento identificable, trazable, validado y vigente bajo las condiciones aplicables al contexto analizado.



El sistema deberá mantener una distinción conceptual entre las fuentes que proporcionan conocimiento, las evidencias que describen o acreditan una condición y las inferencias que se obtienen a partir de dichos antecedentes.



Una inferencia generada por el sistema no deberá presentarse como si correspondiera directamente al contenido de una fuente, norma, disposición legal o reglamentaria, certificado, documento técnico, evidencia de inspección u otro antecedente utilizado para sustentarla.



Cuando el conocimiento disponible sea suficiente y consistente para sustentar una inferencia, el sistema podrá generar resultados y proponer recomendaciones, acciones o directrices, manteniendo la relación con los elementos de conocimiento y evidencias relevantes que participaron en su elaboración.



Cuando existan contradicciones entre fuentes, documentos, versiones, requisitos, evidencias u otros antecedentes relevantes, el sistema deberá identificar y documentar dicha condición, permitiendo reconocer entre qué elementos se produce la discrepancia o inconsistencia.



La existencia de información contradictoria no deberá ser ocultada mediante la generación de una conclusión aparentemente definitiva cuando dicha contradicción pueda afectar materialmente el resultado de la inferencia.



Cuando el conocimiento disponible resulte insuficiente para sustentar adecuadamente una inferencia, el sistema deberá poder declarar dicha insuficiencia e identificar, cuando sea posible, los antecedentes adicionales requeridos para continuar el análisis.



En situaciones de contradicción, insuficiencia o incertidumbre que requieran interpretación o pronunciamiento externo, el sistema podrá recomendar la revisión por un especialista competente o la consulta a la autoridad, organismo o institución que corresponda. El sistema no deberá atribuir a dichos terceros una interpretación, decisión o respuesta que no haya sido efectivamente obtenida y registrada como antecedente.



Los nuevos antecedentes obtenidos como resultado de estas revisiones o consultas deberán incorporarse al sistema de conocimiento conforme a los principios de trazabilidad, validación, vigencia y evolución establecidos en esta metodología antes de ser utilizados para sustentar nuevas inferencias.



El resultado de una inferencia deberá conservar, cuando corresponda, información suficiente para reconstruir los principales antecedentes utilizados y comprender el fundamento de la conclusión o recomendación generada.



Este principio no determina todavía los algoritmos, modelos de inteligencia artificial, motores de inferencia o mecanismos tecnológicos utilizados para producir dichas inferencias. Estos deberán definirse posteriormente en las capas y componentes correspondientes de la arquitectura.



\*\*El conocimiento sustenta la inferencia; toda inferencia relevante debe poder relacionarse con el conocimiento y las evidencias que la sustentan.\*\*





\---



\# 5. Capas del Sistema



Pendiente de desarrollo.



\---



\# 6. Familias Documentales



Pendiente de desarrollo.



\---



\# 7. Sistema de Conocimiento



Pendiente de desarrollo.



\---



\# 8. Ciclo de Desarrollo



Pendiente de desarrollo.



\---



\# 9. Gobernanza y Trazabilidad



Pendiente de desarrollo.



\---



\# 10. Gestión de Decisiones Arquitectónicas



Pendiente de desarrollo.



\---



\# 11. Gestión de Continuidad



Pendiente de desarrollo.



\---



\# 12. Independencia Tecnológica



Pendiente de desarrollo.



\---



\# 13. Validación de la Metodología



Pendiente de desarrollo.



\---



\# 14. Aplicabilidad a Otros Dominios



Pendiente de desarrollo.



\---



\# 15. Limitaciones



Pendiente de desarrollo.



\---



\# 16. Referencias



Pendiente de consolidación.



\---



\# 17. Historial de Cambios



| Versión | Fecha | Descripción |

|---|---|---|

| 0.1 | 2026-08-10 | Creación de la estructura inicial del documento. |

