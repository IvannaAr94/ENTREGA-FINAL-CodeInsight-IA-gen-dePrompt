# CodeInsight AI - Prompt Texto → Texto

## Herramienta utilizada

Groq API

## Modelo utilizado

`openai/gpt-oss-20b`

## Objetivo

Analizar fragmentos de código pertenecientes a una aplicación web e identificar posibles problemas técnicos relacionados con calidad de código, mantenibilidad, manejo de errores, experiencia de usuario y buenas prácticas de desarrollo.

---

## Prompt básico

```text
Analiza el siguiente código y dime qué problemas tiene:

{codigo_prueba}

ROL:
Actúa como un desarrollador web senior especializado en React,
revisión de código y buenas prácticas de desarrollo frontend.

CONTEXTO:
El siguiente código pertenece a una aplicación web de comercio electrónico.
El componente muestra una lista de productos y permite eliminar un producto
mediante una petición HTTP DELETE.

TAREA:
Analiza exclusivamente el código proporcionado e identifica los principales
problemas técnicos relacionados con:

- calidad del código
- mantenibilidad
- manejo de errores
- experiencia de usuario
- buenas prácticas de React

RESTRICCIONES:
- Devuelve como máximo 5 hallazgos.
- No inventes vulnerabilidades ni problemas que no puedan justificarse
  directamente a partir del código.
- No asumas características del backend que no aparecen en el fragmento.
- Evita recomendaciones genéricas.
- Prioriza los problemas más relevantes.
- Clasifica cada problema como prioridad Alta, Media o Baja.

FORMATO DE SALIDA:

Hallazgo:
Categoría:
Prioridad:
Problema:
Recomendación:

EJEMPLO DEL FORMATO ESPERADO:

Hallazgo: Uso de un identificador inestable
Categoría: React
Prioridad: Media
Problema: El componente utiliza un valor que puede cambiar entre renders.
Recomendación: Utilizar un identificador único y estable asociado al elemento.

CÓDIGO A ANALIZAR:

{codigo_prueba}