# Front-end Móvel

O Gerenciador de Tarefas Mobile é um aplicativo projetado para oferecer uma experiência eficiente e organizada no acompanhamento de projetos e tarefas diretamente no celular. Com uma interface intuitiva e responsiva, o app permite que os usuários visualizem seus projetos, adicionem e editem tarefas, configurem notificações personalizadas para lembretes importantes e acessem relatórios detalhados, tudo na palma da mão. Além disso, o aplicativo é focado em promover a produtividade, simplificando o gerenciamento de tarefas em qualquer lugar, a qualquer momento.

## Tecnologias Utilizadas

As seguintes tecnologias foram utilizadas no desenvolvimento deste projeto:

◘ HTML;

◘ CSS;

◘ JavaScript;

◘ React Native;

## Arquitetura

[Descrição da arquitetura das aplicação móvel, incluindo os componentes e suas interações.]

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
[Inclua os wireframes das páginas principais da interface, mostrando a disposição dos elementos na página.]

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

[Diagrama ou descrição do fluxo de dados na aplicação.]

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

[Discuta as considerações de segurança relevantes para a aplicação distribuída, como autenticação, autorização, proteção contra ataques, etc.]

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
