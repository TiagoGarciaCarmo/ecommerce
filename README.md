# 🛒 E-commerce Empório Grão
Site de uma loja online de venda de grãos, com funcionalidades de cadastro, consulta, atualização e exclusão de produtos, categorias e usuários.

---

## 🚀 Começando
Essas instruções permitirão que você obtenha uma cópia do projeto funcionando localmente para fins de desenvolvimento e testes.

---

## 🔧 Instalação

### Pré-requisitos:
- Java JDK 17
- Spring Boot
- Maven
- SQL Server Management Studio (SSMS)
- Postman

### Passos:

1. Baixe os arquivos:
   - `ecommerce.rar` (projeto Spring Boot)
   - Documento Word com o projeto de extensão

2. Extraia o `.rar` no local de sua preferência.

3. No SSMS:
   - Faça login via **Autenticação SQL Server**
   - Crie o banco de dados:
     ```sql
     CREATE DATABASE NomeDoBanco;
     ```
   - No Word, vá até a seção **4. Etapa 2**, copie e execute no SSMS:
     - As **duas views** (vw_usuarios_compras) e (vw_usuarios_compras_detalhado)
     - A **procedure** (sp_registrar_compra_com_itens)
     - A **trigger** (trg_atualizar_estoque)
   > Certifique-se de estar usando o banco correto:
   ```sql
   USE NomeDoBanco;

  6. Abra a pasta ecommerce na IDE de sua preferência, abra /src/main/resources/application.properties e altere o:
     - spring.datasource.username= "seu usuário"
     - spring.datasource.password= "sua senha"
     - spring.datasource.url=jdbc:sqlserver://tiago:1433;databaseName="---";encrypt=true;trustServerCertificate=true;
  8. Execute o backend, o Hibernate criará automaticamente as tabelas no banco.
  9. Teste no POSTMAN:
     - Método GET:
     - http://localhost:8080/categorias
     - Se o retorno for 200 OK, a API está funcionando corretamente.

 ## ⚙️ Executando os testes (POSTMAN)
  | Operação  | Método | URL Exemplo                           | Observação                |
  | --------- | ------ | ------------------------------------- | ------------------------- |
  | Criar     | POST   | `http://localhost:8080/cadastrar`     | Body em JSON              |
  | Consultar | GET    | `http://localhost:8080/produtos`      | Retorna lista de produtos |
  | Atualizar | PUT    | `http://localhost:8080/produtos/{id}` | Body com os novos dados   |
  | Deletar   | DELETE | `http://localhost:8080/produtos/{id}` | Remove produto do sistema |
 

  ## 🛠️ Tecnologias Utilizadas
  - SpringBoot - O framework web usado
  - Maven - Gerente de Dependência
  - SQL Server - Banco de dados relacional

  ## ✒️ Autores
  - Caique Nogueira Silva — Desenvolvedor
  - Joyce Gabriella da Silva Mesquita — Documentação
  - Tiago Garcia do Carmo — Desenvolvedor
