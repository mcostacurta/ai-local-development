# AI Local Environment setup - Ollama | ChromaDB | Langflow

Easily way to set up a local AI tools to validate your AI idea using your local machine.


**Ollama** -> Ollama software that allows you to run Large Language Models (LLMs) and other generative AI models directly on your local machine. https://ollama.com/

**ChromaDB** -> Is an open-source vector database tailored to applications with large language models. https://www.trychroma.com/

**Langflow** -> visual framework for building multi-agent and RAG applications. It is open-source, Python-powered, fully customizable, and LLM and vector store agnostic. https://www.langflow.org


Everything together is a very useful "Swiss army knife" for your AI Learning path.

# Use

1. Clone repo
   
    ```bash
    git clone <repo>
    ```

2. Execute
    ```bash
    docker-compose -f docker-compose-ollama-v2.yml up -d
    ```

3. Validate if everything is running 

      Ollama
      ```bash
      curl http://host.docker.internal:11434/api/tags
      ```

      Qdrant
      ```bash
      curl http://host.docker.internal:6333/dashboard
      ```

      Langflow
      ```bash
      curl http://host.docker.internal:7860
      ```



You can use the file **ollama_api.http** using the **humao.rest-client** vscode plugin to  Load a different Model, remove and pull other models also.

4. Open the Langflow and have fun! 😜
    ```bash
    http://host.docker.internal:7860
    ```