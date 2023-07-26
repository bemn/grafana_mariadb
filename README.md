**Projeto Docker Compose - Grafana e MariaDB**

**Descrição**
Este projeto Docker Compose fornece uma configuração para criar dois contêineres: um contêiner MariaDB para o banco de dados e um contêiner Grafana para a visualização de dados. O Grafana estará disponível na porta 3001.

**Requisitos**
- Docker e Docker Compose instalados no sistema.

**Instruções**
1. Clone este repositório em sua máquina local;

2. Navegue para o diretório do projeto:

```
cd grafana_mariadb_docker
```

3. Crie um arquivo `.env` no diretório do projeto com as variáveis de ambiente:

```
DB_TYPE=mariadb
DB_DBNAME=grafana_db
DB_PORT=3306
DB_USER=grafana_user
DB_PASS=grafana_password
DB_HOST=mysql
JETTY_HOST=0.0.0.0
```

4. Inicie os contêineres com o Docker Compose:

```
docker-compose up -d
```

5. Após os contêineres serem iniciados, você pode acessar o Grafana em seu navegador em `http://localhost:3001`. Faça login com as credenciais:

```
Usuário: admin
Senha: admin
```

6. Agora você está pronto para configurar e visualizar seus painéis no Grafana.

**Personalização**
- Se necessário, você pode alterar as variáveis de ambiente no arquivo `.env` para refletir as configurações desejadas.
- Caso queira personalizar a configuração do Grafana, você pode editar o arquivo `grafana.ini` no diretório `conf`. Lembre-se de reiniciar o contêiner Grafana após fazer as alterações.

**Importante**
- Certifique-se de que as portas 3000 e 3001 não estejam sendo usadas por outros serviços em sua máquina, pois elas são as portas padrão para o Grafana.
- Os dados do MariaDB serão armazenados no diretório `./data/mysql-data` do projeto, garantindo persistência dos dados após a reinicialização dos contêineres.

**Referências**
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Grafana](https://grafana.com/)
- [MariaDB](https://mariadb.org/)

Aproveite o uso do Grafana para visualizar e analisar seus dados! Em caso de dúvidas ou problemas, sinta-se à vontade para entrar em contato com a equipe de suporte do Ligero ou consultar a documentação do Grafana para obter ajuda adicional.
