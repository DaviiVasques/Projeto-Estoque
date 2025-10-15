# Sistema de Gestão de Catálogo de Produtos

Este é um projeto full-stack de gerenciamento de catálogo de produtos desenvolvido com .NET Core, atendendo aos requisitos de um sistema robusto de gestão de dados empresariais.

## 🏆 Funcionalidades

- **CRUD Completo**: Criar, ler, atualizar e deletar produtos
- **APIs REST**: Endpoints para integração com outros sistemas
- **API SOAP**: Serviço SOAP para interoperabilidade
- **Interface Web**: UI responsiva com HTML5, CSS3 e JavaScript ES6+
- **Banco de Dados**: SQLite com Entity Framework Core
- **Importação/Exportação**: Módulo PHP para CSV (diferencial)
- **Versionamento**: Git para controle de versão

## 🛠️ Tecnologias Utilizadas

### Back-End
- **.NET Core 9.0** (MVC com Razor Pages)
- **Entity Framework Core** para ORM
- **SQLite** como banco de dados
- **SoapCore** para serviços SOAP

### Front-End
- **HTML5** e **CSS3** (Bootstrap para responsividade)
- **JavaScript ES6+** para interações dinâmicas
- **jQuery** para AJAX

### APIs
- **REST API**: Controllers ASP.NET Core
- **SOAP API**: Serviço WSDL

### Diferencial
- **PHP 8+** com POO para importação/exportação CSV

## 📁 Estrutura do Projeto

```
ProductCatalogSystem/
├── Controllers/           # Controllers REST API
├── Data/                  # Contexto do banco de dados
├── Models/                # Modelos de dados
├── Pages/                 # Razor Pages (UI)
├── Services/              # Serviços SOAP
├── wwwroot/               # Assets estáticos
├── php/                   # Scripts PHP para import/export
├── Migrations/            # Migrations EF Core
└── Program.cs             # Configuração da aplicação
```

## 🚀 Como Executar

### Pré-requisitos
- .NET 9.0 SDK
- PHP 8+ (para funcionalidade de import/export)
- Git

### Passos para Execução

1. **Clone o repositório**:
   ```bash
   git clone <url-do-repositorio>
   cd ProductCatalogSystem
   ```

2. **Restaure as dependências**:
   ```bash
   dotnet restore
   ```

3. **Execute as migrações do banco**:
   ```bash
   dotnet ef database update
   ```

4. **Execute a aplicação**:
   ```bash
   dotnet run
   ```

5. **Acesse a aplicação**:
   - Interface Web: http://localhost:5163
   - API REST: http://localhost:5163/api/produtos
   - API SOAP: http://localhost:5163/ServicoProduto.svc

## 📡 APIs Disponíveis

### REST API
- `GET /api/produtos` - Lista todos os produtos
- `GET /api/produtos/{id}` - Obtém produto por ID
- `POST /api/produtos` - Cria novo produto
- `PUT /api/produtos/{id}` - Atualiza produto
- `DELETE /api/produtos/{id}` - Remove produto

### SOAP API
- Serviço `IServicoProduto` com métodos equivalentes

### PHP Import/Export
- `GET /php/export.php` - Exporta produtos para CSV
- `POST /php/import.php` - Importa produtos do CSV

## 🎨 Interface Web

A interface oferece:
- Listagem de produtos com paginação
- Formulário para adicionar/editar produtos
- Botões para exportar/importar CSV
- Design responsivo e acessível

## 🗄️ Banco de Dados

### Tabela Produto
- `Id` (int, PK)
- `Nome` (string, obrigatório)
- `Descricao` (string)
- `Preco` (decimal, obrigatório)
- `QuantidadeEstoque` (int)
- `DataCriacao` (datetime)

## 🔧 Configuração

### Connection String
Localizada em `appsettings.json`:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=ProductCatalog.db"
  }
}
```

### PHP
Certifique-se de que o PHP está instalado e no PATH do sistema para a funcionalidade de import/export.

## 📝 Scripts Úteis

```bash
# Limpar e reconstruir
dotnet clean && dotnet build

# Executar testes (se houver)
dotnet test

# Criar nova migração
dotnet ef migrations add NomeDaMigracao

# Atualizar banco
dotnet ef database update
```

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 👨‍💻 Autor

Desenvolvido como projeto de demonstração de habilidades em desenvolvimento full-stack.

---

**Nota**: Este projeto atende aos requisitos técnicos especificados, incluindo back-end robusto, APIs REST e SOAP, proficiência em SQL, front-end responsivo e acessível, versionamento Git e módulo PHP como diferencial.
