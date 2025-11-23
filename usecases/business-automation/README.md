# Sumário
- [Sumário](#sumário)
  - [🥇 Automação de Negócios - Insights Competitivos](#-automação-de-negócios---insights-competitivos)
  - [🤔 O Problema](#-o-problema)
  - [🎯 Objetivo](#-objetivo)
  - [📈 Valor para o Negócio](#-valor-para-o-negócio)
  - [Arquitetura](#arquitetura)
  - [�‍💻👨‍💻 Laboratório Prático Passo a Passo](#-laboratório-prático-passo-a-passo)
  - [Demo Video](#demo-video)

## 🥇 Automação de Negócios - Insights Competitivos

<!--![image](https://github.ibm.com/skol/agentic-ai-client-bootcamp/assets/451557/b9fb42fc-4aa1-4010-b850-5c8f20e3e05a)-->
![image](assets/hypercar3.png)


## 🤔 O Problema

O departamento de vendas da **ABC Motors Corp** enfrentava desafios na preparação de propostas para sua nova linha de veículos de alto desempenho. Sempre que um novo modelo é lançado, a equipe de análise competitiva gasta muito tempo e recursos para gerar insights. Os principais problemas incluem:

- Pesquisas manuais atrasam decisões e reduzem a produtividade.
- Posicionamento fraco prejudica a diferenciação nas vendas.
- Resposta lenta às mudanças de mercado devido à falta de inteligência em tempo real.


## 🎯 Objetivo

A **ABC Motors Corp** planeja implementar um **Sistema de Inteligência Competitiva com IA** para automatizar a pesquisa de mercado e a análise de concorrentes. Esse sistema ajudará as equipes de vendas a:

- Identificar e posicionar rapidamente seus produtos frente aos concorrentes.
- Superar ineficiências da pesquisa manual e insights desatualizados.

O objetivo é criar um sistema habilitado por IA que ofereça:

- Extração de produtos do catálogo da empresa.
- Identificação e extração dos principais recursos de cada produto.
- Pesquisa de produtos concorrentes com base em atributos-chave.
- Geração de uma tabela de comparação competitiva (preço, recursos e diferenciais).
- Análise SWOT (Forças, Fraquezas, Oportunidades e Ameaças) para insights estratégicos.

Com isso, a empresa pretende acelerar processos de vendas, melhorar a precisão dos dados e permitir decisões mais rápidas e informadas.

## 📈 Valor para o Negócio

- Redução no tempo de pesquisa manual da concorrência.
- Atualizações automatizadas e em tempo real sobre o mercado.
- Melhora na eficácia do discurso de vendas.

## Arquitetura

Para agilizar a análise competitiva, projetamos um **Sistema de Automação Multi-Agente de IA** que extrai e analisa dados dos produtos a partir do [Catálogo de Produtos da ABC Motors Corp](../../anexos/businessautomation/ABC_Motor_Product_Catalog_ptbr.pdf)

A arquitetura inclui:

- **Agente de Produto**:  
  - Ponto de entrada para consultas.
  - Pesquisa produtos específicos e recupera detalhes estruturados do catálogo.
  - Delegação de tarefas ao Agente de Comparação.

- **Agente de Comparação**:  
  - Gerencia todo o processo de comparação.
  - Identifica URLs de produtos concorrentes.
  - Analisa ofertas, extrai insights e gera análise SWOT.
  - Apresenta resultados em tabela clara e estruturada.

Este sistema combina:
- **watsonx Orchestrate**: para extrair informações do catálogo e realizar comparações.
- **watsonx.ai (Agent Lab)**: para análises avançadas e geração de insights.

<img width="900" alt="Arquitetura do Sistema" src="assets/Business_Automation_Architecturem via assistente de chat do **watsonx Orchestrate**, automatizando a pesquisa competitiva, fortalecendo discursos de vendas e reduzindo esforço manual.

## 👩‍💻👨‍💻 Laboratório Prático Passo a Passo

👉 [Clique aqui](./hands-on-lab-buisness-automation.md) para implementar este caso de uso.

## Demo Video

Um vídeo de demonstração da solução está aqui:

[▶️ Assistir à demonstração do Automação de Negócios](https://bucket-wxo.s3.us-south.cloud-object-storage.appdomain.cloud/Business%20Automation%20Agente.mp4)
