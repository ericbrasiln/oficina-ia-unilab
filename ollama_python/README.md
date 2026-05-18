# Ollama Python — Script didático

Script Python simples para interagir com modelos locais do Ollama.

## Requisitos

- Python 3.8+
- Ollama instalado e em execução
- Biblioteca `requests`: `pip install requests`

## Uso

```bash
python read_doc.py
```

O script vai:

1. Verificar se o Ollama está rodando
2. Listar modelos locais disponíveis
3. Pedir um arquivo `.txt` e um prompt
4. Enviar ao modelo escolhido e exibir a resposta

## Arquivos incluídos

- `read_doc.py` — script principal
- `resumo.txt` — exemplo de arquivo para teste