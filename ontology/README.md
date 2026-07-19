\# Ontología de PrevInspect AI



\## Propósito



Esta carpeta contiene el modelo formal de conocimiento utilizado por PrevInspect AI para representar la Seguridad y Salud Ocupacional.



La ontología define:



\- las clases que existen;

\- las propiedades de cada clase;

\- las relaciones entre clases;

\- las restricciones del modelo;

\- las reglas utilizadas por el Sistema Experto;

\- los ejemplos empleados para validar el razonamiento.



\---



\## Estructura



\### classes



Contiene las clases ontológicas del sistema.



Ejemplos:



\- Empresa

\- Trabajador

\- Proceso

\- Peligro

\- Riesgo

\- Medida de Control

\- Equipo

\- Sustancia

\- Documento

\- Evento



\### relations



Contiene las relaciones oficiales entre clases.



Ejemplos:



\- PERTENECE\_A

\- TRABAJA\_EN

\- EJECUTA

\- ESTA\_EXPUESTO\_A

\- REQUIERE

\- CONTROLA

\- GENERA

\- EVIDENCIA

\- INTERPRETA



\### rules



Contiene reglas conceptuales y reglas de negocio.



\### schemas



Contiene esquemas técnicos para validar que todas las clases tengan una estructura común.



\### examples



Contiene instancias ficticias y casos de prueba.



\---



\## Principios



1\. La ontología representa conceptos generales, no personas o empresas reales.

2\. Toda relación debe tener un significado explícito.

3\. Toda regla debe poder explicarse.

4\. Toda recomendación debe ser trazable.

5\. La normativa prevalece sobre la experiencia.

6\. La experiencia complementa el conocimiento formal.

7\. La incertidumbre debe declararse.

8\. El juicio profesional permanece en manos del prevencionista.



\---



\## Estado inicial



Versión: 0.1



Estado: En construcción



Primera fase:



1\. Definir plantilla oficial.

2\. Construir diez clases fundamentales.

3\. Crear catálogo de relaciones.

4\. Definir restricciones.

5\. Incorporar reglas de razonamiento.

6\. Validar mediante casos de prueba.

