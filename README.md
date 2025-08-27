# 📌 Projeto: Pipeline de Dados no Azure

## 📖 Descrição
Este projeto implementa um **pipeline de dados no Azure**, com foco na ingestão, preparação e transformação de dados em um ambiente de **Data Engineering moderno**.  

Ele foi desenvolvido como parte de um **laboratório prático da certificação DP-203 (Azure Data Engineer Associate)**, utilizando os serviços do **Azure Synapse Analytics** e **Data Lake Storage**.

O objetivo é demonstrar, de forma prática, como configurar fluxos de dados para carregar, transformar e disponibilizar informações de forma escalável, segura e integrada.

O pipeline realiza a comparação de um registro específico com uma base de dados maior para identificar se ele já existe.
- Fontes de dados: importa informações de duas origens — uma tabela no Data Warehouse e um arquivo CSV.
- Coleta e transformação: os dados são unificados e passam por uma etapa de transformação, onde o registro da tabela do Data Warehouse é comparado com os registros do arquivo CSV.
- Validação: nessa etapa, é verificado se o registro já está presente na base maior.
- Exportação: o resultado final é gravado em uma tabela externa para consulta e uso posterior.

---

## ⚙️ Tecnologias Utilizadas
- **Azure Synapse Analytics** → Criação e orquestração do pipeline de dados  
- **Azure Data Lake Storage** → Armazenamento dos arquivos de entrada e dados preparados  
- **PowerShell** → Automação de setup inicial  
- **Git** → Versionamento e gerenciamento do repositório  
- **SQL** → Transformação e manipulação de dados dentro do Synapse  

---

## 🚀 Etapas Implementadas

### 🔹 1. Configuração do Ambiente
- Clonagem do repositório oficial de laboratórios **DP-203**  
- Execução de scripts de setup (`setup.ps1`) para provisionar os recursos necessários  

### 🔹 2. Criação do Pipeline no Synapse
- Desenvolvimento do fluxo de dados **LoadProducts**  
- Definição de **serviços vinculados (Linked Services)** para integração segura com o Data Lake  
- Configuração de pastas de preparo no storage:  
  - `container = files`  
  - `diretório = stage_products`  

### 🔹 3. Transformação de Dados
- Definição de mapeamento entre origem (arquivos no Data Lake) e destino (tabelas no Synapse)  
- Aplicação de regras de transformação e limpeza  

### 🔹 4. Execução e Validação
- Rodagem do pipeline para ingestão dos dados  
- Validação por meio de **consultas SQL** no Synapse  
- Armazenamento dos resultados prontos para análises posteriores  

---

## 📊 Benefícios do Projeto
✔️ Demonstra boas práticas de **Data Engineering em nuvem**  
✔️ Integra diferentes serviços do Azure em um fluxo orquestrado  
✔️ Facilita a compreensão de pipelines de dados escaláveis  
✔️ Serve como base de estudo para certificações como **DP-203**  

---

## 📸 Exemplos
O projeto inclui capturas de tela que ilustram:
- A configuração do fluxo de dados  
- A execução e monitoramento do pipeline no Synapse  
- Os resultados carregados no ambiente de análise  
