# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL no ambiente de cada aluno (um schema por aluno, escolhido pelo nome).
  Pede a chave de acesso da turma, informada em sala. O último item da lista, Professor, pede uma chave própria
  e entra num ambiente que lê os schemas de todos os alunos.
  Depois da chave, a página também oferece o projeto Java do laboratório.
- [`professor/`](professor): painel do professor, com entrada pela conta Google autorizada.
- `POO_Aula10_Laboratorio.zip.enc`: o projeto Java do laboratório, com o roteiro, cifrado (AES-GCM). Só abre pelo botão
  "Baixar o projeto Java" do Executor, com a chave da turma, porque o `Conexao.java` traz as senhas das duplas.

As páginas não guardam senhas em texto: o segredo do qual saem as senhas dos alunos e a senha do professor estão criptografados, e o painel do professor só recebe dados depois que o banco confere o login do Google.
