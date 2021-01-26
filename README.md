# Web Content Center On Docker WCC 🐳
Dockerfiles for running Oracle WebCenter Content, on Oracle Database

## Arquivos necessários pré-Instalação

Antes de começar faça o download dos arquivos do banco de dados nos links abaixo:

http://download.oracle.com/otn/linux/oracle12c/121020/linuxamd64_12102_database_1of2.zip
http://download.oracle.com/otn/linux/oracle12c/121020/linuxamd64_12102_database_2of2.zip

E deixe dentro de `./images/database/`

e baixe o WCC em:

https://www.oracle.com/middleware/technologies/webcenter-content-download.html#

E deixe dentro de `./images/wcc`

## Imagem de docker necessária ⚙

- Cadastra-se no oracle container registry para acessar as imagens da oracle.

https://container-registry.oracle.com/

- Após isso vá em Middleware Repositories > fmw-infrastructure e aceite os termos.

- Nisso vá no terminal e faça o login nos repository da oracle:

```sh
docker login container-registry.oracle.com
```

- Ao inserir user e senha então baixe a imagem:

```sh
docker pull container-registry.oracle.com/middleware/fmw-infrastructure:12.2.1.4
```
e depois: 
```sh
docker tag container-registry.oracle.com/middleware/fmw-infrastructure:12.2.1.4 oracle/fmw-infrastructure:12.2.1.4
```

## Para a build:

```docker-compose build```

## Para iniciar:

```docker-compose up```

