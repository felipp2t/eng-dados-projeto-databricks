# 🔄 Pipeline de Dados

## 📌 Visão Geral

O pipeline desenvolvido no Databricks foi criado utilizando a arquitetura Medalhão com múltiplas etapas de processamento.

O fluxo do pipeline ocorre de forma sequencial através de Jobs & Pipelines.

---

## 🚀 Fluxo do Projeto

```text
Banco de Dados
      ↓
Landing
      ↓
Bronze
      ↓
Silver
      ↓
Gold
```

---

## 🟢 Etapa Landing

Na etapa Landing ocorre a ingestão inicial dos dados.

Os dados são extraídos da fonte original e armazenados em arquivos:

- CSV
- JSON

Essa camada preserva os dados originais sem transformação.

---

## 🥉 Etapa Bronze

Na camada Bronze os arquivos são lidos e convertidos para o formato Delta Lake.

Objetivos da camada:

- armazenamento bruto
- ingestão no Lakehouse
- rastreabilidade dos dados

---

## 🥈 Etapa Silver

Na camada Silver são aplicadas regras de Data Quality.

Principais tratamentos realizados:

- remoção de valores inválidos
- padronização
- validação dos dados
- limpeza de inconsistências

---

## 🥇 Etapa Gold

A camada Gold é responsável pela estrutura analítica do projeto.

Nesta etapa são criadas:

- tabelas fato
- tabelas dimensão
- dados preparados para análise

---

## ⚙️ Automação

Todas as etapas do pipeline foram automatizadas utilizando Jobs & Pipelines do Databricks.

A execução ocorre de maneira sequencial garantindo:

- integridade
- organização
- confiabilidade
- automação do fluxo