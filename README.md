Opencart em LAMP server com Docker

Solução de E-Commerce Opencart em um LAMP server (Linux, Apache, MariaDB e PHP) com Docker.

Opencart:
Versão: 3.0.3.3 (13/06/2020)

Foram criados 3 containers;
 - WEB com PHP e Apache. exposto na porta 80.
 - DATABASE: Banco de Dados (MariaDB).
 - PHPMYADMIN: Gerenciamento remoto do banco de dados (via browser), exposto na porta 81.

A comunicação entre os containers são feitas através da rede interna do Docker, com nome MYNET, também criada no arquivo yml.

Informações:
As credenciais de acesso ao banco de dados (senha de root e usuário e senha de usuário)  devem ser alteradas no arquivo docker-compose.yml, nas linhas:

MYSQL_ROOT_PASSWORD: root
MYSQL_USER: admin
MYSQL_PASSWORD: admin

Para utilização desta stack, efetuar o clone do projeto e seguir conforme passos abaixo:

Pré-requisitos:
- Docker
- Docker compose
    A instalação dos pré requisitos poderão ser efetuadas conforme documentação oficial da solução, disponível em:
    https://docs.docker.com/engine/install/

Iniciando o ambiente:
    $ docker-compose up -d
        O ambiente será iniciado em background.

Após iniciado os containers, o acesso às soluções serão efetuados via browser:
 - Opencart: http://localhost/install
 - PHPMYADMIN: http://localhost:81