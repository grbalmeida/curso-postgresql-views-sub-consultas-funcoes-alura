# Conversão de dados

### Conversão da data atual para o dia de hoje (14/04/2023)

```sql
SELECT TO_CHAR(NOW(), 'DD');
-- 14
```

### Conversão da data atual para o dia e mês (14/04/2023)

```sql
SELECT TO_CHAR(NOW(), 'DD/MM');
-- 14/04
```

### Conversão da data atual para o formato brasileiro (14/04/2023)

```sql
SELECT TO_CHAR(NOW(), 'DD/MM/YYYY');
-- 14/04/2023
```

### Obtendo o mês por extenso (14/04/2023)

```sql
SELECT TO_CHAR(NOW(), 'DD, MONTH , YYYY');
-- 14, APRIL    , 2023
```

### Conversão do número 128.3 para 2 digitos depois do ponto

```sql
SELECT TO_CHAR(128.3::REAL, '999D99');
-- 128,30
```