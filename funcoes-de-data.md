# Funções de data

### Obtém a idade em anos + meses + dias

```sql
SELECT
    (primeiro_nome || ' ' || ultimo_nome) AS nome_completo,
    AGE(data_nascimento)
FROM aluno
LIMIT 1;
```

| nome_completo | age                     |
| ------------- | ----------------------- |
| João Silva    | 43 years 3 mons 13 days |

### Obtém a idade em anos

```sql
SELECT
    (primeiro_nome || ' ' || ultimo_nome) AS nome_completo,
    EXTRACT(YEAR FROM AGE(data_nascimento)) AS idade
FROM aluno
LIMIT 1;
```

| nome_completo | idade |
| ------------- | ----- |
| João Silva    | 43    |