# Projeto Databricks — Arquitetura Medalhão

## 📌 Sobre o Projeto

Este projeto foi desenvolvido utilizando o Databricks Free Edition com arquitetura Medalhão (Medallion Architecture).

O objetivo é construir um pipeline de dados completo utilizando:

- Landing
- Bronze
- Silver
- Gold

com automação através de Jobs & Pipelines.

---

## 🏗️ Arquitetura Utilizada

O pipeline segue as etapas:

```text
Landing -> Bronze -> Silver -> Gold
```

### 🔹 Landing
Camada responsável pela ingestão dos dados brutos.

### 🔹 Bronze
Armazena os dados em formato Delta Lake.

### 🔹 Silver
Aplicação de Data Quality:
- Limpeza
- Validações
- Padronização

### 🔹 Gold
Modelagem dimensional para análises.

---

## ⚙️ Tecnologias Utilizadas

- Databricks
- Apache Spark
- Delta Lake
- Python (PySpark)
- GitHub
- MkDocs

---

## 📂 Estrutura do Projeto

```text
eng-dados-projeto-databricks/
│
├── notebooks/
├── docs/
├── README.md
└── mkdocs.yml
```

---

## 🚀 Fluxo do Pipeline

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

## 👨‍💻 Autor

Felipe Rosseto da Silva
Lucas Vitali Magenis

---

## 📚 Referências

- Databricks Documentation — https://docs.databricks.com/
- Apache Spark Documentation — https://spark.apache.org/docs/latest/
- Delta Lake Documentation — https://docs.delta.io/latest/
- MkDocs Documentation — https://www.mkdocs.org/
- Material for MkDocs — https://squidfunk.github.io/mkdocs-material/
- Kimball Group — https://www.kimballgroup.com/
