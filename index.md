---
title: "IA Generativa na Vida Universitária"
subtitle: "Pesquisa, Estudo e Escrita com Chatbots e Modelos Locais"
date: 2026-05-19
date-format: full
lang: pt-br
format:
  revealjs:
    theme: [default, _extensions/clean/clean.scss]
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
description: "Oficina sobre IA generativa no contexto universitário: fundamentos, melhores práticas com chatbots web e horizontes de uso avançado."
toc: false
---

## {.center}

![Acesse a oficina online](imgs/qrcode.png){width=120px}

---

## Nota sobre o uso de IA Generativa {.center}

- **Ferramenta**: Hermes Agent (agente de IA pessoal, código aberto)
- **Modelos utilizados**: GLM-5.1 (Qwen/ollama-cloud), DeepSeek V4 Pro, GPT-5.5 (OpenAI)
- **Fases**: concepção, redação dos slides, formatação Quarto/revealjs, geração do QR code
- **Finalidade**: assistência na estruturação, redação e formatação do material

---

## Nota sobre o uso de IA Generativa {.center}

- Todo o conteúdo, análise, escolhas editoriais, metodológicas e pedagógicas são de **responsabilidade exclusiva** do prof. Eric Brasil.

---

## Estrutura da Oficina {.columns}
<br>

### Objetivos  

::: {.column width="46%"}
- Compreender o que é IA generativa e como funciona.  
- Usar chatbots web de forma **crítica e produtiva** na vida acadêmica.
:::

::: {.column width="8%"}
:::
::: {.column width="46%"}
- Conhecer o **horizonte de possibilidades avançadas**: modelos locais, agentes, RAG.  
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
2. **Chatbots na prática acadêmica**  ~50min  
   Pesquisa, estudo, escrita, projetos.

:::

::: {.column width="5%"}
:::

::: {.column width="30%"}
3. **Horizontes avançados**  ~20min  
   Ollama, agentes, RAG.
:::

---

## 1. O que é IA generativa? {.center}

---

## IA Generativa ≠ IA Geral {.center}

🤖 **IA Generativa**  

- Criadora de conteúdos: textos, imagens, áudio, vídeo, código  
- Aprende padrões a partir de grandes volumes de dados  
- Não tem conscience nem compreensão — funciona com **probabilidades**

---

## IA Generativa ≠ IA Geral {.center}

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

---

## Como os LLMs funcionam? {.center}

> ⚠️ O modelo não "entende" nem "pensa" — ele **prevê texto provável**.

---

## Redes neurais {.center}

🧠 Estruturas matemáticas inspiradas no cérebro

- Recebem entradas → processam em camadas → produzem saídas  
- Aprendem a reconhecer padrões ajustando "pesos" internos

---

## Deep Learning {.center}

🔢 Redes neurais com **muitas camadas**

- Cada camada aprende representações mais complexas  
- É a base dos LLMs modernos

---

## Transformers: a revolução {.center}

📄 Introduzidos por Vaswani et al. (2017): *"Attention is All You Need"*  
🔗 [arxiv.org/abs/1706.03762](https://arxiv.org/abs/1706.03762)

**Mecanismo de atenção**: o modelo decide quais partes do texto são mais relevantes para gerar a próxima palavra.

---

## Transformers: a revolução {.center}

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

---

## Parâmetros: o que o modelo "aprende"? {.center}


| Modelo | Ano | Parâmetros  |
|:-------|:----:|:----------:|
| GPT-2 | 2019 | 1,5 bilhão  |
| GPT-3 | 2020 | 175 bilhões |
| GPT-4 | 2023 | ≃ 1 trilhão |
| GPT-5 | 2025 | Mix of Experts |

---

## Alucinações {.center}

🤯 **O que é uma alucinação?**

- O modelo **gera uma resposta incorreta ou inventada**, mas com aparência de verdade  
- Resulta da forma como ele **estima probabilidades** — sem acesso à realidade  
- O modelo não "sabe", apenas **prediz o texto mais provável**

---

## Alucinações {.center}

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

---

## Vieses na IA Generativa {.center}

💡 Causa: dados de treinamento refletem **desigualdades e preconceitos da sociedade**

---

## Custo ambiental {.center}

🌍 Usar IA generativa tem um custo **invisível, mas real**:

- Consumo massivo de energia elétrica  
- Uso intensivo de água para refrigeração de data centers  
- Mineração de recursos naturais para fabricar hardware (GPUs)  
- Emissão de carbono associada a cada consulta

---

## Modelos Fechados vs Abertos {.center}

**🔒 Modelos Fechados**

- Desenvolvidos por big techs (OpenAI, Google)  
- Acesso via APIs ou interfaces web  
- Pouca transparência (_black box_)  
- Seus dados podem ser usados para treinar novos modelos
- Exemplos: GPT-5, Claude, Gemini

---

## Modelos Fechados vs Abertos {.center}

**🔓 Modelos Abertos**

- Código e pesos acessíveis e personalizáveis  
- Executáveis localmente, no seu computador  
- Maior controle e privacidade  
- Ninguém vê seus prompts  
- Exemplos: LLaMA, Mistral, Qwen, Gemma, Deepseek

---

## 2. Chatbots na prática acadêmica {.center}

---

## Chatbots web: os mais usados {.center}

| Chatbot | Empresa | Acesso gratuito | Busca na web |
|:--------|:--------|:---------------|:------------:|
| **ChatGPT** | OpenAI | Sim (limitado) | Sim |
| **Gemini** | Google | Sim | Sim |
| **Copilot** | Microsoft | Sim | Sim |
| **Claude** | Anthropic | Sim (limitado) | Não |

## 📌 Todos funcionam com LLMs por trás. As diferenças principais são: modelo, limite de uso gratuito, busca na web e integração com outros serviços. {.center}

---

## O que é um prompt? {.center}

💬 **Prompt = instrução que você dá à IA**

É como você "fala" com o chatbot. Quanto **melhor o prompt**, **melhor a resposta**.

---

## O que é um prompt? {.center}

> ❌ Prompt vago: "Fale sobre história do Brasil"  
> ✅ Prompt claro: "Liste 3 causas econômicas da Independência do Brasil, com breves explicações, apresentando o debate historiográfico associado a cada uma delas (máx. 500 palavras)"

---

## Prompt engineering: 4 princípios {.center}

1. **Seja específico** — diga exatamente o que quer  
2. **Dê contexto** — para quem é, qual o nível, qual o objetivo  
3. **Defina o formato** — lista, parágrafo, tabela, passo a passo  
4. **Itere** — refine a resposta com follow-ups

---

## Boas práticas: projetos e instruções personalizadas {.center}

🗂️ Os chatbots permitem criar **projetos** e definir **instruções permanentes**

- **[ChatGPT](https://chatgpt.com)**: *Projects* → organize conversas por projeto + *Custom Instructions* em Settings
- **[Claude](https://claude.ai)**: *Projects* → adicione documentos de contexto + instruções do projeto
- **[Gemini](https://gemini.google.com)**: *Gems* → crie personas com instruções salvas

## 💡 Defina sua área, idioma e estilo uma vez — o modelo já começa cada conversa com esse contexto. {.center}

---

## [NotebookLM](https://notebooklm.google.com): IA com seus documentos {.center}

- Faça upload de PDFs, artigos, sites, vídeos do YouTube  
- O modelo responde **com base apenas nos seus fontes** — menos alucinação  
- Gera resumos, fichamentos, mapas conceptuais e podcasts
- - Ideal para **fichamento, revisão de literatura e estudo dirigido**

## ⚠️ Dados enviados ao Google: não use documentos sensíveis. {.center}

---

## Usos na pesquisa {.center}

🔬 Como chatbots podem ajudar:

- **Exploração de conceitos**: "Explique o conceito de X como se eu tivesse 15 anos"  
- **Revisão de literatura**: "Quais são as principais correntes teóricas sobre X?"  
- **Organização de ideias**: "Me ajude a estruturar um projeto sobre X"  
- **Tradução**: traduzir resumos, abstracts, e-mails acadêmicos

---

## Usos na pesquisa: exemplos de prompts {.center}

📌 **Exploração conceitual:**

> "Sou estudante de História e preciso entender o conceito de 'história dos conceitos' de Reinhart Koselleck. Explique em termos simples e depois dê um exemplo de aplicação."

## {.center}

📌 **Revisão de literatura:**

> "Liste as 5 principais abordagens teóricas sobre a Revolução Francesa, com 1 parágrafo cada. Para cada uma, indique um autor representativo e uma obra de referência."

---

## Usos no estudo {.center}

- **Resumo**: "Resuma este texto em 5 pontos-chave"  
- **Flashcards**: "Gere 10 flashcards sobre este conteúdo"  
- **Simulação de questões**: "Crie 5 questões de múltipla escolha sobre X"  
- **Explicação**: "Explique esta fórmula/conceito com um exemplo prático"

---

## Usos no estudo: exemplos de prompts {.center}

📌 **Fichamento:**

> "Aqui está um artigo de 10 páginas sobre X [cole o texto]. Produza um fichamento com: referência completa, tema central, argumento principal, 3 conceitos-chave, 2 citações relevantes com página."

## {.center}

📌 **Questões de estudo:**

> "Gere 8 questões de múltipla escolha sobre o capítulo 3 do texto abaixo, com 4 alternativas cada. Marque a resposta correta."

---

## Usos na escrita acadêmica {.center}

- **Revisão**: identificar problemas de clareza, coesão, gramática  
- **Planejamento**: estruturar o roteiro de um artigo  
- **Tradução**: versões em outros idiomas para publicação  
- **Formatação**: ajustar citações, referências
- **Brainstorm**: ajudar na sugestão de títulos

---

## Usos na escrita: exemplos de prompts {.center}

📌 **Revisão:**

> "Revise este parágrafo quanto a clareza, coerência e gramática. Aponte os problemas e sugira reescritas. Não reescreva o texto todo — apenas indique o que melhorar e como."

## {.center}

📌 **Planejamento:**

> "Preciso escrever um paper para o evento acadêmico X a partir do meu TCC. Leia o TCC em anexo [já publicado] e proponha uma estrutura com seções, subseções e estimativa de páginas por seção."

## {.center}

📌 **Brainstorm:**

> "A partir da estrutura e do TCC, proponha 3 títulos para o paper e 5 palavras-chave. Leve em consideração critérios de indexação de bases científicas."

---

## {.center}

⚠️ **Sempre verifique**: fontes, citações e dados gerados pela IA.

---

## Usos na escrita acadêmica {.center}

❌ O que **NÃO** fazer:

- Deixar a IA escrever o texto por você  
- Copiar e colar sem revisar  
- Não declarar o uso de IA

---

## Regra prática {.center}

> 🎯 **A IA auxilia, não substitui o pensamento crítico.**

---

## Regra prática {.center}

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

## Portaria CNPq  do CNPq: IA Generativa e Integridade {.center}

📜 **[Portaria CNPq nº 2.664, de 6 de março de 2026](http://memoria2.cnpq.br/web/guest/view/-/journal_content/56_INSTANCE_0oED/10157/23142775?COMPANY_ID=10132)** — Política de Integridade na Atividade Científica do CNPq

## {.center}

📌 **Art. 9º, inciso I** — Diretrizes de integridade na pesquisa:

> **c)** declarar o uso de ferramentas de Inteligência Artificial Generativa (IAG), de qualquer espécie e em qualquer fase da pesquisa (concepção, redação, análise de dados, submissão), especificando a ferramenta utilizada e a finalidade;

---

## ⚠️ O que a portaria **veda** {.center}

> **d)** é vedada a submissão de conteúdo gerado por IAG como se fosse de autoria humana, sendo os autores integralmente responsáveis pelo conteúdo final, inclusive por eventuais plágios ou imprecisões geradas pela IAG;

---

## ⚠️ O que a portaria **veda** {.center}

> **e)** é vedada a inserção de projetos de pesquisa de terceiros em ferramentas de IAG para elaboração de pareceres científicos;

> **f)** responsabilizar-se integralmente pelo conteúdo final da pesquisa, inclusive por eventuais plágios ou imprecisões geradas pela IAG.

---

## Portaria CNPq: o que muda na prática? {.center}

✅ **Declarar** sempre que usar IAG — em qualquer fase da pesquisa  
❌ **Nunca** submeter texto gerado por IA como se fosse seu  
❌ **Nunca** inserir projetos de terceiros em IAG para gerar pareceres  
✅ **Responsabilidade total** do autor sobre o conteúdo final

## 💡 Se a IA alucinou uma citação e você incluiu no texto, **a responsabilidade é sua.** {.center}

---

## Infrações e sanções {.center}

⚖️ A portaria classifica infrações por gravidade:

- **Leves**: sem dolo, sem prejuízo (advertência)  
- **Graves**: autoplágio; informação inconsistente no Lattes com efeito na avaliação (suspensão de bolsas, impedimento em editais)  
- **Gravíssimas**: fabricação/falsificação de dados, **plágio**, comercialização de autoria, condutas discriminatórias (revogação de fomento, devolução de recursos)

---

## 📌 Plágio — inclusive via IAG — é infração **gravíssima**. {.center}



---

## 3. Horizontes avançados {.center}

---

## Modelos abertos vs fechados: por que importa? {.center}

🔓 **Modelos abertos** são mais do que código gratuito:

- **Privacidade**: ninguém vê seus prompts ou documentos  
- **Autonomia**: você controla o modelo e os parâmetros  
- **Reprodutibilidade**: mesma versão, mesmo resultado  
- **Personalização**: crie personas e instruções permanentes

---

## Ollama: IA no seu computador {.center}

🦙 O **[Ollama](https://ollama.com)** permite rodar modelos abertos **localmente**:

- Funciona em Linux, Windows e macOS  
- Baixe modelos como `gemma3:4b` ou `phi3:mini` — sem internet  
- Use pelo app (interface gráfica) ou pelo terminal  
- Crie **Modelfiles** com instruções permanentes personalizadas

## 💡 É como ter um ChatGPT privado no seu computador — ninguém vê seus textos. {.center}

---

## Modelfile: seu assistente sob medida {.center}

Define instruções permanentes para o modelo — um "system prompt" que nunca se perde:

```
FROM gemma3:4b

SYSTEM """
Você é um assistente especializado em fichamentos
acadêmicos para estudantes e pesquisadores de
Humanidades e Ciências Sociais.

INSTRUÇÕES:
- Responda SEMPRE em português do Brasil.
- Ao receber um texto, produza um fichamento com:
  1. REFERÊNCIA completa (autor, título, local, ano)
  2. TEMA central em 1 frase
  3. ARGUMENTO PRINCIPAL em até 3 frases
  4. CONCEITOS-CHAVE (3 a 5 termos)
  5. CITAÇÕES RELEVANTES (até 3, com página)
  6. NOTAS CRÍTICAS: pontos fortes, lacunas,
     diálogo com outras obras
- NÃO invente informações nem citações.
- Se faltar informação, indique [não informado].
"""

PARAMETER temperature 0.2
PARAMETER num_ctx 4096
```

---

## Usando o Modelfile {.center}

```bash
# Salve o arquivo Modelfile em qualquer pasta
# Exemplo: ~/documentos/fichamento/Modelfile

cd ~/documentos/fichamento
ollama create assistente -f Modelfile
ollama run assistente
```

📌 Resultado: uma **versão local e personalizada** do modelo — ideal para fichamento, resumo e pesquisa.

---

## RAG: Geração Aumentada por Recuperação {.center}

📚 **RAG** (*Retrieval-Augmented Generation*) combina LLM com **busca em documentos**:

- O modelo **recupera trechos relevantes** de uma base de documentos  
- Gera a resposta **com base nas fontes recuperadas** — não apenas no treinamento  
- Reduz alucinações e permite **citar fontes**

---

## RAG na prática {.center}

🔧 Como funciona um sistema RAG:

1. Você carrega seus documentos (PDFs, artigos, relatórios)  
2. Os documentos são **indexados** e transformados em vetores  
3. Quando você faz uma pergunta, o sistema busca os trechos mais relevantes  
4. O LLM gera a resposta **apoiado nos seus documentos**

---

## Codex e agentes de IA {.center}

🔧 LLMs estão evoluindo de **geradores de texto** para **agentes que tomam decisões a usam ferramentas**:

- Modelos agora podem **chamar ferramentas**: buscar na web, ler arquivos, executar código, acessar APIs
- Exemplos: **Codex CLI** (OpenAI), **Claude Code** (Anthropic), **OpenCode** (Ollama local),
- Isso se desdobra em **agentes de IA**: sistemas autônomos que planejam e executam tarefas multi-etapas: **Hermes Agent** (Nous Research), **OpenClaw**

---

## Codex e agentes de IA {.center}

🔬 **Por que importa para a pesquisa?**

- Agentes podem **automatizar revisões de literatura** em bases de dados
- Podem **analisar corpora inteiros**, cruzar fontes, identificar padrões  
- Executam tarefas repetitivas (limpeza de dados, formatação, transcrição)  
- **Privacidade**: com modelos locais + agentes, seus dados nunca saem do computador

## 💡 O horizonte é promissor, mas ainda está em consolidação — **fica como convite para estudo futuro**. {.center}

---

## Encerramento {.center}

🎯 **Balanço da oficina:**

- IA generativa é uma **ferramenta poderosa**, mas com **limitações reais**  
- Chatbots web são ótimos para exploração, estudo e revisão — **use com crítica e declarando o uso**  
- O horizonte avançado (Ollama, RAG, agentes) amplia possibilidades de **privacidade e autonomia**

---

## Quando usar cada ferramenta? {.center}

| Situação | Recomendação |
|:---------|:-------------|
| Exploração de ideias, brainstorming | Chatbot web |
| Revisão gramatical, tradução | Chatbot web |
| Fichamento e resumo de textos | NotebookLM ou chatbot web |

---

## Quando usar cada ferramenta? {.center}

| Situação | Recomendação |
|:---------|:-------------|
| Análise de documentos sensíveis | Modelo local (Ollama) |
| Reprodutibilidade em pesquisa | Modelo local (Ollama) ou RAG |
| Pesquisa avançada em corpora | RAG + modelo local |

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
- [NotebookLM](https://notebooklm.google.com)  
- [Repositório da oficina](https://github.com/ericbrasiln/oficina-ia-unilab)  
- [2shdufba — oficina anterior](https://github.com/ericbrasiln/2shdufba)

---

## Obrigado! {.center}

Prof. Eric Brasil

ericbrasil.com.br | profericbrasil@gmail.com

UNILAB • PPGIHD/UFRRJ • LABHDUFBA
