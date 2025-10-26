README – Exercícios de Modelagem Conceitual e MER

Este repositório contém soluções teóricas e práticas sobre Modelagem Entidade-Relacionamento (MER), abordando conceitos fundamentais, diagramas e cenários aplicados. O conteúdo é dividido em questões teóricas e questões práticas, com explicações detalhadas, exemplos e sugestões de implementação.

Questões Teóricas
Questão 1 – Importância da Modelagem Conceitual

A modelagem conceitual é crucial no desenvolvimento de sistemas de informação, pois:

Facilita a comunicação entre usuários e desenvolvedores, traduzindo requisitos em um modelo visual compreensível.

Promove a independência de dados, separando a forma como os dados são armazenados da forma como são utilizados pelos sistemas.

Serve como base para o projeto lógico e físico, evitando retrabalho e inconsistências.

Questão 2 – Entidade Forte vs Entidade Fraca

Entidade Forte: possui existência independente e uma chave primária própria.

Exemplo: Na gestão acadêmica, Aluno (id_aluno) é uma entidade forte.

Entidade Fraca: depende da existência de outra entidade para ser identificada; sua chave é parcial e combinada com a chave da entidade forte.

Exemplo: Histórico de Matrícula depende do Aluno (id_aluno) e da Disciplina (id_disciplina).

Questão 3 – Chave Primária, Candidata e Superchave

Superchave: conjunto de atributos que identifica unicamente uma tupla em uma tabela.

Chave Candidata: superchave mínima, sem atributos redundantes.

Chave Primária: chave candidata escolhida para identificar registros de forma única.

A escolha correta da chave primária é essencial para garantir integridade referencial e evitar duplicidade de dados.

Questão 4 – Relacionamentos Ternários

Relacionamentos ternários envolvem três entidades simultaneamente.

Exemplo: Em um hospital: Médico, Paciente e Tratamento. O relacionamento registra qual médico realizou qual tratamento em qual paciente.

Evita perder informações se fosse representado como múltiplos relacionamentos binários.

Questão 5 – Atributos Multivalorados e Derivados

Multivalorados: podem ter múltiplos valores para uma mesma entidade.

Exemplo: Telefone de um aluno.

Representação: dupla elipse ligada à entidade no MER.

Derivados: podem ser calculados a partir de outros atributos.

Exemplo: Idade derivada da data de nascimento.

É recomendável normalizar multivalorados em tabelas separadas para evitar redundância.

🛠 Questões Práticas
Questão 6 – MER: Livraria

Entidades e Atributos:

Cliente: id_cliente (PK), nome, email, telefone, endereco

Livro: id_livro (PK), titulo, ano_publicacao, preco, id_editora (FK)

Editora: id_editora (PK), nome, telefone, endereco

Compra: id_compra (PK), id_cliente (FK), data_compra, total

Relacionamentos:

Cliente ↔ Compra: 1:N

Compra ↔ Livro: N:M → Tabela associativa: Compra_Livro (id_compra, id_livro, quantidade)

Livro ↔ Editora: N:1

Questão 7 – MER: Hospital

Entidades e Atributos:

Paciente: id_paciente (PK), nome, data_nascimento, telefone, id_plano (FK)

Médico: id_medico (PK), nome, especialidade, crm

Enfermeiro: id_enfermeiro (PK), nome, coren

Plano de Saúde: id_plano (PK), nome, tipo

Atendimento: id_atendimento (PK), id_paciente (FK), id_medico (FK), id_enfermeiro (FK), data, descricao

Relacionamentos:

Paciente ↔ Plano de Saúde: N:1

Atendimento ↔ Paciente, Médico, Enfermeiro: N:1

Questão 9 – Caso Prático: Escola

Entidades e Atributos:

Aluno: id_aluno (PK), nome, data_nascimento, email

Disciplina: id_disciplina (PK), nome, carga_horaria

Professor: id_professor (PK), nome, especialidade

Matrícula: id_matricula (PK), id_aluno (FK), id_disciplina (FK), id_professor (FK), ano, semestre, nota

Relacionamentos:

Aluno ↔ Matrícula: 1:N

Disciplina ↔ Matrícula: 1:N

Professor ↔ Matrícula: 1:N

Questão 10 – Projeto Livre: Sistema de E-commerce

Entidades e Atributos:

Usuário: id_usuario (PK), nome, email, senha

Produto: id_produto (PK), nome, descricao, preco, estoque

Pedido: id_pedido (PK), id_usuario (FK), data, total

Item_Pedido: id_item (PK), id_pedido (FK), id_produto (FK), quantidade, preco_unitario

Relacionamentos:

Usuário ↔ Pedido: 1:N

Pedido ↔ Produto: N:M (via Item_Pedido)

Mapeamento Relacional:

Cada entidade → tabela

Relacionamentos N:M → tabelas associativas (Item_Pedido)

PKs e FKs garantem integridade referencial

📝 Observações Gerais

Todos os modelos consideram chaves primárias, atributos essenciais e cardinalidades.

Diagramas ER podem ser construídos em ferramentas como Draw.io, Lucidchart ou DBDesigner.

O material é adequado para implementação em SGBDs relacionais (MySQL, PostgreSQL, SQLite).
