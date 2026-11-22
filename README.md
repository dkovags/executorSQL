# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL no ambiente de cada aluno (um schema por aluno, escolhido pelo nome).
  O aluno escolhe a turma e o nome e digita a chave própria (8 caracteres), entregue pelo professor. A chave abre o
  cofre do aluno, com a senha dele no banco, e os arquivos da AP2 dele (caderno de questões e correção). O último item da lista, Professor, entra com a conta Google
  autorizada: os comandos vão pela Data API do Neon, que confere o login, e rodam no schema docente.
  Depois da entrada, a página também oferece os cadernos de atividades da revisão, em PDF.
- [`professor/`](professor): painel do professor, com entrada pela conta Google autorizada.
- `Revisao_AP2_Atividade_1.pdf.enc` a `_3`: cadernos de atividades cifrados (AES-GCM). A chave fica no cofre de
  cada aluno, então os arquivos só abrem no Executor, depois da entrada com a chave do aluno.
- `ap2/`: caderno de questões e correção individualizada de cada aluno, cifrados com a chave dele.

As páginas não guardam senhas em texto: a senha de cada aluno está criptografada com a chave dele, e o painel e a entrada do professor só recebem dados depois que o banco confere o login do Google.
