![TaskTide](https://github.com/user-attachments/assets/684f7dbf-3db6-49e7-a0fc-70560403f4e1)

# Taskide

Taskide es una potente aplicación de gestión de tareas que permite a los usuarios crear, actualizar y eliminar tareas de manera eficiente. Con un diseño moderno y funcionalidades intuitivas, Taskide facilita la organización y el seguimiento de tareas diarias, además de implementar autenticación de usuarios para asegurar un acceso controlado.

## Tecnologías Utilizadas

- **Backend**: Laravel
- **Frontend**: React, Next.js
- **Base de Datos**: MySQL
- **Control de Versiones**: Git
- **Entorno de Desarrollo**: Laragon

## Instalación

### Backend (Laravel)

1. **Clonar el Repositorio**:
   ```bash
   git clone https://github.com/Ghrout/Taskide.git
   ```

2. **Navegar al Directorio del Backend**:
   ```bash
   cd Taskide/backend
   ```

3. **Instalar las Dependencias de Laravel**:
   ```bash
   composer install
   ```

4. **Configurar el Archivo de Entorno**:
   - Copia el archivo `.env.example` a `.env`:
   ```bash
   cp .env.example .env
   ```
   - Configura los detalles de tu base de datos en el archivo `.env`.

5. **Generar la Clave de Aplicación**:
   ```bash
   php artisan key:generate
   ```

6. **Ejecutar las Migraciones**:
   ```bash
   php artisan migrate
   ```

7. **Iniciar el Servidor de Laravel**:
   ```bash
   php artisan serve
   ```

### Frontend (React y Next.js)

1. **Navegar al Directorio del Frontend**:
   ```bash
   cd Taskide/frontend
   ```

2. **Instalar las Dependencias de Node.js**:
   ```bash
   npm install
   ```

3. **Iniciar el Servidor de Desarrollo**:
   ```bash
   npm run dev
   ```

## Uso

- Accede a la aplicación en `http://localhost:3000`.
- Regístrate o inicia sesión para comenzar a gestionar tus tareas de manera eficiente.

## Si después de seguir los pasos no puedes ingresar sesión, asegúrate de realizar las siguientes acciones para corregir problemas relacionados con JWT y CORS:

Configurar la Clave Secreta de JWT: Si encuentras problemas de autenticación relacionados con el token, asegúrate de que la clave secreta de JWT esté configurada correctamente en tu archivo .env. Si no la tienes configurada, usa el siguiente comando para generarla:

```bash
JWT_SECRET=your_secret_key
php artisan jwt:secret
```
Instalar y Configurar CORS: Si tu aplicación frontend está en un dominio o puerto diferente al backend, es posible que necesites configurar CORS para permitir que las solicitudes del frontend lleguen al backend. Para ello, instala el paquete CORS con:

```bash
composer require fruitcake/laravel-cors

```
Luego, asegúrate de que la configuración de CORS permita solicitudes desde el origen de tu frontend. Revisa el archivo config/cors.php para confirmar que esté configurado correctamente.

## Contribución

¡Las contribuciones son bienvenidas! Si deseas contribuir a Taskide, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama:
   ```bash
   git checkout -b nombre-de-la-rama
   ```
3. Realiza tus cambios y haz commit:
   ```bash
   git commit -m "Descripción de los cambios"
   ```
4. Envía tus cambios a tu fork:
   ```bash
   git push origin nombre-de-la-rama
   ```
5. Abre un pull request.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
