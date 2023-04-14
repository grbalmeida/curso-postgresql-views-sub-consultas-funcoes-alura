# Equivalentes

### Obtém os cursos com mais alunos utilizando HAVING

```sql
SELECT
    curso.nome,
    COUNT(aluno_curso.aluno_id) numero_alunos
FROM curso
JOIN aluno_curso ON aluno_curso.curso_id = curso.id
GROUP BY 1
HAVING COUNT(aluno_curso.aluno_id) > 2
ORDER BY numero_alunos DESC;
```

### Obtém os cursos com mais alunos utilizando subquerie

```sql
SELECT
    t.curso,
    t.numero_alunos
FROM (
    SELECT
        curso.nome AS curso,
        COUNT(aluno_curso.aluno_id) numero_alunos
    FROM curso
    JOIN aluno_curso ON aluno_curso.curso_id = curso.id
    GROUP BY 1
) AS t
WHERE t.numero_alunos > 2
ORDER BY t.numero_alunos DESC;
```