# IA Generativa na Vida Universitária

**Pesquisa, Estudo e Escrita com Chatbots e Modelos Locais**

Ministrante: Prof. Eric Brasil (UNILAB • PPGIHD/UFRRJ • LABHDUFBA)  
Data: 19/05/2026 (terça-feira) | 9h30–11h30  
Público-alvo: Estudantes de graduação e pós-graduação e docentes da UNILAB

---

## Resumo

Oficina prática sobre inteligência artificial generativa no contexto universitário. Aborda os fundamentos dos LLMs, estratégias de uso de chatbots web (ChatGPT, Claude, Gemini, Copilot) na pesquisa, estudo e escrita acadêmica, cuidados éticos (alucinações, vieses, transparência) e o horizonte de possibilidades avançadas: execução de modelos abertos localmente com Ollama, RAG e agentes de IA. Não requer conhecimento prévio de programação.

## Estrutura

### Parte 1 — O que é IA generativa? (~30min)

- IA generativa ≠ IA Geral: distinções essenciais
- LLMs: o que são, como funcionam (transformers, parâmetros, treinamento)
- Alucinações, vieses e limitações
- Custo ambiental e infraestrutural
- Modelos fechados vs abertos

### Parte 2 — Chatbots na prática acadêmica (~50min)

- ChatGPT, Claude, Gemini, Copilot: semelhanças e diferenças
- Prompt engineering: 4 princípios
- Projetos e instruções personalizadas
- NotebookLM: IA com seus documentos
- Usos na pesquisa, no estudo e na escrita acadêmica (com exemplos de prompts)
- Cuidados éticos: plágio, transparência, limites institucionais
- Portaria CNPq nº 2.664/2026: IA Generativa e integridade científica

### Parte 3 — Horizontes avançados (~20min)

- Modelos abertos vs fechados: por que importa?
- Ollama: execução local de modelos abertos
- Modelfile: assistente personalizado (fichamento acadêmico)
- RAG: Geração Aumentada por Recuperação
- Codex e agentes de IA

### Encerramento — Discussão (~15min)

- Quando usar cada ferramenta
- Perguntas e troca de experiências

## Conteúdo do repositório

```
oficina-ia-unilab/
├── index.md                       # Fonte da apresentação (Quarto / reveal.js)
├── custom.scss                    # Personalizações adicionais de tema
├── _extensions/clean/             # Extensão quarto-revealjs-clean (tema base)
│   ├── _extension.yml
│   ├── clean.scss
│   └── mathjax-config.js
├── imgs/
│   ├── logo.png
│   ├── privacy.png
│   └── qrcode.png                 # QR code para ericbrasil.com.br/oficina-ia-unilab
├── ollama_modelfile/
│   └── Modelfile                  # Exemplo: assistente de fichamento acadêmico
├── CITATION.cff                   # Metadados para citação
├── LICENSE.md                     # CC BY-NC-SA 4.0
└── README.md
```

## Como renderizar os slides

Requisitos: [Quarto](https://quarto.org) ≥ 1.4 instalado.

```bash
git clone https://github.com/ericbrasiln/oficina-ia-unilab.git
cd oficina-ia-unilab
quarto render index.md --to revealjs
```

Abra `index.html` no navegador. Para edição interativa:

```bash
quarto preview index.md
```

### Tema visual

A apresentação usa o tema [quarto-revealjs-clean](https://github.com/grantmcdermott/quarto-revealjs-clean) (Grant McDermott) com personalizações em `custom.scss`. O tema combina:

- Tipografia **Roboto** (corpo e títulos)
- Fundo branco, layout limpo
- Cor de destaque teal (`#107895`)

## Requisitos para a oficina

- Laptop (obrigatório)
- Não é necessário conhecimento prévio de programação
- Para explorar modelos locais: instalar o [Ollama](https://ollama.com) antes ou durante a oficina

## Observação sobre autoria e IA

Parte dos conteúdos desta apresentação foi produzida com o apoio de assistentes de IA (Hermes Agent — GLM-5.1 e DeepSeek V4 Pro; GPT-5.5 para design do template visual), sob a curadoria e as escolhas editoriais do professor Eric Brasil. Todo o conteúdo, análise e decisões pedagógicas são de responsabilidade exclusiva do autor. O uso de IA foi declarado em conformidade com a Portaria CNPq nº 2.664/2026, Art. 9º, inciso I, alínea (c).

## Citação sugerida

Eric Brasil (2026). oficina-ia-unilab: IA Generativa na Vida Universitária — materiais da oficina. GitHub. https://github.com/ericbrasiln/oficina-ia-unilab

### BibTeX

```bibtex
@misc{brasil_oficina-ia-unilab_2026,
  author = {Eric Brasil},
  title = {oficina-ia-unilab: IA Generativa na Vida Universitária — Materiais da oficina},
  year = {2026},
  url = {https://github.com/ericbrasiln/oficina-ia-unilab},
  note = {CC BY-NC-SA 4.0}
}
```

## Licença

Os materiais textuais e os exemplos neste repositório estão sob a licença Creative Commons Atribuição‑NãoComercial‑CompartilhaIgual 4.0 Internacional (CC BY‑NC‑SA 4.0). Consulte `LICENSE.md` para detalhes.

<a rel="license" href="https://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Licença Creative Commons" style="border-width:0" src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" /></a>

## Contato

Eric Brasil — [ericbrasil.com.br/contact](https://ericbrasil.com.br/contact/)