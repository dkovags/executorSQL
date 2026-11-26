# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL no ambiente de cada aluno (um schema por aluno em cada turma). O aluno entra
  com a conta do Gmail vinculada à turma; com uma turma só, entra direto. O professor entra com a conta Google
  autorizada: no próprio schema (docente), para exemplos em aula, ou na área de qualquer aluno.
- [`professor/`](professor): Painel de Execução de SQL, com entrada pela conta Google autorizada. Também abre dentro da
  Área do professor do portal (academico.kovags.com/professor), onde ficam as turmas: a lista importada cria os
  schemas dos alunos e controla o cadastro do Gmail.

As páginas não guardam senhas: os dados só chegam depois que a API do portal (kovags.com) confere o login do Google.
