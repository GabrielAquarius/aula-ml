# Relatorio de Comparacao: chamados-r1 vs chamados-r2

## Alteracao Realizada
- Dataset (v1 -> v2): Correcao do rotulo do chamado 006 (bloqueio de acesso) de comum para urgente em data/chamados.csv, mantendo data/split.csv inalterado.

## Tabela de Metricas (Particao de Teste Fixa)

| Metrica | Modelo chamados-r1 (dados-v1) | Modelo chamados-r2 (dados-v2) |
| :--- | :---: | :---: |
| Acuracia Geral | 0.75 (3/4) | 1.00 (4/4) |
| Recall (urgente) | 0.50 (1/2) | 1.00 (2/2) |
| Recall (comum) | 1.00 (2/2) | 1.00 (2/2) |

## Verificacao de Integridade (modelo-r1)
Os hashes SHA-256 verificados no clone limpo (aula-ml-restauracao) coincidem integralmente com os registrados em reports/modelo.json da tag modelo-r1.

## Decisao
Aceitar chamados-r2 (modelo-r2): a correcao do rotulo elevou o recall da classe urgente de 50% para 100% sem degradar o recall da classe comum (mantido em 100%), utilizando exatamente a mesma particao de teste.
