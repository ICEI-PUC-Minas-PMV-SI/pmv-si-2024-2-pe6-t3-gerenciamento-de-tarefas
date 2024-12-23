# Front-end Móvel

O Gerenciador de Tarefas Mobile é um aplicativo projetado para oferecer uma experiência eficiente e organizada no acompanhamento de projetos e tarefas diretamente no celular. Com uma interface intuitiva e responsiva, o app permite que os usuários visualizem seus projetos, adicionem e editem tarefas, configurem notificações personalizadas para lembretes importantes e acessem relatórios detalhados, tudo na palma da mão. Além disso, o aplicativo é focado em promover a produtividade, simplificando o gerenciamento de tarefas em qualquer lugar, a qualquer momento.

## Tecnologias Utilizadas

As seguintes tecnologias foram utilizadas no desenvolvimento deste projeto:

◘ HTML;

◘ CSS;

◘ JavaScript;

◘ React Native;

## Arquitetura

A arquitetura do sistema de Gerenciador de Tarefas Mobile foi projetada para ser modular e escalável, utilizando o framework React Native para criar uma experiência otimizada em dispositivos móveis. Com integração à API REST desenvolvida no back-end, a aplicação segue uma estrutura em camadas e componentes bem definidos, garantindo flexibilidade, eficiência e facilidade de manutenção.

### Descrição da Arquitetura

◘ React Native: A interface do usuário será construída com componentes reutilizáveis e otimizados para dispositivos móveis, oferecendo uma navegação fluida e responsiva.

### Componente de Navegação e Rotas

◘ React Navigation: Responsável por gerenciar a navegação entre telas, com suporte a pilhas, abas e rotas condicionais.

◘ Expo Router: Simplifica a configuração de rotas com uma abordagem baseada em arquivos, inspirada no modelo do Next.js, mas adaptada para React Native.


### Componentes da Interface 

◘ Formulários de Cadastro e Login: Componentes que gerenciam autenticação e registro de usuários.

◘ Formulários de Tarefas: Componentes que permitem criar, editar e excluir tarefas.

### Interações Dinâmicas

◘ JavaScript: Gerencia ações dinâmicas, como validação de formulários, navegação condicional e controle de estados (por exemplo, autenticação).

◘ Axios: Para comunicação com a API, enviando e recebendo dados de forma eficiente.


## Modelagem da Aplicação

A modelagem da aplicação apresentada no diagrama representa um sistema de gerenciamento de tarefas:


## Estrutura de Dados:

![image](https://github.com/user-attachments/assets/fc247797-fb5e-4ee3-946f-af76f1f43d79)


## Tabela projeto

 ##### •	Contém informações relacionadas ao projeto.

 ##### •	Campos principais.

◘ Id: <kbd>identificador único</kbd>

◘ Nome: <kbd>Nome do Projeto</kbd>

◘ Descricao: <kbd>Descrição do projeto</kbd>

◘ DataInicio: <kbd>Data de inicio do projeto</kbd>

◘ DataFim: <kbd>Data final do projeto</kbd>

◘ Status: <kbd>Status do projeto</kbd>


## Tabela tarefas

##### •	Contém cadastros das tarefas.

##### •	Campos principais.

◘ TarefaId: <kbd>identificador único</kbd>

◘ Titulo: <kbd>Título da tarefa</kbd>

◘ Descricao: <kbd>Descrição da tarefa</kbd>

◘ Prioridade: <kbd>Prioridade: 'alta', 'média', 'baixa'</kbd>

◘ Status: <kbd>Status da tarefa</kbd>

◘ UsuarioAtribuido: <kbd>Id do usuário atribuído à tarefa</kbd>

◘ DataVencimento: <kbd>Data de vencimento da tarefa</kbd>

◘ CriadoEm: <kbd>Data de criação da tarefa</kbd>

◘ AtualizadoEm: <kbd>Data de última atualização da tarefa</kbd>

◘ ProjetoId: <kbd>chave estrangeira relacionada à tabela projeto</kbd>

## Tabela usuarios

  ##### •	Contém dados cadastrados dos usários.
 
  ##### •	Campos principais.
 
◘ Id: <kbd>identificador único</kbd>

◘ Nome: <kbd>Nome do usuário</kbd>

◘ Email: <kbd>E-mail do usuário</kbd>

◘ senha: <kbd>Senha do usuário</kbd>

◘ Perfil:<kbd>"Administrador" "Cliente"</kbd>


## Tabela usuarioprojeto

##### •	Campos principais.

◘ UsuarioId

◘ ProjetoId

 
## Projeto da Interface

### Wireframes
Tela de Login:

![image](https://github.com/user-attachments/assets/cb661cd3-8496-472b-a9fd-cccb84b03049)

Tela de Projetos:

![image](https://github.com/user-attachments/assets/b5abb509-a451-4868-9992-40d4fe2d875a)

Tela de Tarefas:

![image](https://github.com/user-attachments/assets/b715d4b9-431d-4a78-aa52-a34497753bb3)

### Design Visual

O design visual da interface será orientado para a simplicidade e a eficiência, com um estilo moderno e minimalista que prioriza a usabilidade. O objetivo é criar um ambiente visual agradável e intuitivo, que auxilie os usuários a focarem em suas tarefas sem distrações.

#### Estrutura e Paleta de Cores:

A paleta de cores será composta por tons neutros e sutis, com destaques em cores mais vivas para indicar ações importantes ou alertas:

◘ Primária: Tons de azul suave, usados para menus e botões principais, trazendo uma sensação de calma e organização.

◘ Secundária: Tons de cinza para planos de fundo e separadores, criando um contraste harmonioso sem sobrecarregar a interface.

◘ Destaques: Vermelho para erros/alertas, verde para tarefas concluídas.


### Layout Responsivo

A interface da aplicação de gerenciamento de tarefas será projetada com um layout responsivo para oferecer uma experiência consistente e intuitiva em dispositivos de diferentes tamanhos, como tablets e smartphones.

Smartphones: Navegação simplificada com menus acessíveis. Conteúdo disposto verticalmente, priorizando informações mais relevantes, como tarefas do dia e notificações. Funções de edição e detalhes de projetos/tarefas serão acessadas por modais ou novas páginas.

Tablets: O layout será ajustado para manter menus laterais ou superiores compactados, dependendo da orientação do dispositivo. Painéis serão reorganizados em colunas ou pilhas, para evitar sobreposição de informações.


### Interações do Usuário

A interface da aplicação de gerenciamento de tarefas será projetada para oferecer interações suaves, responsivas e intuitivas, promovendo uma experiência de usuário agradável e eficiente. As interações serão compostas por animações, transições e feedbacks visuais que ajudam os usuários a entenderem suas ações e o estado atual do sistema.

####  Feedback em Ações:
◘ Adicionar ou Atualizar Tarefas: Exibição de um alerta visual (como um pop-up ou um breve destaque colorido) indicando o sucesso ou falha da operação.

◘ Alteração de Status: Mudanças de status (ex.: de "Em andamento" para "Concluído") serão acompanhadas por animações sutis, como um ícone de check sendo marcado ou uma mudança de cor.

#### Gestos para Dispositivos Móveis:
◘ Deslizar para a esquerda ou direita para marcar tarefas como concluídas ou excluí-las.

◘ Toque longo para abrir opções de edição ou detalhamento.


## Fluxo de Dados

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t3-gerenciamento-de-tarefas/blob/main/docs/img/fluxo%20de%20dados%20mobile.jpg)

## Requisitos Funcionais

| ID     | Descrição do Requisito                                                                                                                                         | Prioridade |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| RF-001 | O app deve permitir que o usuário crie, edite e exclua tarefas, associando cada tarefa a um projeto específico.                                           | Alta       |
| RF-002 | O app deve possibilitar ao usuário configurar notificações para tarefas e projetos, alertando sobre prazos e atualizações por meio de pop-ups ou uma área de notificações. | Média      |
| RF-003 | O app deve gerar relatórios personalizados sobre o andamento dos projetos e tarefas, exibindo informações como número de tarefas concluídas, status dos projetos e tempo gasto em cada tarefa. | Média      |

## Requisitos Não Funcionais

| ID     | Descrição do Requisito                                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| RNF-001 | O aplicativo deve carregar as telas e executar operações como criação e edição de tarefas em até 2 segundos, garantindo uma experiência fluida para o usuário.          |
| RNF-002 | O app deve ser compatível com os sistemas operacionais Android (versão 8.0 ou superior) e iOS (versão 13 ou superior), mantendo a responsividade e funcionalidade em diferentes tamanhos de tela.                 |


## Considerações de Segurança

Para garantir a segurança do Gerenciador de Tarefas Mobile, utilizaremos o JSON Web Token (JWT) para autenticar a sessão dos usuários. O JWT é uma maneira segura de garantir que as informações de autenticação sejam transmitidas de forma confiável entre o cliente e o servidor, sem a necessidade de armazenar dados de sessão no servidor.

### Autenticação com JWT no React Native:

◘ O usuário se autentica utilizando seu e-mail e senha na aplicação.

◘ Após a autenticação, o backend gera um token JWT, que é enviado para o cliente.

◘ O token JWT contém informações relevantes, como o ID do usuário e seu tipo (administrador, usuário), além de uma data de expiração definida para aumentar a segurança.

◘ Em cada requisição subsequente, o token é enviado no header Authorization, permitindo que o backend valide a autenticidade do usuário.

◘ O backend valida o token em cada requisição para garantir que o usuário tenha permissão para acessar o recurso solicitado.

## Implantação

#### 1.	Pré-requisitos:
##### ◘ Node.js e dependências instaladas no servidor de produção.
##### ◘ Banco de dados configurado (PostgreSQL).
#### 2.	Etapas de Deploy:
##### ◘ Configurar variáveis de ambiente no servidor (porta, URLs, chaves JWT).
##### ◘ Realizar build do front-end (ReactJS para web e React Native para mobile).
##### ◘ Implantar o back-end e banco de dados em um serviço como.
#### 3.	Teste no Ambiente de Produção:
##### ◘ Verificar tempos de resposta e funcionalidade geral.
##### ◘ Garantir que a aplicação esteja acessível em dispositivos variados.


## Testes
### ◘ 1.0 - Caso de Teste: Login e Logout com autenticação utilizando token JWT:

| Passo  |  Descrição                                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Acessar a página de login.          |
| 2 |Inserir as credenciais (e-mail e senha) nos campos exibidos.          |
| 3 | Clicar no botão "Entrar" para autenticar. O usuário será redirecionado para a página "Home".          |
| 4 |Clicar no botão "Sair". O usuário será redirecionado novamente para a página de login.          |

### ◘ Resultados:

|  Resultado Esperado  |  Resultado Alcançado                                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| Login bem-sucedido Request: 200 OK | Usuário autenticado com sucesso. O token JWT foi gerado e armazenado no Local Storage.          |
| Logout bem-sucedido Request: 200 OK | Usuário redirecionado para a página de login. O token JWT foi "removido/resetado" corretamente.          |

### ◘ 1.1 Caso de Teste: Tentativa de Login:

| Passo  |  Descrição                                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Acessar a página de login.          |
| 2 |Inserir um e-mail válido e uma senha incorreta nos campos exibidos.          |
| 3 | Clicar no botão "Entrar" para tentar autenticar.          |
| 4 |Caso a senha esteja incorreta, será exibido um pop-up com a mensagem "Senha incorreta". O usuário deve clicar no botão de fechar para tentar realizar o login novamente          |
| 5 |	Inserir as credenciais corretas e clicar no botão "Entrar". O usuário será redirecionado para a página "Home".         |

### ◘ Resultados:
| Cenário  |  Resultado Esperado                                                       |   Resultado Alcançado  |
|--------|------------------------------------------------------------------|------------------------------------------------------------------|
| Login com senha correta | Request: 200 OK - Login bem-sucedido.          |  Usuário autenticado com sucesso. O token JWT foi gerado e armazenado no Local Storage. O usuário foi redirecionado para a página "Home".    |
| Login com senha incorreta | Request: 401 Unauthorized - Login não-sucedido.          |  Um pop-up exibiu a mensagem "Senha incorreta". O usuário não foi autenticado, e o token JWT não foi gerado. O usuário permaneceu na página de login.    |

## Testes

### ◘ 2.0 - Caso de Teste: Criação de Projetos

| Passo  | Descrição                                                                                  |
|--------|--------------------------------------------------------------------------------------------|
| 1      | Acessar a página "Seus Projetos".                                                         |
| 2      | Clicar no botão verde "Novo Projeto".                                                    |
| 3      | Preencher os campos obrigatórios, como nome do projeto, descrição e status inicial.      |
| 4      | Clicar no botão de confirmação para criar o projeto.                                    |

### ◘ Resultados:

| Resultado Esperado                                 | Resultado Alcançado                                                               |
|---------------------------------------------------|----------------------------------------------------------------------------------|
| Request: 201 Created - Projeto criado com sucesso | O novo projeto aparece listado na tela "Seus Projetos". Os dados foram salvos.  |

### ■ 2.1 - Caso de Teste: Edição e Exclusão de Projetos

| Passo  | Descrição                                                                                           |
|--------|---------------------------------------------------------------------------------------------------|
| 1      | Na página "Seus Projetos", localizar um projeto existente.                                       |
| 2      | Clicar no botão azul "Editar" para abrir os detalhes do projeto.                                 |
| 3      | Modificar as informações desejadas, como nome ou descrição, e clicar no botão de confirmação.  |
| 4      | Para testar a exclusão, clicar no botão vermelho "Excluir" e confirmar a exclusão.               |

### ◘ Resultados:

| Cenário          | Resultado Esperado                                          | Resultado Alcançado                                      |
|-------------------|------------------------------------------------------------|---------------------------------------------------------|
| Edição bem-sucedida | Request: 200 OK - Informações do projeto atualizadas com sucesso | Os dados foram alterados corretamente e salvos no backend. |
| Exclusão bem-sucedida | Request: 200 OK - Projeto removido com sucesso               | O projeto foi excluído e não aparece mais na lista.         |

---

### ◘ 3.0 - Caso de Teste: Criação de Tarefas no Projeto

| Passo  | Descrição                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------|
| 1      | Na página "Seus Projetos", clicar no botão azul "Entrar" em um projeto.                                        |
| 2      | Na página "Tarefas do Projeto", clicar no botão azul "Nova Tarefa".                                            |
| 3      | Preencher os campos obrigatórios, como nome da tarefa, descrição, prioridade, status inicial e data de vencimento. |
| 4      | Clicar no botão de confirmação para criar a tarefa.                                                            |

### ◘ Resultados:

| Resultado Esperado                                 | Resultado Alcançado                                                                 |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| Request: 201 Created - Tarefa criada com sucesso  | A nova tarefa aparece listada na tela "Tarefas do Projeto". Os dados foram salvos. |

### ◘ 3.1 - Caso de Teste: Edição e Exclusão de Tarefas

| Passo  | Descrição                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------|
| 1      | Na página "Tarefas do Projeto", localizar uma tarefa existente.                                           |
| 2      | Clicar no botão azul "Editar" para abrir os detalhes da tarefa.                                           |
| 3      | Modificar as informações desejadas, como nome ou descrição, e clicar no botão de confirmação.            |
| 4      | Para testar a exclusão, clicar no botão vermelho "Excluir" e confirmar a exclusão.                          |

### ◘ Resultados:

| Cenário          | Resultado Esperado                                          | Resultado Alcançado                                      |
|-------------------|------------------------------------------------------------|---------------------------------------------------------|
| Edição bem-sucedida | Request: 200 OK - Informações da tarefa atualizadas com sucesso | Os dados foram alterados corretamente e salvos no backend. |
| Exclusão bem-sucedida | Request: 200 OK - Tarefa removida com sucesso                | A tarefa foi excluída e não aparece mais na lista.         |

### ◘ Prints de Teste:

#### ◘ Caso de Teste: Login:
![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t3-gerenciamento-de-tarefas/blob/main/docs/img/1testeloginmobile.jpg)

#### ◘ Caso de Teste: Criação e Edição de Projetos:

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t3-gerenciamento-de-tarefas/blob/main/docs/img/1testeprojetomobile.jpg)

#### ◘ Caso de Teste: Criação e Edição de Tarefas:

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t3-gerenciamento-de-tarefas/blob/main/docs/img/1testetarefaprojetomobile.jpg)


# Referências

https://callstack.github.io/react-native-paper/

https://www.uninter.com/qualificacao-profissional/a-distancia/desenvolvimento-mobile-e-multiplataforma/?gad_source=1&gclid=Cj0KCQiAx9q6BhCDARIsACwUxu4-0J3M4mGmffC_M_QekadKyWBD7XLB_j2yCtc4kGH3HZUIL2Ohs-UaAphWEALw_wcB&gclsrc=aw.ds
