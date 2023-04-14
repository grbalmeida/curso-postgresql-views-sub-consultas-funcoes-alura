# Preparando dados

### Carga da tabela aluno

```sql
INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento)
VALUES
('Vinicius', 'Dias', '1997-10-15'),
('Patrícia', 'Freitas', '1996-10-25'),
('Diogo', 'Oliveira', '1994-08-27'),
('Maria', 'Rosa', '1985-01-01');
```

### Carga da tabela categoria

```sql
INSERT INTO categoria (nome) VALUES ('Banco de dados');
```

### Carga da tabela curso

```sql
INSERT INTO curso (nome, categoria_id)
VALUES
('HTML', 2),
('CSS', 2),
('JS', 2),
('PHP', 1),
('C++', 1),
('MySQL', 8),
('Oracle', 8),
('SQL Server', 8),
('SQLite', 8),
('Pandas', 3),
('Machine Learning', 3),
('Power BI', 3);
```

### Carga da tabela aluno_curso

```sql
INSERT INTO aluno_curso
VALUES
(11, 11),
(11, 18),
(12, 11),
(12, 12),
(13, 11),
(13, 10),
(14, 11),
(14, 13),
(14, 12);
```