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

[Descrição da arquitetura das APIs, incluindo os componentes e suas interações.]

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

[Descreva a estratégia de teste, incluindo os tipos de teste a serem realizados (unitários, integração, carga, etc.) e as ferramentas a serem utilizadas.]

1. Crie casos de teste para cobrir todos os requisitos funcionais e não funcionais da aplicação.
2. Implemente testes unitários para testar unidades individuais de código, como funções e classes.
3. Realize testes de integração para verificar a interação correta entre os componentes da aplicação.
4. Execute testes de carga para avaliar o desempenho da aplicação sob carga significativa.
5. Utilize ferramentas de teste adequadas, como frameworks de teste e ferramentas de automação de teste, para agilizar o processo de teste.

# Referências

Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.
