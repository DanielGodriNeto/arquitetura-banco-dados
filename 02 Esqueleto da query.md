# Esqueleto da query

Ordem em que se ESCREVE:
```sql
SELECT   colunas / cálculos que quero ver
FROM     tabela
JOIN     outra tabela ON regra de ligação
WHERE    filtro de LINHAS
GROUP BY forma grupos
HAVING   filtro de GRUPOS
ORDER BY ordena
LIMIT    corta N linhas
```
Memorize: **S F J W G H O L**.

Ordem em que o SQL EXECUTA: FROM/JOIN -> WHERE -> GROUP BY -> COUNT/SUM -> HAVING -> SELECT -> ORDER BY -> LIMIT.
O SELECT é como o "print": mostra o que sobrou. A tabela original nunca muda; cada etapa gera um resultado temporário.

Sinais no enunciado:
- "para cada ..." / "total por ..." -> [[04 GROUP BY]]
- "maior que / menor que" -> [[03 WHERE vs HAVING]]
- "os N mais caros" -> [[06 ORDER BY e LIMIT]]
- duas tabelas envolvidas -> [[05 JOIN]]
