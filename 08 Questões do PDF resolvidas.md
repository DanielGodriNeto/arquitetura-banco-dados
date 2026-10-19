# Questões do PDF resolvidas

| Q | Resposta | Por quê |
|---|---|---|
| 1 | **A** | JOIN + `WHERE preco < 1000`. B usa `>`, C usa HAVING sem GROUP BY e ID ambíguo, D filtra por categoria e não por preço. ([[05 JOIN]], [[03 WHERE vs HAVING]]) |
| 2 | **B** | `COUNT(DISTINCT IP.ID_PRODUTO)` com JOIN e GROUP BY por cliente. A sem DISTINCT, C soma quantidade, D conta pedidos. ([[07 COUNT e SUM]]) |
| 3 | **A** | `WHERE VALOR_TOTAL > 1000` direto em PEDIDO. B é o inverso (`< 1000`), C compara QUANTIDADE, D traz só o maior pedido. ([[03 WHERE vs HAVING]]) |
| 4 | **B** | JOIN + `ORDER BY preco DESC LIMIT 3`. A usa ASC, C usa TOP, D sem DESC. ([[06 ORDER BY e LIMIT]]) |
| 5 | **B** | `SUM(QUANTIDADE * PRECO_VENDA)` por pedido. A soma com `+`, C só copia VALOR_TOTAL, D usa AVG. ([[07 COUNT e SUM]]) |

Método para qualquer questão:
1. Olhar o FROM e abrir a tabela certa.
2. Ver sinais do enunciado ("para cada", "distintos", "mais caros").
3. Eliminar opções por: sinal trocado, ASC/DESC, função errada (AVG/COUNT no lugar de SUM), falta de DISTINCT, falta de JOIN, HAVING sem GROUP BY.
