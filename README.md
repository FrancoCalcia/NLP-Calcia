# Trabajo Práctico 2 (TP2): Chatbot Experto en **Viticulture**

Este repositorio contiene el Trabajo Práctico 2 (TP2) de la materia, en el cual se desarrolla un chatbot experto en el juego de mesa **Viticulture** utilizando la técnica **RAG (Retrieval Augmented Generation)** y el concepto de agentes **ReAct**. El trabajo está implementado en un entorno **Google Colab**, lo que permite ejecutarlo directamente en la nube.

---

## 📋 Contenido del Repositorio

- **TP2/**
  - `Informe_TP2.pdf`: Informe detallado con introducción, desarrollo, conclusiones y justificaciones del trabajo.
  - `TP2_Viticulture.ipynb`: Cuaderno Jupyter con el código implementado.
  - `archivos`: Archivos generados en la ejecución del programa y PDF de Guía Rápida.

---

## 📖 Descripción del Trabajo

### Ejercicio 1: Chatbot Experto con RAG
Se desarrolla un chatbot que responde preguntas sobre el juego de mesa **Viticulture** a partir de tres fuentes de datos principales:
1. **Documentos de texto**: Información extraída de manuales, guías y otros documentos relevantes.
2. **Datos numéricos en formato tabular**: Información organizada en tablas para acceder de manera dinámica.
3. **Base de datos de grafos**: Estructuración de conocimiento en forma de tríadas.

El chatbot clasifica las consultas de los usuarios y utiliza las fuentes más relevantes para generar respuestas en español o inglés.

#### Principales características:
- **División del texto en chunks** utilizando herramientas como Langchain.
- **Vectorización** del contenido mediante embeddings y almacenamiento en ChromaDB.
- **Clasificadores**:
  - Basado en un **LLM** (Unidad 6).
  - Entrenado con ejemplos y embeddings (Unidad 3).
- **Búsquedas híbridas** (semánticas y por palabras clave) con mecanismos de **ReRank**.

### Ejercicio 2: Agente ReAct
Se incorpora un **agente inteligente** basado en **ReAct**, que utiliza herramientas para buscar información en las fuentes implementadas en el Ejercicio 1.  

#### Herramientas implementadas:
- `get_info_vector_db()`: Busca en los documentos.
- `get_info_graph_db()`: Busca en la base de datos de grafos.
- `get_info_tabular_db()`: Busca en los datos tabulares.  

El agente evalúa consultas complejas que requieren combinar varias herramientas. Además, se analizan ejemplos exitosos y casos de fallos, proponiendo mejoras.

---

## 🚀 Cómo Ejecutar el Proyecto

### Requisitos
- Una cuenta de **Google** para acceder a **Google Colab**.
- Acceso a Internet para cargar el cuaderno Jupyter y descargar los datasets.

### Pasos para ejecutar:
1. Haz clic en el siguiente enlace para abrir el cuaderno Jupyter en Google Colab:  
   [TP2_Viticulture.ipynb](https://colab.research.google.com/drive/1RCz8d6-ExaSZP8XdxxkD0_19C0bUgRy9?usp=sharing).
2. Una vez abierto, selecciona `Archivo > Guardar una copia en Drive` si deseas trabajar en tu propio entorno.
3. Ejecuta cada celda del cuaderno en orden.
4. Asegúrate de que los recursos y datasets externos se descarguen correctamente desde el código.

---

## 📊 Fuentes de Datos

1. **Documentos de texto**: Instrucciones y guías de Viticulture (mínimo 3 documentos y 100 páginas en total).
2. **Datos tabulares**: Información estructurada en CSV o DataFrames.
3. **Base de datos de grafos**: Construida dinámicamente a partir de las fuentes anteriores.

---

## 🛠️ Herramientas y Librerías Utilizadas

- **Google Colab** para la ejecución en la nube.
- **Langchain** para procesar textos y realizar búsquedas híbridas.
- **ChromaDB** para almacenamiento y recuperación de embeddings.
- **Llama-Index** para implementar el agente ReAct.
- **Modelos LLM**: Puedes usar cualquier modelo compatible para embeddings y generación de texto.
- **Python** y librerías adicionales:
  - `pandas`
  - `numpy`
  - `networkx` o `neo4j` (para la base de datos de grafos)
  - `sqlalchemy` o `sqlite3` (para consultas tabulares)
  - `spacy` y `nltk` (para procesamiento de lenguaje natural)

---

## 📌 Observaciones

- **Nota importante**: Este proyecto fue desarrollado como parte de una asignatura académica. Las fuentes y herramientas cumplen con los requerimientos establecidos.



