
# Docker Symfony Mysql Apache phpMyAdmin

A very simple Docker-compose to discover Symfony 6 with PHP 8.0.13
## Run Locally

Clone the project

```bash
  git@github.com:yoanbernabeu/symfony6-php8-in-docker-compose.git
```

Run the docker-compose

```bash
  docker-compose build
  docker-compose up -d
```

Log into the PHP container

```bash
  docker exec -it php8-sf6 bash
```

Create your Symfony application and launch the internal server

```bash
  symfony new new-project --full
  cd new-project
  symfony serve -d
```

Create an account (identical to your local session)

```bash
  adduser username
  chown username:username -R .
```

*Your application is available at http://127.0.0.1:9000*

If you need a database, modify the .env file like this example:

```yaml
  DATABASE_URL=mysql://root:password@database:3306/main?serverVersion=5.7
```

## Ready to use with

This docker-compose provides you :

- PHP-8.0.13-cli (Debian)
    - Composer
    - Symfony CLI
    - and some other php extentions
    - nodejs, npm, yarn
- mysql


## Author

- [@hugolebihan56](https://github.com/hugolebihan56)

