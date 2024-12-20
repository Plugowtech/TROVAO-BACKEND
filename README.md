# Partnership Backend

![JavaScript](https://img.shields.io/badge/JavaScript-%23F7DF1E.svg?style=flat&logo=javascript&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-%23336791.svg?style=flat&logo=postgresql&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-%23339933.svg?style=flat&logo=nodedotjs&logoColor=white)
![Status](https://img.shields.io/badge/status-em_desenvolvimento-yellow)

## Descrição

O backend do sistema **Partnership** é um serviço projetado para gerenciar parcerias entre empresas e profissionais,
como arquitetos, engenheiros e designers de interiores. O sistema oferece funcionalidades de cadastro, autenticação,
controle de dados administrativos e um sistema de pontos baseado em compras realizadas.

### Tecnologias

- **Linguagem**: JavaScript
- **Framework**: Node.js com Express
- **Banco de Dados**: PostgreSQL
- **Autenticação**: JSON Web Token (JWT)

---

## Funcionalidades

### Para Usuários:
1. **Cadastro de Profissionais e Empresas**:
   - Engenheiros, arquitetos e designers de interiores podem se registrar no sistema.
2. **Login Seguro**:
   - Autenticação baseada em JWT para usuários e administradores.
3. **Sistema de Pontuação**:
   - **Engenheiros/Arquitetos**: 1 ponto para cada R$ 1,00 em compras.
   - **Designers de Interiores**: 0,5 ponto para cada R$ 1,00 em compras.
4. **Acompanhamento de Pontos**:
   - Consulta de saldo e histórico de pontos acumulados.

### Para Administradores:
1. **Acesso Centralizado**:
   - Um único login administrativo com acesso completo.
2. **Manipulação de Dados**:
   - Controle de usuários, empresas e pontuações diretamente pelo painel administrativo.
3. **Validação de Dados**:
   - Administradores aprovam ou editam registros de usuários e empresas.

---

## Estrutura do Projeto

📂 partnership-backend ├── 📂 src │ ├── 📂 controllers # Controladores das rotas │ ├── 📂 models # Modelos de dados │ ├── 📂 routes # Rotas da API │ ├── 📂 services # Regras de negócio │ └── index.js # Entrada principal do servidor ├── 📂 config # Configurações do banco de dados e JWT ├── 📂 tests # Testes automatizados ├── .env.example # Exemplo de variáveis de ambiente ├── package.json # Dependências do projeto └── README.md # Documentação do projeto



---

## Endpoints Planejados

| Método  | Endpoint            | Descrição                            |
|---------|---------------------|--------------------------------------|
| POST    | `/login`            | Login de usuários e administradores |
| POST    | `/register`         | Cadastro de usuários                |
| GET     | `/users/:id`        | Consulta de dados de um usuário     |
| PATCH   | `/users/:id`        | Atualização de dados de usuários    |
| DELETE  | `/users/:id`        | Exclusão de um usuário              |
| GET     | `/points/:id`       | Consulta do saldo de pontos         |
| POST    | `/points/add`       | Adiciona pontos ao usuário          |

---

## Como Rodar o Projeto Localmente

### Pré-requisitos

- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- Editor de código, como [VS Code](https://code.visualstudio.com/)

### Passo a Passo

1. Clone o repositório:
  
   git clone https://github.com/Plugowtech/TROVAO-BACKEND.git
   cd TROVAO-BACKEND
Instale as dependências:

npm install
Configure as variáveis de ambiente:

Renomeie o arquivo .env.example para .env e configure os valores (ex.: credenciais do PostgreSQL).
Crie o banco de dados:

Certifique-se de que o PostgreSQL está rodando.
Execute as migrações:

npx sequelize-cli db:migrate
Inicie o servidor:

npm start
O backend estará disponível em http://localhost:3000.

Melhorias Futuras
Integração de Segurança:
Implementar proteção contra ataques de força bruta usando bibliotecas como express-rate-limit.
Validação de Dados:
Usar Joi ou Yup para validar os dados enviados pelos usuários.
Hospedagem:
Planejar a hospedagem em serviços como Heroku, AWS ou Railway.
Documentação da API:
Adicionar documentação automática com Swagger ou Postman.
Contribuições
Contribuições são bem-vindas!
Por favor, siga as etapas abaixo:

Faça um fork do repositório.
Crie sua branch para a funcionalidade: git checkout -b minha-feature.
Faça o commit das alterações: git commit -m 'Minha nova feature'.
Envie para o repositório remoto: git push origin minha-feature.
Abra um pull request.
Contato
Desenvolvido por Padua Vinicius (TROVÃO).

Email: fullstackpaduavinicius@gmail.com
LinkedIn: https://www.linkedin.com/in/ivan-vin%C3%ADcius-832821330/

