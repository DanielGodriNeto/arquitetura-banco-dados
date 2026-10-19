# JOIN

Une tabelas pela chave (FK = PK). Sem `ON`, juntaria tudo com tudo.

```sql
SELECT P.NOME_PRODUTO, C.NOME_CATEGORIA, P.PRECO_UNITARIO
FROM PRODUTO P
JOIN CATEGORIA C ON P.ID_CATEGORIA = C.ID_CATEGORIA
WHERE P.PRECO_UNITARIO < 1000;
```
- `P` e `C` são apelidos; `P.coluna` diz de qual tabela a coluna vem.
- O JOIN põe colunas lado a lado; o WHERE depois escolhe quais linhas ficam.

Tipos:
- `JOIN` (INNER): só o que casa nas duas.
- `LEFT JOIN`: tudo da esquerda + o que casar da direita (sem par = NULL). Ex.: `FROM CATEGORIA C LEFT JOIN PRODUTO P` mostra *Softwares* com NULL.
- `RIGHT JOIN`: tudo da direita.
- `FULL JOIN`: tudo dos dois lados.

Dica: a opção de prova com `FROM A, B WHERE A.id = B.id` também é um join válido (estilo antigo). Opção com `LEFT JOIN ... ON ID_CATEGORIA = ID_CATEGORIA` (sem prefixo) é ambígua = errada.
Voltar: [[02 Esqueleto da query]].
