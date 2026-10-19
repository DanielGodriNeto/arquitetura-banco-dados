# ORDER BY e LIMIT

- `ORDER BY coluna ASC` = do menor pro maior (padrão). `DESC` = do maior pro menor.
- `LIMIT n` corta nas n primeiras linhas; vem por último.
- "Os N **mais caros**" = `ORDER BY preco DESC LIMIT N`. "Mais baratos" = `ASC`.
- `LIMIT` sem `ORDER BY` NÃO garante nada (o SQL não promete ordem).
- `TOP 3` é de SQL Server, não é o padrão ANSI. `ORDER BY 2` ordena pela 2ª coluna, mas sem DESC é ascendente.

```sql
SELECT P.NOME_PRODUTO, P.PRECO_UNITARIO, C.NOME_CATEGORIA
FROM PRODUTO P
JOIN CATEGORIA C ON P.ID_CATEGORIA = C.ID_CATEGORIA
ORDER BY P.PRECO_UNITARIO DESC
LIMIT 3;
```
Conferir sempre: DESC para os maiores (erro comum de pressa: escrever ASC).
