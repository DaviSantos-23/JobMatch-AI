# JobMatch-AI

Sistema inteligente para automação da busca e análise de oportunidades
profissionais utilizando n8n e Inteligência Artificial.

O projeto automatiza a descoberta de vagas, estrutura os dados das
oportunidades, compara os requisitos com um currículo base, calcula um
Match Score, identifica lacunas de habilidades e gera uma versão
personalizada do currículo para as vagas com maior aderência.

---

## Sobre o projeto

Buscar vagas manualmente, analisar requisitos e adaptar o currículo para
cada oportunidade pode consumir bastante tempo.

O JobMatch-AI foi desenvolvido para automatizar esse processo.

A solução combina automação de workflows, APIs, Inteligência Artificial
Generativa e armazenamento estruturado para transformar uma busca manual
em um processo automatizado de análise e preparação para candidatura.

---

# Workflow

![Workflow](images/workflow.png)

# Google Sheets 

![Google Sheets](images/googlesheets1.png)
![Google Sheets](images/googlesheets2.png)

# Gif Funcionamento e CV Teste

![Gif Funcionamento e CV Teste](gifs/demo.gif)
![Gif Funcionamento e CV Teste](images/curriculobase.gif)

## Fluxo da solução

Schedule Trigger
       ↓
Busca de vagas
       ↓
Extração dos dados
       ↓
Filtragem das oportunidades
       ↓
Currículo base
       ↓
IA — Análise de compatibilidade
       ↓
Match Score
       ↓
Filtro de oportunidades
       ↓
IA — Adaptação do currículo
       ↓
Google Sheets

----

# Principais funcionalidades

Busca automatizada de oportunidades
Integração com API de vagas
Extração e estruturação dos dados
Filtragem de oportunidades
Análise de compatibilidade com currículo
Cálculo de Match Score
Identificação de gaps de habilidades
Seleção automática das vagas mais aderentes
Adaptação do currículo utilizando IA Generativa
Registro estruturado das oportunidades
Armazenamento dos resultados no Google Sheets

----

# Tecnologias utilizadas

Automação
n8n
Workflow Automation
Inteligência Artificial
Generative AI
LLM
AI Agents
APIs
JSearch API
RapidAPI
Dados
Google Sheets
Desenvolvimento
Python
JSON
APIs REST

----

# Arquitetura

              JobMatch AI
                   │
       ┌───────────┼───────────┐
       ↓           ↓           ↓
   Automação      IA          Dados
       │           │           │
      n8n         LLM      Google Sheets
       │           │
       ↓           ↓
      APIs    Match Score
       │           │
       └───────┬───┘
               ↓
        Currículo adaptado

----

# Match Score

Cada oportunidade é analisada considerando a compatibilidade entre os
requisitos da vaga e o currículo base.

A análise considera:

linguagens;
tecnologias;
ferramentas;
competências;
experiências;
projetos;
requisitos da oportunidade;
palavras-chave.

Vagas que atingem o percentual mínimo configurado seguem para a etapa
de adaptação do currículo.

----

# Adaptação do currículo

Após a aprovação pelo Match Score, a oportunidade é encaminhada para um
agente de IA responsável por adaptar o currículo.

A adaptação prioriza:

palavras-chave da vaga;
competências relevantes;
tecnologias solicitadas;
projetos relacionados;
experiências compatíveis.

O sistema não deve inventar experiências, cargos ou competências.

----

# Resultado

As oportunidades processadas são organizadas em uma estrutura contendo
informações como:

nome da vaga;
empresa;
link da oportunidade;
Match Score;
skills gap;
currículo adaptado.

Os resultados são registrados no Google Sheets para facilitar o
acompanhamento das oportunidades.

----

# Estrutura do projeto

JobMatch-AI/
│
├── docs/
│   ├── arquitetura.md
│   ├── fluxo.md
│   ├── regras-negocio.md
│   ├── match-score.md
│   └── adaptacao-curriculo.md
│
├── images/
│   ├── workflow-principal.png
│   ├── google-sheets.png
│   ├── match-score.png
│   └── curriculo-adaptado.png
│
├── gifs/
│   └── demo.gif
│
├── workflows/
│   └── jobmatch-ai.json
│
├── prompts/
│   ├── match-job.txt
│   └── adaptar-curriculo.txt
│
├── data/
│   └── exemplo-vagas.csv
│
├── .env.example
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt

-----

# Regras de negócio

O sistema segue algumas regras para garantir que os resultados sejam
relevantes e consistentes:

oportunidades abaixo do Match Score mínimo são descartadas;
somente vagas aprovadas seguem para adaptação do currículo;
o currículo adaptado deve permanecer fiel ao currículo base;
informações profissionais não devem ser inventadas;
palavras-chave relevantes da vaga podem ser priorizadas;
oportunidades processadas são armazenadas para acompanhamento.

----

# Objetivo profissional

O projeto foi desenvolvido como estudo prático de:

automação de processos;
integração entre APIs;
Inteligência Artificial Generativa;
agentes de IA;
análise semântica;
processamento de dados;
automação de workflows;
personalização de informações;
integração com ferramentas externas.

-----

Sistema inteligente para automação da busca e análise de oportunidades
profissionais utilizando n8n e Inteligência Artificial.

# Autor

Davi Santos.

Ciência da Computação | Python | IA Generativa | Automação | Dados | n8n