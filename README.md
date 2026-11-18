# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL no ambiente de cada aluno (um schema por aluno, escolhido pelo nome).
  Pede a chave de acesso da turma, informada em sala. Os ambientes de todos os alunos ficam visíveis no painel do professor.
  Depois da chave, a página também oferece os cadernos de atividades da revisão, em PDF.
- [`professor/`](professor): painel do professor, com entrada pela conta Google autorizada.
- `Revisao_AP2_Atividade_1.pdf.enc` a `_3`: cadernos de atividades cifrados (AES-GCM). A chave vem do banco, por uma
  função que só o usuário da turma executa, então os arquivos só abrem no Executor, depois da chave de acesso da turma.

As páginas não guardam senhas em texto: o segredo do qual saem as senhas dos alunos está criptografado, e o painel do professor só recebe dados depois que o banco confere o login do Google.
