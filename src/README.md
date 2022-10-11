# This is where your Laravel or php app goes

Add your Laravel/php project here (or create a new blank one).

---

**Note:** IF exist problems generate the project delete this README.md

---

## Remember

The configuration of the database **must be the same on both sides** .

```dotenv
# .env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=db_name
DB_USERNAME=db_user
DB_PASSWORD=db_password
DB_ROOT_PASSWORD=secret
```

```dotenv
# src/.env
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=db_name
DB_USERNAME=db_user
DB_PASSWORD=db_password
```

The only change is the `DB_HOST` in the `src/.env` where is called to the container of `mysql`:

```dotenv
# src/.env
DB_HOST=mysql
```

---

## Help

A little help to create the project:

### Make a new Project

```sh
docker exec -it <container phpApache name or id> bash
```

```sh
composer create-project laravel/laravel .
```

### Copy Environment

```sh
cp .env.example .env
```

---

### Install Libraries from Node

```sh
docker-compose run --rm -w /var/www/html/<name_of_project> npm install
```

### Install Libraries from Composer

```sh
docker exec -it <container phpApache name or id> bash
```

```sh
composer install
```

### Clear/Clean the project

```sh
docker exec -it <container phpApache name or id> bash
```

```sh
php artisan clear:data
php artisan cache:clear
php artisan view:clear
php artisan route:clear
php artisan clear-compiled
php artisan config:cache
php artisan storage:link
```

### Generate Keys

```sh
docker exec -it <container phpApache name or id> bash
```

```sh
php artisan key:generate
```

### Run migrations

```sh
docker exec -it <container phpApache name or id> bash
```

```sh
php artisan migrate --seed
```