# GROUP BY

Forma **montinhos**, um por valor da coluna. Quem calcula é o COUNT/SUM/AVG, dentro de cada montinho.

```sql
SELECT ID_CLIENTE, COUNT(*) AS TOTAL_PEDIDOS
FROM PEDIDO
GROUP BY ID_CLIENTE;
```
Resultado: 501 -> 2, 502 -> 1.

Padrão "para cada X": X vai no SELECT **e** no GROUP BY; a função (SUM/COUNT) vai no SELECT.
Só aparece grupo que existe nas linhas: quem não tem linha não aparece com 0 (para isso, LEFT JOIN, ver [[05 JOIN]]).
Não confundir com ORDER BY ([[06 ORDER BY e LIMIT]]), que só muda a ordem e não junta linhas.
Se a pergunta não tem "para cada", "quantos" nem "total", normalmente não tem GROUP BY.
