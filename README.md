# CodeInsight AI

## Fast Prompting en Acción

**CodeInsight AI** es una Prueba de Concepto (POC) desarrollada para la materia **Inteligencia Artificial: Generación de Prompts** de Coderhouse.

El proyecto utiliza técnicas de **Prompt Engineering y Fast Prompting** para asistir en la revisión final de proyectos web mediante Inteligencia Artificial Generativa.

Como caso de estudio se utiliza **Tienda Cool**, una aplicación web de comercio electrónico desarrollada con **PHP, HTML, CSS y JavaScript**.

---

## Estudiante

**Ivanna Micaela Arzamendia**

**Curso:** Inteligencia Artificial: Generación de Prompts
**Proyecto:** CodeInsight AI
**Entrega:** Preentrega N.º 2 – Fast Prompting en Acción

---

# 1. Introducción

La Inteligencia Artificial Generativa puede asistir a los desarrolladores en diferentes tareas relacionadas con la revisión de software, como el análisis de código, la identificación de errores, la detección de posibles riesgos de seguridad y la generación de documentación.

Sin embargo, la calidad de las respuestas obtenidas depende en gran medida de la forma en que se construyen las instrucciones enviadas al modelo.

CodeInsight AI busca demostrar cómo la utilización de técnicas de **Fast Prompting** permite obtener respuestas más estructuradas, específicas y reutilizables en comparación con prompts simples o poco detallados.

La implementación se realiza mediante una **Jupyter Notebook ejecutada en Google Colab**, utilizando Python y la API de Groq.

---

# 2. Presentación del problema

Durante la etapa final de un proyecto web pueden quedar aspectos sin revisar aunque la aplicación funcione correctamente.

Entre ellos se encuentran:

* Código poco optimizado.
* Problemas de organización y mantenibilidad.
* Posibles errores de programación.
* Vulnerabilidades o malas prácticas de seguridad.
* Falta de documentación.
* Dificultad para priorizar las mejoras necesarias.

Realizar una revisión completa de forma manual puede requerir tiempo y conocimientos en diferentes áreas.

La Inteligencia Artificial puede utilizarse como herramienta de apoyo para este proceso, pero un prompt demasiado general puede producir respuestas poco organizadas, extensas o difíciles de aplicar.

Por este motivo, CodeInsight AI propone analizar cómo diferentes configuraciones de prompts pueden mejorar la calidad de los resultados obtenidos.

---

# 3. Propuesta de solución

CodeInsight AI implementa una cadena de prompts especializados para analizar diferentes aspectos de un proyecto web.

La solución divide el problema en etapas más pequeñas y reutiliza los resultados obtenidos anteriormente mediante **Prompt Chaining**.

El flujo implementado en la POC es:

```text
Código fuente de Tienda Cool
          ↓
Comparación de prompts
          ↓
Análisis técnico optimizado
          ↓
Análisis de seguridad
          ↓
Reporte ejecutivo
          ↓
Backlog de mejoras
          ↓
Dashboard de resultados
```

El objetivo de CodeInsight AI no es reemplazar una auditoría técnica o de seguridad realizada por profesionales, sino funcionar como una herramienta de apoyo para identificar oportunidades de mejora y organizar la información obtenida.

---

# 4. Objetivos

## Objetivo general

Demostrar mediante una Prueba de Concepto cómo las técnicas de Fast Prompting pueden mejorar el análisis automatizado de código perteneciente a un proyecto web.

## Objetivos específicos

* Analizar un fragmento real de código mediante Inteligencia Artificial.
* Comparar un prompt básico con un prompt optimizado.
* Aplicar técnicas de Fast Prompting.
* Evaluar cómo la estructura del prompt modifica la calidad de la respuesta.
* Detectar oportunidades de mejora en el código.
* Identificar posibles riesgos de seguridad.
* Aplicar Prompt Chaining para reutilizar resultados.
* Generar un reporte ejecutivo.
* Construir un backlog priorizado de mejoras.
* Crear una representación visual de los resultados.
* Reducir consultas innecesarias a la API.

---

# 5. Caso de estudio

Para validar el funcionamiento de la POC se utiliza **Tienda Cool**, una aplicación web de comercio electrónico desarrollada previamente.

El proyecto utiliza tecnologías como:

* PHP
* HTML
* CSS
* JavaScript
* MySQL

Para esta POC se seleccionó un fragmento real del archivo `productos.php`.

En lugar de enviar todo el proyecto a la API, se trabaja con un fragmento representativo para reducir la cantidad de información procesada y facilitar el análisis.

---

# 6. Metodología

La implementación se desarrolla mediante las siguientes etapas:

1. Selección de un fragmento real del código fuente.
2. Ejecución de un prompt básico.
3. Análisis del resultado obtenido.
4. Diseño de un prompt optimizado.
5. Ejecución del prompt aplicando técnicas de Fast Prompting.
6. Comparación de ambos resultados.
7. Reutilización del análisis optimizado para una revisión de seguridad.
8. Generación de un reporte ejecutivo.
9. Creación de un backlog priorizado de mejoras.
10. Generación de gráficos mediante Python.
11. Análisis de resultados y conclusiones.

Este procedimiento permite experimentar con diferentes configuraciones de prompts y evaluar de forma práctica su influencia sobre las respuestas generadas.

---

# 7. Técnicas de Prompting utilizadas

## Prompt básico

Se utiliza inicialmente una instrucción breve y poco estructurada:

```text
Revisa el siguiente código y dime si se puede mejorar.
```

Su objetivo es generar una línea base para posteriormente comparar los resultados.

---

## Role Prompting

Se asigna un rol específico al modelo:

```text
Actúa como un desarrollador web senior especializado en PHP,
revisión de código y buenas prácticas de seguridad.
```

Esto permite orientar la respuesta hacia un perfil técnico determinado.

---

## Context Prompting

Se proporciona información sobre el proyecto analizado:

```text
El siguiente código pertenece a Tienda Cool,
una aplicación web de comercio electrónico desarrollada
con PHP, HTML, CSS y JavaScript.
```

El contexto permite que el modelo interprete mejor la tarea solicitada.

---

## Definición de restricciones

El prompt optimizado establece límites concretos, por ejemplo:

* Máximo de cinco hallazgos.
* No inventar problemas.
* Priorizar problemas de seguridad o funcionamiento.
* Evitar recomendaciones genéricas.
* Utilizar un lenguaje técnico pero comprensible.

---

## Formato de salida

También se define previamente cómo debe organizarse la respuesta:

* Hallazgo.
* Categoría.
* Prioridad.
* Explicación.
* Recomendación.

Esto permite obtener resultados más uniformes y fáciles de interpretar.

---

## Prompt Chaining

CodeInsight AI utiliza **Prompt Chaining**, donde el resultado generado por una etapa se convierte en la entrada de la siguiente.

Ejemplo:

```text
Análisis técnico
       ↓
Análisis de seguridad
       ↓
Reporte ejecutivo
       ↓
Backlog de mejoras
```

Esta estrategia permite dividir una tarea compleja en problemas más pequeños y reutilizar la información existente.

---

# 8. Análisis de seguridad

Una de las etapas de CodeInsight AI está orientada específicamente al análisis de seguridad.

Los hallazgos obtenidos previamente son evaluados utilizando buenas prácticas de desarrollo seguro y referencias de **OWASP Top 10:2025** cuando existe una correspondencia clara.

Entre los riesgos analizados se incluyen problemas relacionados con:

* SQL Injection.
* Validación de datos.
* Escape de contenido HTML.
* Manejo seguro de información proveniente del usuario.

Los resultados de la IA representan recomendaciones de apoyo y **no reemplazan una auditoría profesional de seguridad**.

---

# 9. Implementación

La POC fue desarrollada mediante:

* Python
* Jupyter Notebook
* Google Colab
* Groq API
* Pandas
* Matplotlib

El modelo utilizado durante las pruebas es:

```text
openai/gpt-oss-20b
```

La API Key se solicita durante la ejecución mediante `getpass`, evitando almacenarla directamente dentro del Notebook.

Ejemplo:

```python
from groq import Groq
from getpass import getpass

api_key = getpass("Ingresá tu GROQ_API_KEY: ")

client = Groq(api_key=api_key)
```

De esta forma la credencial privada no queda almacenada en el repositorio público.

---

# 10. Comparación de prompts

Durante la POC se compararon dos configuraciones.

| Criterio                         | Prompt básico | Prompt optimizado   |
| -------------------------------- | ------------- | ------------------- |
| Contexto del proyecto            | No            | Sí                  |
| Rol definido                     | No            | Sí                  |
| Criterios de análisis            | No definidos  | Definidos           |
| Priorización                     | Limitada      | Alta / Media / Baja |
| Formato estructurado             | Parcial       | Sí                  |
| Cantidad de hallazgos controlada | No            | Máximo 5            |
| Facilidad de interpretación      | Media         | Alta                |

Los resultados permiten observar que el prompt optimizado proporciona mayor control sobre el tipo de respuesta esperada.

---

# 11. Reporte ejecutivo

Luego del análisis técnico y de seguridad, CodeInsight AI reutiliza los resultados para generar un reporte ejecutivo.

El reporte incluye:

* Resumen general.
* Principales hallazgos.
* Riesgos de seguridad.
* Recomendaciones prioritarias.
* Conclusión.

El objetivo es transformar información técnica en contenido que pueda ser comprendido tanto por desarrolladores como por usuarios con perfiles menos técnicos.

---

# 12. Backlog de mejoras

A partir de los resultados anteriores se genera un backlog priorizado.

Cada tarea incluye:

* ID.
* Descripción.
* Origen del hallazgo.
* Prioridad.
* Impacto esperado.
* Acción recomendada.

Esto permite convertir los resultados generados por la IA en acciones concretas que pueden incorporarse a futuras versiones del proyecto.

---

# 13. Dashboard de resultados

Los principales hallazgos son representados visualmente mediante gráficos desarrollados con Python.

Para ello se utilizan:

```python
pandas
matplotlib
```

El dashboard permite visualizar los resultados según:

* Categoría.
* Nivel de prioridad.

La visualización se genera directamente dentro de la Jupyter Notebook y no requiere una API externa de generación de imágenes.

---

# 14. Optimización del uso de la API

Uno de los objetivos de la implementación fue evitar consultas innecesarias al modelo.

Durante la POC se realizan consultas para:

1. Probar la conexión con la API.
2. Ejecutar el prompt básico.
3. Ejecutar el prompt optimizado.
4. Realizar el análisis de seguridad.
5. Generar el reporte ejecutivo.
6. Generar el backlog.

Las etapas posteriores reutilizan los resultados ya obtenidos siempre que sea posible.

La comparación de resultados y los gráficos son generados directamente mediante Python y no requieren nuevas consultas a la API.

Este enfoque permite:

* Reducir información repetida.
* Reducir el consumo de tokens.
* Disminuir la cantidad de consultas.
* Optimizar el costo de ejecución.
* Mejorar la reutilización de resultados.

---

# 15. Estructura del repositorio

```text
ENTREGA2-CodeInsight-AI/
│
├── CodeInsight_AI_Entrega2.ipynb
├── README.md
└── requirements.txt
```

---

# 16. Instalación

Para instalar las dependencias necesarias:

```bash
pip install groq pandas matplotlib
```

También pueden instalarse utilizando:

```bash
pip install -r requirements.txt
```

Contenido de `requirements.txt`:

```text
groq
pandas
matplotlib
```

---

# 17. Ejecución

1. Abrir `CodeInsight_AI_Entrega2.ipynb` en Google Colab o Jupyter Notebook.
2. Ejecutar la celda de instalación de dependencias.
3. Ingresar una API Key válida de Groq cuando sea solicitada.
4. Ejecutar las celdas del Notebook en orden.
5. Analizar los resultados generados por cada etapa.

La API Key **no debe incluirse dentro del código ni subirse al repositorio**.

---

# 18. Resultados

La implementación permitió comprobar que un prompt básico puede encontrar problemas relevantes, pero ofrece menor control sobre la estructura y priorización de la respuesta.

Al aplicar técnicas de Fast Prompting se obtuvieron resultados más estructurados y específicos.

La utilización de roles, contexto, restricciones, formatos de salida y Prompt Chaining permitió organizar el proceso de análisis en distintas etapas y reutilizar los resultados generados anteriormente.

---

# 19. Conclusión

CodeInsight AI permitió transformar la propuesta conceptual inicial en una Prueba de Concepto funcional.

La experimentación realizada demuestra que la construcción del prompt influye directamente en la claridad, estructura y utilidad de las respuestas generadas por un modelo de Inteligencia Artificial.

Las técnicas de Fast Prompting permitieron mejorar la organización de los resultados, establecer prioridades y dividir un problema complejo en tareas más simples.

Además, el uso de Prompt Chaining permitió reutilizar información obtenida previamente, evitando procesar nuevamente el código completo en cada etapa.

Como resultado, la POC fue capaz de realizar un análisis técnico, identificar posibles riesgos de seguridad, generar un reporte ejecutivo, construir un backlog de mejoras y representar visualmente los principales hallazgos.

De esta manera, CodeInsight AI demuestra cómo una estrategia adecuada de Prompt Engineering puede utilizarse para construir soluciones de Inteligencia Artificial más organizadas, eficientes y reutilizables.

---

## Nota de seguridad

Este proyecto fue desarrollado con fines académicos.

Las respuestas generadas por Inteligencia Artificial deben considerarse recomendaciones de apoyo y no reemplazan una revisión profesional del código ni una auditoría de seguridad especializada.

**Nunca se deben publicar API Keys, credenciales, contraseñas o información sensible dentro del repositorio.**
