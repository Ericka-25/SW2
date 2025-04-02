# SW2
cafeteria
esta en la RAMA MASTER EL PROYECTO.
Paso para desplegar:
-1- crear en postgres una db llamado inventarioDB
-2-ahora en la terminal de tallerWeb colocar esto:
  1. php artisan key:generate
  2. npm i
  3. npm run build
  4. php artisan migrate:fresh --seed
  5. ya creado inventarioDB ejecutar recien los scripts "CreateScript.sql" y "InsertScript.sql" en postgres
-3- el .env debe tener esto antes de desplegar los comandos anteriores:

APP_NAME=Laravel
APP_ENV=local
APP_KEY=base64:C6SlCnB6NBi+aF8asbOkAXGE7Y0UzqOI0D+0W6BFdB8=
APP_DEBUG=true
APP_TIMEZONE=UTC
APP_URL=http://localhost

APP_LOCALE=en
APP_FALLBACK_LOCALE=en
APP_FAKER_LOCALE=en_US

APP_MAINTENANCE_DRIVER=file
APP_MAINTENANCE_STORE=database

BCRYPT_ROUNDS=12

LOG_CHANNEL=stack
LOG_STACK=single
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=inventarioDB
DB_USERNAME=postgres
DB_PASSWORD=1234

SESSION_DRIVER=database
SESSION_LIFETIME=120
SESSION_ENCRYPT=false
SESSION_PATH=/
SESSION_DOMAIN=null

BROADCAST_CONNECTION=log
FILESYSTEM_DISK=local
QUEUE_CONNECTION=database

CACHE_STORE=database
CACHE_PREFIX=

MEMCACHED_HOST=127.0.0.1

REDIS_CLIENT=phpredis
REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=log
MAIL_HOST=127.0.0.1
MAIL_PORT=2525
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

VITE_APP_NAME="${APP_NAME}"


 (opcional)
LUEGO PARA QUE FUNCIONE LAS NOTOFICACIONES sw2-notificaciones-socket
abrir otra terminal : nodemon app (opcional)
