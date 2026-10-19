# Tabelas do PDF

**PRODUTO**: ID_PRODUTO (PK), NOME_PRODUTO, PRECO_UNITARIO, ID_CATEGORIA (FK)
**CATEGORIA**: ID_CATEGORIA (PK), NOME_CATEGORIA
**PEDIDO**: ID_PEDIDO (PK), DATA_PEDIDO, ID_CLIENTE, VALOR_TOTAL
**ITEM_PEDIDO**: ID_PEDIDO (PK, FK), ID_PRODUTO (PK, FK), QUANTIDADE, PRECO_VENDA

## PRODUTO
| ID | NOME | PRECO | CAT |
|---|---|---|---|
| 101 | Laptop X | 4500 | 1 |
| 102 | Mouse G | 50 | 2 |
| 103 | Teclado M | 120 | 2 |
| 104 | Cabo ethernet | 2200 | 1 |
| 105 | Monitor LED | 800 | 3 |

## CATEGORIA
1 Eletrônicos, 2 Periféricos, 3 Monitores, 4 Softwares (sem produto)

## PEDIDO
| ID | DATA | CLIENTE | VALOR_TOTAL |
|---|---|---|---|
| 1 | 2025-09-01 | 501 | 4550 |
| 2 | 2025-09-02 | 502 | 800 |
| 3 | 2025-09-03 | 501 | 1340 |

## ITEM_PEDIDO
| PEDIDO | PRODUTO | QTD | PRECO_VENDA |
|---|---|---|---|
| 1 | 101 | 1 | 4500 |
| 1 | 102 | 1 | 50 |
| 2 | 105 | 1 | 800 |
| 3 | 103 | 2 | 240 |
| 3 | 104 | 0.5 | 1100 |

Conceitos: **tabela** = planilha, **coluna** = campo, **linha** = registro. O que vem no `FROM` é sempre uma tabela.
PK identifica a linha. FK aponta para a PK de outra tabela (é a "ponte" do [[05 JOIN]]).

Erros do PDF: ver [[10 Falta estudar]].
