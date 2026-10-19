# Falta estudar

- Ciclo 3 não foi feito: COUNT DISTINCT com JOIN (Q2) e SUM com cálculo (Q5). Reler [[07 COUNT e SUM]] e refazer à mão:
  1. Quantas linhas tem o montinho do cliente 501 depois de juntar PEDIDO e ITEM_PEDIDO? (4) E o do 502? (1)
  2. `COUNT(*)` por cliente na junção: 501 -> 4, 502 -> 1.
  3. "Quantos **pedidos** cada cliente fez": `COUNT(*)` só em PEDIDO, com `GROUP BY ID_CLIENTE` (parecida com a opção D da Q2).
  4. Soma de QUANTIDADE por cliente: JOIN PEDIDO + ITEM_PEDIDO, `SUM(IP.QUANTIDADE)`, `GROUP BY P.ID_CLIENTE`.
- Simulado final: refazer as 5 questões do PDF sem olhar o gabarito ([[08 Questões do PDF resolvidas]]).
- LEFT JOIN: treinar mais um pouco ([[05 JOIN]]).

## Erros do PDF (não é você)
- Q2: o resultado esperado diz 501 -> 3 produtos distintos, mas pelos dados são 4 (101, 102, 103, 104). Marcar B mesmo assim.
- Q5: pedido 3 soma 1030 pelos itens (2x240 + 0.5x1100), mas VALOR_TOTAL em PEDIDO é 1340. O PDF admite.
