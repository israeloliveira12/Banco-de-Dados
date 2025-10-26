README – Modelagem Conceitual e MER

Este repositório reúne soluções teóricas e práticas sobre Modelagem Entidade-Relacionamento (MER), incluindo conceitos, diagramas e exemplos aplicados.

Questões Teóricas

Importância da Modelagem Conceitual: Facilita comunicação entre usuários e desenvolvedores e garante independência de dados.

Entidade Forte x Entidade Fraca: Forte tem existência própria (ex: Aluno), fraca depende de outra (ex: Histórico de Matrícula).

Chaves:

Superchave: identifica unicamente registros.

Chave candidata: superchave mínima.

Chave primária: escolhida para identificação única.

Relacionamentos Ternários: Envolvem 3 entidades simultaneamente (ex: Médico–Paciente–Tratamento).

Atributos Multivalorados/Derivados:

Multivalorados: vários valores por entidade (ex: telefones).

Derivados: calculados a partir de outros (ex: idade).

Questões Práticas

Livraria: Cliente, Livro, Editora, Compra. Relacionamentos: Cliente–Compra 1:N, Compra–Livro N:M, Livro–Editora N:1.

Hospital: Paciente, Médico, Enfermeiro, Plano, Atendimento. Relacionamentos: Atendimento conecta paciente, médico e enfermeiro.

Escola: Aluno, Disciplina, Professor, Matrícula. Histórico acadêmico derivado da matrícula.

Projeto Livre (E-commerce): Usuário, Produto, Pedido, Item_Pedido. Relacionamentos N:M via tabela associativa.

Observações

Todas as soluções consideram PKs, FKs, cardinalidades e atributos essenciais.

Diagramas ER podem ser criados em Draw.io, Lucidchart ou DBDesigner.

Modelos prontos para implementação em bancos de dados relacionais.
