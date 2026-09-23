# Sistema de Gestão Escolar

## Sistema para gerenciar funcionários, alunos, cursos e matrículas

1. Quem utilizará o sistema (usuários)?
  - Funcionários

2. Quais os tipos de usuários e o que cada tipo consegue fazer?
  - Colaboradores: Cadastrar alunos, cadastrar cursos, editar dados dos alunos, editar dados dos cursos, excluir alunos, excluir cursos, listar alunos, listar cursos, matricular alunos nos cursos, desmatricular alunos dos cursos e atualizar os próprios dados
  - Admin: Todas as funções acima, mais: cadastrar outros funcionários, listar outros funcionários, editar dados dos outros funcionários e excluir outros funcionários

3. Quais informações iremos armazenar?
  - Funcionários: Nome, email, cargo, data de nascimento, cpf, senha, telefone, endereço
  - Alunos: Matrícula, CPF, Nome, data de nascimento, email, telefone, endereço
  - Cursos: Descrição, carga horária, nome
  - Matrículas: Quais alunos estão cadastrados em quais cursos

4. Quais regras ou restrições são necessárias?
  - Apenas funcionários admin podem criar/deletar outros funcionários
  - Funcionários colaboradores não podem editar dados de outros funcionários
  - CPF não pode repetir, email não pode repetir
  - Nome, email, cargo, cpf, senha, carga horária, matrícula são dados obrigatórios
  - Um aluno não pode ser matriculado duas ou mais vezes no mesmo curso
  - O sistema deve validar as informações

## PROBLEMA:
  - Esses sistema é direcionado a funcionários de escolas
  - Permite cadastrar, editar, listar e deletar alunos, cursos, matrículas e funcionários
  
## MODELO DE NEGÓCIO:
  ![Business Model Canvas](images/business-model-canvas.png)

## REQUISITOS:
1. Requisitos Funcionais:
  - Cadastrar alunos
  - Cadastrar funcionários
  - Cadastrar cursos
  - Listar alunos
  - Listar cursos
  - Listar funcionários
  - Mostrar os dados do aluno
  - Mostrar os dados do funcionário
  - Mostrar os dados do curso
  - Realizar as matrículas
  - Editar os dados do aluno
  - Editar os dados do funcionário
  - Editar os dados do curso
  - Excluir os alunos
  - Excluir os funcionários
  - Excluir os cursos
  - Excluir as matrículas
  - Login de usuários
  - Buscar aluno pelo nome
  - Buscar aluno pelo CPF
  - Buscar funcionário pelo nome
  - Buscar funcionário pelo CPF
  - Mostrar os cursos em que cada aluno está matriculado
  - Mostrar os alunos que estão matriculados em cada curso
2. Requisitos Não Funcionais:
  - Autenticação
  - Interface com navegação padronizada e consistente entre as telas
  - Interface responsiva e adaptativa a diversas resoluções de tela e dispositivos diferentes, como computador, celular e tablet
  - Interface deve ser compatível com os principais navegadores web
  - Criptografar as senhas antes de salvá-las no banco de dados
  - Disponível durante todo o horário de funcionamento da instituição
  - Restringir acesso pelo tipo de usuário
  
## REGRAS DE NEGÓCIO:
- CPF de cada aluno deve ser único
- CPF de cada funcionário deve ser único
- Email de cada funcionário deve ser único
- A matrícula de cada aluno deve ser única
- Nome de cada curso deve ser único
- Impedir exclusão de cursos que tenham alunos matriculados
- Impedir exclusão de alunos que estejam matriculados em 1 ou mais cursos

## CASOS DE USO:
  ![Casos de uso](images/diagrama-casos-de-uso.png)

## Classes:
  ![Classes](images/diagrama-classes.png)

## Sequências:
- Login:
  
  ![Login](images/login.png)

- Cadastro funcionário:
  
  ![Cadastro funcionário](images/cad_func.png)

- Cadastro aluno:
  
  ![Cadastro aluno](images/cad_alunos.png)

- Cadastro curso:
  
  ![Cadastro curso](images/cad_cursos.png)

- Lista de funcionários:
  
  ![Lista funcionários](images/list_func.png)

- Lista de alunos:
  
  ![Lista alunos](images/list_alunos.png)

- Lista de cursos:
  
  ![Lista cursos](images/list_cursos.png)

- Dados do aluno:
  
  ![Dados do aluno](images/dados_aluno.png)

- Dados do curso:
  
  ![Dados do curso](images/dados_curso.png)

- Dados do funcionário:
  
  ![Dados do funcionário](images/dados_func.png)

- Edição do aluno:
  
  ![Edição do aluno](images/edit_aluno.png)

- Edição do curso:
  
  ![Edição do curso](images/edit_curso.png)

- Edição do funcionário:
  
  ![Edição do funcionário](images/edit_func.png)

- Exclusão do aluno:
  
  ![Exclusão do aluno](images/del_aluno.png)

- Exclusão do curso:
  
  ![Exclusão do curso](images/del_curso.png)

- Exclusão do funcionário:
  
  ![Exclusão do funcionário](images/del_func.png)

- Lista alunos pelo nome:
  
  ![Lista alunos pelo nome](images/busca_aluno_nome.png)

- Lista alunos pelo CPF:
  
  ![Lista alunos pelo CPF](images/busca_aluno_cpf.png)

- Lista funcionários pelo nome:
  
  ![Lista funcionários pelo nome](images/busca_func_nome.png)

- Lista funcionários pelo CPF:
  
  ![Lista funcionários pelo CPF](images/busca_func_cpf.png)

- Matricula alunos em cursos:

  ![Matricula alunos em cursos](images/matriculas.png)

- Exclusão de matrículas

  ![Exclusão de matrículas](images/del_mat.png)