# TÍTULO DO PROJETO

`CURSO: Sistemas de Informação`

`DISCIPLINA: Projeto - Arquitetura de Sistemas Distribuídos`

`SEMESTRE: 6º`

O projeto em desenvolvimento tem como objetivo criar um sistema web de gerenciamento de tarefas. Essa ferramenta permitirá que os usuários organizem e acompanhem suas atividades diárias on-line, facilitando a gestão de suas responsabilidades e o cumprimento de prazos. Para os gestores e equipes, o sistema oferecerá uma plataforma para centralizar e priorizar tarefas, otimizando o fluxo de trabalho e a colaboração entre os membros. Em resumo, o sistema busca melhorar a produtividade individual e coletiva, aumentar a transparência no andamento das tarefas e a eficiência na execução de projetos.

## Integrantes

* Lucas Vinicius Oliveira Mendes
* João Victor Dias Lopes
* João Pedro Madeira Cristino

## Orientador

* Kléber Jacques Ferreira de Souza

# Planejamento

| Etapa         | Atividades |
|  :----:   | ----------- |
| ETAPA 1         |[Documentação de Contexto](docs/contexto.md) <br> |
| ETAPA 2         |[Planejar, desenvolver e gerenciar APIs e Web Services](docs/backend-apis.md) <br> |
| ETAPA 3         |[Planejar, desenvolver e gerenciar uma aplicação Web](docs/frontend-web.md) |
| ETAPA 4        |[Planejar, desenvolver e gerenciar uma aplicação Móvel](docs/frontend-mobile.md) <br>  |
| ETAPA 5         | [Apresentação](presentation/README.md) |
## Instruções de utilização

### Pré-requisitos  
Certifique-se de que os seguintes itens estão instalados em sua máquina:  
- **Node.js** (v16 ou superior) e npm (ou yarn)
- **.NET SDK** (versão 6 ou superior)
- **SQL Server** (ou outro banco de dados configurado no backend)
- **Expo CLI** (para executar o aplicativo mobile)
- **Git** (para clonar os repositórios do projeto)

---

### Configuração do Backend  
1. Clone o repositório do backend:  
   ```bash  
   git clone https://github.com/lucasviniciusom/GerenciamentoApiRest.git 
   cd GerenciamentoApiRest
   ```  

2. Instale as dependências do projeto:
   ```bash  
    dotnet restore
   ```   

4. Aplique as migrações para configurar o banco de dados: 
   ```bash  
   dotnet ef database update 
   ```

 5. Execute a aplicação:
   ```bash  
   dotnet run
   ```  

A API estará disponível em https://localhost:44374

---

### Configuração do Frontend Web  
1. Clone o repositório do frontend web:  
   ```bash  
   git clone https://github.com/lucasviniciusom/gerenciamento-front-api.git  
   cd gerenciamento-front-api
   ```  

2. Instale as dependências:  
   ```bash  
   npm install  
   ```  

3. Execute a aplicação em modo de desenvolvimento:  
   ```bash  
   npm start  
   ```  
A aplicação estará disponível em http://localhost:3000

---

### Configuração do Frontend Mobile  
1. Clone o repositório do frontend mobile:  
   ```bash  
   git clone https://github.com/lucasviniciusom/gerenciamento-mobile.git 
   cd gerenciamento-mobile
   ```  

2. Instale as dependências:  
   ```bash  
   npm install  
   ```  

3. Inicie o Expo Go:  
   ```bash  
   expo start  
   ```  

# Código

<li><a href="https://github.com/lucasviniciusom/gerenciamento-front-api">Front-end</a></li>
<li><a href="https://github.com/lucasviniciusom/gerenciamento-mobile">Mobile</a></li>
<li><a href="https://github.com/lucasviniciusom/GerenciamentoApiRest">Back-end</a></li>

# Apresentação

<li><a href="presentation/README.md"> Apresentação da solução</a></li>
