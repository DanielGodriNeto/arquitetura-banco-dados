# WHERE vs HAVING

- **WHERE**: condição sobre **uma linha** (preço > 500, minuto > 50, categoria = 2). Roda ANTES de agrupar.
- **HAVING**: condição sobre **um total** (COUNT, SUM, AVG). Roda DEPOIS de agrupar.

`WHERE COUNT(*) > 1` não funciona: o COUNT ainda não existe quando o WHERE roda.

```sql
SELECT ID_CLIENTE, COUNT(*)
FROM PEDIDO
GROUP BY ID_CLIENTE
HAVING COUNT(*) > 1;      -- clientes com mais de 1 pedido
```
Truque de prova: `HAVING` sem `GROUP BY` e filtro de linha comum em HAVING = opção errada (ex.: Questão 1, opção C).
Ver [[04 GROUP BY]].
