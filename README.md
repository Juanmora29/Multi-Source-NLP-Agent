# Asistente Virtual "ElectroHogar" 🤖

Este repositorio contiene el desarrollo final de la materia **Procesamiento del Lenguaje Natural**. 

El proyecto consiste en un **Agente Autónomo** basado en el paradigma **ReAct**, capaz de orquestar múltiples fuentes de datos heterogéneas (Texto, Tablas y Grafos) para responder consultas complejas de negocio y soporte técnico.

## 🚀 Características Principales

*   **Arquitectura Multi-Fuente:** Integración simultánea de tres tipos de bases de datos:
    *   📚 **Vectorial (ChromaDB):** Para manuales y reseñas (Búsqueda Híbrida BM25 + Semántica + Re-Ranking).
    *   📊 **Tabular (Pandas):** Para ventas y stock (Generación dinámica de código Python).
    *   🕸️ **Grafos (Neo4j):** Para relaciones entre productos y categorías (Generación dinámica de Cypher).
*   **Custom ReAct Agent:** Implementación de una arquitectura de agente personalizada (`AgenteManual`) que gestiona el ciclo de razonamiento *Thought-Action-Observation*, superando las limitaciones de estabilidad de las librerías estándar.
*   **Analytics en Tiempo Real:** Capacidad de generar y renderizar gráficos estadísticos (`matplotlib`) bajo demanda.
*   **Clasificación Avanzada:** Uso de LLM con *Few-Shot Prompting* para la detección de intención con 100% de accuracy.

## 🛠️ Stack Tecnológico

*   **LLM:** Google Gemini 2.0 Flash.
*   **Embeddings:** `intfloat/multilingual-e5-small`.
*   **Re-Ranker:** `BAAI/bge-reranker-v2-m3`.
*   **Infraestructura:** LangChain (Core), ChromaDB, Neo4j AuraDB.
*   **Entorno:** Google Colab.

## 📋 Instalación y Ejecución

El proyecto está autocontenido en un cuaderno de Jupyter (`.ipynb`).

1.  Abrir el archivo `TP_NLP_Final.ipynb` en **Google Colab**.
2.  Configurar las API Keys en los secretos de Colab (`GOOGLE_API_KEY`, `NEO4J_PASSWORD`).
3.  Ejecutar las celdas secuencialmente. 
    *   *Nota:* El sistema incluye una carga optimizada de la base vectorial mediante `gdown` para evitar el reprocesamiento de archivos.

## 📄 Estructura del Proyecto

*   **Ejercicio 1 (RAG):** Construcción de los recuperadores, índices y el orquestador determinista.
*   **Ejercicio 2 (Agente):** Implementación del Agente Autónomo, memoria conversacional y herramientas (Tools).

---
**Autor:** Juan Andres Morales
