# Queries aninhadas ou subqueries

### Obtém os cursos de categorias que não possuem espaço

```sql
SELECT * FROM curso WHERE categoria_id IN (
    SELECT id FROM categoria WHERE nome NOT LIKE '% %'
);
```

### Obtém os cursos de categorias com a palavra "de"

```sql
SELECT * FROM curso WHERE categoria_id IN (
    SELECT id FROM categoria WHERE nome LIKE '% de %'
);
```