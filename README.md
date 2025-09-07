# Projeto ASP.NET Core para Gerenciar Funcionários

## 🚀 Funcionalidades

### CRUD de Funcionários

- `GET /Funcionario/{id}` → Obter funcionário por ID  
- `POST /Funcionario` → Criar funcionário  
- `PUT /Funcionario/{id}` → Atualizar funcionário  
- `DELETE /Funcionario/{id}` → Remover funcionário  

### Registro de Logs

Sempre que um funcionário é criado, atualizado ou deletado, um log é gravado em `FuncionarioLog`.

Cada log contém:

- `PartitionKey` → Departamento do funcionário  
- `RowKey` → GUID único  
- JSON com os dados do funcionário  
- Tipo de ação (`Inclusao`, `Atualizacao`, `Remocao`)


## ⚙️ Como Funciona

1. A aplicação salva o funcionário no SQL Server utilizando Entity Framework.  
2. Em seguida, cria um `FuncionarioLog` e grava no Azure Table Storage.

## 🛠️ Tecnologias

- .NET C#
- Entity Framework Core (SQL Server)
- Azure Table Storage
- Swagger para documentação da API
