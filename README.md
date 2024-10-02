# PyCon ES 2024 - Demostración de Flujos de Trabajo con Agentes de IA

Este repositorio contiene el código y los ejemplos utilizados en la charla **Flujos de trabajo con agentes de IA en Python**, presentada en la **PyCon ES 2024**. El objetivo de este proyecto es mostrar cómo aprovechar modelos de lenguaje (LLM) y flujos de trabajo basados en agentes de IA para automatizar procesos de desarrollo de software con Python.

## Instalación

Para ejecutar este proyecto en tu entorno local, asegúrate de tener instalado **Python 3.9 o superior**.

1. Clona este repositorio:

    ```bash
    git clone https://github.com/rael-my/pycon24_agents
    cd pycon24_agents
    ```

2. Instala las dependencias necesarias:

    ```bash
    pip install -r requirements.txt
    ```

3. Crea un archivo `.env` con las credenciales de la OpenAI API Key. **Nota**: El código es fácilmente adaptable para cambiar el proveedor de la API a cualquiera soportado por LangChain, incluyendo la ejecución local con Ollama: https://python.langchain.com/docs/integrations/chat/

## Aspectos clave del notebook

1. **Selección y configuración del modelo de lenguaje**: Se define el modelo que se usará para generar respuestas algorítmicas y gestionar la interacción con el agente. En esta demostración, se ha utilizado el modelo `gpt-4o-mini` de OpenAI.
   
2. **Gestión del estado del grafo de mensajes entre agentes**: Se implementa un grafo de estado personalizado que almacena información clave para el flujo de trabajo, como la descripción general, requisitos funcionales, retroalimentación humana y propuestas algorítmicas.

3. **Prompts especializados para diferentes roles**: Los agentes de IA reciben instrucciones claras para desempeñar funciones específicas, como analistas funcionales, desarrolladores y revisores de calidad (QA). Cada uno tiene un conjunto de instrucciones predefinido que guía su comportamiento y toma de decisiones.

4. **Construcción y ejecución del grafo**: Se utiliza una estructura de nodos y aristas para crear el flujo de trabajo. El grafo se ejecuta de manera iterativa, permitiendo a los agentes proponer soluciones y pasar por múltiples etapas de validación.

5. **Incorporación de retroalimentación humana**: El flujo de trabajo permite que los humanos intervengan en puntos clave, proporcionando retroalimentación que se incorpora en iteraciones posteriores.

6. **Revisión y documentación final**: El analista funcional genera la documentación final del proyecto basada en las soluciones refinadas por los desarrolladores y el equipo de QA. Finalmente, el agente utliza herramientas específicas para almacenar el código y la documentación.

## Tecnologías

Este proyecto utiliza las siguientes bibliotecas:

- **LangGraph**: Para la gestión de agentes y flujos de trabajo.
- **OpenAI**: Como backend de los modelos de lenguaje de gran tamaño.
- **Jupyter**: Para facilitar la interacción y ejecución del código.

## Licencia

Este proyecto está licenciado bajo los términos de la **MIT License**. Esto significa que puedes utilizar, modificar y distribuir el código libremente, siempre que se incluya el aviso de derechos de autor original.

Puedes leer más sobre los términos de la licencia en el archivo [LICENSE](./LICENSE).

---

¡Gracias por asistir a PyCon ES 2024 y por tu interés en los flujos de trabajo con agentes de IA!
