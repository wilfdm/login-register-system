# Proyecto Login y Registro con Vue y Laravel

Este proyecto es una aplicación simple de login y registro de usuarios usando **Vue 3** para el frontend y **Laravel** como backend. El proyecto permite a los usuarios registrarse, iniciar sesión y ver su perfil.

## Requisitos

Antes de ejecutar el proyecto, asegúrate de tener instalados los siguientes programas:

- **Node.js** y **npm** (para instalar dependencias del frontend)
- **PHP** (para ejecutar el servidor de Laravel)
- **Composer** (para gestionar las dependencias de Laravel)
- **SQLite** (como base de datos)

## Instalación y ejecución

Clona el repositorio en tu máquina local:

    git clone https://github.com/tu-usuario/login-register-system.git
    cd login-register-system


Instalación de dependencias del backend (Laravel)
Dentro del directorio del proyecto, instala las dependencias de Laravel utilizando Composer: 
    composer install


Configura el archivo .env
Copia el archivo .env.example y renómbralo a .env. Luego, configura los parámetros de la base de datos según tu configuración: 
    cp .env.example .env

Configura las variables de entorno en el archivo .env como sigue:
    DB_CONNECTION=sqlite
    DB_DATABASE=/ruta/a/tu/base-de-datos.sqlite

Ejecuta las migraciones de la base de datos
Realiza las migraciones para crear las tablas necesarias en la base de datos:
    php artisan migrate

Instalación de dependencias del frontend (Vue)
Dentro del directorio resources/js, instala las dependencias de Vue utilizando npm:
    cd resources/js
    npm install

Inicia el servidor de desarrollo
Para el backend de Laravel, ejecuta:
    php artisan serve

esto iniciará el servidor de Laravel en http://127.0.0.1:8000.

Para el frontend de Vue, ejecuta:
    npm run dev

Accede a la aplicación
Abre tu navegador y ve a http://localhost:3000 para ver la aplicación en acción.

Funcionalidades
Registro de usuario: Los usuarios pueden registrarse proporcionando su nombre, apellido, correo electrónico y contraseña.
Login: Los usuarios pueden iniciar sesión utilizando su correo electrónico y contraseña.
Perfil: Después de iniciar sesión, los usuarios pueden ver su perfil con su nombre y correo electrónico.
