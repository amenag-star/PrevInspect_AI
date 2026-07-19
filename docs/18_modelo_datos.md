\# Modelo de Datos Maestro

\## PrevInspect AI

\### Sistema Experto Inteligente para la Gestión Integral de Seguridad y Salud Ocupacional



\---



\# Objetivo



Este documento define todas las entidades que conforman la Base de Conocimiento de PrevInspect AI.



Cada entidad representa un objeto real del mundo de la prevención de riesgos.



Todas ellas estarán relacionadas entre sí formando un grafo de conocimiento capaz de razonar sobre riesgos, controles, cumplimiento legal, accidentes, auditorías y aprendizaje operacional.



\---



\# Filosofía



PrevInspect AI no almacenará solamente documentos.



Almacenará conocimiento.



Cada documento alimentará una o más entidades del sistema.



Cada entidad podrá relacionarse con cientos de otras entidades.



Eso permitirá responder preguntas complejas utilizando múltiples fuentes de información al mismo tiempo.



\---



\# Entidades Principales



\## 1. Empresa



Representa una organización evaluada.



Información:



\- Nombre

\- Rut

\- Rubro

\- Cantidad de trabajadores

\- Centros de trabajo

\- Sistema de gestión

\- Mutualidad

\- Certificaciones ISO

\- Nivel de cumplimiento

\- Historial de auditorías



Relacionada con:



• Trabajadores



• Procesos



• Riesgos



• Auditorías



• Accidentes



• Documentación



\---



\## 2. Trabajador



Información:



\- Nombre

\- Cargo

\- Área

\- Antigüedad

\- Competencias

\- Capacitaciones

\- Aptitud médica

\- Restricciones

\- Exámenes preocupacionales

\- Exámenes ocupacionales



Relacionado con:



• Accidentes



• Enfermedades profesionales



• Capacitaciones



• Riesgos



• EPP



\---



\## 3. Cargo



Información



\- Funciones

\- Descripción

\- Riesgos asociados

\- Controles requeridos

\- Competencias mínimas

\- Exámenes exigidos

\- EPP obligatorio



\---



\## 4. Área



Ejemplos



Producción



Bodega



Mantenimiento



Laboratorio



Oficinas



Faena



Cada área posee:



\- Riesgos

\- Equipos

\- Procedimientos

\- Inspecciones

\- Accidentes

\- Indicadores



\---



\## 5. Riesgo



Información



\- Código

\- Nombre

\- Tipo

\- Probabilidad

\- Consecuencia

\- Nivel

\- Fuente legal

\- Controles asociados



Puede relacionarse con:



\- Procesos

\- Máquinas

\- Personas

\- Sustancias

\- Áreas



\---



\## 6. Control



Información



\- Tipo



(Eliminación



Sustitución



Ingeniería



Administrativo



EPP)



Estado



Efectividad



Periodicidad



Responsable



Normativa asociada



\---



\## 7. Inspección



Puede ser:



Planeada



No planeada



Investigación



Fiscalización



Autoinspección



Auditoría



Registra



\- Hallazgos

\- Evidencias

\- Riesgos detectados

\- Incumplimientos

\- Acciones



\---



\## 8. Auditoría



Tipos



ISO 45001



ISO 9001



DS 44



DS 594



Ley 16.744



Mutualidades



Clientes



Interna



Externa



Resultado



Conformidades



No conformidades



Observaciones



Planes de acción



\---



\## 9. Documento



Ejemplos



Ley



Decreto



Resolución



Dictamen



PTS



RIOHS



AST



Matriz IPER



DIAT



DIEP



Ficha Técnica



HDS



Manual



Procedimiento



Cada documento tendrá



Versión



Fecha



Vigencia



Jerarquía



Estado



\---



\## 10. Accidente



Información



Fecha



Lugar



Actividad



Lesión



Parte afectada



Agente



Causa inmediata



Causa básica



Actos inseguros



Condiciones inseguras



Controles existentes



Controles vulnerados



Investigación



Medidas correctivas



Lecciones aprendidas



\---



\## 11. Enfermedad Profesional



Información



Agente



Exposición



Tiempo de exposición



Diagnóstico



Exámenes



Descripción del cargo



Sustancias



Controles



Vigilancia



DIEP



Dictamen SUSESO



\---



\## 12. Acción Correctiva



Información



Responsable



Fecha compromiso



Estado



Evidencia



Verificación



Resultado



\---



\## 13. Evidencia



Tipos



Fotografía



Documento



Firma



Video



Registro



Medición



Informe



Certificado



\---



\## 14. Aprendizaje Operacional



Esta entidad representa el conocimiento adquirido por PrevInspect AI.



Se alimentará desde



Accidentes



Enfermedades



Auditorías



Fiscalizaciones



Investigaciones



Nuevas leyes



Actualizaciones normativas



Buenas prácticas



Experiencia del prevencionista



Su función será mejorar continuamente las recomendaciones futuras.



\---



\# Relaciones principales



Empresa

│

├── Trabajadores

├── Áreas

├── Procesos

├── Documentos

├── Auditorías

├── Riesgos

├── Accidentes

└── Enfermedades



Trabajador

│

├── Cargo

├── Riesgos

├── Controles

├── Capacitaciones

├── Accidentes

└── Exámenes



Riesgo

│

├── Norma

├── Controles

├── Inspecciones

├── Accidentes

└── Auditorías



Accidente

│

├── Investigación

├── Evidencias

├── Medidas

└── Aprendizaje



\---



\# Visión Final



Toda la información almacenada será utilizada por PrevInspect AI para razonar de manera similar a un Prevencionista Senior.



El sistema podrá integrar información legal, operacional, médica, documental y estadística para apoyar la toma de decisiones preventivas.

