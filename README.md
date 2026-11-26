# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL no ambiente de cada aluno (um schema por aluno em cada turma). O aluno entra
  com a conta do Gmail vinculada à turma; com uma turma só, entra direto. O professor entra com a conta Google
  autorizada: no próprio schema (docente), para exemplos em aula, ou na área de qualquer aluno.
  Depois da entrada, a página oferece os cadernos de atividades da revisão e os arquivos da AP2 do aluno, em PDF.
- [`professor/`](professor): Painel de Execução de SQL, com entrada pela conta Google autorizada. Também abre dentro da
  Área do professor do portal (academico.kovags.com/professor), onde ficam as turmas: a lista importada cria os
  schemas dos alunos e controla o cadastro do Gmail.
- `Revisao_AP2_Atividade_1.pdf.enc` a `_3`: cadernos de atividades cifrados (AES-GCM); a chave vem do banco depois
  da senha do aluno.
- `ap2/`: caderno de questões e correção individualizada de cada aluno, cifrados com uma chave aleatória guardada no
  banco e entregue só ao próprio aluno, depois da senha.

As páginas não guardam senhas: os dados só chegam depois que o banco confere o login do Google.
