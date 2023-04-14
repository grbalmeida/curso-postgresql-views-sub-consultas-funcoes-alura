# Criando uma view

### View que lista a quantidade de cursos por categoria

```sql
CREATE VIEW vw_cursos_por_categoria AS SELECT categoria.nome AS categoria,
        COUNT(curso.id) AS numero_cursos
    FROM categoria
    JOIN curso ON curso.categoria_id = categoria.id
GROUP BY categoria;
```

### Consulta na view vw_cursos_por_categoria

```sql
SELECT * FROM vw_cursos_por_categoria;
```

| categoria         | numero_cursos |
| ----------------- | ------------- |
| UX & Design       | 1             |
| Devops            | 1             |
| Mobile            | 1             |
| Inovação e Gestão | 1             |
| Banco de dados    | 4             |
| Data Science      | 4             |
| Front-End         | 4             |
| Programação       | 3             |

### Filtrando dados de uma view

```sql
SELECT categoria
FROM vw_cursos_por_categoria
WHERE numero_cursos >= 3;
```

| categoria      |
| -------------- |
| Banco de dados |
| Data Science   |
| Front-End      |
| Programação    |

### View que lista todos os cursos da categoria Programação

```sql
CREATE VIEW vw_cursos_programacao AS SELECT nome FROM curso WHERE categoria_id = (SELECT id FROM categoria WHERE nome = 'Programação');
```

### Consulta na view vw_cursos_programacao

```sql
SELECT * FROM vw_cursos_programacao;
```

| nome |
| ---- |
| Java |
| PHP  |
| C++  |