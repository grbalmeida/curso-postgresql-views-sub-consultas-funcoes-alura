# Trabalhando na View

### Filtrando a view vw_cursos_programacao onde o nome do curso é PHP

```sql
SELECT * FROM vw_cursos_programacao WHERE nome = 'PHP';
```

### Join de uma tabela com uma view

```sql
SELECT
    categoria.id,
    vw_cursos_por_categoria.*
FROM vw_cursos_por_categoria
JOIN categoria ON categoria.nome = vw_cursos_por_categoria.categoria;
```

| id | categoria         | numero_cursos |
| -- | ----------------- | ------------- |
| 1  | Programação       | 3             |
| 2  | Front-End         | 4             |
| 3	 | Data Science      | 4             |
| 4	 | Devops            | 1             |
| 5	 | UX & Design       | 1             |
| 6	 | Mobile            | 1             |
| 7	 | Inovação e Gestão | 1             |
| 8	 | Banco de dados    | 4             |