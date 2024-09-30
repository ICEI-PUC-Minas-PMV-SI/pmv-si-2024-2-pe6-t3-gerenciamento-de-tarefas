# APIs e Web Services

A API e Web Service do projeto "GerenciamentoApiRest" oferece funcionalidades de gerenciamento de tarefas e projetos, permitindo criar, atribuir, e acompanhar atividades de forma colaborativa. A arquitetura RESTful, com autenticação via JWT e banco de dados PostgreSQL, garante segurança e escalabilidade. É uma solução eficiente para organizar e monitorar projetos em equipe.

## Objetivos da API

**API Gerenciamento de Tarefas:**
Objetivo: Prover funcionalidades para gerenciamento de projetos e tarefas, voltado ao público que necessita ter um controle melhor sobre projetos ou atividades cotidianas.

**Recursos**:

- API de projeto: Inclusão, alteração, exclusão e pesquisa por projeto.
- API de usuário: Inclusão, alteração, exclusão e autenticação de usuários.
- API de tarefa: Inclusão, alteração, exclusão e pesquisa de tarefas, com informações como título, descrição, data, dentre outras.
- API de integração: Integração com o google agenda, de forma que ao se criar uma tarefa o usuario receba a notificação durante o prazo da mesma.
- Relatório de tarefas: Lista de Tarefas por projeto.



## Arquitetura

A arquitetura das APIs do projeto "GerenciamentoApiRest" é baseada em uma estrutura RESTful, proporcionando uma comunicação eficiente e organizada entre o cliente e o servidor para gerenciamento de tarefas e projetos. A seguir estão os principais componentes e suas interações:

API RESTful
Desenvolvida com ASP.NET Core, seguindo os princípios de APIs RESTful para permitir a criação, leitura, atualização e exclusão de dados de forma organizada.
Modelo de Dados
Usuário: Contém informações dos usuários, como nome, e-mail, senha e perfil (Administrador ou Cliente).
Projeto: Representa projetos que contêm várias tarefas, com informações como título, descrição e data de criação.
Tarefa: Contém os detalhes das atividades atribuídas aos projetos, incluindo título, descrição, prioridade, status (não iniciada, em andamento, finalizada), usuário atribuído e prazo de conclusão.
DTOs (Data Transfer Objects)
Utilizados para transferir dados entre a API e o cliente, garantindo que apenas as informações necessárias sejam transmitidas, melhorando a eficiência e a segurança da aplicação.
Dados
Utiliza o Entity Framework Core para gerenciar as interações com o banco de dados PostgreSQL, permitindo a persistência de dados de forma segura e estruturada.
Autenticação e Segurança
Implementa autenticação e autorização por meio de JWT (JSON Web Token) para proteger os endpoints da API.
As senhas dos usuários são armazenadas de forma segura utilizando BCrypt para hash, garantindo a integridade e proteção dos dados sensíveis.
Interações
Requisições do Cliente: O cliente faz requisições HTTP (GET, POST, PUT, DELETE) para a API, interagindo com os recursos de usuários, projetos e tarefas.
Controle de Dados: Os controladores (Controllers) da API processam as requisições, validam os dados recebidos e utilizam os serviços e repositórios para manipular os dados no banco de dados.
Fluxo de Dados:
Exemplo de Criação de Tarefa:
O cliente envia uma requisição POST com os dados da nova tarefa.
O controlador de Tarefas (TarefasController) valida a requisição e encaminha a tarefa ao serviço (TarefaService) para ser processada.
A tarefa é persistida no banco de dados via Entity Framework Core.
A API retorna uma resposta de sucesso com os detalhes da tarefa criada.
Esta arquitetura modular e organizada facilita o desenvolvimento e a manutenção da aplicação, garantindo que a API seja segura, eficiente e escalável, atendendo aos requisitos de gerenciamento de projetos e tarefas de forma robusta.

## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]


## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Requisitos Funcionais

[Liste os principais requisitos funcionais da aplicação.]

## Requisitos Não Funcionais

[Liste os principais requisitos não funcionais da aplicação, como desempenho, segurança, escalabilidade, etc.]

## Tecnologias Utilizadas

Existem muitas tecnologias diferentes que podem ser usadas para desenvolver APIs Web. A tecnologia certa para o seu projeto dependerá dos seus objetivos, dos seus clientes e dos recursos que a API deve fornecer.

[Lista das tecnologias principais que serão utilizadas no projeto.]

## API Endpoints

[Liste os principais endpoints da API, incluindo as operações disponíveis, os parâmetros esperados e as respostas retornadas.]

### Endpoint 1
- Método: POST
- URL: /api/Usuarios/register
- Parâmetros: Sem Parametros

- Corpo da Requisição:
   ```json
    {
  "id": 0,
  "nome": "Pessoa1",
  "email": "user@example.com",
  "senha": "SenhaSegura@123"}
   
- Resposta:
  - Sucesso (201 CREATED)
   ```json
   {
    "$id": "1",
    "nome": "Pessoa1",
    "email": "user@example.com",
    "senha": "$2a$11$WnPB5LqYL5TqOr57JNqNTeHO2fWdR4j6sJO7QzVU60LMu7tpMAtjG",
    "perfil": 1,
    "perfilDescricao": "Cliente",
    "id": 4
   }
  
  - 400 Bad Request
    {
    "$id": "1",
    "type": "https://tools.ietf.org/html/rfc9110#section-15.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "errors": {
        "$id": "2",
        "Senha": [
            "A senha deve ter pelo menos 8 caracteres."
        ]
    },
    "traceId": "00-fee99bfcd684fa34c704557dcd967cae-ff439ed4a936c69a-00"}
   


## Considerações de Segurança

Para garantir a segurança da aplicação adotamos diversas medidas de proteção, focadas em autenticação, autorização.

Autenticação:

O sistema utiliza JWT (JSON Web Token), implementado com o pacote JWTBearer, para autenticação segura dos usuários. Ao fazer login, o usuário recebe um token que é utilizado nas solicitações subsequentes para identificar e autenticar o acesso. Esse token é assinado de forma criptografada, garantindo que não possa ser alterado sem a chave de assinatura.

Autorização:

A autorização é tratada por meio de políticas e claims definidas nos tokens JWT. Essas claims indicam o nível de acesso do usuário, garantindo que ele tenha permissões adequadas para acessar recursos específicos.
## Implantação

[Instruções para implantar a aplicação distribuída em um ambiente de produção.]

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.
4. Faça o deploy da aplicação no ambiente escolhido, seguindo as instruções específicas da plataforma de hospedagem.
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

## Testes

Para os testes utilizaremos o Postman. Será realizado o registro de um usuário, após o registro esse usuário fará o login e depois irá criar uma tarefa.
![Captura de Tela (47)](https://github.com/user-attachments/assets/5715d125-ac74-4647-8091-1e41aba327ed)
![Captura de Tela (48)](https://github.com/user-attachments/assets/dc6158f4-d50e-4a01-b5b0-45717e3c7d5c)
![Captura de Tela (49)](https://github.com/user-attachments/assets/5ed4a455-83dd-47fa-be76-a1d8335a5784)



# Referências

Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.
