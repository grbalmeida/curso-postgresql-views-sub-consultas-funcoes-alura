# Alunos em mais cursos

### Obtém o primeiro nome, ultimo nome e a quantidade de cursos que o aluno está matriculado, ordenando pela quantidade de cursos

```sql
SELECT
    aluno.primeiro_nome,
    aluno.ultimo_nome,
    COUNT(aluno_curso.curso_id) numero_cursos
FROM aluno
JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
GROUP BY 1, 2
ORDER BY numero_cursos DESC; 
```

### Obtém o aluno com mais cursos

```sql
SELECT
    aluno.primeiro_nome,
    aluno.ultimo_nome,
    COUNT(aluno_curso.curso_id) numero_cursos
FROM aluno
JOIN aluno_curso ON aluno_curso.aluno_id = aluno.id
GROUP BY 1, 2
ORDER BY numero_cursos DESC
LIMIT 1;
```