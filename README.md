# Ollama Server - Docker Environment

Easily way to set up a local Ollama server and try some models flavors like Mistral, Llama 3.1 and others.

# Use

1. Clone repo
```bash
git clone <repo>
```

2. Execute
```bash
docker-compose up -d
```

3. Test Ollama server 
```bash
curl http://localhost:11434/api/tags
```

You should see the somthing like this

```json
{
  "models": [
    {
      "name": "llama3.1:latest",
      "model": "llama3.1:latest",
      "modified_at": "2024-07-24T13:48:38.133337995Z",
      "size": 4661226402,
      "digest": "a340353013fdd762755b791c475fc4781d9f77019fe25ece2ce76e3135f5b8c8",
      "details": {
        "parent_model": "",
        "format": "gguf",
        "family": "llama",
        "families": [
          "llama"
        ],
        "parameter_size": "8.0B",
        "quantization_level": "Q4_0"
      }
    }
  ]
}
```

You can use the file ollama_api.http using the humao.rest-client vscode plugin to  Load a different Model, remove and pull other models also.

4. Test using chat UI (open-webui)
```bash
http://host.docker.internal:3030/
```

