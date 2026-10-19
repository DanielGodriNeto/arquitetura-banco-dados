# COUNT e SUM

- `COUNT(*)` conta linhas do grupo. `COUNT(coluna)` conta linhas com a coluna preenchida.
- `COUNT(DISTINCT coluna)` conta valores **diferentes**. Sinal no enunciado: "**distintos**".
- `SUM(coluna)` soma. `SUM(QUANTIDADE * PRECO_VENDA)` soma o produto linha a linha (valor do pedido).
- `AVG` = média (errado quando o enunciado pede soma).
- `AS` só dá apelido à coluna do resultado.

```sql
SELECT P.ID_CLIENTE, COUNT(DISTINCT IP.ID_PRODUTO) AS TOTAL_PRODUTOS_DISTINTOS
FROM PEDIDO P
JOIN ITEM_PEDIDO IP ON P.ID_PEDIDO = IP.ID_PEDIDO
GROUP BY P.ID_CLIENTE;
```
Exemplo de por que DISTINCT: cliente que comprou o mesmo produto em 2 pedidos tem 2 linhas, mas 1 produto distinto.

```sql
SELECT ID_PEDIDO, SUM(QUANTIDADE * PRECO_VENDA) AS VALOR_CALCULADO
FROM ITEM_PEDIDO
GROUP BY ID_PEDIDO;
```
Ver [[04 GROUP BY]] e [[05 JOIN]].
