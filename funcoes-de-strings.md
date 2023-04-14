# Funções de strings

### Concatenação do nome e sobrenome do aluno

```sql
SELECT (primeiro_nome || ' ' || ultimo_nome) AS nome_completo FROM aluno;
```

### Concatenação do nome Vinicius com sobrenome Dias

```sql
SELECT 'Vinicius' || ' ' || 'Dias';
-- Vinicius Dias
```

### Concatenação do nome Vinicius com NULL

```sql
SELECT 'Vinicius' || ' ' || NULL;
-- [null]
```

### Concatenação do nome Vinicius com NULL utilizando função CONCAT

```sql
SELECT CONCAT('Vinicius', ' ', NULL);
-- Vinicius 
```

### Concatenação do nome Vinicius com NULL e sobrenome Dias

```sql
SELECT CONCAT('Vinicius', NULL, 'Dias');
-- ViniciusDias
```

### Concatenação do nome com sobrenome e conversão para letras maiusculas

```sql
SELECT UPPER(CONCAT('Vinicius', ' ', 'Dias'));
-- VINICIUS DIAS
```

### Remoção de espaços do inicio e do fim com TRIM

```sql
SELECT TRIM(UPPER(CONCAT('Vinicius', ' ', 'Dias')) || ' ');
-- VINICIUS DIAS
```