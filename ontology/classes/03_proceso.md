\# Clase ontológica: Proceso



\## 1. Identificación



\### Nombre



Proceso



\### Código



CLS\_ORGANIZACION\_PROCESO



\### Dominio



Organización y Operación



\### Versión



0.1



\### Estado



Borrador



\---



\## 2. Definición conceptual



Conjunto organizado de actividades relacionadas que utiliza recursos, información, personas, equipos, materiales o servicios para transformar entradas en resultados.



Dentro de PrevInspect AI, la clase Proceso representa el contexto operacional en el cual se ejecutan tareas, se utilizan equipos y sustancias, aparecen peligros, se generan exposiciones y se implementan medidas de control.



Un proceso puede ser:



\- estratégico;

\- operativo;

\- productivo;

\- logístico;

\- administrativo;

\- de mantenimiento;

\- de apoyo;

\- de emergencia;

\- externalizado;

\- temporal;

\- continuo;

\- discontinuo.



El proceso no debe entenderse solamente como un diagrama o documento. Debe representar la forma real en que las actividades son ejecutadas dentro de la organización.



\---



\## 3. Propósito dentro de PrevInspect AI



Representar la unidad funcional y operacional donde se conectan:



\- empresa;

\- centro de trabajo;

\- áreas;

\- trabajadores;

\- cargos;

\- tareas;

\- equipos;

\- herramientas;

\- sustancias;

\- materiales;

\- peligros;

\- riesgos;

\- medidas de control;

\- procedimientos;

\- registros;

\- indicadores;

\- eventos;

\- acciones correctivas;

\- requisitos normativos.



La clase Proceso permite que el sistema analice la prevención desde el funcionamiento real de la organización.



También permite detectar diferencias entre:



\- proceso documentado;

\- proceso declarado;

\- proceso observado;

\- proceso realmente ejecutado.



\---



\## 4. Propiedades



| Propiedad | Descripción | Tipo | Obligatoria | Cardinalidad |

|---|---|---|---|---|

| identificador | Identificador único del proceso | Texto | Sí | 1 |

| nombre | Nombre oficial del proceso | Texto | Sí | 1 |

| codigo | Código interno del proceso | Texto | No | 0:1 |

| descripcion | Explicación general del proceso | Texto | Sí | 1 |

| tipo\_proceso | Estratégico, operativo, apoyo u otro | Catálogo | Sí | 1 |

| empresa | Empresa responsable | Referencia | Sí | 1:N |

| centro\_trabajo | Centro donde se ejecuta | Referencia | Sí | 1:N |

| area\_responsable | Área propietaria o responsable | Referencia | Sí | 1:N |

| responsable\_proceso | Persona o rol responsable | Referencia | Condicional | 0:N |

| objetivo | Resultado esperado del proceso | Texto | Sí | 1:N |

| entradas | Recursos o antecedentes recibidos | Referencia/Texto | Sí | 1:N |

| salidas | Productos, servicios o resultados generados | Referencia/Texto | Sí | 1:N |

| tareas | Actividades que componen el proceso | Referencia | Sí | 1:N |

| trabajadores | Personas que participan | Referencia | Condicional | 0:N |

| cargos | Funciones que intervienen | Referencia | No | 0:N |

| equipos | Equipos y máquinas utilizados | Referencia | No | 0:N |

| herramientas | Herramientas utilizadas | Referencia | No | 0:N |

| sustancias | Sustancias utilizadas o generadas | Referencia | No | 0:N |

| materiales | Materias primas o insumos | Referencia | No | 0:N |

| residuos | Residuos generados | Referencia | No | 0:N |

| peligros | Peligros asociados | Referencia | No | 0:N |

| riesgos | Riesgos evaluados | Referencia | No | 0:N |

| controles | Medidas de control asociadas | Referencia | No | 0:N |

| procedimientos | Procedimientos aplicables | Referencia | No | 0:N |

| normativa | Requisitos normativos aplicables | Referencia | No | 0:N |

| indicadores | Indicadores de desempeño | Referencia | No | 0:N |

| frecuencia | Frecuencia de ejecución | Catálogo/Texto | No | 0:1 |

| duracion | Duración estimada | Número/Texto | No | 0:1 |

| horario | Jornada o período de ejecución | Catálogo/Texto | No | 0:N |

| condiciones\_operacionales | Condiciones normales de ejecución | Texto/Referencia | No | 0:N |

| condiciones\_anormales | Desviaciones previsibles | Texto/Referencia | No | 0:N |

| situaciones\_emergencia | Emergencias asociadas | Referencia | No | 0:N |

| nivel\_criticidad | Criticidad operacional o preventiva | Catálogo/Indicador | No | 0:1 |

| estado | Activo, suspendido, en cambio u obsoleto | Catálogo | Sí | 1 |

| fecha\_revision | Fecha de última revisión | Fecha | No | 0:1 |



\---



\## 5. Relaciones



| Relación | Clase destino | Cardinalidad | Descripción |

|---|---|---|---|

| PERTENECE\_A | Empresa | 1:N | Identifica la organización responsable |

| SE\_EJECUTA\_EN | Centro de Trabajo | 1:N | Ubica físicamente el proceso |

| ES\_RESPONSABILIDAD\_DE | Área | 1:N | Identifica el área responsable |

| ES\_GESTIONADO\_POR | Persona o Rol | 0:N | Identifica responsables del proceso |

| RECIBE | Entrada | 1:N | Representa recursos recibidos |

| GENERA | Salida | 1:N | Representa resultados obtenidos |

| CONTIENE | Tarea | 1:N | Identifica las actividades que lo componen |

| ES\_EJECUTADO\_POR | Trabajador | 0:N | Relaciona personas participantes |

| REQUIERE | Competencia | 0:N | Identifica conocimientos o habilidades necesarias |

| UTILIZA | Equipo | 0:N | Registra equipos empleados |

| UTILIZA | Herramienta | 0:N | Registra herramientas utilizadas |

| UTILIZA | Sustancia | 0:N | Identifica sustancias empleadas |

| CONSUME | Material | 0:N | Relaciona materias primas o insumos |

| GENERA | Residuo | 0:N | Identifica residuos resultantes |

| PRESENTA | Peligro | 0:N | Registra peligros asociados |

| GENERA | Exposición | 0:N | Relaciona exposiciones derivadas |

| POSEE | Riesgo | 0:N | Relaciona riesgos evaluados |

| REQUIERE | Medida de Control | 0:N | Identifica controles necesarios |

| ESTA\_REGULADO\_POR | Documento Normativo | 0:N | Relaciona requisitos aplicables |

| SE\_EJECUTA\_MEDIANTE | Procedimiento | 0:N | Vincula instrucciones de trabajo |

| GENERA | Evidencia | 0:N | Registra documentos o registros resultantes |

| ES\_EVALUADO\_MEDIANTE | Indicador | 0:N | Relaciona mediciones de desempeño |

| ES\_REVISADO\_MEDIANTE | Auditoría | 0:N | Vincula revisiones formales |

| ES\_VERIFICADO\_MEDIANTE | Inspección | 0:N | Relaciona verificaciones en terreno |

| PUEDE\_GENERAR | Evento | 0:N | Vincula accidentes, incidentes o desviaciones |

| REQUIERE | Mantenimiento | 0:N | Relaciona actividades de mantenimiento |

| INTERACTUA\_CON | Proceso | 0:N | Representa interfaces entre procesos |

| DEPENDE\_DE | Proceso | 0:N | Identifica dependencias operacionales |

| ENTREGA\_A | Proceso | 0:N | Representa la continuidad del flujo |

| ES\_MODIFICADO\_POR | Cambio | 0:N | Registra modificaciones operacionales |

| GENERA | Acción Correctiva | 0:N | Relaciona mejoras derivadas de hallazgos |

| GENERA | Lección Aprendida | 0:N | Registra conocimiento obtenido |



\---



\## 6. Restricciones ontológicas



1\. Todo proceso debe pertenecer al menos a una empresa.



2\. Todo proceso activo debe tener un objetivo definido.



3\. Todo proceso debe poseer al menos una entrada, una tarea y una salida.



4\. Todo proceso operacional debe estar asociado a uno o más centros de trabajo o contextos de ejecución.



5\. Un proceso no debe asociarse directamente a riesgos sin identificar las tareas, condiciones o peligros que los originan.



6\. Los peligros de un proceso pueden variar según:



&#x20;  - centro de trabajo;

&#x20;  - turno;

&#x20;  - etapa;

&#x20;  - equipo utilizado;

&#x20;  - sustancia presente;

&#x20;  - trabajador involucrado;

&#x20;  - condición ambiental;

&#x20;  - interacción con otros procesos.



7\. Un proceso documentado no necesariamente representa la forma real de ejecución.



8\. La ausencia de procedimientos no implica que el proceso no exista.



9\. La existencia de un procedimiento no demuestra que el proceso se ejecute conforme a él.



10\. Los procesos externalizados deben permanecer dentro del análisis cuando puedan afectar la seguridad y salud de las personas.



11\. Los procesos administrativos también pueden contener peligros y riesgos.



12\. Las actividades no rutinarias deberán distinguirse de las rutinarias.



13\. Las condiciones normales, anormales y de emergencia deberán representarse por separado cuando generen riesgos diferentes.



14\. Un cambio de proceso puede modificar los riesgos, aunque el nombre del proceso se mantenga.



15\. La criticidad productiva no equivale necesariamente a criticidad preventiva.



16\. Un proceso puede ser responsabilidad de más de un área, pero debe existir una responsabilidad claramente coordinada.



\---



\## 7. Reglas de negocio



1\. Todo proceso debe tener un responsable o propietario claramente identificado cuando corresponda.



2\. Las tareas reales deben estar representadas dentro del proceso.



3\. Los peligros deben identificarse considerando todas las etapas del proceso.



4\. La evaluación de riesgos debe considerar:



&#x20;  - operación normal;

&#x20;  - puesta en marcha;

&#x20;  - detención;

&#x20;  - limpieza;

&#x20;  - ajuste;

&#x20;  - mantenimiento;

&#x20;  - reparación;

&#x20;  - fallas;

&#x20;  - emergencias;

&#x20;  - actividades no rutinarias.



5\. Los controles deben relacionarse con peligros y riesgos específicos.



6\. Los trabajadores deben conocer:



&#x20;  - su participación en el proceso;

&#x20;  - las tareas asignadas;

&#x20;  - los peligros asociados;

&#x20;  - los controles requeridos;

&#x20;  - las respuestas ante emergencias.



7\. Los procedimientos deben reflejar la forma real de ejecución.



8\. Las interfaces entre procesos deben analizarse porque pueden generar riesgos no visibles dentro de un proceso aislado.



9\. Todo cambio significativo debe activar una revisión preventiva.



10\. Los indicadores del proceso deben permitir detectar desviaciones antes de que ocurra un daño.



11\. Los hallazgos repetidos deben analizarse como posibles fallas del proceso y no solamente como errores individuales.



12\. Los controles críticos deben contar con mecanismos de verificación.



13\. Las tareas externalizadas deben tener responsabilidades y controles coordinados.



14\. La información de entrada debe ser suficiente para ejecutar el proceso de forma segura.



15\. Las salidas del proceso no deben generar riesgos no controlados para procesos posteriores.



\---



\## 8. Reglas de inferencia



\### Regla PROC-001 — Proceso sin tareas



SI un proceso está activo



Y no posee tareas identificadas



ENTONCES el sistema debe clasificarlo como proceso insuficientemente modelado.



\---



\### Regla PROC-002 — Tarea con peligro



SI un proceso contiene una tarea



Y la tarea presenta un peligro



ENTONCES el proceso hereda ese peligro como peligro potencial asociado.



La exposición concreta deberá evaluarse según el contexto.



\---



\### Regla PROC-003 — Peligro sin evaluación



SI un proceso presenta un peligro



Y no existe un riesgo evaluado asociado



ENTONCES el sistema debe generar una alerta por evaluación incompleta.



\---



\### Regla PROC-004 — Riesgo sin control



SI un proceso posee un riesgo evaluado



Y el riesgo no tiene medidas de control asociadas



ENTONCES el sistema debe generar una brecha preventiva.



\---



\### Regla PROC-005 — Control sin verificación



SI un proceso declara un control implementado



Y no existe evidencia de verificación



ENTONCES el control debe clasificarse como no verificado.



\---



\### Regla PROC-006 — Procedimiento desactualizado



SI un proceso ha sido modificado



Y el procedimiento asociado no ha sido revisado posteriormente



ENTONCES el sistema debe generar una alerta por posible desactualización documental.



\---



\### Regla PROC-007 — Diferencia entre proceso y tarea real



SI las tareas observadas no coinciden con las tareas documentadas



ENTONCES el sistema debe generar una alerta por brecha entre diseño y ejecución.



\---



\### Regla PROC-008 — Cambio de equipo



SI un proceso incorpora un equipo nuevo



ENTONCES el sistema debe verificar:



\- peligros nuevos;

\- riesgos modificados;

\- competencias requeridas;

\- mantenimiento;

\- protecciones;

\- procedimiento;

\- capacitación;

\- emergencia;

\- autorizaciones.



\---



\### Regla PROC-009 — Cambio de sustancia



SI un proceso incorpora una sustancia nueva



ENTONCES el sistema debe verificar:



\- HDS;

\- clasificación de peligros;

\- almacenamiento;

\- manipulación;

\- exposición;

\- ventilación;

\- EPP;

\- residuos;

\- respuesta ante emergencias;

\- vigilancia de salud.



\---



\### Regla PROC-010 — Interacción entre procesos



SI dos procesos se ejecutan simultáneamente



Y comparten espacio, personas, equipos o fuentes de energía



ENTONCES el sistema debe evaluar riesgos de interacción.



\---



\### Regla PROC-011 — Proceso externalizado



SI un proceso es ejecutado por una empresa contratista



ENTONCES el sistema debe identificar:



\- empresa responsable;

\- empresa ejecutora;

\- trabajadores involucrados;

\- coordinación preventiva;

\- procedimientos;

\- controles;

\- supervisión;

\- evidencias.



\---



\### Regla PROC-012 — Evento repetido



SI un mismo tipo de evento se repite dentro de un proceso



ENTONCES el sistema debe aumentar la probabilidad de que exista:



\- una causa sistémica;

\- un control ineficaz;

\- una supervisión insuficiente;

\- una acción correctiva no eficaz;

\- una desviación normalizada.



Estas hipótesis deberán validarse mediante evidencia.



\---



\### Regla PROC-013 — Desviación normalizada



SI una práctica insegura se observa de manera repetida



Y es aceptada como parte habitual del proceso



ENTONCES el sistema debe generar una alerta por normalización de la desviación.



\---



\### Regla PROC-014 — Falta de responsable



SI un proceso no posee responsable identificado



ENTONCES el sistema debe generar una alerta de gobernanza operacional.



\---



\### Regla PROC-015 — Información insuficiente



SI faltan antecedentes sobre tareas, equipos, sustancias o condiciones de ejecución



ENTONCES el sistema no debe concluir ausencia de peligro.



Debe solicitar información adicional.



\---



\### Regla PROC-016 — Control crítico



SI un proceso depende de un control crítico



Y dicho control falla, está ausente o no puede verificarse



ENTONCES el sistema debe elevar la prioridad del análisis.



\---



\### Regla PROC-017 — Condición anormal



SI un proceso opera fuera de sus parámetros normales



ENTONCES el sistema debe evaluar si cambian:



\- peligros;

\- nivel de riesgo;

\- controles requeridos;

\- competencias;

\- respuesta operacional.



\---



\### Regla PROC-018 — Salida peligrosa



SI la salida de un proceso genera una exposición o peligro para otro proceso



ENTONCES ambos procesos deben quedar relacionados dentro del análisis preventivo.



\---



\## 9. Fuentes normativas y técnicas



| Fuente | Tipo de autoridad | Aplicación |

|---|---|---|

| Legislación laboral aplicable | Jurídica | Protección de las personas durante la ejecución de actividades |

| Ley 16.744 | Jurídica | Prevención de accidentes y enfermedades profesionales |

| Reglamentos de gestión preventiva vigentes | Jurídica reglamentaria | Identificación de peligros, responsabilidades y controles |

| DS 594 | Jurídica reglamentaria | Condiciones sanitarias y ambientales |

| Normativa sectorial | Jurídica/técnica | Exigencias específicas según actividad |

| ISO 45001 | Técnica | Planificación, operación, control y gestión del cambio |

| ISO 9001 | Técnica | Enfoque basado en procesos, seguimiento y mejora |

| Procedimientos internos | Organizacional | Forma establecida de ejecución |

| Manuales de equipos | Técnica | Condiciones seguras de operación |

| HDS | Técnica | Información sobre sustancias peligrosas |

| Dictámenes y pronunciamientos | Interpretativa oficial | Aplicación práctica de obligaciones |



> La vigencia y aplicabilidad específica de cada fuente deberá ser confirmada por el Motor Normativo.



\---



\## 10. Evidencias relacionadas



\- Mapa de procesos.

\- Diagramas de flujo.

\- Fichas de proceso.

\- Procedimientos.

\- Instructivos.

\- Registros operacionales.

\- Descripciones de cargo.

\- Matrices IPER.

\- Permisos de trabajo.

\- Registros de producción.

\- Registros de mantenimiento.

\- Manuales de equipos.

\- HDS.

\- Registros de capacitación.

\- Inspecciones.

\- Auditorías.

\- Fotografías de terreno.

\- Observaciones de tareas.

\- Entrevistas a trabajadores.

\- Indicadores de proceso.

\- Registros de incidentes.

\- Investigaciones de accidentes.

\- Acciones correctivas.

\- Registros de gestión del cambio.

\- Planes de emergencia.

\- Evaluaciones ambientales.

\- Informes técnicos.



La evidencia deberá analizarse considerando:



\- correspondencia con la realidad;

\- vigencia;

\- alcance;

\- trazabilidad;

\- responsable;

\- integridad;

\- frecuencia de actualización;

\- consistencia entre fuentes.



\---



\## 11. Preguntas de competencia



La clase Proceso debe permitir responder:



1\. ¿Cuál es el objetivo del proceso?

2\. ¿A qué empresa pertenece?

3\. ¿Dónde se ejecuta?

4\. ¿Qué área es responsable?

5\. ¿Quién administra el proceso?

6\. ¿Qué entradas utiliza?

7\. ¿Qué salidas genera?

8\. ¿Qué tareas lo componen?

9\. ¿Qué trabajadores participan?

10\. ¿Qué competencias necesitan?

11\. ¿Qué equipos se utilizan?

12\. ¿Qué herramientas se emplean?

13\. ¿Qué sustancias están presentes?

14\. ¿Qué residuos se generan?

15\. ¿Qué peligros existen?

16\. ¿Qué riesgos han sido evaluados?

17\. ¿Qué controles están definidos?

18\. ¿Qué controles son críticos?

19\. ¿Qué controles cuentan con evidencia?

20\. ¿Qué procedimientos aplican?

21\. ¿Los procedimientos reflejan la operación real?

22\. ¿Qué normativa aplica?

23\. ¿Qué procesos interactúan con este?

24\. ¿Qué riesgos aparecen en las interfaces?

25\. ¿Qué cambios recientes se han realizado?

26\. ¿Los cambios fueron evaluados?

27\. ¿Qué incidentes se han registrado?

28\. ¿Qué hallazgos se repiten?

29\. ¿Existen desviaciones normalizadas?

30\. ¿Qué información falta?

31\. ¿Cuál es la criticidad preventiva del proceso?

32\. ¿Qué acciones deberían priorizarse?

33\. ¿Cuál es el nivel de confianza de la evaluación?



\---



\## 12. Casos de uso



\- Identificación de peligros.

\- Evaluación de riesgos.

\- Elaboración de matrices IPER.

\- Diseño de controles.

\- Revisión de procedimientos.

\- Auditorías de procesos.

\- Inspecciones en terreno.

\- Gestión del cambio.

\- Investigación de accidentes.

\- Investigación de incidentes.

\- Evaluación de contratistas.

\- Diseño de capacitación.

\- Determinación de EPP.

\- Revisión de vigilancia de salud.

\- Evaluación de procesos críticos.

\- Detección de interfaces peligrosas.

\- Comparación entre proceso documentado y proceso real.

\- Priorización de acciones correctivas.

\- Análisis de madurez operacional.

\- Construcción del Knowledge Graph.



\---



\## 13. Ejemplos de instancias



\### Proceso de soldadura



Entradas:



\- estructuras metálicas;

\- electrodos;

\- gases;

\- energía eléctrica.



Tareas:



\- preparación de piezas;

\- conexión del equipo;

\- soldadura;

\- limpieza;

\- inspección.



Peligros posibles:



\- radiación;

\- humos metálicos;

\- proyección de partículas;

\- electricidad;

\- incendio;

\- posturas forzadas.



\---



\### Proceso de mantenimiento mecánico



Entradas:



\- equipo a intervenir;

\- herramientas;

\- repuestos;

\- lubricantes.



Tareas:



\- diagnóstico;

\- bloqueo;

\- desmontaje;

\- reparación;

\- montaje;

\- prueba.



Peligros posibles:



\- energía residual;

\- atrapamiento;

\- caída de objetos;

\- contacto con sustancias;

\- puesta en marcha inesperada.



\---



\### Proceso de almacenamiento



Entradas:



\- productos;

\- repuestos;

\- sustancias;

\- información de recepción.



Tareas:



\- recepción;

\- descarga;

\- clasificación;

\- almacenamiento;

\- preparación;

\- despacho.



Peligros posibles:



\- caída de materiales;

\- tránsito de equipos;

\- sobreesfuerzo;

\- incendio;

\- derrames;

\- golpes.



\---



\### Proceso administrativo



Entradas:



\- documentos;

\- información;

\- requerimientos.



Tareas:



\- digitación;

\- revisión;

\- reuniones;

\- atención de personas.



Peligros posibles:



\- carga mental;

\- posturas mantenidas;

\- fatiga visual;

\- factores psicosociales;

\- emergencias del lugar de trabajo.



\---



\## 14. Exclusiones



La clase Proceso no debe confundirse con:



\- Tarea: actividad concreta ejecutada dentro de un proceso.

\- Procedimiento: documento que describe cómo ejecutar actividades.

\- Área: división funcional responsable del proceso.

\- Centro de Trabajo: lugar donde se ejecuta.

\- Proyecto: esfuerzo temporal con objetivos definidos.

\- Operación: ejecución concreta de actividades.

\- Equipo: recurso físico utilizado.

\- Producto: salida generada.

\- Riesgo: posibilidad de daño asociada a una exposición.

\- Actividad económica: clasificación general de la empresa.



Un proceso puede contener múltiples tareas y puede ejecutarse en más de un centro de trabajo.



\---



\## 15. Nivel de madurez



\### Nivel actual



Nivel 2 — Relaciones iniciales.



La clase posee:



\- definición;

\- propiedades;

\- relaciones;

\- restricciones;

\- reglas de negocio;

\- reglas de inferencia iniciales;

\- evidencias;

\- preguntas de competencia;

\- ejemplos.



\### Pendientes para Nivel 3 — Normativa



\- validar fuentes aplicables;

\- incorporar normativa sectorial;

\- relacionar requisitos por tipo de proceso;

\- definir controles regulatorios críticos;

\- integrar obligaciones de gestión del cambio.



\### Pendientes para Nivel 4 — Casos



\- probar procesos industriales;

\- probar procesos administrativos;

\- analizar procesos externalizados;

\- relacionar accidentes reales anonimizados;

\- validar diferencias entre proceso declarado y observado.



\### Pendientes para Nivel 5 — Razonamiento experto



\- crear reglas por tipo de proceso;

\- identificar patrones de falla;

\- calcular confianza de las inferencias;

\- integrar Motor de Contexto;

\- integrar Motor de Hipótesis;

\- integrar Motor de Evidencias;

\- generar explicaciones trazables;

\- validar resultados con profesionales.



\---



\## 16. Observaciones



La clase Proceso es uno de los principales conectores de la ontología.



Permite representar la cadena:



Empresa



↓



Centro de Trabajo



↓



Área



↓



Proceso



↓



Tarea



↓



Peligro



↓



Riesgo



↓



Medida de Control



↓



Evidencia



PrevInspect AI deberá analizar los procesos considerando la realidad operacional y no solamente la documentación disponible.



El sistema deberá prestar especial atención a:



\- actividades no rutinarias;

\- mantenimiento;

\- limpieza;

\- ajustes;

\- fallas;

\- emergencias;

\- cambios;

\- interacción entre empresas;

\- interacción entre procesos;

\- diferencias entre turnos;

\- trabajo real no documentado.



Un proceso aparentemente simple puede contener riesgos importantes cuando se analiza en condiciones anormales o durante actividades de apoyo.



Por esta razón, la clase Proceso deberá mantener siempre una relación explícita con las tareas concretas que lo componen.

