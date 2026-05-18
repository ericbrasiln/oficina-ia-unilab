---
title: "IA Generativa na Vida Universitária"
subtitle: "Pesquisa, Estudo e Escrita com Chatbots e Modelos Locais"
date: 2026-05-19
date-format: full
lang: pt-br
format:
  revealjs:
    theme: [serif, custom.scss]
    slide-number: true
    incremental: false
    chalkboard:
      buttons: true
    footer: "Eric Brasil | <a href='https://ericbrasil.com.br/contact/'>Entre em contato</a> | Oficina UNILAB"
    logo: https://raw.githubusercontent.com/ericbrasiln/cclhm0081/refs/heads/main/imgs/logos.png
author:
  - name: Eric Brasil
    orcid: 0000-0001-5067-8475
    affiliation: (UNILAB • PPGIHD/UFRRJ • LABHDUFBA)
description: "Oficina prática sobre IA generativa no contexto universitário: fundamentos, melhores práticas com chatbots web e demonstração de modelos locais com Ollama."
toc: false
---

## {.center}

🧠 **IA Generativa na Vida Universitária**
Pesquisa, Estudo e Escrita com Chatbots e Modelos Locais

Prof. Eric Brasil | UNILAB • PPGIHD/UFRRJ • LABHDUFBA

19 de maio de 2026

---

## Nota sobre o uso de IA Generativa {.center}

🛠️ Esta apresentação foi **produzida com o apoio de assistentes de IA**, sob curadoria e escolhas editoriais do professor **Eric Brasil**.

🤖 Todo o conteúdo, formatação e exemplos práticos foram gerados de forma **colaborativa**, preservando as escolhas **editoriais, metodológicas e pedagógicas** do autor.

---

## Estrutura da Oficina {.columns}
<br>

### Objetivos  

::: {.column width="46%"}
- Compreender o que é IA generativa e como funciona.  
- Aprender a usar chatbots web de forma crítica na vida universitária.

:::

::: {.column width="8%"}
:::
::: {.column width="46%"}
- Conhecer modelos abertos e rodá-los localmente com Ollama.  
- Refletir sobre ética, vieses e limitações da IA generativa.
:::

---

## Estrutura da Oficina {.columns}
<br>

### Estrutura  

::: {.column width="30%"}
1. **O que é IA generativa?**  ~30min  
   Fundamentos, LLMs, limites.

:::

::: {.column width="5%"}
:::

::: {.column width="30%"}
2. **Melhores práticas com chatbots web**  ~45min  
   Pesquisa, estudo, escrita.

:::

::: {.column width="5%"}
:::

::: {.column width="30%"}
3. **Modelos locais com Ollama**  ~30min  
   Demo prática + Modelfile.
:::

---

## 1. O que é IA generativa? {.center}

---

## IA Generativa ≠ IA Geral {.center}

🤖 **IA Generativa**  

- Criadora de conteúdos: textos, imagens, áudio, vídeo, código  
- Aprende padrões a partir de grandes volumes de dados  
- Não tem conscience nem compreensão — funciona com **probabilidades**

🧠 **IA Geral (AGI)**  

- Habilidade de aprender qualquer tarefa cognitiva  
- Equivalente (ou superior) à inteligência humana  
- Ainda é **teórica** — não existe hoje

---

## O que são LLMs? {.center}

📚 **LLM** = *Large Language Model* (Modelo de Linguagem de Grande Escala)

São programas treinados com **bilhões de textos** para:

- Entender e gerar linguagem natural  
- Resumir, traduzir, responder perguntas, analisar textos

Exemplos: GPT-5, Claude, Gemini, LLaMA, Qwen

---

## Como os LLMs funcionam? {.center}

Simplificando:

1. O modelo **lê bilhões de textos** durante o treinamento  
2. Aprende **padrões estatísticos** de linguagem  
3. Quando você escreve algo, ele **prevê** qual palavra vem em seguida  
4. Gera respostas **palavra por palavra**, com base em probabilidade

> ⚠️ O modelo não "entende" nem "pensa" — ele **prevê texto provável**.

---

## Redes neurais e Deep Learning {.center}

🧠 **Redes neurais**: estruturas matemáticas inspiradas no cérebro

- Recebem entradas → processam em camadas → produzem saídas  
- Aprendem a reconhecer padrões ajustando "pesos" internos

🔢 **Deep Learning**: redes neurais com **muitas camadas**

- Cada camada aprende representações mais complexas  
- É a base dos LLMs modernos

---

## Transformers: a revolução {.center}

📄 Introduzidos por Vaswani et al. (2017): *"Attention is All You Need"*

**Mecanismo de atenção**: o modelo decide quais partes do texto são mais relevantes para gerar a próxima palavra.

Resultado:

- Lida com **longos contextos**  
- Mantém **coerência** em textos longos  
- Base do GPT, Claude, Gemini e todos os LLMs modernos

---

## Treinamento: como o modelo aprende? {.center}

1. O modelo **prevê uma palavra** em uma sequência  
2. Compara com a palavra real do corpus  
3. Calcula o **erro** entre previsão e realidade  
4. **Ajusta os pesos** para errar menos na próxima vez  
5. Repete **bilhões de vezes**

---

## Parâmetros: o que o modelo "aprende"? {.center}

🔢 **Parâmetros = números ajustados durante o treinamento**

- Cada parâmetro define como uma entrada influencia uma saída  
- Quanto mais parâmetros, maior a capacidade de representar padrões complexos

| Modelo | Ano | Parâmetros  |
|:-------|:----:|:----------:|
| GPT-2 | 2019 | 1,5 bilhão  |
| GPT-3 | 2020 | 175 bilhões |
| GPT-4 | 2023 | ≃ 1 trilhão |

---

## Alucinações {.center}

🤯 **O que é uma alucinação?**

- O modelo **gera uma resposta incorreta ou inventada**, mas com aparência de verdade  
- Resulta da forma como ele **estima probabilidades** — sem acesso à realidade  
- O modelo não "sabe", apenas **prediz o texto mais provável**

📌 **Exemplos:**

- Citações inexistentes  
- Fatos históricos trocados  
- Nomes, datas ou dados inventados

---

## Alucinações: por que importam? {.center}

⚠️ Na universidade, isso é **crítico**:

- Um artigo pode citar uma referência que **não existe**  
- Um resumo pode incluir informações **inventadas**  
- Dados estatísticos podem ser **falsos** mas convincentes

✅ **Regra fundamental:** Sempre **verifique** as informações geradas por IA.

---

## Vieses na IA Generativa {.center}

🔍 **Tipos de viés:**

- **Viés de representatividade**: grupos sub-representados nos dados de treinamento  
- **Viés de exclusão**: ausência total de certos grupos e perspectivas  
- **Viés de automação**: confiança cega nas respostas da IA  
- **Viés de contexto**: falha ao interpretar corretamente nuances culturais

💡 Causa: dados de treinamento refletem **desigualdades e preconceitos da sociedade**

---

## Custo ambiental {.center}

🌍 Usar IA generativa tem um custo **invisível, mas real**:

- Consumo massivo de energia elétrica  
- Uso intensivo de água para refrigeração de data centers  
- Mineração de recursos naturais para fabricar hardware (GPUs)  
- Emissão de carbono associada a cada consulta

> ⚠️ Cada prompt enviado consome energia. Use com consciência.

---

## Modelos Fechados vs Abertos {.columns}

::: {.column width="50%"}
**🔒 Modelos Fechados**

- Desenvolvidos por empresas (OpenAI, Google)  
- Acesso via APIs ou interfaces web  
- Pouca transparência (_black box_)  
- Seus dados podem ser usados para treinar  
- Exemplos: GPT-5, Claude, Gemini
:::

::: {.column width="50%"}
**🔓 Modelos Abertos**

- Código e pesos acessíveis e personalizáveis  
- Executáveis localmente, no seu computador  
- Maior controle e privacidade  
- Ninguém vê seus prompts  
- Exemplos: LLaMA, Mistral, Qwen, Gemma
:::

---

## 2. Melhores práticas com chatbots web {.center}

---

## Chatbots web: os mais usados {.center}

| Chatbot | Empresa | Acesso gratuito | Busca na web |
|:--------|:--------|:---------------|:------------:|
| **ChatGPT** | OpenAI | Sim (limitado) | Sim |
| **Gemini** | Google | Sim | Sim |
| **Copilot** | Microsoft | Sim | Sim |
| **Claude** | Anthropic | Sim (limitado) | Não |

📌 Todos funcionam com LLMs por trás. As diferenças principais são: modelo, limite de uso gratuito, busca na web e integração com outros serviços.

---

## O que é um prompt? {.center}

💬 **Prompt = instrução que você dá à IA**

É como você "fala" com o chatbot. Quanto **melhor o prompt**, **melhor a resposta**.

> ❌ Prompt vago: "Fale sobre história do Brasil"  
> ✅ Prompt claro: "Liste 3 causas econômicas da Independência do Brasil, com breves explicações (máx. 200 palavras)"

---

## Prompt engineering: 4 princípios {.center}

1. **Seja específico** — diga exatamente o que quer  
2. **Dê contexto** — para quem é, qual o nível, qual o objetivo  
3. **Defina o formato** — lista, parágrafo, tabela, passo a passo  
4. **Itere** — refine a resposta com follow-ups

---

## Usos na pesquisa {.center}

🔬 Como chatbots podem ajudar:

- **Exploração de conceitos**: "Explique o conceito de X como se eu tivesse 15 anos"  
- **Revisão de literatura**: "Quais são as principais correntes teóricas sobre X?"  
- **Organização de ideias**: "Me ajude a estruturar um projeto sobre X"  
- **Tradução**: Traduzir resumos, abstracts, e-mails acadêmicos

⚠️ **Sempre verifique**: fontes, citações e dados gerados pela IA.

---

## Usos no estudo {.center}

📖 Como chatbots podem ajudar:

- **Resumo**: "Resuma este texto em 5 pontos-chave"  
- **Flashcards**: "Gere 10 flashcards sobre este conteúdo"  
- **Simulação de questões**: "Crie 5 questões de múltipla escolha sobre X"  
- **Explicação**: "Explique esta fórmula/conceito com um exemplo prático"

---

## Usos na escrita acadêmica {.center}

✍️ Como chatbots podem ajudar:

- **Planejamento**: estruturar o roteiro de um artigo  
- **Revisão**: identificar problemas de clareza, coesão, gramática  
- **Tradução**: versões em outros idiomas para publicação  
- **Formatação**: ajustar citações, referências

❌ O que **NÃO** fazer:

- Deixar a IA escrever o texto por você  
- Copiar e colar sem revisar  
- Não declarar o uso de IA

---

## Regra prática {.center}

> 🎯 **A IA auxilia, não substitui o pensamento crítico.**

Use como:

- Um **assistente de brainstorming**  
- Um **revisor** que aponta lacunas  
- Um **tradutor** e **organizador**  

Mas nunca como:

- Um **substituto** da sua análise  
- Uma **fonte** primária de informação

---

## Cuidados éticos {.center}

⚖️ Questões fundamentais:

- **Plágio**: texto gerado por IA sem atribuição é plágio?  
- **Transparência**: devo declarar que usei IA?  
- **Limites institucionais**: sua universidade tem regulamento?  
- **Privacidade**: não insira dados pessoais ou sensíveis em chatbots web  
- **Equidade**: nem todos têm acesso igual a essas ferramentas

---

## Declaração de uso de IA {.center}

📋 Boa prática: **sempre declare** quando usar IA

Exemplo:

> "O autor utilizou o ChatGPT (modelo GPT-5) como ferramenta auxiliar na revisão gramatical e organização de ideias deste trabalho. Todo o conteúdo, análise e argumentação são de responsabilidade exclusiva do autor."

---

## Portaria CNPq 2.664/2026: IA Generativa e Integridade {.center}

📜 **[Portaria CNPq nº 2.664, de 6 de março de 2026](http://memoria2.cnpq.br/web/guest/view/-/journal_content/56_INSTANCE_0oED/10157/23142775?COMPANY_ID=10132)** — Política de Integridade na Atividade Científica do CNPq

📌 **Art. 9º, inciso I** — Diretrizes de integridade na pesquisa:

> **c)** declarar o uso de ferramentas de Inteligência Artificial Generativa (IAG), de qualquer espécie e em qualquer fase da pesquisa (concepção, redação, análise de dados, submissão), especificando a ferramenta utilizada e a finalidade;

---

## Portaria CNPq 2.664/2026: vedações {.center}

⚠️ O que a portaria **veda**:

> **d)** é vedada a submissão de conteúdo gerado por IAG como se fosse de autoria humana, sendo os autores integralmente responsáveis pelo conteúdo final, inclusive por eventuais plágios ou imprecisões geradas pela IAG;

> **e)** é vedada a inserção de projetos de pesquisa de terceiros em ferramentas de IAG para elaboração de pareceres científicos;

> **f)** responsabilizar-se integralmente pelo conteúdo final da pesquisa, inclusive por eventuais plágios ou imprecisões geradas pela IAG.

---

## Portaria CNPq: o que muda na prática? {.center}

✅ **Declarar** sempre que usar IAG — em qualquer fase da pesquisa  
❌ **Nunca** submeter texto gerado por IA como se fosse seu  
❌ **Nunca** inserir projetos de terceiros em IAG para gerar pareceres  
✅ **Responsabilidade total** do autor sobre o conteúdo final

> 💡 Se a IA alucinou uma citação e você incluiu no texto — **a responsabilidade é sua.**

---

## Infrações e sanções {.center}

⚖️ A portaria classifica infrações por gravidade:

- **Leves**: sem dolo, sem prejuízo (advertência)  
- **Graves**: autoplágio; informação inconsistente no Lattes com efeito na avaliação (suspensão de bolsas, impedimento em editais)  
- **Gravíssimas**: fabricação/falsificação de dados, **plágio**, comercialização de autoria, condutas discriminatórias (revogação de fomento, devolução de recursos)

📌 Plágio — inclusive via IAG — é infração **gravíssima**.

---

## Temperatura e criatividade {.center}

🌡️ **Temperatura** = parâmetro que controla a aleatoriedade da resposta

| Valor | Efeito |
|:------|:-------|
| 🔹 **Baixa (0.1–0.3)** | Respostas previsíveis e consistentes |
| 🔸 **Média (0.5–0.7)** | Equilíbrio entre coerência e criatividade |
| 🔺 **Alta (0.8–1.0+)** | Respostas criativas, porém menos estáveis |

💡 Nos chatbots web, a temperatura vem pré-definida. Na API ou no Ollama, você controla.

---

## Codex: IA no terminal {.center}

💻 **Codex** são interfaces de terminal (TUI) que conectam LLMs ao seu computador — vão além do chatbot web:

- Lêem e escrevem **arquivos locais**  
- Executam **comandos no terminal**  
- Operam **direto no seu projeto** — contexto real, não texto colado

> 💡 Pense neles como um "assistente de programação e automação" que mora no seu terminal.

---

## Codex: principais exemplos {.center}

| Ferramenta | Empresa | Modelo | Código aberto |
|:-----------|:--------|:-------|:------------:|
| **Codex CLI** | OpenAI | GPT-5 / o-series | Sim |
| **Claude Code** | Anthropic | Claude | Não |
| **OpenCode** | Comunidade | Ollama (local) | Sim |

📋 Cada uma tem abordagem própria, mas o princípio é o mesmo: **IA que atua no seu sistema de arquivos e terminal.**

---

## Codex CLI (OpenAI) {.center}

🔑 Roda modelos da OpenAI (GPT-5, o-series) direto no terminal

- Modos: **suggest** (sugere, você aprova), **auto-edit** (edita com aprovação), **full-auto** (autônomo)  
- Pode ler código, escrever arquivos, rodar comandos  
- Requer **API Key** da OpenAI (uso pago)

```bash
codex "Crie um arquivo README.md para este projeto"
```

---

## Claude Code (Anthropic) {.center}

🔑 Roda o modelo Claude no terminal com acesso ao seu projeto

- Entende o código do repositório automaticamente  
- Pode criar, editar e buscar arquivos  
- Requer **API Key** da Anthropic (uso pago)  
- Indicado para projetos de software

```bash
claude "Explique a função principal deste repositório"
```

---

## OpenCode {.center}

🔓 Roda modelos **locais via Ollama** — sem API Key, sem custo

- Usa modelos que você já baixou: phi3, gemma3, qwen3...  
- **Privacidade total** — nada sai do computador  
- Ideal para experimentar codex sem pagar

```bash
opencode "Revise o estilo deste texto e sugira melhorias"
```

---

## Codex: quando usar? {.center}

📌 **Use codex quando:**

- Precisa que a IA **leia ou altere arquivos** no seu computador  
- Quer automação de tarefas repetitivas em projetos  
- Trabalha com **código, dados ou textos** estruturados

⚠️ **Cuidados:**

- APIs pagas — custo por token  
- Sempre **revise** o que o codex cria ou modifica  
- Arquivos sensíveis: prefira modelos locais (OpenCode + Ollama)

---

## 3. Modelos locais com Ollama {.center}

---

## Modelos abertos vs fechados: por que rodar localmente? {.center}

🔓 **Rodar localmente significa:**

- 🔒 **Privacidade**: ninguém vê seus prompts ou documentos  
- ⚖️ **Autonomia**: você controla o modelo e os parâmetros  
- 🧪 **Reprodutibilidade**: sempre a mesma versão, mesmo resultado  
- 🪶 **Modelos leves**: funcionam em laptops sem GPU  
- 💰 **Sem custos por uso**: depois de baixar, é grátis

---

## O que é o Ollama? {.columns}

::: {.column width="65%"}
- Plataforma para **rodar LLMs localmente**  
- Suporte a modelos **abertos**  
- Funciona em **Linux**, **Windows** e **macOS**  
- Usa **Modelfile** para personalizar o modelo  
- Fácil de instalar e usar
:::

::: {.column width="5%"}
:::

::: {.column width="30%"}
![](https://ollama.com/public/ollama.png)
:::

---

## Instalação do Ollama {.center}

📌 **Passo 1:** Baixe e instale o Ollama no seu computador

- 🪟 **Windows**: [ollama.com/download/windows](https://ollama.com/download/windows)  
- 🍎 **macOS**: [ollama.com/download/mac](https://ollama.com/download/mac)  
- 🐧 **Linux**: siga as instruções em [ollama.com/download/linux](https://ollama.com/download/linux)

💡 A instalação é simples: baixe, execute e siga os passos na tela.

---

## Aplicativo Ollama {.center}

🖥️ Depois de instalar, abra o **aplicativo Ollama** no seu computador:

- Ele fica rodando em **segundo plano** (ícone na bandeja do sistema)  
- Não precisa usar o terminal — tudo pode ser feito pelo app  
- O app mostra os **modelos disponíveis** e permite baixar e conversar

---

## Baixando modelos pelo app {.center}

📦 No aplicativo Ollama, clique em **"Models"** e busque:

- `phi3:mini` — leve, rápido, bom para textos curtos  
- `gemma3:4b` — bom equilíbrio entre qualidade e velocidade  
- `qwen3:0.6b` — ultra-leve, ideal para testes

💡 Ou baixe pelo terminal, se preferir:

```bash
ollama pull phi3:mini
ollama pull gemma3:4b
ollama pull qwen3:0.6b
```

📌 Prefira modelos **small/mini** em PCs sem placa de vídeo dedicada (GPU).

---

## Conversando com o modelo {.center}

💬 Clique no modelo baixado no app e comece a conversar — como em um chat:

> "Explique o conceito de arquivo histórico em 3 linhas."  
> "Resuma este texto: [cole o texto aqui]"  
> "Quais as principais causas da Independência do Brasil?"

💡 A interface é semelhante à do ChatGPT — mas tudo roda **no seu computador**.

---

## Ollama pelo terminal (opcional) {.center}

⌨️ Se você gosta de terminal, também pode usar:

```bash
# Iniciar conversa interativa
ollama run phi3:mini

# Prompt direto (sem entrar no modo interativo)
ollama run phi3:mini "Resuma em 2 linhas: democracia participativa"

# Listar modelos instalados
ollama list
```

Para sair do modo interativo: digite `/bye`

---

## Modelfile: criando seu assistente personalizado {.center}

Um **Modelfile** é um arquivo de texto que permite:

- Definir **instruções permanentes** (persona, estilo, tom)  
- Ajustar **parâmetros** (temperatura, tamanho do contexto)  
- Criar uma **versão local sob medida** para suas necessidades

> 💡 Pense no Modelfile como um "system prompt permanente" — você define uma vez e o modelo sempre segue.

---

### 📝 Exemplo de `Modelfile` {.center}

Crie um arquivo de texto chamado `Modelfile` com o conteúdo:

```
FROM phi3:mini

SYSTEM """
Você é um assistente especializado em resumo de textos,
com foco em Humanidades e Ciências Sociais.

REGRAS:
- Responda SEMPRE em português do Brasil.
- Seja direto, claro e objetivo.
- Não inventar informações.
"""

PARAMETER temperature 0.2
```

---

## Como usar o Modelfile {.center}

No terminal, crie e rode o modelo personalizado:

```bash
ollama create assistente -f Modelfile
ollama run assistente
```

Ou use pelo app: o modelo "assistente" aparece na lista após a criação.

📌 *Resultado:* uma **versão local e personalizada** do modelo — ideal para pesquisa e ensino.

---

## Onde ficam os modelos? {.center}

Os modelos baixados ficam no seu computador:

- 🐧 **Linux**: `~/.ollama/models`  
- 🪟 **Windows**: `%USERPROFILE%\.ollama\models`  
- 🍎 **macOS**: `~/.ollama/models`

💡 Eles ocupam espaço em disco. Modelos leves como `phi3:mini` usam ~2 GB.

---

## Vantagens dos modelos locais {.center}

✅ **Privacidade total**: seus textos não saem do computador  
✅ **Sem custo por uso**: depois de baixar, é gratuito  
✅ **Reprodutibilidade**: mesma versão, mesmo resultado  
✅ **Autonomia**: você decide o modelo, os parâmetros, o estilo  
✅ **Sem internet**: funciona offline (depois de baixar)  
✅ **Aprendizado**: entender melhor como LLMs funcionam

---

## Limitações dos modelos locais {.center}

⚠️ Modelos pequenos (que cabem em laptop):

- Respostas menos sofisticadas que GPT-5 ou Claude  
- Mais propensos a alucinações  
- Janela de contexto menor (menos texto de uma vez)  
- Sem acesso à internet para busca

💡 **Use o modelo certo para cada tarefa.**

---

## Encerramento {.center}

🎯 **Balanço da oficina:**

- IA generativa é uma **ferramenta poderosa**, mas com **limitações reais**  
- Chatbots web são ótimos para exploração e revisão — **use com crítica**  
- Modelos locais oferecem **privacidade e autonomia** — experimente!

---

## Quando usar cada um? {.center}

| Situação | Recomendação |
|:---------|:-------------|
| Exploração de ideias, brainstorming | Chatbot web |
| Revisão gramatical, tradução | Chatbot web |
| Análise de documentos sensíveis | Modelo local |
| Reprodutibilidade em pesquisa | Modelo local |
| Sem internet | Modelo local |
| Tarefas que exigem qualidade alta | Chatbot web + verificação |

---

## Discussão {.center}

💬 **Perguntas e troca de experiências:**

- Você já usa IA generativa? Como?  
- Quais são suas preocupações?  
- Que usos você imagina na sua rotina acadêmica?

---

## Referências e recursos {.center}

📚 **Para saber mais:**

- [Documentação do Ollama](https://ollama.com)  
- [Repositório da oficina](https://github.com/ericbrasiln/oficina-ia-unilab)  
- [2shdufba — oficina anterior](https://github.com/ericbrasiln/2shdufba)

---

## Obrigado! {.center}

Prof. Eric Brasil

ericbrasil.com.br | profericbrasil@gmail.com

UNILAB • PPGIHD/UFRRJ • LABHDUFBA