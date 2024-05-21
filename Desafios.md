# Desafio:

####  Desafio 01 - Banco de DadosPostgreSQL
Crie um comando para criar um banco de dados PostgreSQL no ambiente do desenvolvedor de uma forma que cumpra os seguintes requisitos:
  * **O nome do banco de dados deve ser curso_docker** 
  * **O usuário de acesso ao banco deve ser docker_usr**
  * **A senha do usuário deve ser docker_pwd**
  
Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.
Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados PostgreSQL com esses requisitos.

    #docker container run -d -p 5432:5432 --name postsql -e POSTGRES_DB=curso_docker -e POSTGRES_PASSWORD='docker_pwd' -e POSTGRES_USER=docker_usr  postgres
    
    #docker ps
    CONTAINER ID   IMAGE      COMMAND                  CREATED          STATUS          PORTS                                       NAMES
    41a8fc60d17aa   postgres   "docker-entrypoint.s…"   2 minutes ago    Up 2 minutes    0.0.0.0:5432->5432/tcp, :::5432->5432/tcp              postsql

    #docker rm -f $(docker ps -qa)
    42e1b78b41a5
    f4e5dab09495

#### Desafio 02 - Banco de Dados MySQL
Crie o comando pra criar o banco de dados MySQL usando os requisitos abaixo:

  * **O nome do banco de dados deve ser docker_db**
  * **O usuário de acesso ao banco deve ser docker_usr**
  * **A senha do usuário deve ser docker_pwd**

Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual. Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados MySQL com esses requisitos:

    #docker container run -d -p 3306:3306  --name mysql -e MYSQL_ROOT_PASSWORD=curso123 -e MYSQL_USER=docker_usr -e MYSQL_PASSWORD=docker_pwd -e MYSQL_DATABASE=docker_db  mysql
    8a0d7638bc935bb695161eb99f960722788a2e5a651f4b54e39e8b4115f1e642

    #docker ps
    CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                                                  NAMES
  2a94b6fcc22b   mysql      "docker-entrypoint.s…"   6 minutes ago    Up 6 minutes    0.0.0.0:3306->3306/tcp, :::3306->3306/tcp, 33060/tcp   mysql

#### Desafio 03 - Banco de Dados MongoDB
Crie o comando pra criar o banco de dados MongoDB usando os requisitos abaixo:

  * **O usuário root do banco deve ser mongo_usr**
  * **A senha do usuário root deve ser mongo_pwd**

Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual. Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados MongoDB com esses requisitos:

    #docker container run -d -p 27017:27017  --name mongo -e MONGO_INITDB_ROOT_USERNAME=mongo_usr -e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd mongo
    e28756022bc0c336b2f8905e822804e8e97aa56dbebe57daee9a2dfe395c781

    #docker ps
    d468f53f2a01   mongo      "docker-entrypoint.s…"   2 minutes ago        Up 2 minutes        0.0.0.0:27017->27017/tcp, :::27017->27017/tcp          dbmongo

#### Final`
    #docker ps
    CONTAINER ID   IMAGE      COMMAND                  CREATED          STATUS          PORTS                                                  NAMES
    e28756022bc0   mongo      "docker-entrypoint.s…"   4 seconds ago    Up 3 seconds    0.0.0.0:27017->27017/tcp, :::27017->27017/tcp          mongo
    1a8fc60d17aa   postgres   "docker-entrypoint.s…"   6 minutes ago    Up 6 minutes    0.0.0.0:5432->5432/tcp, :::5432->5432/tcp              postsql
    2a94b6fcc22b   mysql      "docker-entrypoint.s…"   10 minutes ago   Up 10 minutes   0.0.0.0:3306->3306/tcp, :::3306->3306/tcp, 33060/tcp   mysql

![Desafio1.png](./img/desafios.png)
