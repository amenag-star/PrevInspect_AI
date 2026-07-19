\# Clase ontológica: Tarea



\## 1. Identificación



\### Nombre



Tarea



\### Código



CLS\_OPERACION\_TAREA



\### Dominio



Operación



\### Versión



0.1



\### Estado



Borrador



\---



\## 2. Definición conceptual



Unidad mínima de trabajo ejecutada por una persona o grupo de personas para cumplir un objetivo dentro de un proceso.



Una tarea representa la actividad real que ejecuta el trabajador.



Es durante la ejecución de la tarea donde aparecen las exposiciones, los peligros y los riesgos.



La tarea constituye el principal objeto de análisis preventivo dentro de PrevInspect AI.



\---



\## 3. Propósito dentro del Sistema Experto



Representar la actividad específica que ejecuta el trabajador.



Permite conectar:



\- trabajador

\- proceso

\- equipos

\- herramientas

\- sustancias

\- ambiente

\- peligros

\- riesgos

\- controles

\- evidencia



La mayoría de las inferencias preventivas partirán desde esta clase.



\---



\## 4. Propiedades



| Propiedad | Tipo | Obligatoria |

|------------|------|-------------|

| identificador | Texto | Sí |

| nombre | Texto | Sí |

| descripción | Texto | Sí |

| proceso | Referencia | Sí |

| frecuencia | Catálogo | Sí |

| duración | Número | No |

| trabajadores | Referencia | Sí |

| cargo | Referencia | No |

| equipos | Referencia | No |

| herramientas | Referencia | No |

| sustancias | Referencia | No |

| materiales | Referencia | No |

| ambiente | Referencia | No |

| peligros | Referencia | No |

| riesgos | Referencia | No |

| controles | Referencia | No |

| procedimiento | Referencia | No |

| permisos | Referencia | No |

| epp | Referencia | No |

| competencias | Referencia | No |

| criticidad | Catálogo | No |



\---



\## 5. Relaciones



PERTENECE\_A → Proceso



ES\_EJECUTADA\_POR → Trabajador



REQUIERE → Competencia



UTILIZA → Equipo



UTILIZA → Herramienta



UTILIZA → Sustancia



GENERA → Exposición



PRESENTA → Peligro



GENERA → Riesgo



REQUIERE → Medida de Control



UTILIZA → EPP



ESTÁ\_REGULADA\_POR → Procedimiento



REQUIERE → Permiso



PUEDE\_GENERAR → Evento



GENERA → Evidencia



\---



\## 6. Restricciones Ontológicas



Toda tarea debe pertenecer a un proceso.



Toda tarea debe poseer un objetivo.



Toda tarea debe ser ejecutada por al menos un trabajador.



Una tarea puede ejecutarse de distintas formas dependiendo del contexto.



Los peligros pueden variar según:



\- horario

\- clima

\- turno

\- experiencia

\- equipo utilizado

\- sustancia utilizada

\- cantidad de personas

\- fatiga

\- emergencia

\- mantenimiento



La tarea documentada puede diferir de la tarea realmente observada.



\---



\## 7. Reglas de Negocio



Toda tarea debe tener peligros identificados cuando exista exposición.



Los controles deben relacionarse con cada peligro.



El EPP nunca debe ser el único control cuando exista una medida de ingeniería viable.



Los permisos de trabajo deberán relacionarse únicamente con tareas que realmente los requieran.



Toda modificación importante de una tarea obliga a revisar:



\- IPER

\- procedimiento

\- capacitación

\- controles

\- permisos



\---



\## 8. Reglas de Inferencia



\### TAR-001



SI una tarea utiliza una sustancia peligrosa



ENTONCES existe una exposición potencial.



\---



\### TAR-002



SI una tarea utiliza un equipo



Y el equipo posee partes móviles



ENTONCES existe peligro mecánico potencial.



\---



\### TAR-003



SI una tarea requiere trabajo en altura



ENTONCES verificar:



\- sistema anticaídas

\- capacitación

\- permiso

\- inspección

\- rescate



\---



\### TAR-004



SI una tarea requiere energía eléctrica



ENTONCES verificar:



\- bloqueo

\- aislamiento

\- competencias

\- herramientas aisladas

\- autorización



\---



\### TAR-005



SI una tarea cambia respecto del procedimiento



ENTONCES generar alerta de desviación operacional.



\---



\### TAR-006



SI dos tareas incompatibles se ejecutan simultáneamente



ENTONCES evaluar interacción.



\---



\### TAR-007



SI una tarea presenta repetidamente incidentes



ENTONCES aumentar prioridad del análisis.



\---



\### TAR-008



SI una tarea no posee procedimiento



NO asumir incumplimiento.



Solicitar información adicional.



\---



\### TAR-009



SI una tarea posee peligros



Y no posee controles



ENTONCES generar alerta crítica.



\---



\### TAR-010



SI un trabajador ejecuta una tarea para la cual no posee competencias



ENTONCES generar alerta por brecha de capacitación.



\---



\## 9. Fuentes Normativas



\- Ley 16.744

\- Código del Trabajo

\- DS 594

\- DS 40

\- ISO 45001

\- Procedimientos internos

\- Permisos de trabajo

\- Manuales de fabricante

\- HDS

\- Instructivos



\---



\## 10. Evidencias



\- Observaciones de tarea

\- AST

\- ART

\- IPER

\- Procedimientos

\- Checklists

\- Fotografías

\- Videos

\- Permisos

\- Registros de capacitación

\- Entrevistas

\- Investigaciones

\- Auditorías



\---



\## 11. Preguntas de Competencia



El sistema debe responder:



¿Qué hace exactamente esta tarea?



¿Quién la ejecuta?



¿Cada cuánto?



¿Qué equipos utiliza?



¿Qué sustancias utiliza?



¿Qué herramientas utiliza?



¿Qué peligros aparecen?



¿Qué riesgos genera?



¿Qué controles existen?



¿Qué controles faltan?



¿Qué EPP requiere?



¿Qué permisos necesita?



¿Qué capacitación requiere?



¿Qué normativa aplica?



¿Qué accidentes se relacionan?



¿Qué evidencia existe?



¿Qué información falta?



\---



\## 12. Casos de Uso



\- AST

\- ART

\- IPER

\- Permisos de trabajo

\- Investigación de accidentes

\- Observaciones preventivas

\- Capacitación

\- Auditorías

\- Inspecciones

\- Gestión del Cambio



\---



\## 13. Ejemplos



Cambio de rodamiento.



Soldadura de estructura.



Conducción de grúa horquilla.



Cambio de neumático.



Carga de combustible.



Ingreso a espacio confinado.



Limpieza de reactor.



Pintura con pistola.



Trabajo administrativo.



Inspección de extintores.



\---



\## 14. Exclusiones



No confundir con:



Proceso



Procedimiento



Cargo



Puesto de trabajo



Proyecto



Actividad económica



\---



\## 15. Nivel de Madurez



Nivel actual:



2



Pendiente:



\- Casos reales

\- Reglas específicas

\- Patrones de accidentes

\- IA predictiva

\- Aprendizaje continuo



\---



\## 16. Observaciones



La clase Tarea constituye el núcleo operacional de PrevInspect AI.



Toda evaluación preventiva debería poder descender hasta este nivel.



Las recomendaciones del Sistema Experto deberán emitirse considerando siempre la tarea real ejecutada y no únicamente el procedimiento escrito.



Una misma tarea puede presentar riesgos completamente diferentes dependiendo del contexto operacional, la experiencia del trabajador, los equipos utilizados, el entorno y las condiciones existentes al momento de su ejecución.

