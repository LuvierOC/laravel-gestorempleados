# Proyecto Laravel con Autenticación

Este proyecto es una aplicación Laravel que incluye autenticación básica (login) y utiliza PostgreSQL como base de datos. A continuación, se detallan los pasos para configurar y ejecutar el proyecto.

## Requisitos Previos

Asegúrate de tener instalados los siguientes requisitos previos en tu sistema:

- PHP 8.2-FPM
- Composer
- PostgreSQL
- Node.js y npm

## Instalación

Sigue estos pasos para instalar y configurar el proyecto:

1. **Clonar el Repositorio**

   Clona el repositorio del proyecto en tu máquina local:

   ```bash
   git clone https://github.com/usuario/proyecto-laravel.git
   cd proyecto-laravel
   ```

2. **Instalar Dependencias de PHP**

   Usa Composer para instalar las dependencias del proyecto:

   ```bash
   composer install
   ```

3. **Configurar el Archivo .env**

   Copia el archivo `.env.example` a `.env` y configura las variables de entorno. Asegúrate de configurar correctamente la conexión a la base de datos PostgreSQL:

   ```env
   DB_CONNECTION=pgsql
   DB_HOST=127.0.0.1
   DB_PORT=5432
   DB_DATABASE=nombre_de_tu_base_de_datos
   DB_USERNAME=tu_usuario
   DB_PASSWORD=tu_contraseña

   SESSION_DRIVER=database
   ```

4. **Generar la Clave de la Aplicación**

   Genera una clave de aplicación:

   ```bash
   php artisan key:generate
   ```

5. **Crear la Base de Datos**

   Crea la base de datos en PostgreSQL y asegúrate de que el nombre coincida con el configurado en el archivo `.env`.

6. **Ejecutar las Migraciones**

   Ejecuta las migraciones para crear las tablas necesarias en la base de datos:

   ```bash
   php artisan migrate
   ```

7. **Instalar Dependencias de Node.js**

   Usa npm para instalar las dependencias de Node.js:

   ```bash
   npm install
   npm run dev
   ```

## Uso

Para iniciar el servidor de desarrollo de Laravel, ejecuta:

```bash
php artisan serve
```

Por defecto, la aplicación estará disponible en `http://127.0.0.1:8000`.

## Características

- **Autenticación**: El proyecto incluye un sistema de autenticación básica (registro, login, restablecimiento de contraseña).
- **PostgreSQL**: Utiliza PostgreSQL como sistema de gestión de bases de datos.

## Migración de la Tabla de Sesiones

Si no tienes la tabla de sesiones creada, puedes generar la migración manualmente y ejecutarla:


3. **Ejecutar la Migración**

   ```bash
   php artisan migrate
   ```

## Contribuir

Si deseas contribuir al proyecto, por favor, sigue estos pasos:

1. Realiza un fork del repositorio.
2. Crea una rama nueva (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza los cambios necesarios y haz commits (`git commit -m 'Agregar nueva funcionalidad'`).
4. Sube los cambios a tu repositorio (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request en el repositorio original.

## Licencia

Este proyecto está licenciado bajo la licencia MIT. Consulta el archivo `LICENSE` para más información.

---

Con este README, deberías poder configurar y ejecutar tu proyecto Laravel con autenticación y PostgreSQL. Si tienes alguna pregunta o necesitas más ayuda, no dudes en contactarme.
