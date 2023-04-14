# Operador IN

### Obtém os cursos da categoria 1 e 2 sem o operador IN

```sql
SELECT * FROM curso WHERE categoria_id = 1 OR categoria_id = 2;
```

### Obtém os cursos da categoria 1 e 2 com o operador IN

```sql
SELECT * FROM curso WHERE categoria_id IN (1, 2);
```