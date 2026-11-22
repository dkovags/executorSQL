# Executor de SQL

Páginas de apoio ao laboratório de banco de dados.

- [`index.html`](index.html): executa SQL no ambiente de cada aluno (um schema por aluno). O aluno escolhe a turma e o
  nome e digita a senha. A senha é conferida no banco (hash bcrypt, bloqueio de 10 minutos depois de 5 erros); no
  primeiro acesso, com a senha provisória entregue pelo professor, o aluno cria a senha dele. Só depois disso o banco
  devolve a senha do usuário do aluno e as chaves dos arquivos. O último item da lista, Professor, entra com a conta
  Google autorizada: os comandos vão pela Data API do Neon, que confere o login, e rodam no schema docente.
  Com o botão "Entrar como professor", o professor usa a conta Google para entrar na área de qualquer aluno, sem
  trocar a senha dele.
  Depois da entrada, a página oferece os cadernos de atividades da revisão e os arquivos da AP2 do aluno, em PDF.
- [`professor/`](professor): painel do professor, com entrada pela conta Google autorizada. No cadastro da turma,
  o botão Senha gera uma senha provisória nova para o aluno da vaga.
- `Revisao_AP2_Atividade_1.pdf.enc` a `_3`: cadernos de atividades cifrados (AES-GCM); a chave vem do banco depois
  da senha do aluno.
- `ap2/`: caderno de questões e correção individualizada de cada aluno, cifrados com uma chave aleatória guardada no
  banco e entregue só ao próprio aluno, depois da senha.

As páginas só guardam em texto a senha do usuário portal, que não lê nenhum dado e apenas confere senhas; as senhas dos alunos ficam no banco, com hash, e o painel e a entrada do professor só recebem dados depois que o banco confere o login do Google.
