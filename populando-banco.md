# Populando banco

### Tabela aluno

```sql
INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento) VALUES ('João', 'Silva', '1980-01-01');
INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento) VALUES ('Pedro', 'Santos', '1981-02-02');
INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento) VALUES ('Lucas', 'Oliveira', '1982-03-03');
INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento) VALUES ('Rafael', 'Souza', '1983-04-04');
INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento) VALUES ('Bruno', 'Costa', '1984-05-05');

INSERT INTO aluno (primeiro_nome, ultimo_nome, data_nascimento)
VALUES
('Ana', 'Pereira', '1985-06-06'),
('Isabela', 'Almeida', '1986-07-07'),
('Juliana', 'Ribeiro', '1987-08-08'),
('Camila', 'Rodrigues', '1988-09-09'),
('Larissa', 'Gomes', '1989-10-10'); 
```

### Tabela categoria

```sql
INSERT INTO categoria (nome)
VALUES
('Programação'),
('Front-End'),
('Data Science'),
('Devops'),
('UX & Design'),
('Mobile'),
('Inovação e Gestão');
```

### Tabela curso

```sql
INSERT INTO curso (nome, categoria_id)
VALUES
('Java', 1),
('React', 2),
('PostgreSQL', 3),
('Git', 4),
('Figma', 5),
('React Native', 6),
('Scrum', 7);
```

### Tabela aluno_curso

```sql
INSERT INTO aluno_curso (aluno_id, curso_id)
VALUES
(1, 1),
(2, 2),
(3, 3),
(4, 4),
(5, 5),
(6, 6),
(7, 7),
(8, 1),
(9, 2),
(10, 3);
```