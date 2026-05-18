# IA Generativa na Vida Universitária: Pesquisa, Estudo e Escrita com Chatbots e Modelos Locais

**Ministrante:** Prof. Eric Brasil (UNILAB • PPGIHD/UFRRJ • LABHDUFBA)  
**Data:** 19/05/2026 (terça-feira) | **Horário:** 9h30–11h30 | **Local:** a definir pelo núcleo  
**Público-alvo:** Estudantes de graduação e pós-graduação e docentes da UNILAB

---

## Resumo

Esta oficina apresenta os fundamentos e usos práticos da inteligência artificial generativa — em especial os Large Language Models (LLMs) — no contexto universitário. Serão abordados: o que é IA generativa e como funcionam os chatbots baseados em LLMs; estratégias e melhores práticas para uso de chatbots web (ChatGPT, Gemini, Copilot) na pesquisa, no estudo e na escrita acadêmica; cuidados éticos, vieses e alucinações; e uma demonstração prática de execução de modelos abertos em máquina local com Ollama. A oficina é voltada para estudantes de graduação e pós-graduação e docentes que desejam incorporar essas ferramentas de forma crítica e responsável em suas rotinas acadêmicas.

## Estrutura da Oficina

### Parte 1 — O que é IA generativa? (~30min)

- IA generativa ≠ IA Geral: distinções essenciais
- LLMs: o que são, como funcionam (treinamento, transformers, parâmetros)
- Alucinações, vieses e limitações
- Custo ambiental e infraestrutural

### Parte 2 — Melhores práticas com chatbots web (~45min)

- ChatGPT, Gemini, Copilot: semelhanças e diferenças
- Prompt engineering básico
- Usos na pesquisa, no estudo e na escrita acadêmica
- Cuidados éticos: plágio, transparência, limites institucionais
- Regra prática: a IA auxilia, não substitui o pensamento crítico

### Parte 3 — Modelos locais com Ollama (~30min)

- Modelos abertos vs. fechados: por que rodar localmente?
- Instalação e comandos básicos do Ollama
- Baixando e rodando modelos leves
- Criando um Modelfile personalizado
- Vantagens: privacidade, autonomia, reprodutibilidade

### Encerramento — Discussão (~15min)

- Balanço e perguntas

## Conteúdo do repositório

```
oficina-ia-unilab/
├── index.md                  # Fonte da apresentação (Quarto / Reveal.js)
├── custom.scss               # Folha de estilos personalizada
├── imgs/                     # Imagens usadas nos slides
│   ├── logo.png
│   └── privacy.png
├── ollama_modelfile/
│   └── Modelfile              # Exemplo de Modelfile (assistente de resumo)
├── CITATION.cff              # Metadados para citação
├── LICENSE.md                # Licença CC BY-NC-SA 4.0
└── README.md                 # Este arquivo
```

## Como renderizar os slides

Requisitos: [Quarto](https://quarto.org) instalado.

```bash
git clone https://github.com/ericbrasiln/oficina-ia-unilab.git
cd oficina-ia-unilab
quarto render index.md --to revealjs
```

Abra `index.html` no navegador.

## Requisitos para a oficina

- Laptop (obrigatório)
- Não é necessário conhecimento prévio de programação
- Para a Parte 3: instalar o [Ollama](https://ollama.com) antes ou durante a oficina

## Observação sobre autoria e IA

Parte dos conteúdos desta apresentação foi produzida com o apoio de assistentes de IA, sob a curadoria e as escolhas editoriais do professor Eric Brasil. O uso de assistentes de IA foi informado e acompanhado de decisões metodológicas do autor.

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