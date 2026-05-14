# 📌 Projeto: NotebookLM - Fundamentos da Engenharia de Dados

Este projeto consiste na criação de um caderno temático utilizando o NotebookLM, uma ferramenta de IA da Google para organização, síntese e curadoria de conhecimento. O tema escolhido foi **Fundamentos da Engenharia de Dados**.

---

## 🎯 Contexto e Objetivos

### Tema escolhido:
**Fundamentos da Engenharia de Dados**

A Engenharia de Dados é uma das áreas mais estratégicas do mercado de tecnologia atualmente, responsável por construir e manter a infraestrutura que permite a coleta, armazenamento, processamento e disponibilização de dados para análise e tomada de decisão.

### Objetivos de estudo:
- Compreender o papel e as responsabilidades de um Engenheiro de Dados
- Dominar os conceitos de pipelines de dados (ETL/ELT)
- Conhecer as principais ferramentas do ecossistema de dados
- Entender arquiteturas de dados modernas (Data Lake, Data Warehouse, Lakehouse)
- Aprender sobre governança, qualidade e segurança de dados

---

## 📚 Curadoria de Fontes

Lista de fontes utilizadas para alimentar o NotebookLM:

| Fonte | Tipo | Link |
|-------|------|------|
| 1. "The Data Engineering Cookbook" - Andreas Kretz | E-book | https://github.com/andkret/Cookbook |
| 2. Artigo: "What is Data Engineering?" - Datacamp | Artigo | https://www.datacamp.com/blog/what-is-data-engineering |
| 3. "Fundamentals of Data Engineering" - Joe Reis & Matt Housley | Livro | https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/ |
| 4. Data Engineering Wiki | Wiki | https://github.com/DataEngineeringCommunity/DataEngineeringCommunity |
| 5. Documentação oficial - dbt | Documentação | https://docs.getdbt.com/docs/introduction |

---

## 🧪 Engenharia de Prompts e Cicatrizes

### Perguntas Estratégicas

| # | Pergunta | Objetivo |
|---|----------|----------|
| 1 | "Explique o que é Engenharia de Dados e qual a diferença para Análise de Dados e Ciência de Dados" | Diferenciar papéis |
| 2 | "Quais são as principais etapas de um pipeline de dados?" | Entender ETL/ELT |
| 3 | "Compare Data Lake, Data Warehouse e Lakehouse. Quais as vantagens e desvantagens?" | Arquiteturas |
| 4 | "Liste as ferramentas mais utilizadas em Engenharia de Dados e categorize por função" | Ferramentas |
| 5 | "O que é governança de dados e por que é importante?" | Governança |

### Variações de Prompts Testadas

| Prompt Original | Variação | Resultado |
|-----------------|----------|-----------|
| "O que é Engenharia de Dados?" | "Explique Engenharia de Dados para um iniciante, com analogias do mundo real" | Resposta mais didática e acessível |
| "Quais ferramentas de ETL?" | "Crie uma tabela comparativa das principais ferramentas de ETL com prós e contras" | Resposta mais estruturada e visual |
| "Explique Data Lake" | "Data Lake vs Data Warehouse: quadro comparativo com exemplos de uso" | Melhor para entender diferenças práticas |
| "O que é governança de dados?" | "Quais os pilares da governança de dados e como implementar na prática?" | Resposta mais acionável e aplicável |

### Troubleshooting (Dificuldades e Soluções)

| Dificuldade Encontrada | Solução Aplicada |
|------------------------|------------------|
| Respostas muito genéricas no primeiro prompt | Refinei o prompt adicionando "para iniciantes" ou "com exemplos práticos" |
| IA confundiu conceitos de Engenharia de Dados com Ciência de Dados | Adicionei contexto: "do ponto de vista da Engenharia de Dados" |
| Lista de ferramentas desatualizada | Solicitei "ferramentas mais usadas em 2024/2025" |
| Faltavam exemplos práticos | Adicionei "dê exemplos de casos de uso reais" ao prompt |
| Resposta muito longa e difícil de ler | Solicitei "responda em tópicos com no máximo 3 linhas por tópico" |

### Cicatrizes (Aprendizados sobre Prompts)

```txt
Cicatriz 1: Prompts vagos geram respostas vagas. Quanto mais contexto e especificidade, melhor a qualidade da resposta.
```

```txt
Cicatriz 2: Pedir um formato específico (tabela, tópicos, mapa mental) organiza o pensamento e facilita o estudo.
```

```txt
Cicatriz 3: A IA alucina menos quando você pede fontes ou "com base nas fontes fornecidas".
```

### Prompts Reutilizáveis que Funcionaram Melhor

```txt
1. "Com base nas fontes fornecidas, explique [CONCEITO] como se eu fosse um estagiário na área. Use analogias do mundo real e responda em até 5 tópicos principais."
```

```txt
2. "Crie uma tabela comparativa entre [TECNOLOGIA A] e [TECNOLOGIA B]. Colunas: critério, tecnologia A, tecnologia B, quando escolher cada uma."
```

```txt
3. "Atue como um Engenheiro de Dados sênior revisando o trabalho de um júnior. Liste os 5 erros mais comuns em [TÓPICO] e como corrigi-los."
```

---

## 📖 Miniguia de Estudo - Resultado Final

### Resumos Estruturados

#### 1. O que é Engenharia de Dados?

Engenharia de Dados é a área responsável por projetar, construir e manter a infraestrutura de dados. Envolve a coleta, armazenamento, processamento e disponibilização de dados de forma confiável, escalável e segura.

**Principais responsabilidades:**
- Construção de pipelines de dados (ETL/ELT)
- Gestão de bancos de dados e data warehouses
- Garantia de qualidade e governança
- Otimização de performance e custos
- Manutenção da disponibilidade dos dados

**Diferenças entre papéis:**

| Papel | Foco Principal |
|-------|----------------|
| **Engenheiro de Dados** | Infraestrutura, pipelines, disponibilidade |
| **Analista de Dados** | Consultas, dashboards, insights |
| **Cientista de Dados** | Modelagem, algoritmos, predições |

#### 2. Pipelines de Dados (ETL vs ELT)

| Abordagem | ETL | ELT |
|-----------|-----|-----|
| Ordem | Extração → Transformação → Carga | Extração → Carga → Transformação |
| Onde transforma | Antes do destino (staging area) | Dentro do destino (data warehouse) |
| Ideal para | Dados estruturados, conformidade, privacidade | Big Data, dados brutos, agilidade |
| Ferramentas | Informatica, Talend, AWS Glue | dbt, Snowflake, BigQuery, Databricks |

#### 3. Arquiteturas de Dados

| Arquitetura | Característica | Vantagem | Desvantagem |
|-------------|----------------|----------|--------------|
| **Data Lake** | Dados brutos, qualquer formato | Flexível, baixo custo | Pode virar "data swamp" |
| **Data Warehouse** | Dados estruturados, modelados | Performance, confiabilidade | Caro, inflexível |
| **Lakehouse** | Híbrido (flexibilidade + estrutura) | Melhor dos dois mundos | Tecnologia mais nova |

#### 4. Ferramentas do Ecossistema

| Categoria | Ferramentas |
|-----------|-------------|
| Orquestração | Apache Airflow, Prefect, Dagster, Mage |
| Processamento | Apache Spark, Apache Flink, dbt |
| Armazenamento (Lake) | AWS S3, Google Cloud Storage, Azure Blob |
| Armazenamento (Warehouse) | Snowflake, BigQuery, Redshift |
| Infraestrutura | Terraform, Docker, Kubernetes |
| Versionamento de Dados | dbt, LakeFS, DVC |

### Glossário de Conceitos

| Termo | Definição |
|-------|-----------|
| **ETL** | Processo de Extração, Transformação e Carga de dados |
| **ELT** | Processo de Extração, Carga e Transformação (transformação no destino) |
| **Data Lake** | Repositório de dados brutos em formato nativo |
| **Data Warehouse** | Repositório centralizado de dados estruturados e modelados |
| **Lakehouse** | Arquitetura que combina Data Lake e Data Warehouse |
| **Pipeline** | Conjunto de etapas para processamento de dados |
| **Orquestração** | Coordenação automatizada de tarefas de dados |
| **Governança** | Conjunto de políticas para gestão de dados |
| **Data Mesh** | Arquitetura descentralizada de dados por domínios |
| **Batch vs Streaming** | Processamento por lotes vs processamento em tempo real |
| **Data Swamp** | Data Lake sem governança, difícil de usar |
| **Schema** | Estrutura/organização dos dados (colunas, tipos) |

### Prompts Reutilizáveis para Estudos Futuros

```txt
Prompt para resumo de novo tópico:
"Com base nas fontes fornecidas, explique o conceito de [INSERIR TÓPICO] no contexto da Engenharia de Dados. Inclua: definição, importância, exemplos práticos e ferramentas relacionadas. Responda em até 5 tópicos."
```

```txt
Prompt para comparação:
"Crie uma tabela comparativa entre [TECNOLOGIA A] e [TECNOLOGIA B] considerando: caso de uso, vantagens, desvantagens e quando escolher cada uma. Formato: tabela com 4 linhas."
```

```txt
Prompt para troubleshooting:
"Estou com dificuldade em [DESCREVER DIFICULDADE]. Me explique como um engenheiro de dados experiente faria para resolver este problema. Liste o passo a passo."
```

```txt
Prompt para revisão:
"Atue como um tutor de Engenharia de Dados. Me faça 5 perguntas sobre [TÓPICO] para testar meu entendimento. Depois de cada resposta, me dê feedback."
```

---

## 🚀 Conclusão

Este projeto demonstrou o poder do NotebookLM como ferramenta de aprendizagem ativa, combinando curadoria de fontes, engenhagem de prompts e organização do conhecimento.

**Principais aprendizados:**
- A qualidade da resposta da IA está diretamente ligada à qualidade do prompt
- Múltiplas fontes de qualidade geram respostas mais ricas e precisas
- O refinamento de prompts (iteração) é essencial para extrair o melhor da IA
- Documentar as "cicatrizes" (dificuldades) é tão importante quanto documentar os acertos
- Pedir formatos específicos (tabelas, tópicos) melhora a usabilidade do conteúdo

**Valor para o portfólio:**
Este projeto demonstra competências valorizadas pelo mercado:
✅ Pensamento crítico e curadoria de informação
✅ Engenharia de prompts e interação com IA
✅ Organização e estruturação do conhecimento
✅ Capacidade de sintetizar informações complexas
✅ Documentação de processo e aprendizado contínuo

---

> 🏠 [Voltar ao índice](../README.md)