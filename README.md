🚀 API REST de Gerenciamento de Personagens (DBZ)

Este projeto consiste em uma Web API RESTful desenvolvida em C# com ASP.NET Core para gerenciamento de personagens. A aplicação foi construída seguindo boas práticas de arquitetura em camadas, com foco em organização, escalabilidade e fácil manutenção.

A API permite operações completas de CRUD, utilizando Entity Framework Core para persistência em banco MySQL, além de documentação interativa via Swagger.

📋 Funcionalidades

Cadastro de Personagens: Inclusão de novos personagens com suas respectivas características.

Listagem de Registros: Consulta de todos os personagens cadastrados.

Busca por ID: Recuperação de registros específicos.

Atualização de Dados: Edição de informações de personagens existentes.

Remoção de Registros: Exclusão de personagens do banco de dados.

Validação de Dados: Verificação básica dos dados recebidos pela API.

Documentação Interativa: Testes facilitados via Swagger.

Testes via Postman: Suporte completo para testes externos de API.

🏛️ Arquitetura do Projeto

A aplicação segue uma arquitetura em camadas (N-Tier / Clean-friendly), promovendo separação de responsabilidades e melhor manutenibilidade.

🔄 Fluxo da Requisição
Client → Controller → Service Layer → Repository/DbContext → MySQL

📊 Arquitetura do Sistema
![Projeto API DBZ](https://github.com/user-attachments/assets/3d9f6f83-7994-4ce1-9bbc-e2f6a5cfe566)

<iframe width="768" height="432" src="https://miro.com/app/live-embed/uXjVG5nqRMM=/?embedMode=view_only_without_ui&moveToViewport=-580,-244,899,814&embedId=755786054297" frameborder="0" scrolling="no" allow="fullscreen; clipboard-read; clipboard-write" allowfullscreen></iframe>

link: https://miro.com/app/live-embed/uXjVG5nqRMM=/?embedMode=view_only_without_ui&moveToViewport=-580%2C-244%2C899%2C814&embedId=755786054297

🔹 Camadas da Aplicação

Camada de Apresentação (Controllers)
Responsável por receber as requisições HTTP, validar entradas e retornar respostas padronizadas.

Camada de Aplicação / Serviços
Contém a lógica de negócio, regras e orquestração das operações.

Camada de Infraestrutura (Repository / DbContext)
Realiza o acesso ao banco de dados utilizando Entity Framework Core.

Camada de Persistência (MySQL)
Responsável pelo armazenamento físico dos dados.

🛠️ Tecnologias Utilizadas

Linguagem: C#

Framework: ASP.NET Core Web API

ORM: Entity Framework Core

Banco de Dados: MySQL

Documentação: Swagger (Swashbuckle)

Testes de API: Postman

IDE: VS Code

⚙️ Como Executar o Projeto
✅ Pré-requisitos

.NET SDK instalado

MySQL em execução

Git instalado

📥 Clone o repositório
git clone https://github.com/seu-usuario/projeto-dbz-api.git
cd projeto-dbz-api
🔧 Configure o banco de dados

Abra o arquivo appsettings.json

Ajuste a connection string:

"ConnectionStrings": {
  "DefaultConnection": "server=localhost;database=dbz;user=root;password=pedro3366987"
}
🗄️ Execute as migrations
dotnet ef database update
▶️ Execute a aplicação
dotnet run
📄 Acesse o Swagger
https://localhost:[5055]/swagger
📡 Exemplo de Endpoint
🔹 GET /api/personagens

Descrição: Retorna todos os personagens cadastrados.

Resposta (200 OK):

[
  {
    "id": 1,
    "nome": "Vegeta",
    "tipo": "Saiyajin"
  }
]
📈 Melhorias Futuras

 Implementar DTOs

 AutoMapper

 FluentValidation

 Autenticação JWT

 Testes unitários

 Docker

 CI/CD

✒️ Autor

Pedro Henrique
💼 Analista de TI | .NET | APIs REST
