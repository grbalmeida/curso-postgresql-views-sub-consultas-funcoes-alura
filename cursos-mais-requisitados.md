# Cursos mais requisitados

### Obtém o nome do curso e quantidade de alunos matriculados, ordenando pelo numero de alunos

```sql
SELECT
    curso.nome,
    COUNT(aluno_curso.aluno_id) numero_alunos
FROM curso
JOIN aluno_curso ON aluno_curso.curso_id = curso.id
GROUP BY 1
ORDER BY numero_alunos DESC;
```

### Obtém o curso com mais alunos

```sql
SELECT
    curso.nome,
    COUNT(aluno_curso.aluno_id) numero_alunos
FROM curso
JOIN aluno_curso ON aluno_curso.curso_id = curso.id
GROUP BY 1
ORDER BY numero_alunos DESC
LIMIT 1;
```

### Obtém o nome e a quantidade de cursos das categorias

```sql
SELECT
    categoria.nome,
    COUNT(curso.id) numero_cursos
FROM categoria
JOIN curso ON curso.categoria_id = categoria.id
GROUP BY 1
ORDER BY numero_cursos DESC;
```

### Obtém a categoria mais requisitada

```sql
SELECT
    categoria.nome,
    COUNT(curso.id) numero_cursos
FROM categoria
JOIN curso ON curso.categoria_id = categoria.id
GROUP BY 1
ORDER BY numero_cursos DESC
LIMIT 1;
```