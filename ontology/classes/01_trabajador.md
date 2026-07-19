\# Clase ontológica: Trabajador



\## 1. Identificación



\### Nombre



Trabajador



\### Código



CLS\_PERSONA\_TRABAJADOR



\### Dominio



Personas



\### Versión



0.1



\### Estado



Borrador



\---



\## 2. Definición conceptual



Persona que presta servicios personales bajo una relación laboral o que ejecuta actividades dentro de una organización, y que puede encontrarse expuesta a peligros derivados de sus tareas, procesos, equipos, sustancias y condiciones del entorno de trabajo.



La clase representa al sujeto principal sobre el cual se desarrollan las acciones de protección, prevención, capacitación, vigilancia y control de los riesgos laborales.



\---



\## 3. Propósito dentro de PrevInspect AI



Representar a la persona protegida por el sistema de Seguridad y Salud Ocupacional.



La clase permite relacionar al trabajador con:



\- su organización;

\- su cargo;

\- las tareas que ejecuta;

\- los procesos en los que participa;

\- los peligros existentes;

\- los riesgos evaluados;

\- los controles requeridos;

\- las competencias necesarias;

\- las capacitaciones recibidas;

\- la vigilancia de salud;

\- los incidentes o accidentes relacionados.



\---



\## 4. Propiedades



| Propiedad | Descripción | Tipo | Obligatoria | Cardinalidad |

|---|---|---|---|---|

| identificador | Identificador único | Texto | Sí | 1 |

| nombre | Nombre de la persona | Texto | Condicional | 0:1 |

| cargo | Cargo formal asignado | Referencia | Sí | 1 |

| empresa | Organización a la que pertenece | Referencia | Sí | 1 |

| centro\_trabajo | Centro donde realiza funciones | Referencia | Sí | 1:N |

| area | Área organizacional | Referencia | Sí | 1:N |

| proceso | Proceso en el que participa | Referencia | Sí | 1:N |

| tareas | Actividades que ejecuta | Referencia | Sí | 1:N |

| antiguedad | Tiempo en la organización o cargo | Número/fecha | No | 0:N |

| competencias | Competencias acreditadas | Referencia | No | 0:N |

| capacitaciones | Actividades formativas realizadas | Referencia | No | 0:N |

| exposiciones | Exposiciones laborales identificadas | Referencia | No | 0:N |

| epp\_asignados | EPP entregados o requeridos | Referencia | No | 0:N |

| vigilancia\_salud | Programas de vigilancia aplicables | Referencia | No | 0:N |

| restricciones | Restricciones laborales vigentes | Referencia | No | 0:N |

| estado\_laboral | Estado de la relación laboral | Catálogo | Sí | 1 |



\---



\## 5. Relaciones



| Relación | Clase destino | Cardinalidad | Descripción |

|---|---|---|---|

| PERTENECE\_A | Empresa | 1:1 | Identifica la organización responsable |

| TRABAJA\_EN | Centro de Trabajo | 1:N | Indica dónde desarrolla sus actividades |

| DESEMPEÑA | Cargo | 1:N | Identifica su función formal |

| EJECUTA | Tarea | 1:N | Representa las actividades realizadas |

| PARTICIPA\_EN | Proceso | 1:N | Relaciona al trabajador con procesos operacionales |

| ESTA\_EXPUESTO\_A | Peligro | 0:N | Identifica fuentes potenciales de daño |

| POSEE | Riesgo | 0:N | Relaciona al trabajador con riesgos evaluados |

| REQUIERE | Medida de Control | 0:N | Indica controles necesarios |

| UTILIZA | EPP | 0:N | Registra protección personal asociada |

| RECIBE | Capacitación | 0:N | Registra formación preventiva |

| REQUIERE | Vigilancia de Salud | 0:N | Identifica vigilancia aplicable |

| REPORTA | Incidente | 0:N | Registra eventos informados |

| PARTICIPA\_EN | Investigación | 0:N | Registra participación en investigaciones |

| ESTA\_ASOCIADO\_A | DIAT | 0:N | Relaciona accidentes denunciados |

| ESTA\_ASOCIADO\_A | DIEP | 0:N | Relaciona enfermedades denunciadas |



\---



\## 6. Restricciones ontológicas



1\. Todo trabajador debe pertenecer a una empresa o entidad responsable.

2\. Todo trabajador debe tener al menos un cargo o función identificada.

3\. Todo trabajador debe estar relacionado con al menos una tarea o proceso.

4\. Un trabajador no debe asociarse directamente a un riesgo sin identificar el peligro, la tarea o la condición que origina la exposición.

5\. Los datos de salud deberán manejarse con acceso restringido.

6\. Una restricción médica no equivale automáticamente a una incapacidad laboral.

7\. La ausencia de registros no demuestra la ausencia de exposición.



\---



\## 7. Reglas de negocio



1\. El cargo formal debe coincidir razonablemente con las tareas reales.

2\. Las capacitaciones requeridas deben guardar relación con los peligros de las tareas ejecutadas.

3\. El EPP asignado debe corresponder al riesgo residual identificado.

4\. La vigilancia de salud debe relacionarse con exposiciones verificadas o razonablemente posibles.

5\. Los trabajadores nuevos, reasignados o expuestos a cambios operacionales deben ser reevaluados.

6\. El trabajador debe recibir información comprensible sobre los riesgos y controles relacionados con su trabajo.



\---



\## 8. Reglas de inferencia



\### Regla TRAB-001



SI un trabajador ejecuta una tarea



Y la tarea está asociada a un peligro



ENTONCES el trabajador puede estar expuesto a ese peligro.



\### Regla TRAB-002



SI un trabajador está expuesto a un peligro



Y existe un riesgo evaluado para dicha exposición



ENTONCES el trabajador hereda ese riesgo dentro de su contexto laboral.



\### Regla TRAB-003



SI un riesgo requiere una medida de control



ENTONCES el trabajador debe estar relacionado con dicha medida cuando corresponda.



\### Regla TRAB-004



SI una exposición se encuentra asociada a vigilancia de salud



ENTONCES el sistema debe verificar si el trabajador está incorporado al programa correspondiente.



\### Regla TRAB-005



SI las tareas reales no coinciden con la descripción del cargo



ENTONCES el sistema debe generar una alerta por posible brecha documental y preventiva.



\### Regla TRAB-006



SI falta información sobre tareas, exposición o controles



ENTONCES el sistema no debe concluir ausencia de riesgo.



Debe solicitar información adicional.



\---



\## 9. Fuentes normativas y técnicas



| Fuente | Tipo de autoridad | Aplicación |

|---|---|---|

| Código del Trabajo | Jurídica | Relación laboral y deberes generales |

| Ley 16.744 | Jurídica | Protección frente a accidentes y enfermedades profesionales |

| DS 594 | Jurídica reglamentaria | Condiciones sanitarias y ambientales |

| DS 40 o normativa que corresponda según vigencia | Jurídica reglamentaria | Gestión preventiva e información de riesgos |

| ISO 45001 | Técnica | Participación, competencia, exposición y control operacional |

| Reglamento Interno | Organizacional | Obligaciones y reglas internas aplicables |



> La vigencia y aplicación exacta de cada fuente deberá validarse en el Motor Normativo antes de utilizarla en una respuesta definitiva.



\---



\## 10. Evidencias relacionadas



\- Contrato de trabajo.

\- Anexo de contrato.

\- Descripción de cargo.

\- Registro de inducción.

\- Matriz IPER.

\- Registro de capacitación.

\- Registro de entrega de EPP.

\- Exámenes ocupacionales.

\- Registros de vigilancia.

\- Permisos de trabajo.

\- Procedimientos e instructivos.

\- Investigaciones de accidentes.

\- DIAT.

\- DIEP.



\---



\## 11. Preguntas de competencia



La clase debe permitir responder:



1\. ¿A qué empresa pertenece el trabajador?

2\. ¿Qué cargo desempeña?

3\. ¿Qué tareas realiza realmente?

4\. ¿En qué procesos participa?

5\. ¿A qué peligros se encuentra expuesto?

6\. ¿Qué riesgos tiene asociados?

7\. ¿Qué controles le corresponden?

8\. ¿Qué EPP requiere?

9\. ¿Qué capacitaciones debe tener?

10\. ¿Qué capacitaciones están vencidas o ausentes?

11\. ¿Qué vigilancia de salud le corresponde?

12\. ¿Existe coherencia entre su cargo y sus tareas?

13\. ¿Existe evidencia suficiente de cumplimiento?

14\. ¿Qué información falta para emitir una conclusión?

15\. ¿Qué normativa se relaciona con su situación?



\---



\## 12. Casos de uso



\- Evaluación del perfil preventivo de un trabajador.

\- Identificación de brechas de capacitación.

\- Verificación de entrega de EPP.

\- Incorporación a vigilancia ocupacional.

\- Investigación de accidentes.

\- Investigación de enfermedades profesionales.

\- Auditorías internas.

\- Inspecciones en terreno.

\- Evaluación de cambios de puesto.

\- Revisión de empresas contratistas.



\---



\## 13. Ejemplos de instancias



\- Operador de grúa horquilla.

\- Soldador.

\- Mecánico industrial.

\- Bodeguero.

\- Pintor industrial.

\- Operador de maquinaria.

\- Supervisor de terreno.

\- Personal administrativo.

\- Trabajador contratista.



\---



\## 14. Exclusiones



La clase Trabajador no debe confundirse con:



\- Cargo: función formal dentro de la organización.

\- Persona: concepto general que puede existir fuera de una relación laboral.

\- Contratista: organización o modalidad contractual.

\- Supervisor: rol particular que puede desempeñar un trabajador.

\- Usuario externo: persona que no necesariamente mantiene una relación laboral.

\- Paciente: concepto clínico que no corresponde directamente al modelo laboral.



\---



\## 15. Nivel de madurez



Nivel actual: 2 — Relaciones iniciales.



Pendientes para alcanzar niveles superiores:



\- validar normativa;

\- relacionar casos reales;

\- definir catálogos técnicos;

\- probar reglas de inferencia;

\- incorporar evidencia histórica;

\- revisar con criterio profesional;

\- convertir la clase a formato estructurado.



\---



\## 16. Observaciones



Esta clase es central dentro de PrevInspect AI.



La protección de la vida y salud del trabajador tiene prioridad sobre los objetivos productivos.



Las recomendaciones del sistema deberán considerar la privacidad de los datos personales y de salud.



PrevInspect AI no deberá emitir diagnósticos médicos ni reemplazar la evaluación de profesionales competentes.

