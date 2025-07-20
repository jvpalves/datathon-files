
# Aplicação de Inteligência Artificial em Recrutamento e Seleção

## Objetivo do Projeto  
Criar um sistema de recrutamento inteligente para:

- **Analisar currículos automaticamente**: Identificar os melhores talentos que se encaixam nos requisitos técnicos e comportamentais da vaga.

- **Verificar o "fit" cultural**: Entender se o candidato tem afinidade com o jeito de ser e trabalhar da empresa.

- **Prever o desempenho futuro**: Usar dados para identificar os candidatos com maior potencial de sucesso na função.

## Como a Inteligência Artificial é Usada

### 1. Entendendo os Currículos (Processamento de Linguagem Natural)
-   **Leitura de informações:** A IA lê os currículos e extrai dados importantes, como experiência profissional, formação e competências.
-   **Conversão de texto em números:** Para que o computador possa comparar, os textos são transformados em um formato numérico.
-   **Análise de compatibilidade:** O sistema calcula uma pontuação que mostra o quanto o currículo do candidato combina com a descrição da vaga.

### 2. Prevendo o Sucesso dos Candidatos
-   **Classificação inicial:** Um primeiro modelo classifica os candidatos de forma rápida, separando os que têm ou não o perfil para a vaga.
-   **Previsão avançada:** Um modelo mais potente é usado para analisar os detalhes e prever com mais precisão a chance de sucesso de cada candidato.
-   **Otimização:** Ajustamos os modelos constantemente para garantir que as previsões sejam as melhores possíveis.

## Ferramentas Utilizadas

-   **Python:** A principal linguagem de programação do projeto.
-   **Pandas e NumPy:** Para organizar, limpar e preparar os dados dos currículos.
-   **Scikit-learn:** Para criar e testar os modelos de Machine Learning.
-   **XGBoost:** Ferramenta para o nosso modelo de classificação mais avançado e preciso.
-   **NLTK e sentence_transformers:** Para a análise e interpretação dos textos dos currículos.
-   **Streamlit:** Para construir a interface web interativa do sistema, onde tudo acontece.

## Etapas do Projeto

-   **Preparação dos Dados:**
    -   Os currículos são importados e os dados são limpos e organizados para análise.
    -   Aplicamos técnicas para garantir que o modelo seja justo e não tenha viés.

-   **Criação dos Modelos de IA:**
    -   Os modelos são treinados e testados para garantir que funcionem corretamente.
    -   Analisamos o que o modelo considera mais importante para tomar suas decisões (ex: experiência, competências).

-   **Interface do Usuário:**
    -   Uma tela simples para que o recrutador possa enviar os currículos.
    -   Exibição clara da pontuação de cada candidato e das recomendações do sistema.
    -   Um painel para o administrador gerenciar as vagas e os perfis.

-   **Fluxo Automatizado:**
    -   Um processo automático e contínuo: o currículo entra, a IA analisa e o resultado sai rapidamente na tela.

---

## Como a IA Funciona

### 1. Análise de Texto
-   **Extração de Dados:** Identifica automaticamente informações chave nos currículos;
-   **Tradução para Números:** Converte textos em formato numérico para que possam ser analisados pelo algoritmo;
-   **Cálculo de Similaridade:** Compara o currículo com a vaga para medir a compatibilidade.

### 2. Modelos de Previsão
-   **Filtro Rápido:** Um modelo simples faz uma primeira triagem dos candidatos.
-   **Análise Profunda:** Um modelo avançado (XGBoost) prevê o potencial de sucesso do candidato com alta precisão.
-   **Ajuste Fino:** Os modelos são otimizados para entregar os melhores resultados.

## Tecnologias
-   **Python:** Linguagem principal do projeto.
-   **Pandas e NumPy:** Para manipulação e limpeza de dados.
-   **Scikit-learn e XGBoost:** Para criação dos modelos de Machine Learning.
-   **NLTK e sentence_transformers:** Para todo o processamento de texto.
-   **Streamlit:** Para a interface web interativa do sistema.

## Estrutura do Projeto
-   **Preparação:** Os dados dos currículos são coletados, limpos e balanceados para evitar viés.
-   **Modelagem:** Os modelos de IA são treinados, validados e interpretados.
-   **Interface:** Uma plataforma web permite o upload de currículos e a visualização clara dos resultados e scores.
-   **Automação:** Todo o processo, da entrada do currículo à análise, acontece de forma automática e integrada.

## Funcionalidades
- **Upload de Currículos:** Suporte para PDF, com parser inteligente para extração das informações.  
- **Análise de candidato:** Compatibilidade técnica, comportamental e _fit_ cultural com a vaga desejada.  
- **Previsão de Desempenho:** Score preditivo baseado no histórico de candidatos similares e resultados anteriores da empresa.

## Estrutura do Repositório
O repositório se divide em diversos arquivos e diretórios:

### 1. Notebooks Jupyter (.ipynb):

datathon.ipynb e model.ipynb: Incluem análise exploratória de dados, desenvolvimento e avaliação dos modelos de avaliação.

Scripts Python (.py):

cv_recomendation.py: Funções para recomendação de currículos.

### 2. Arquivos de Dados:

applicants.json, prospects.json, jobs.json: Arquivos JSON que contem dados de candidatos e vagas de emprego, e as prospecções

applicant_ids.pkl, job_data.pkl, vagas.pkl: Arquivos serializados para melhora de performance.

### 3. Modelos Treinados:

logistic_model.pkl, xgboost_model.pkl: Modelos de machine learning treinados com regressão logística e XGBoost.

### 4. Dependências:

requirements.txt: Lista de bibliotecas Python necessárias para executar o projeto.

### 5. Streamlit:

Dentro da pasta projeto é possível encontrar os scripts que estão sendo utilizados no server do streamlit e são responsáveis pelo funcionamento da aplicação.

- **Sub-estrutura:** 
  - Home.py (Responsável pelo início da aplicação e acesso às demais páginas da aplicação)
  - requirements.txt (lista de libs utilizadas)
  - utils.py (funções e base de dados mock para o funcionamento da aplicação)
  - pages (pasta de sub-páginas)
    - Candidatos.py: lista os candidatos - Admin
    - Criar_Vaga.py: abre formulário para criação de vagas - Admin
    - Detalhes_Candidato.py: mostra as informações detalhadas para cada candidato - Admin
    - Listar_Vagas.py: lista todas as vagas - Candidato ou Admin
    - Minhas_Candidaturas.py: mostra todas as aplicações em vagas - Candidato
    - Recomendacao_CVs.py: recomenda CVs após a criação de uma vaga - Admin
    - Recomendacao_Vagas.py: recomenda vagas com base no CV do usuário - Candidato
