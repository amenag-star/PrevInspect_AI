\# Clase ontológica: Empresa



\## 1. Identificación



\### Nombre



Empresa



\### Código



CLS\_ORGANIZACION\_EMPRESA



\### Dominio



Organización



\### Versión



0.1



\### Estado



Borrador



\---



\## 2. Definición conceptual



Organización pública o privada que desarrolla una o más actividades económicas, productivas, comerciales, administrativas o de servicios, y que puede contratar trabajadores, administrar centros de trabajo, ejecutar procesos y asumir responsabilidades en materia de Seguridad y Salud Ocupacional.



Dentro de PrevInspect AI, la clase Empresa representa a la entidad organizacional responsable de establecer, implementar, mantener y mejorar las condiciones necesarias para proteger la vida y salud de las personas que participan en sus operaciones.



La empresa puede actuar como:



\- empleador directo;

\- empresa principal;

\- empresa contratista;

\- empresa subcontratista;

\- empresa de servicios transitorios;

\- organización usuaria;

\- mandante;

\- proveedor;

\- cliente;

\- entidad pública;

\- institución sin fines de lucro.



La función específica que desempeñe dependerá del contexto contractual y operacional analizado.



\---



\## 3. Propósito dentro de PrevInspect AI



Representar a la organización sobre la cual recaen obligaciones, responsabilidades, procesos, recursos, controles y evidencias relacionadas con la Seguridad y Salud Ocupacional.



Esta clase permite relacionar a la empresa con:



\- trabajadores;

\- centros de trabajo;

\- áreas;

\- procesos;

\- tareas;

\- instalaciones;

\- máquinas y equipos;

\- sustancias;

\- peligros;

\- riesgos;

\- medidas de control;

\- documentos;

\- procedimientos;

\- capacitaciones;

\- inspecciones;

\- auditorías;

\- incidentes;

\- accidentes;

\- enfermedades profesionales;

\- empresas contratistas y subcontratistas;

\- organismos administradores;

\- autoridades fiscalizadoras;

\- acciones correctivas y preventivas.



La clase Empresa constituye uno de los principales puntos de entrada para evaluar el nivel de gestión preventiva de una organización.



\---



\## 4. Propiedades



| Propiedad | Descripción | Tipo | Obligatoria | Cardinalidad |

|---|---|---|---|---|

| identificador | Identificador único de la organización | Texto | Sí | 1 |

| razon\_social | Nombre legal de la organización | Texto | Sí | 1 |

| nombre\_fantasia | Nombre comercial utilizado | Texto | No | 0:1 |

| identificacion\_tributaria | Identificador tributario o equivalente | Texto protegido | Condicional | 0:1 |

| tipo\_organizacion | Clasificación jurídica u organizacional | Catálogo | Sí | 1 |

| actividad\_economica | Actividad principal desarrollada | Catálogo/Texto | Sí | 1:N |

| actividades\_secundarias | Otras actividades desarrolladas | Catálogo/Texto | No | 0:N |

| tamaño\_empresa | Clasificación por tamaño | Catálogo | No | 0:1 |

| numero\_trabajadores | Dotación propia o estimada | Número | No | 0:N |

| numero\_contratistas | Dotación externa o estimada | Número | No | 0:N |

| representante\_legal | Persona que representa legalmente a la organización | Referencia | Condicional | 0:N |

| responsable\_sst | Persona, área o entidad responsable de SST | Referencia | Condicional | 0:N |

| organismo\_administrador | Organismo administrador asociado | Referencia | Condicional | 0:N |

| centros\_trabajo | Centros en los que desarrolla operaciones | Referencia | Sí | 1:N |

| areas | Divisiones funcionales u operativas | Referencia | No | 0:N |

| procesos | Procesos desarrollados por la organización | Referencia | Sí | 1:N |

| trabajadores | Personas vinculadas laboralmente | Referencia | Condicional | 0:N |

| empresas\_relacionadas | Contratistas, mandantes, clientes o proveedores | Referencia | No | 0:N |

| instalaciones | Infraestructura bajo su responsabilidad | Referencia | No | 0:N |

| equipos | Máquinas y equipos asociados | Referencia | No | 0:N |

| sustancias | Sustancias utilizadas, almacenadas o generadas | Referencia | No | 0:N |

| peligros | Peligros identificados en sus actividades | Referencia | No | 0:N |

| riesgos | Riesgos evaluados por la organización | Referencia | No | 0:N |

| controles | Medidas de control implementadas | Referencia | No | 0:N |

| documentos\_sst | Documentación preventiva vigente o histórica | Referencia | No | 0:N |

| certificaciones | Certificaciones de sistemas de gestión | Referencia | No | 0:N |

| estado\_operacional | Situación operacional de la empresa | Catálogo | Sí | 1 |

| nivel\_madurez\_sst | Evaluación del desarrollo preventivo | Catálogo/Indicador | No | 0:1 |



\---



\## 5. Relaciones



| Relación | Clase destino | Cardinalidad | Descripción |

|---|---|---|---|

| EMPLEA\_A | Trabajador | 0:N | Relaciona a la empresa con sus trabajadores directos |

| ADMINISTRA | Centro de Trabajo | 1:N | Identifica los centros bajo su gestión |

| CONTIENE | Área | 0:N | Representa divisiones organizacionales |

| EJECUTA | Proceso | 1:N | Identifica los procesos desarrollados |

| DEFINE | Cargo | 0:N | Registra cargos establecidos por la organización |

| ASIGNA | Tarea | 0:N | Relaciona funciones o actividades con personas y procesos |

| OPERA | Equipo | 0:N | Identifica equipos utilizados en sus actividades |

| ADMINISTRA | Instalación | 0:N | Relaciona infraestructura bajo su responsabilidad |

| UTILIZA | Sustancia | 0:N | Registra sustancias empleadas |

| ALMACENA | Sustancia | 0:N | Identifica sustancias almacenadas |

| GENERA | Residuo | 0:N | Representa residuos derivados de sus actividades |

| IDENTIFICA | Peligro | 0:N | Registra peligros reconocidos por la organización |

| EVALUA | Riesgo | 0:N | Relaciona la empresa con riesgos evaluados |

| IMPLEMENTA | Medida de Control | 0:N | Representa controles preventivos aplicados |

| EMITE | Documento | 0:N | Relaciona documentos internos emitidos |

| MANTIENE | Evidencia | 0:N | Identifica registros que respaldan cumplimiento |

| REALIZA | Inspección | 0:N | Registra inspecciones efectuadas |

| REALIZA | Auditoría | 0:N | Registra auditorías internas o externas |

| INVESTIGA | Evento | 0:N | Relaciona investigaciones con accidentes o incidentes |

| EJECUTA | Capacitación | 0:N | Identifica actividades formativas organizadas |

| GENERA | Acción Correctiva | 0:N | Representa medidas derivadas de hallazgos |

| GENERA | Acción Preventiva | 0:N | Representa medidas destinadas a evitar eventos |

| CONTRATA\_A | Empresa | 0:N | Relaciona a una empresa con contratistas o proveedores |

| PRESTA\_SERVICIOS\_A | Empresa | 0:N | Representa relaciones de prestación de servicios |

| ES\_PRINCIPAL\_DE | Empresa | 0:N | Identifica relaciones de empresa principal |

| ES\_CONTRATISTA\_DE | Empresa | 0:N | Identifica relaciones contractuales |

| ES\_SUBCONTRATISTA\_DE | Empresa | 0:N | Identifica relaciones de subcontratación |

| COORDINA\_CON | Empresa | 0:N | Representa coordinación preventiva entre organizaciones |

| ESTA\_ADHERIDA\_A | Organismo Administrador | 0:1 | Identifica el organismo administrador correspondiente |

| ES\_FISCALIZADA\_POR | Autoridad Fiscalizadora | 0:N | Relaciona autoridades competentes |

| DEBE\_CUMPLIR | Obligación | 0:N | Relaciona obligaciones legales, técnicas u organizacionales |

| ESTA\_REGULADA\_POR | Documento Normativo | 0:N | Identifica normas aplicables |

| REPORTA | Indicador SST | 0:N | Registra indicadores de desempeño preventivo |

| APRENDE\_DE | Lección Aprendida | 0:N | Relaciona mejoras derivadas de experiencia previa |



\---



\## 6. Restricciones ontológicas



1\. Toda empresa debe poseer un identificador único dentro del sistema.



2\. Toda empresa debe tener al menos una actividad económica o función organizacional identificada.



3\. Toda empresa operacional debe estar relacionada con al menos un proceso.



4\. Una empresa puede poseer varios centros de trabajo, y cada centro puede presentar condiciones, peligros y obligaciones diferentes.



5\. Las obligaciones aplicables no deben determinarse únicamente por el nombre o tamaño de la empresa.



6\. La normativa aplicable deberá considerar, entre otros factores:



&#x20;  - actividad económica;

&#x20;  - número de trabajadores;

&#x20;  - ubicación;

&#x20;  - procesos desarrollados;

&#x20;  - equipos utilizados;

&#x20;  - sustancias presentes;

&#x20;  - tipo de contratación;

&#x20;  - existencia de subcontratación;

&#x20;  - exposición a agentes;

&#x20;  - características del centro de trabajo;

&#x20;  - requisitos sectoriales.



7\. La relación contractual entre dos empresas no elimina las responsabilidades preventivas que correspondan a cada una.



8\. Una empresa principal, contratista y subcontratista deberán representarse como instancias diferentes, aunque participen en una misma faena.



9\. La existencia de documentos no demuestra por sí sola su implementación efectiva.



10\. La ausencia de accidentes registrados no demuestra necesariamente un adecuado desempeño preventivo.



11\. Una certificación de sistema de gestión no implica automáticamente cumplimiento total de todas las obligaciones legales.



12\. La empresa no debe ser evaluada como una entidad homogénea cuando posea centros, procesos o áreas con realidades diferentes.



13\. Los datos comerciales, personales o estratégicos deberán tener controles de acceso adecuados.



14\. El nivel de madurez preventiva no debe calcularse utilizando una sola variable.



\---



\## 7. Reglas de negocio



1\. Toda empresa debe identificar los procesos que forman parte de sus operaciones.



2\. Todo proceso debe relacionarse con sus tareas, peligros, riesgos y medidas de control.



3\. La empresa debe asignar responsabilidades preventivas dentro de su estructura organizacional.



4\. La documentación preventiva debe estar vigente, controlada, accesible y relacionada con la operación real.



5\. Los controles definidos deben contar con evidencia de implementación cuando corresponda.



6\. La empresa debe revisar su gestión preventiva ante cambios como:



&#x20;  - incorporación de nuevas tareas;

&#x20;  - modificaciones de procesos;

&#x20;  - adquisición de maquinaria;

&#x20;  - ingreso de sustancias;

&#x20;  - cambios de instalaciones;

&#x20;  - aumento de dotación;

&#x20;  - incorporación de contratistas;

&#x20;  - accidentes o incidentes;

&#x20;  - enfermedades profesionales;

&#x20;  - cambios normativos;

&#x20;  - resultados de auditorías o fiscalizaciones.



7\. Las empresas contratistas deben ser evaluadas considerando los riesgos de las tareas que ejecutarán.



8\. La empresa principal debe coordinar las actividades preventivas cuando varias organizaciones compartan una faena o centro de trabajo, según corresponda.



9\. Las acciones correctivas deberán tener:



&#x20;  - responsable;

&#x20;  - plazo;

&#x20;  - estado;

&#x20;  - evidencia de implementación;

&#x20;  - verificación de eficacia.



10\. Los indicadores preventivos deben combinar información reactiva y preventiva.



11\. Las decisiones de producción no deben invalidar controles esenciales para la protección de las personas.



12\. Toda brecha crítica debe ser comunicada a un responsable con capacidad para adoptar medidas.



13\. La empresa debe diferenciar entre:



&#x20;  - cumplimiento documental;

&#x20;  - implementación operacional;

&#x20;  - eficacia del control.



\---



\## 8. Reglas de inferencia



\### Regla EMP-001 — Procesos sin evaluación



SI una empresa ejecuta un proceso



Y el proceso no posee peligros identificados



ENTONCES el sistema debe generar una alerta por evaluación preventiva incompleta.



\---



\### Regla EMP-002 — Riesgo sin control



SI una empresa posee un riesgo identificado



Y no existe una medida de control asociada



ENTONCES el sistema debe clasificar la situación como una brecha preventiva.



La criticidad dependerá del nivel de riesgo y de la posible consecuencia.



\---



\### Regla EMP-003 — Control sin evidencia



SI una empresa declara una medida de control implementada



Y no existe evidencia suficiente de su aplicación



ENTONCES el sistema debe clasificar el control como no verificado.



No deberá considerarlo automáticamente inexistente ni plenamente implementado.



\---



\### Regla EMP-004 — Documento y realidad operacional



SI un documento interno establece una condición



Y la evidencia operacional muestra una práctica diferente



ENTONCES el sistema debe generar una alerta por falta de correspondencia entre documentación y operación.



\---



\### Regla EMP-005 — Contratistas



SI una empresa contrata a otra para ejecutar una tarea



Y la tarea presenta peligros relevantes



ENTONCES el sistema debe verificar:



\- coordinación preventiva;

\- identificación de riesgos;

\- competencias del personal;

\- procedimientos aplicables;

\- controles operacionales;

\- responsabilidades de cada organización;

\- evidencia de supervisión.



\---



\### Regla EMP-006 — Cambio operacional



SI una empresa introduce un cambio en:



\- proceso;

\- tarea;

\- equipo;

\- sustancia;

\- instalación;

\- dotación;

\- organización del trabajo;



ENTONCES el sistema debe verificar si corresponde actualizar:



\- identificación de peligros;

\- evaluación de riesgos;

\- medidas de control;

\- procedimientos;

\- capacitación;

\- vigilancia de salud;

\- planes de emergencia;

\- documentación relacionada.



\---



\### Regla EMP-007 — Repetición de eventos



SI una empresa registra eventos similares de manera repetida



ENTONCES el sistema debe considerar como hipótesis:



\- controles ineficaces;

\- acciones correctivas incompletas;

\- causas raíz no identificadas;

\- falta de supervisión;

\- aprendizaje organizacional insuficiente.



La hipótesis deberá validarse con evidencia adicional.



\---



\### Regla EMP-008 — Ausencia de accidentes



SI una empresa no registra accidentes durante un periodo



ENTONCES el sistema no deberá concluir automáticamente que existe una gestión preventiva eficaz.



Deberá revisar además:



\- incidentes;

\- cuasi accidentes;

\- inspecciones;

\- observaciones;

\- reportabilidad;

\- exposición;

\- cumplimiento de controles;

\- indicadores preventivos.



\---



\### Regla EMP-009 — Certificación



SI una empresa posee certificación de un sistema de gestión



ENTONCES el sistema podrá considerarla como evidencia favorable.



PERO no deberá inferir cumplimiento legal absoluto ni eficacia total de los controles.



\---



\### Regla EMP-010 — Diferencias entre centros



SI una empresa posee varios centros de trabajo



Y estos desarrollan actividades o presentan condiciones distintas



ENTONCES la evaluación deberá realizarse también a nivel de cada centro.



\---



\### Regla EMP-011 — Información insuficiente



SI faltan antecedentes relevantes sobre la empresa



ENTONCES el sistema debe identificar explícitamente:



\- qué información falta;

\- por qué es necesaria;

\- qué conclusión no puede confirmarse;

\- qué antecedentes deberían solicitarse.



\---



\### Regla EMP-012 — Responsabilidad no asignada



SI existe una obligación o acción preventiva



Y no posee responsable asignado



ENTONCES el sistema debe generar una alerta de gobernanza preventiva.



\---



\### Regla EMP-013 — Acción vencida



SI una acción correctiva supera su plazo



Y continúa abierta



ENTONCES el sistema debe aumentar su nivel de prioridad considerando:



\- criticidad del hallazgo;

\- posible consecuencia;

\- exposición vigente;

\- existencia de controles temporales;

\- reincidencia.



\---



\### Regla EMP-014 — Madurez preventiva



SI una empresa posee documentación



Y posee evidencia de implementación



Y verifica la eficacia de sus controles



Y aprende de eventos y hallazgos



ENTONCES el sistema podrá aumentar su nivel estimado de madurez preventiva.



La madurez deberá presentarse como evaluación fundamentada, no como verdad absoluta.



\---



\## 9. Fuentes normativas y técnicas



| Fuente | Tipo de autoridad | Aplicación |

|---|---|---|

| Código del Trabajo | Jurídica | Deberes derivados de la relación laboral y protección de los trabajadores |

| Ley 16.744 | Jurídica | Prevención y protección frente a accidentes del trabajo y enfermedades profesionales |

| Reglamentos asociados a la gestión preventiva | Jurídica reglamentaria | Organización, obligaciones y actividades preventivas |

| DS 594 | Jurídica reglamentaria | Condiciones sanitarias y ambientales básicas en los lugares de trabajo |

| Normativa sobre subcontratación | Jurídica | Responsabilidades y coordinación entre empresas |

| Normativa sectorial aplicable | Jurídica/técnica | Obligaciones específicas según actividad |

| ISO 45001 | Técnica | Sistema de gestión de Seguridad y Salud en el Trabajo |

| ISO 9001 | Técnica | Gestión de procesos, documentación, auditorías y mejora |

| Reglamento Interno | Organizacional | Reglas internas aplicables a la organización |

| Procedimientos internos | Organizacional | Controles operacionales definidos |

| Dictámenes y pronunciamientos oficiales | Interpretativa oficial | Interpretación de obligaciones en casos concretos |



> Las referencias específicas, su vigencia y aplicabilidad deberán ser verificadas por el Motor Normativo antes de utilizarlas como fundamento definitivo.



\---



\## 10. Evidencias relacionadas



La existencia y gestión de una empresa puede respaldarse mediante:



\- antecedentes legales de constitución;

\- identificación tributaria;

\- organigrama;

\- contratos de trabajo;

\- contratos con empresas contratistas;

\- registros de dotación;

\- centros de trabajo registrados;

\- descripción de procesos;

\- mapas de procesos;

\- descripciones de cargo;

\- matrices de identificación de peligros y evaluación de riesgos;

\- reglamentos internos;

\- procedimientos;

\- instructivos;

\- registros de capacitación;

\- entrega de EPP;

\- inspecciones;

\- auditorías;

\- registros de mantenimiento;

\- evaluaciones ambientales;

\- vigilancia de salud;

\- estadísticas de accidentabilidad;

\- DIAT;

\- DIEP;

\- investigaciones de eventos;

\- actas de comités;

\- planes de emergencia;

\- acciones correctivas;

\- fiscalizaciones;

\- resoluciones;

\- certificados de sistemas de gestión.



La calidad de la evidencia deberá evaluarse según:



\- autenticidad;

\- vigencia;

\- integridad;

\- trazabilidad;

\- correspondencia con la operación;

\- responsable;

\- fecha;

\- alcance;

\- verificabilidad.



\---



\## 11. Preguntas de competencia



La clase Empresa debe permitir responder:



1\. ¿Qué actividad desarrolla la empresa?

2\. ¿Cuántos centros de trabajo posee?

3\. ¿Qué procesos ejecuta?

4\. ¿Qué trabajadores y contratistas participan en sus operaciones?

5\. ¿Qué peligros existen en sus procesos?

6\. ¿Qué riesgos han sido evaluados?

7\. ¿Qué controles están definidos?

8\. ¿Qué controles cuentan con evidencia?

9\. ¿Qué obligaciones normativas podrían aplicar?

10\. ¿Qué normativa específica debe verificarse?

11\. ¿Existe coherencia entre los documentos y la operación real?

12\. ¿Qué documentos se encuentran vencidos o incompletos?

13\. ¿Qué acciones correctivas permanecen pendientes?

14\. ¿Qué hallazgos se repiten?

15\. ¿Qué centros de trabajo presentan mayores brechas?

16\. ¿Qué procesos concentran los riesgos más críticos?

17\. ¿Qué empresas contratistas participan?

18\. ¿Existe coordinación preventiva con contratistas?

19\. ¿Se encuentran claramente asignadas las responsabilidades?

20\. ¿Qué evidencia falta para demostrar cumplimiento?

21\. ¿Qué cambios operacionales requieren reevaluación?

22\. ¿Qué accidentes, incidentes o enfermedades se han registrado?

23\. ¿Existen señales de subregistro?

24\. ¿Cuál es el nivel estimado de madurez preventiva?

25\. ¿Qué información adicional necesita el sistema antes de concluir?

26\. ¿Qué recomendaciones son prioritarias?

27\. ¿Qué recomendaciones poseen fundamento legal, técnico u organizacional?

28\. ¿Cuál es el nivel de confianza de la evaluación?



\---



\## 12. Casos de uso



\- Diagnóstico general de gestión preventiva.

\- Evaluación inicial de una organización.

\- Preparación para auditorías.

\- Preparación para fiscalizaciones.

\- Control de cumplimiento legal.

\- Revisión documental.

\- Evaluación de centros de trabajo.

\- Gestión de empresas contratistas.

\- Coordinación de actividades preventivas.

\- Investigación de accidentes.

\- Investigación de enfermedades profesionales.

\- Seguimiento de acciones correctivas.

\- Identificación de documentos vencidos.

\- Evaluación de cambios operacionales.

\- Revisión del sistema de gestión.

\- Comparación entre centros de trabajo.

\- Priorización de riesgos y recursos.

\- Elaboración de planes preventivos.

\- Generación de indicadores.

\- Evaluación de madurez organizacional.

\- Construcción del perfil preventivo de la empresa.



\---



\## 13. Ejemplos de instancias



Ejemplos ficticios:



\### Empresa industrial



Metalúrgica Ejemplo S.A.



Características:



\- fabricación de estructuras metálicas;

\- procesos de soldadura y mecanizado;

\- 120 trabajadores;

\- dos centros de trabajo;

\- uso de grúas, tornos y sustancias químicas;

\- presencia de empresas contratistas.



\### Empresa de servicios



Servicios Técnicos Ejemplo Ltda.



Características:



\- mantenimiento de maquinaria;

\- trabajadores desplegados en instalaciones de clientes;

\- uso de vehículos y herramientas;

\- exposición variable según faena.



\### Empresa principal



Constructora Ejemplo S.A.



Características:



\- administra una obra;

\- contrata distintas especialidades;

\- coordina varias empresas;

\- posee riesgos compartidos en una misma faena.



\### Empresa contratista



Montajes Ejemplo SpA.



Características:



\- presta servicios en instalaciones de terceros;

\- ejecuta trabajos de montaje;

\- debe coordinar procedimientos y controles con la empresa principal.



\---



\## 14. Exclusiones



La clase Empresa no debe confundirse con:



\- Centro de Trabajo: lugar específico donde se desarrollan actividades.

\- Área: división funcional de la organización.

\- Proceso: conjunto de actividades que transforma entradas en resultados.

\- Faena: contexto operacional particular que puede involucrar varias empresas.

\- Contratista: rol que una empresa puede desempeñar en una relación contractual.

\- Empleador: función jurídica que puede asumir una empresa u otra entidad.

\- Persona Jurídica: concepto legal más amplio.

\- Cliente: rol comercial desempeñado frente a otra organización.

\- Organismo Administrador: entidad externa vinculada al sistema de protección laboral.

\- Grupo Empresarial: conjunto de empresas relacionadas que mantienen identidades distintas.

\- Instalación: elemento físico bajo administración de una organización.



Una misma empresa puede desempeñar simultáneamente diferentes roles según el contrato o la operación analizada.



\---



\## 15. Nivel de madurez



\### Nivel actual



Nivel 2 — Relaciones iniciales.



La clase posee:



\- definición conceptual;

\- propiedades iniciales;

\- relaciones principales;

\- restricciones;

\- reglas de negocio;

\- primeras reglas de inferencia;

\- preguntas de competencia;

\- ejemplos ficticios.



\### Pendientes para alcanzar el Nivel 3 — Normativa



\- validar las fuentes jurídicas vigentes;

\- identificar obligaciones según tamaño y actividad;

\- incorporar normativa sectorial;

\- relacionar dictámenes y pronunciamientos;

\- definir jerarquía entre fuentes;

\- crear catálogo de roles empresariales.



\### Pendientes para alcanzar el Nivel 4 — Casos



\- probar la clase con organizaciones ficticias;

\- relacionar casos reales anonimizados;

\- analizar casos de contratistas;

\- validar diferencias entre centros de trabajo;

\- probar eventos con documentación incompleta.



\### Pendientes para alcanzar el Nivel 5 — Razonamiento experto



\- construir reglas de cumplimiento contextual;

\- crear índice de madurez preventiva;

\- establecer niveles de confianza;

\- integrar Motor Normativo;

\- integrar Motor de Contexto;

\- integrar Motor de Evidencias;

\- validar inferencias con profesionales;

\- registrar explicación y trazabilidad de cada conclusión.



\---



\## 16. Observaciones



La empresa es una entidad central, pero PrevInspect AI no debe reducir la gestión preventiva a una evaluación general de la organización.



El análisis deberá poder descender desde:



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



La responsabilidad preventiva deberá analizarse según el contexto real y no solamente según la denominación contractual utilizada.



PrevInspect AI deberá distinguir claramente entre:



\- obligación aplicable;

\- cumplimiento declarado;

\- evidencia presentada;

\- implementación observada;

\- eficacia comprobada.



Una empresa podrá tener un alto nivel documental y, al mismo tiempo, presentar deficiencias operacionales.



Del mismo modo, una organización pequeña podría tener controles eficaces aunque posea una estructura documental menos compleja.



Por esta razón, las conclusiones deberán considerar proporcionalidad, actividad, exposición, tamaño, complejidad y evidencia disponible.



PrevInspect AI apoyará la evaluación profesional, pero no reemplazará la determinación jurídica de una autoridad, el criterio técnico del especialista ni la responsabilidad de la organización.

