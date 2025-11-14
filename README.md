# Otimização para Sistema de Apoio à Decisão Clínica: Uma Proposta Embarcada com SLM e XAI
Este repositório contém o código e a Prova de Conceito (PoC) da nossa pesquisa, que propõe uma arquitetura inovadora para enfrentar as barreiras de implementação dos Sistemas de Apoio à Decisão Clínica (SADC).

➡️**Artigo Completo (PDF):** [Acesse o Artigo Aceito no Congresso Pan-Amazônico de Oncologia](https://github.com/gabrielqueeiroz/aps-poc/blob/2b7a9360eac354d95c8996c05ea87b2f6bb68101/gabriel-pan-amazonico2.pdf)
➡️**Poster Apresentado:** [Acesse o Artigo Aceito no Congresso Pan-Amazônico de Oncologia](https://github.com/gabrielqueeiroz/aps-poc/blob/main/Poster-Pan-Amazonico-1.pdf)

## 💡 O Problema: Por que os SADCs falham na implementação?
Apesar de seu valor, a implementação de SADCs em Contextos de Recursos Limitados enfrenta desafios significativos. Entre as barreiras mais comuns, destacam-se:
* Altos Custos e Infraestrutura Precária de TI.
* Baixa Confiança dos profissionais de saúde nos sistemas de IA.
* Complexidade de Interpretação de resultados e falta de transparência.

## 🛠️ Nossa Solução: Uma Arquitetura Embarcada, Segura e Transparente
Nossa arquitetura de SADC Embarcado de baixo custo (Edge AI) ataca o problema da infraestrutura e custos por meio de um dispositivo de baixo custo (Raspberry Pi). O pipeline de processamento é composto por tecnologias estratégicas:
- **Coleta de Dados Eficiente:** Utilizamos um **Small Language Model (SLM)**, como o TinyLlama, para extrair sintomas de relatos de pacientes com eficiência, uma alternativa viável a modelos maiores (LLMs).
- **Classificação e Padronização:** O modelo **Random Forest** classifica a especialidade médica mais adequada, utilizando dados padronizados pela ontologia médica **CIAP-2.**
- **Transparência Garantida (XAI):** Aplicamos a técnica SHAP (SHapley Additive exPlanations) para gerar uma justificativa clara e visual para cada recomendação. Isso promove a confiança dos usuários e supera uma das principais barreiras de adoção.

## ✨ Contribuição Principal
O principal mérito deste trabalho reside na demonstração metodológica de que é possível construir um pipeline de processamento de dados convergindo SLM, XAI e Arquitetura Embarcada. 

Esta convergência ataca as lacunas não resolvidas da literatura, representando um passo significativo em direção a uma solução prática e acessível para o encaminhamento de pacientes na Atenção Primária à Saúde (APS) em ambientes com recursos limitados, tornando a IA viável por ser baixo custo, local e transparente.

## 💻 Como Reproduzir
Após clonar o projeto, executar o comando
```bash
docker compose up
```
Após isso, você pode executar o notebook normalmente.
