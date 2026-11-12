# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL na tabela da dupla. Pede a chave de acesso da turma, informada em sala.
  Depois da chave, a página também oferece o Roteiro de Atividades – JDBC e o projeto Java do laboratório.
- [`professor/`](professor): painel do professor, com entrada pela conta Google autorizada.
- [`POO_Aula10_Roteiro_de_Atividades_JDBC.pdf`](POO_Aula10_Roteiro_de_Atividades_JDBC.pdf): roteiro do laboratório de JDBC.
- `POO_Aula10_Laboratorio.zip.enc`: o projeto Java do laboratório, cifrado (AES-GCM). Só abre pelo botão
  "Baixar o projeto Java" do Executor, com a chave da turma, porque o `Conexao.java` traz as senhas das duplas.

As páginas não guardam senhas em texto: as credenciais das duplas estão criptografadas, e o painel do professor só recebe dados depois que o banco confere o login do Google.
