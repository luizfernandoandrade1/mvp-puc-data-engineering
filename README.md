# MVP PUC — Pipeline Unificada BCB

Pipeline de dados unificado para ingestão, transformação e modelagem de dados públicos do **Banco Central do Brasil** (SCR e Desenrola Brasil) usando arquitetura medalhão (Bronze, Silver, Gold) sobre Databricks Lakehouse.

## Fonte de dados

- **SCR (Sistema de Informações de Crédito):** https://www.bcb.gov.br/pda/desig/scrdata_{ANO}.zip
- **Desenrola Brasil:** https://www.bcb.gov.br/pda/desig/desenrola/dados_desenrola.csv

## Arquitetura

| Camada | Descrição |
| --- | --- |
| Bronze | Ingestão raw com metadados de auditoria |
| Silver | Transformação, tipagem e padronização |
| Gold | Modelo dimensional (Star Schema) com dimensões e fatos |

## Estrutura

- `pipeline_unificada_bcb.ipynb` — Notebook com o pipeline completo
- `pipeline.png` — Diagrama da arquitetura
- `catalog.png` — Catálogo de dados
- `schedulers.png` — Agendamento de execução