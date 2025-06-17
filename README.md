# E-commerce Emporio Grão
Site de uma loja online de venda de grãos
# 🚀 Começando
Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste.

Consulte Implantação para saber como implantar o projeto.
# 🔧 Instalação
  1. Certifique-se de ter o java jdk 17, SQL Server Management Studio instaladoe o Postman instalado.
  2. Baixe os dois arquivos: ecommerce.rar e o word do projeto de extensão.
  3. Extraia o .rar no seu local de preferência.
  4. Abra o SSMS, efetue o login via autenticação sql server e crie um banco com o comando "create dabatase (nome do banco)"
  5. Abra o Word baixado, em "4. Etapa 2", copie as duas views, a procedure e a trigger e cole no SSMS e execute (F5). Ps: certifique-se de estar usando o banco (use bd...).
  6. Abra a pasta ecommerce na IDE de sua preferência, abra /src/main/resources/application.properties e altere o:
     spring.datasource.username= "seu usuário"
     spring.datasource.password= "sua senha"
     spring.datasource.url=jdbc:sqlserver://tiago:1433;databaseName="---";encrypt=true;trustServerCertificate=true;
                                                                    /\ altere os --- para o nome do banco criado no SSMS
  8. Execute o backend, assim as tabelas serão criadas automaticamente no seu banco.
  9. Para ter certeza de que o backend e o banco estão 100%, abra o Postman, selecione GET e coloque a URL: http://localhost:8080/categorias. Se der um retorno "200 OK", está tudo funcionando.

# ⚙️ Executando os testes
  Nosso projeto é basicamente um CRUD, e todos os testes são feitos pelo POSTMAN.
  Para inserir, utilize o POST, para ler, o GET, para Atualizar o PUT e para deletar o DELETE.
  Todos os endpoints estão na classe controller. Ex: (POST > body > raw (JSON)) http://localhost:8080/cadastrar para criar um usuário novo, ou (GET) http://localhost:8080/produtos para ver todos os produtos cadastrados no sistema.

# 🛠️ Construído com
  SpringBoot - O framework web usado
  Maven - Gerente de Dependência

  # ✒️ Autores
  Desenvolvedores
  Tiago Garcia do Carmo e Caique Nogueira Silva
  Documentação
  Joyce Gabriella da Silva Mesquita
