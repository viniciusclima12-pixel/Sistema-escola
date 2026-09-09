<style>
  body {
    background: linear-gradient(180deg, #0b1020 0%, #111827 100%);
  }

  .space-title {
    display: inline-block;
    color: rgb(130, 204, 255);
    animation: spaceCycle 3s ease-in-out infinite alternate;
    text-shadow: 0 0 10px rgba(130, 204, 255, 0.5), 0 0 20px rgba(96, 165, 250, 0.3);
    transition: transform 0.45s ease, filter 0.45s ease, text-shadow 0.45s ease, letter-spacing 0.45s ease;
    transform-origin: center left;
    cursor: default;
    font-weight: 700;
  }

  .space-title:hover {
    transform: scale(1.12) translateY(-3px);
    filter: brightness(1.35) saturate(1.4);
    letter-spacing: 0.5px;
    text-shadow: 0 0 16px rgba(147, 197, 253, 0.95), 0 0 30px rgba(96, 165, 250, 0.8), 0 0 48px rgba(59, 130, 246, 0.7);
  }

  img {
    display: block;
    margin: 16px auto;
    border-radius: 14px;
    box-shadow: 0 10px 26px rgba(0, 0, 0, 0.28);
    transition: transform 0.4s ease, box-shadow 0.4s ease, filter 0.4s ease;
    max-width: 100%;
    height: auto;
    border: none;
  }

  img:hover {
    transform: scale(1.03) translateY(-3px);
    box-shadow: 0 14px 30px rgba(59, 130, 246, 0.18), 0 0 18px rgba(147, 197, 253, 0.12);
    filter: brightness(1.04) saturate(1.08);
  }

  @keyframes spaceCycle {
    0%   { color: rgb(125, 211, 252); }
    20%  { color: rgb(96, 165, 250); }
    40%  { color: rgb(59, 130, 246); }
    60%  { color: rgb(147, 197, 253); }
    80%  { color: rgb(96, 165, 250); }
    100% { color: rgb(191, 219, 254); }
  }

  .bot-figure {
    position: relative;
    width: 220px;
    height: 220px;
    margin: 30px auto 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    user-select: none;
  }

  .bot-body {
    position: relative;
    width: 120px;
    height: 120px;
    background: linear-gradient(180deg, #dfeefc 0%, #a9d4ff 100%);
    border-radius: 50% 50% 46% 46%;
    box-shadow: inset -8px -8px 0 rgba(64, 116, 205, 0.2), 0 0 20px rgba(96, 165, 250, 0.35);
    transition: transform 0.25s ease, box-shadow 0.25s ease;
  }

  .bot-figure:hover .bot-body {
    transform: translateY(-4px) scale(1.02);
    box-shadow: inset -8px -8px 0 rgba(64, 116, 205, 0.2), 0 0 26px rgba(96, 165, 250, 0.55);
  }

  .bot-head {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translateX(-50%);
    width: 78px;
    height: 78px;
    background: linear-gradient(180deg, #ffffff 0%, #d8ecff 100%);
    border-radius: 50%;
    box-shadow: inset -6px -6px 0 rgba(96, 165, 250, 0.18);
  }

  .bot-eye {
    position: absolute;
    top: 35px;
    width: 10px;
    height: 10px;
    background: #0f172a;
    border-radius: 50%;
    transition: transform 0.2s ease, height 0.2s ease;
  }

  .bot-eye.left { left: 52px; }
  .bot-eye.right { right: 52px; }

  .bot-mouth {
    position: absolute;
    bottom: 32px;
    left: 50%;
    transform: translateX(-50%);
    width: 34px;
    height: 16px;
    border-bottom: 4px solid #0f172a;
    border-radius: 0 0 14px 14px;
    transition: all 0.2s ease;
  }

  .bot-arm {
    position: absolute;
    top: 94px;
    width: 18px;
    height: 70px;
    background: linear-gradient(180deg, #d9f0ff 0%, #a9d4ff 100%);
    border-radius: 14px;
    transition: transform 0.2s ease;
  }

  .bot-arm.left {
    left: 10px;
    transform: rotate(18deg);
  }

  .bot-arm.right {
    right: 10px;
    transform: rotate(-18deg);
  }

  .bot-leg {
    position: absolute;
    bottom: 0;
    width: 18px;
    height: 52px;
    background: linear-gradient(180deg, #d9f0ff 0%, #a9d4ff 100%);
    border-radius: 14px;
  }

  .bot-leg.left { left: 76px; }
  .bot-leg.right { right: 76px; }

  .bot-figure:active .bot-body,
  .bot-figure:focus .bot-body {
    transform: scale(0.96);
  }

  .bot-figure:active .bot-eye,
  .bot-figure:focus .bot-eye {
    transform: scaleY(0.7);
    height: 8px;
  }

  .bot-figure:active .bot-mouth,
  .bot-figure:focus .bot-mouth {
    width: 24px;
    height: 12px;
    border-bottom-width: 3px;
  }

  .bot-figure:active .bot-arm.left,
  .bot-figure:focus .bot-arm.left {
    transform: rotate(36deg) translateY(4px);
  }

  .bot-figure:active .bot-arm.right,
  .bot-figure:focus .bot-arm.right {
    transform: rotate(-36deg) translateY(4px);
  }

  .bot-tag {
    text-align: center;
    color: rgba(191, 219, 254, 0.9);
    font-size: 13px;
    letter-spacing: 1px;
    margin-top: 8px;
    text-transform: uppercase;
  }
</style>

<div class="bot-figure" tabindex="0" aria-label="Boneco interativo">
  <div class="bot-head">
    <div class="bot-eye left"></div>
    <div class="bot-eye right"></div>
    <div class="bot-mouth"></div>
  </div>
  <div class="bot-body"></div>
  <div class="bot-arm left"></div>
  <div class="bot-arm right"></div>
  <div class="bot-leg left"></div>
  <div class="bot-leg right"></div>
</div>
<div class="bot-tag">Clique no robô</div>

# <span class="space-title">Sistema de Gestão Escolar</span>

## <span class="space-title">Sistema para gerenciar funcionários, alunos, cursos e matrículas</span>

### <span class="space-title">Usuários</span>

- **Funcionários**
- **Colaboradores**
- **Admin**

### <span class="space-title">Funcionalidades</span>

- Cadastrar, listar, editar e excluir alunos
- Cadastrar, listar, editar e excluir cursos
- Cadastrar, listar, editar e excluir funcionários
- Realizar e excluir matrículas
- Login de usuários
- Buscar alunos e funcionários por nome ou CPF

## <span class="space-title">PROBLEMA</span>

- Sistema direcionado a funcionários de escolas.
- Permite cadastrar, editar, listar e deletar alunos, cursos, matrículas e funcionários.

## <span class="space-title">MODELO DE NEGÓCIO</span>

![Business Model Canvas](images/business-model-canvas.png)

**Descrição:** Modelo de negócio do sistema, apresentando a proposta e os principais elementos envolvidos na solução.

## <span class="space-title">REQUISITOS</span>

### <span class="space-title">Requisitos Funcionais</span>

- Cadastrar alunos
- Cadastrar funcionários
- Cadastrar cursos
- Listar alunos
- Listar cursos
- Listar funcionários
- Mostrar dados de aluno, funcionário e curso
- Realizar matrículas
- Editar dados de aluno, funcionário e curso
- Excluir alunos, funcionários, cursos e matrículas
- Login de usuários
- Buscar aluno por nome e CPF
- Buscar funcionário por nome e CPF
- Mostrar cursos de cada aluno
- Mostrar alunos de cada curso

### <span class="space-title">Requisitos Não Funcionais</span>

- Autenticação
- Interface padronizada e consistente
- Interface responsiva
- Compatibilidade com os principais navegadores
- Senhas criptografadas no banco de dados
- Disponibilidade durante o horário de funcionamento
- Acesso restrito pelo tipo de usuário

## <span class="space-title">REGRAS DE NEGÓCIO</span>

- CPF de aluno deve ser único
- CPF de funcionário deve ser único
- Email de funcionário deve ser único
- Matrícula de aluno deve ser única
- Nome de curso deve ser único
- Não permitir excluir cursos com alunos matriculados
- Não permitir excluir alunos matriculados em cursos

## <span class="space-title">CASOS DE USO</span>

![Casos de uso](images/diagrama-casos-de-uso.png)

**Descrição:** Diagrama que mostra os usuários do sistema e as principais funções que cada tipo de usuário pode executar.

## <span class="space-title">CLASSES</span>

![Classes](images/diagrama-classes.png)

**Descrição:** Diagrama de classes que representa a estrutura do sistema, suas classes, atributos e relacionamentos.

## <span class="space-title">SEQUÊNCIAS</span>

### <span class="space-title">Login</span>

![Login](images/login.png)

**Descrição:** Mostra o processo de autenticação do funcionário, incluindo validação dos dados e retorno do acesso ou mensagem de erro.

### <span class="space-title">Cadastrar alunos</span>

![Cadastrar alunos](images/cad_alunos.png)

**Descrição:** Mostra o fluxo para cadastrar um novo aluno no sistema, incluindo o envio e a validação dos dados.

### <span class="space-title">Cadastrar cursos</span>

![Cadastrar cursos](images/cad_cursos.png)

**Descrição:** Mostra o fluxo para cadastrar um novo curso, validando as informações obrigatórias e a existência de outro curso com o mesmo nome.

### <span class="space-title">Cadastrar funcionários</span>

![Cadastrar funcionários](images/cad_func.png)

**Descrição:** Mostra o fluxo de cadastro de funcionários, disponível de acordo com o nível de acesso do usuário.

### <span class="space-title">Listar alunos</span>

![Listar alunos](images/list_alunos.png)

**Descrição:** Mostra o processo de consulta e apresentação da lista de alunos cadastrados no sistema.

### <span class="space-title">Listar cursos</span>

![Listar cursos](images/list_cursos.png)

**Descrição:** Mostra o processo de consulta e apresentação dos cursos cadastrados no sistema.

### <span class="space-title">Listar funcionários</span>

![Listar funcionários](images/list_func.png)

**Descrição:** Mostra o processo de consulta e apresentação dos funcionários cadastrados, respeitando as permissões de acesso.

### <span class="space-title">Mostrar dados de aluno</span>

![Dados aluno](images/dados_aluno.png)

**Descrição:** Mostra o fluxo para consultar e visualizar os dados completos de um aluno.

### <span class="space-title">Mostrar dados de curso</span>

![Dados curso](images/dados_curso.png)

**Descrição:** Mostra o fluxo para consultar e visualizar os dados de um curso.

### <span class="space-title">Mostrar dados de funcionário</span>

![Dados funcionário](images/dados_func.png)

**Descrição:** Mostra o fluxo para consultar e visualizar os dados de um funcionário.

### <span class="space-title">Editar aluno</span>

![Editar aluno](images/edit_aluno.png)

**Descrição:** Mostra o processo de alteração dos dados de um aluno e a validação das novas informações.

### <span class="space-title">Editar curso</span>

![Editar curso](images/edit_curso.png)

**Descrição:** Mostra o processo de alteração dos dados de um curso e a validação das informações.

### <span class="space-title">Editar funcionário</span>

![Editar funcionário](images/edit_func.png)

**Descrição:** Mostra o processo de alteração dos dados de um funcionário conforme as permissões do usuário.

### <span class="space-title">Excluir aluno</span>

![Excluir aluno](images/del_aluno.png)

**Descrição:** Mostra o fluxo de exclusão de um aluno, incluindo a verificação de matrículas antes da exclusão.

### <span class="space-title">Excluir curso</span>

![Excluir curso](images/del_curso.png)

**Descrição:** Mostra o fluxo de exclusão de um curso, impedindo a operação quando existem alunos matriculados.

### <span class="space-title">Excluir funcionário</span>

![Excluir funcionário](images/del_func.png)

**Descrição:** Mostra o fluxo de exclusão de um funcionário, respeitando as permissões do usuário Admin.

### <span class="space-title">Excluir matrículas</span>

![Excluir matrículas](images/del_mat.png)

**Descrição:** Mostra o processo de exclusão de uma matrícula entre um aluno e um curso.

### <span class="space-title">Buscar aluno por nome</span>

![Buscar aluno por nome](images/busca_aluno_nome.png)

**Descrição:** Mostra o fluxo para localizar um aluno utilizando seu nome como critério de busca.

### <span class="space-title">Buscar aluno por CPF</span>

![Buscar aluno por CPF](images/busca_aluno_cpf.png)

**Descrição:** Mostra o fluxo para localizar um aluno utilizando seu CPF como critério de busca.

### <span class="space-title">Buscar funcionário por nome</span>

![Buscar funcionário por nome](images/busca_func_nome.png)

**Descrição:** Mostra o fluxo para localizar um funcionário utilizando seu nome como critério de busca.

### <span class="space-title">Buscar funcionário por CPF</span>

![Buscar funcionário por CPF](images/busca_func_cpf.png)

**Descrição:** Mostra o fluxo para localizar um funcionário utilizando seu CPF como critério de busca.

### <span class="space-title">Realizar matrículas</span>

![Matrículas](images/matriculas.png)

**Descrição:** Mostra o processo de matrícula de um aluno em um curso, incluindo a verificação para impedir matrículas duplicadas.
