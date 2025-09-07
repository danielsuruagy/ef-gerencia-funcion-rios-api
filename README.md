# Projeto ASP.NET Core para Gerenciar Funcionários

## 💻 Tecnologias

- .NET C#
- Entity Framework Core (SQL Server)
- Azure Table Storage
- Swagger para documentação da API

## 🚀 Funcionalidades

### CRUD de Funcionários

- GET /Funcionario/{id} → Obter funcionário por ID  
- POST /Funcionario → Criar funcionário  
- PUT /Funcionario/{id} → Atualizar funcionário  
- DELETE /Funcionario/{id} → Remover funcionário  

### Registro de Logs

Sempre que um funcionário é criado, atualizado ou deletado, um log é gravado em FuncionarioLog. Cada log contém:

- PartitionKey → Departamento do funcionário  
- RowKey → GUID único  
- JSON com os dados do funcionário  
- Tipo de ação (Inclusao, Atualizacao, Remocao)
