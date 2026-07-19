\# Motor de Contexto

\## PrevInspect AI



\## Propósito



El Motor de Contexto tiene como objetivo comprender las condiciones reales en las que ocurre una consulta, actividad, inspección, accidente, auditoría o decisión preventiva.



Antes de emitir una conclusión, PrevInspect AI deberá verificar que dispone de información suficiente sobre la empresa, el lugar, la actividad, las personas expuestas, los equipos, los materiales y los controles existentes.



El contexto podrá modificar la prioridad, pertinencia y nivel de confianza de una recomendación.



\---



\## Principio de funcionamiento



Una misma situación puede requerir medidas diferentes dependiendo de las condiciones en que ocurre.



Por esta razón, el sistema no deberá aplicar una regla de manera automática sin revisar previamente su contexto operacional.



El flujo general será:



Consulta del usuario



↓



Identificación del tema



↓



Recopilación del contexto disponible



↓



Detección de información faltante



↓



Preguntas de aclaración



↓



Aplicación de reglas



↓



Evaluación de alternativas



↓



Recomendación fundamentada



\---



\## Dimensiones del contexto



\### 1. Contexto de la empresa



\- Rubro

\- Tamaño

\- Cantidad de trabajadores

\- Centros de trabajo

\- Mutualidad

\- Sistema de gestión

\- Empresas contratistas

\- Historial de accidentes

\- Historial de enfermedades profesionales

\- Nivel de cumplimiento normativo



\### 2. Contexto del lugar de trabajo



\- Área

\- Instalación

\- Faena

\- Condiciones ambientales

\- Espacios disponibles

\- Vías de acceso

\- Señalización

\- Orden y limpieza

\- Presencia de terceros

\- Condiciones de emergencia



\### 3. Contexto de la actividad



\- Actividad realizada

\- Tarea específica

\- Frecuencia

\- Duración

\- Actividad rutinaria o no rutinaria

\- Trabajo individual o grupal

\- Procedimiento aplicable

\- Permiso de trabajo

\- Supervisión disponible



\### 4. Contexto del trabajador



\- Cargo

\- Funciones

\- Experiencia

\- Competencias

\- Capacitación

\- Aptitud para la tarea

\- Restricciones laborales

\- Exposiciones

\- EPP asignado

\- Antigüedad



Los datos médicos sensibles deberán ser tratados con acceso restringido y solo cuando sean necesarios para la gestión preventiva.



\### 5. Contexto de equipos y herramientas



\- Equipo

\- Máquina

\- Herramienta

\- Estado operacional

\- Mantención

\- Manual del fabricante

\- Protecciones

\- Dispositivos de seguridad

\- Modificaciones

\- Inspección previa



\### 6. Contexto de sustancias y materiales



\- Nombre de la sustancia

\- Tipo

\- Cantidad

\- Forma de uso

\- HDS disponible

\- Vía de exposición

\- Tiempo de exposición

\- Almacenamiento

\- Compatibilidad

\- Controles existentes



\### 7. Contexto documental



\- Procedimiento vigente

\- Descripción de cargo

\- Matriz de riesgos

\- Reglamento interno

\- HDS

\- Registro de capacitación

\- Inspecciones

\- Auditorías

\- Investigación de accidentes

\- Acciones correctivas



\### 8. Contexto normativo



\- Normativa legal aplicable

\- Normas técnicas

\- Requisitos contractuales

\- Reglamento interno

\- Procedimientos internos

\- Jerarquía de las fuentes

\- Vigencia de los documentos

\- Posibles contradicciones



\---



\## Información crítica faltante



El motor deberá distinguir entre:



\### Información indispensable



Sin ella no se puede emitir una recomendación responsable.



Ejemplos:



\- Actividad desconocida

\- Sustancia no identificada

\- Altura de trabajo desconocida

\- Equipo sin identificar

\- No se conoce si existe exposición

\- No se sabe si el control está instalado



\### Información importante



Permite mejorar la precisión de la recomendación.



Ejemplos:



\- Antigüedad del trabajador

\- Historial de incidentes

\- Frecuencia de la tarea

\- Última mantención

\- Última capacitación



\### Información complementaria



Aporta contexto, pero no impide un análisis preliminar.



\---



\## Preguntas inteligentes



El sistema deberá formular únicamente preguntas relevantes.



Ejemplo: trabajo con sustancia química



\- ¿Qué sustancia se utiliza?

\- ¿Existe HDS vigente?

\- ¿Cómo se manipula?

\- ¿Existe contacto con la piel?

\- ¿Qué tiempo de exposición tiene el trabajador?

\- ¿La descripción de cargo reconoce esta exposición?

\- ¿Existe evaluación ambiental?

\- ¿Existe vigilancia de la salud aplicable?

\- ¿Qué EPP se utiliza?

\- ¿Se ha registrado algún caso similar?



Ejemplo: máquina con protección retirada



\- ¿La máquina puede funcionar sin la protección?

\- ¿Quién retiró la protección?

\- ¿Por qué fue retirada?

\- ¿Existe enclavamiento?

\- ¿La protección estaba dañada?

\- ¿Existía supervisión?

\- ¿El trabajador conocía el procedimiento?

\- ¿Se había detectado antes la misma desviación?



\---



\## Evaluación de alternativas



Cuando existan varias soluciones, el motor deberá considerar:



\- Riesgo generado por cada alternativa

\- Viabilidad operacional

\- Jerarquía de controles

\- Cumplimiento legal

\- Condiciones reales del lugar

\- Exposición de los trabajadores

\- Recursos disponibles

\- Consecuencias de aplicar o no aplicar la medida

\- Existencia de una alternativa más segura



\---



\## Caso de prueba: uso de hervidor



El sistema no deberá responder automáticamente que el hervidor está permitido o prohibido.



Deberá evaluar:



\- ¿Existe una prohibición legal general?

\- ¿El reglamento interno regula su utilización?

\- ¿La instalación eléctrica es adecuada?

\- ¿Existe riesgo de quemadura o incendio?

\- ¿Dónde se encuentra instalado?

\- ¿Existe una alternativa segura para acceder a agua caliente?

\- ¿El traslado hacia otra instalación genera un riesgo mayor?

\- ¿La restricción es razonable y proporcional?

\- ¿La medida interna contradice alguna norma superior?



La respuesta deberá diferenciar entre:



\- Prohibición legal

\- Regulación interna

\- Medida preventiva

\- Recomendación técnica

\- Alternativa operacional



\---



\## Salida del Motor de Contexto



El motor deberá entregar:



\- Contexto disponible

\- Información faltante

\- Preguntas necesarias

\- Riesgos preliminares

\- Normativa posiblemente aplicable

\- Reglas que pueden activarse

\- Alternativas iniciales

\- Nivel de confianza preliminar

\- Indicación de si es posible continuar con el análisis



\---



\## Regla de seguridad



Si falta información esencial o existe riesgo grave e inminente, el sistema deberá evitar conclusiones definitivas.



Podrá recomendar detener temporalmente la actividad, aislar el peligro o solicitar evaluación de un profesional competente, según corresponda.



\---



\## Resultado esperado



El Motor de Contexto permitirá que PrevInspect AI no aplique reglas de forma rígida o descontextualizada.



Su función será asegurar que las recomendaciones sean pertinentes, proporcionales, explicables y adaptadas a las condiciones reales de trabajo.

