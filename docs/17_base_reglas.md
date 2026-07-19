\# Base de Reglas - PrevInspect AI



\## Propósito



Este documento define las reglas lógicas que utilizará PrevInspect AI para razonar, detectar brechas, activar motores especializados, generar alertas y proponer acciones preventivas.



La Base de Reglas será el puente entre el conocimiento técnico-documental y las decisiones que el sistema recomendará al usuario.



\## Principio central



PrevInspect AI no debe responder solo por similitud de texto. Debe razonar mediante reglas explícitas, trazables y revisables por un profesional de prevención de riesgos.



\## Estructura estándar de una regla



Cada regla deberá contener:



\- Código

\- Nombre

\- Tipo de regla

\- Objetivo

\- Condición

\- Acción

\- Prioridad

\- Motor asociado

\- Fuente normativa o técnica

\- Evidencia requerida

\- Puede aprender

\- Estado

\- Observaciones



\## Tipos de reglas



\- Regla legal

\- Regla técnica

\- Regla documental

\- Regla operacional

\- Regla de auditoría

\- Regla de investigación

\- Regla de seguimiento

\- Regla predictiva

\- Regla de aprendizaje



\## Regla R-0001 - Descripción de cargo obligatoria



\### Tipo



Documental / Auditoría



\### Objetivo



Verificar que cada trabajador cuente con una descripción de cargo vigente.



\### Condición



SI existe un trabajador registrado  

Y no existe descripción de cargo asociada



\### Acción



Generar alerta de incumplimiento documental.



Solicitar creación o actualización de la descripción de cargo.



\### Prioridad



Alta



\### Motor asociado



Motor de Auditoría y Cumplimiento



\### Evidencia requerida



Descripción de cargo vigente.



\---



\## Regla R-0002 - Descripción de cargo sin riesgos asociados



\### Tipo



Documental / Riesgos



\### Objetivo



Verificar que la descripción de cargo indique los riesgos y exposiciones relevantes del puesto.



\### Condición



SI existe descripción de cargo  

Y no contiene riesgos, peligros o exposiciones asociadas



\### Acción



Solicitar revisión de la descripción de cargo.



Cruzar información con matriz IPER.



\### Prioridad



Alta



\### Motor asociado



Motor de Riesgos



\---



\## Regla R-0003 - Sustancia química sin HDS



\### Tipo



Legal / Técnica



\### Objetivo



Verificar que toda sustancia química cuente con Hoja de Datos de Seguridad.



\### Condición



SI existe sustancia química registrada  

Y no existe HDS asociada



\### Acción



Generar incumplimiento crítico.



Solicitar HDS vigente.



\### Prioridad



Crítica



\### Motor asociado



Motor Normativo / Motor Auditoría



\---



\## Regla R-0004 - Exposición química sin evaluación de vigilancia



\### Tipo



Salud ocupacional / Preventiva



\### Objetivo



Detectar exposiciones químicas que puedan requerir evaluación de salud ocupacional.



\### Condición



SI un cargo está expuesto a sustancias químicas  

Y no existe evaluación de exposición o vigilancia asociada



\### Acción



Generar alerta preventiva.



Recomendar revisión con organismo administrador o profesional competente.



\### Prioridad



Alta



\### Motor asociado



Motor de Riesgos / Motor de Accidentes y Enfermedades



\---



\## Regla R-0005 - Control implementado sin seguimiento



\### Tipo



Seguimiento / Mejora continua



\### Objetivo



Verificar que toda medida preventiva implementada tenga seguimiento posterior.



\### Condición



SI existe una medida de control implementada  

Y no existe seguimiento registrado



\### Acción



Generar alerta de seguimiento pendiente.



\### Prioridad



Media



\### Motor asociado



Motor de Aprendizaje Operacional

