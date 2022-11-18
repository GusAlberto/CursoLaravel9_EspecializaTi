# Curso de Laravel 9

Curso de Laravel 9 pelo canal @EspecializaTi criado pelo Carlos Ferreira

## Setup Docker Para Projetos Laravel

### Passo a passo
Clone Repositório
```sh
<<<<<<< HEAD
git clone https://github.com/GusAlberto/Curso_Laravel9.git
```
```sh
cd my-project/
```


Alterne para a branch laravel 9.x
```sh
git checkout laravel-9-com-php-8
```


Remova o versionamento (opcional)
```sh
rm -rf .git/
```


=======
git clone https://github.com/especializati/setup-docker-laravel.git
```

Clone os Arquivos do Laravel
```sh
git clone https://github.com/laravel/laravel.git app-laravel
```


Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -rf setup-docker-laravel/* app-laravel/
```
```sh
cd app-laravel/
```

>>>>>>> fcc2156caf253f0c23a1846226019955e6db750f
Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME="Curso Laravel"
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acesse o container app com o bash
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```


Gere a key do projeto Laravel
```sh
php artisan key:generate
```


Acesse o projeto
[http://localhost:8989](http://localhost:8989)
