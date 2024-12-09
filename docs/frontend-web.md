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

O design e os wireframes principais das páginas incluem:
- **Formulário de criação de projeto** (como visto nas imagens fornecidas), com campos de nome, descrição, data de início e data de fim do projeto, além de um botão para criar o projeto.
- **Listagem de Projetos**: Exibe todos os projetos criados pelo usuário, permitindo navegação fácil entre eles.

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

Instruções para implantar a aplicação distribuída em um ambiente de produção:

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.
4. Faça o deploy da aplicação no ambiente escolhido, seguindo as instruções específicas da plataforma de hospedagem.
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

## Testes

A estratégia de teste inclui:

1. Criação de casos de teste para cobrir todos os requisitos funcionais e não funcionais da aplicação.
2. Implementação de testes unitários para testar unidades individuais de código, como funções e classes.
3. Testes de integração para verificar a interação correta entre os componentes da aplicação.
4. Testes de carga para avaliar o desempenho da aplicação sob carga significativa.
5. Utilização de ferramentas de teste adequadas, como frameworks de teste e ferramentas de automação de teste, para agilizar o processo de teste.

## Referências

https://developer.mozilla.org/pt-BR/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_getting_started
https://pt-br.legacy.reactjs.org/docs/getting-started.html
