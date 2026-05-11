# 🏗️ Arquitetura Medalhão

## 📌 O que é a Arquitetura Medalhão?

A Arquitetura Medalhão (Medallion Architecture) é um modelo utilizado em projetos de Engenharia de Dados para organizar o fluxo de transformação dos dados em camadas.

Seu principal objetivo é melhorar:

- qualidade dos dados
- organização
- governança
- desempenho
- confiabilidade

---

## 📚 Estrutura das Camadas

A arquitetura utilizada no projeto segue o fluxo:

```text
Landing → Bronze → Silver → Gold
```

Cada camada possui uma responsabilidade específica dentro do pipeline de dados.

---

## 🟢 Landing

A camada Landing é responsável pela ingestão inicial dos dados.

Nessa etapa os dados são extraídos da fonte original e armazenados sem alterações.

Os arquivos podem estar nos formatos:

- CSV
- JSON

---

## 🥉 Bronze

A camada Bronze armazena os dados brutos no formato Delta Lake.

Nesta etapa:

- os dados ainda não são tratados
- o objetivo é preservar os dados originais
- ocorre a ingestão inicial no Lakehouse

---

## 🥈 Silver

A camada Silver é responsável pela qualidade e tratamento dos dados.

Nesta etapa são aplicados:

- limpeza
- validações
- padronização
- remoção de inconsistências
- regras de negócio

O objetivo é transformar os dados em informações confiáveis.

---

## 🥇 Gold

A camada Gold representa os dados refinados para análise.

Nesta etapa são criadas:

- tabelas dimensionais
- tabelas fato
- estruturas analíticas

A modelagem utilizada segue conceitos de Ralph Kimball.

---

## 🚀 Benefícios da Arquitetura

- Melhor organização do pipeline
- Facilidade de manutenção
- Separação das responsabilidades
- Maior qualidade dos dados
- Escalabilidade
- Melhor governança