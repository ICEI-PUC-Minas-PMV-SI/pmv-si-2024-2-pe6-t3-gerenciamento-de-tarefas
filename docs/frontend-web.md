# Front-end Web

O sistema de gerenciamento de tarefas é projetado para oferecer uma experiência eficiente e organizada no acompanhamento de projetos e tarefas. Isso permitirá que os usuários visualizem seus projetos, adicionem e editem tarefas, configurem notificações para lembretes e recebam relatórios personalizados. O objetivo é criar uma plataforma responsiva com navegação intuitiva, que simplifique o gerenciamento de tarefas e promova a produtividade.

## Tecnologias Utilizadas

- **ReactJS**: Para a criação de uma interface de usuário dinâmica e interativa.
- **Context API (React)**: Para gerenciamento de estado global na aplicação, garantindo que os dados fluam corretamente entre os componentes.

## Arquitetura

A aplicação está estruturada em componentes React dentro da pasta `src`. A divisão em componentes é a seguinte:

- **Navbar**: Responsável pela barra de navegação no topo da aplicação.
- **Pages**: Contém as páginas principais, como `AddProject`, `HomePage`, `LoginPage`, e `ProjectPage`.

Os arquivos de estilo estão localizados principalmente na pasta `src`, como `App.css` e `HomePage.css`, organizando o layout e estilo visual de cada página.

## Modelagem da Aplicação

A modelagem é baseada em uma estrutura simples de componentes para garantir a modularidade e a escalabilidade da aplicação. Cada página contém elementos principais para gerenciar o estado e enviar ou buscar dados da API, implementada no arquivo `api.js`. 

## Projeto da Interface Web

A interface web da aplicação de gerenciamento de tarefas será projetada para oferecer uma experiência de usuário limpa, intuitiva e focada na produtividade. O design visual segue uma abordagem minimalista e funcional, com cores suaves e ícones claros para guiar o usuário e evitar distrações. A interface busca uma organização lógica das funcionalidades para que os usuários possam navegar facilmente entre os projetos, tarefas e relatórios.

### Wireframes
Tela de Projetos:
![image](https://github.com/user-attachments/assets/3330a3d7-7fa1-46df-a9d1-75b1327fd7e5)

Tela de Tarefas:
![image](https://github.com/user-attachments/assets/25d07064-75be-49ff-a7ee-41dc7d0139a0)

![image](https://github.com/user-attachments/assets/ae56a033-fa3b-4247-bb9c-f6c66cb71f1b)

![image](https://github.com/user-attachments/assets/e847804e-a190-40d6-b3b1-5e3c87951acd)

![image](https://github.com/user-attachments/assets/607b9ae8-8d67-4d41-b3e8-ce3755779853)



### Design Visual

A interface usa uma paleta de cores neutras, com destaques em azul para botões e notificações importantes. Tipografia clara e espaçamento entre os elementos garantem uma leitura fácil e uma navegação intuitiva.

### Layout Responsivo

A interface da aplicação de gerenciamento de tarefas será projetada com um layout totalmente responsivo, garantindo que a experiência do usuário seja consistente e intuitiva em diferentes dispositivos, incluindo desktops, tablets e smartphones.

### Interações do Usuário

As interações serão projetadas para maximizar a eficiência. O usuário poderá adicionar e atualizar informações sem sair da página atual, utilizando pop-ups e modais para evitar recarregamentos de página. Animações suaves indicarão mudanças, como a atualização do status de uma tarefa, e as ações serão confirmadas visualmente (ex.: feedback de sucesso ou erro).

## Fluxo de Dados

O fluxo de dados segue uma arquitetura onde a aplicação React se comunica diretamente com a API do back-end para buscar e enviar dados. Ao acessar um projeto ou tarefa, os detalhes correspondentes serão recuperados via API, permitindo ao usuário visualizar, atualizar e gerenciar tarefas em tempo real. Essa abordagem garante que as interações dos usuários sejam refletidas instantaneamente na interface, promovendo uma experiência dinâmica e responsiva.

## Requisitos Funcionais

| ID     | Descrição do Requisito                                                                                                                                         | Prioridade |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| RF-001 | O sistema deve permitir que o usuário crie, edite e exclua tarefas, associando cada tarefa a um projeto específico.                                           | Alta       |
| RF-002 | O sistema deve possibilitar ao usuário configurar notificações para tarefas e projetos, alertando sobre prazos e atualizações por meio de pop-ups ou uma área de notificações. | Média      |
| RF-003 | O sistema deve gerar relatórios personalizados sobre o andamento dos projetos e tarefas, exibindo informações como número de tarefas concluídas, status dos projetos e tempo gasto em cada tarefa. | Média      |

## Requisitos Não Funcionais

| ID     | Descrição do Requisito                                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| RNF-001 | O sistema deve garantir que as páginas e componentes carreguem em menos de 2 segundos, mesmo em redes de baixa velocidade.          |
| RNF-002 | A aplicação deve ser escalável para suportar um número crescente de usuários e dados sem comprometer a performance.                 |

## Considerações de Segurança

A aplicação incluirá considerações de segurança, como autenticação de usuário, controle de acesso a dados, e proteção contra ataques comuns como SQL Injection e XSS (Cross-Site Scripting).

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

## Testes Front-End: Criação de Projetos e Tarefas

### 1.0 - Caso de Teste: Criação de Projetos

| Passo  | Descrição                                                                                                                 |
|-------|-------------------------------------------------------------------------------------------------------------------------|
| 1     | Acessar a aba "Projetos" na barra de navegação superior.                                                                      |
| 2     | Clicar no botão "Adicionar Novo Projeto".                                                                                  |
| 3     | Preencher os campos obrigatórios (título, descrição, data de início, data de término).                                         |
| 4     | Clicar no botão "Salvar".                                                                                                   |

#### Resultados:

| Cenário                   | Resultado Esperado                                                        | Resultado Alcançado                                              |
|----------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------|
| Campos preenchidos         | Request: 201 Created - Projeto criado com sucesso.                       | Projeto adicionado à lista e exibido na página "Todos os Projetos". |
| Campos obrigatórios vazios | Request: 400 Bad Request - Informações incompletas.                     | Exibição de mensagem de erro "Preencha todos os campos obrigatórios".|

### 2.0 - Caso de Teste: Criação de Tarefas em Projetos

| Passo  | Descrição                                                                                                                 |
|-------|-------------------------------------------------------------------------------------------------------------------------|
| 1     | Acessar um projeto existente na página "Todos os Projetos" clicando no botão "Editar".                                          |
| 2     | Navegar até a seção "Tarefas" do projeto.                                                                                 |
| 3     | Clicar no botão "Adicionar Nova Tarefa".                                                                                   |
| 4     | Preencher os campos obrigatórios (título, descrição, prioridade, data de vencimento).                                        |
| 5     | Clicar no botão "Salvar".                                                                                                   |

#### Resultados:

| Cenário                   | Resultado Esperado                                                        | Resultado Alcançado                                              |
|----------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------|
| Campos preenchidos         | Request: 201 Created - Tarefa criada com sucesso.                         | Tarefa adicionada à lista na seção "Tarefas" do projeto.           |
| Campos obrigatórios vazios | Request: 400 Bad Request - Informações incompletas.                     | Exibição de mensagem de erro "Preencha todos os campos obrigatórios".|


### ◘ Prints de Teste:

#### ◘ Caso de Teste: Criação e Edição de Projetos:

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t3-gerenciamento-de-tarefas/blob/main/docs/img/1testeprojetoweb.jpg)

#### ◘ Caso de Teste: Criação e Edição de Tarefas:

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe6-t3-gerenciamento-de-tarefas/blob/main/docs/img/1testetarefaweb.jpg)

### Observações:
- Verifique se os dados enviados estão sendo armazenados corretamente no banco de dados.
- Teste casos adicionais, como edição e exclusão de projetos e tarefas, para garantir a consistência das operações CRUD.
- Caso encontre bugs ou inconsistências, documente o comportamento observado e o esperado.



## Referências

https://developer.mozilla.org/pt-BR/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_getting_started
https://pt-br.legacy.reactjs.org/docs/getting-started.html
