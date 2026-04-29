<div align="center">
<img src="../assets/readme/banner.png" style="width: 400px">
</div>

<h1 align="center">Demo README</h1>

<p align="center"><b>README específico para la demo del proyecto Platinum</b><br>Proyecto Intermodular del Grado Superior de Desarrollo de Aplicaciones Web</p>

# índice

- [Preparación del entorno](#preparación-del-entorno)
  - [Versiones de las tecnologías](#versiones-de-las-tecnologías)
  - [Dependencias NPM](#dependencias-npm)
  - [Dependencias Maven](#dependencias-maven)
  - [Base de Datos](#base-de-datos)
- [Ejecución](#ejecución)
- [Uso de la demo](#uso-de-la-demo)
  - [Usuarios Disponibles](#usuarios-disponibles)
  - [Crear Usuario](#crear-usuario)
- [Que hacer?](#que-hacer)

# Preparación del entorno

Para ejecutar la demo de Platinum es necesario preparar el entorno de desarrollo. Para ello se deben seguir los siguientes pasos:

## Versiones de las tecnologías

Es necesario tener instaladas las siguientes tecnologías en las versiones indicadas para que la demo funcione correctamente:

| Tecnologia | Versión |
| ---------- | ------- |
| Node.js    | 18      |
| npm        | 11.11.1 |
| Angular    | 21.0.0  |
| JDK        | 21      |
| SpringBoot | 4.0.1   |
| Maven      | 3.9.12  |
| PostgreSQL | 17      |

> [!IMPORTANT]
> Es fundamental asegurar que todas las versiones de las tecnologías estén correctamente instaladas para que la demo funcione sin problemas. No aseguramos el correcto funcionamiento de la demo si se utilizan versiones diferentes a las indicadas. Se recomienda seguir las instrucciones de instalación de cada tecnología para asegurar que se instalen correctamente.

## Dependencias NPM

Se deben instalar las dependencias de npm necesarias para el correcto funcionamiento del proyecto. Para ello, se debe ejecutar el siguiente comando en la ruta `/demo/src/frontend`:

```powershell
npm install
```

Con esto se instalarán todas las dependencias necesarias para la ejecución de la demo. Es importante asegurarse de que no haya errores durante la instalación de las dependencias, ya que esto podría afectar el correcto funcionamiento de la demo.

## Dependencias Maven

Se deben instalar las dependencias de maven necesarias para el correcto funcionamiento del proyecto. Para ello, se debe ejecutar el siguiente comando en la ruta `/demo/src/backend`:

```powershell
mvn install
```

## Base de Datos

Para el uso de la demo es necesario restaurar la base de datos proporcionada en el archivo `platinum.sql` que se encuentra en la raíz de la carpeta `/demo/src`. Este archivo contiene toda la información necesaria para la correcta ejecución de la demo, incluyendo datos de usuarios, juegos y logros.

Para restaurar la base de datos, se debe seguir los siguientes pasos:
1. Abrir pgAdmin en la versión 9.11 o superior. Es necesario tener esta versión o superior para poder utilizar la opción de restaurar la base de datos desde un archivo SQL.
2. Crear una nueva base de datos con el nombre `platinum`. Para ello seguimos los siguientes pasos:
    - Click derecho en `Databases` -> `Create` -> `Database`
    - Nombre: `platinum`
    - Click en `Save`
3. Restaurar la base de datos desde el archivo `platinum.sql`. Para ello seguimos los siguientes pasos:
    - Click derecho en la base de datos `platinum` -> `Restore`
    - Formato: `Plain`
    - Seleccionar el archivo `platinum.sql` que se encuentra en la raíz de la carpeta `/demo/src`
    - Click en `Restore`

> [!NOTE]
> Es **importante** que el nombre de usuario y contraseña de la base de datos sean `postgres` y `root` respectivamente, ya que estos datos están configurados en el proyecto para la conexión a la base de datos. Si se utilizan otros datos, será necesario modificar la configuración del proyecto para que funcione correctamente.

# Ejecución

Una vez se han seguido todos los pasos anteriores, se puede proceder a la ejecución de la demo. Para ello, se deben ejecutar los siguientes comandos en las rutas correspondientes:

> [!IMPORTANT]
> Para que la demo funciona correctamente, es **fundamental** que la base de datos debe de estar en ejecución antes de ejecutar el servidor de desarrollo. Si se intenta ejecutar el servidor de desarrollo sin tener la base de datos en ejecución, es posible que se produzcan errores y la demo no funcione correctamente.

Se debe ejecutar el siguiente comando en la ruta `/demo/src/frontend`:

```powershell
ng serve
```

Y el siguiente comando en la ruta `/demo/src/backend`:

```powershell
mvn spring-boot:run
```

# Uso de la demo

Una vez se han ejecutado los comandos anteriores, se puede acceder a la demo de Platinum a través de la siguiente URL: `http://localhost:4200`. Es importante asegurarse de que el servidor de desarrollo esté en ejecución antes de intentar acceder a la demo, ya que de lo contrario no se podrá acceder a ella.

## Usuarios disponibles

En la demo se han creado tres usuarios con cuentas vinculadas de Steam para facilitar su uso y permitir la visualización de las funciones de la aplicación. Estos usuarios son:

| Nombre de usuario | Contraseña    |
| ----------------- | ------------- |
| Luis              | Luis12345     |
| Cristian          | Cristian12345 |
| Erik              | Erik12345     |

## Crear Usuario

Si se desea crear un nuevo usuario, se puede hacer a través de la página de registro de la demo. Una vez se ha creado el usuario, es necesario vincularlo con una cuenta de Steam para poder acceder a las funciones de la aplicación relacionadas con los juegos y logros. Para vincular una cuenta de Steam, se debe acceder al perfil de usuario y hacer click en el botón de vinculación de Steam. Es importante tener en cuenta que para vincular una cuenta de Steam, es necesario crear previamente una cuenta de Steam.

> [!IMPORTANT]
> Si se decide crear un usuario y vincularlo a una cuenta de Steam, es posible encontrarse un error. Una vez has iniciado tu sesión de Steam y se te redirige a la página de tu perfil de usuario en la demo, no verás tus datos hasta que no refresques la página.

# ¿Qué otras cosas se pueden hacer?

Una vez se ha accedido a la demo, las funcionalidades dependen de si estás logueado o no. Si no estás logueado, podrás acceder a las siguientes funcionalidades:
- Ver el catálogo de juegos.
- Buscar juegos.
- Buscar usuarios registrados.
- Ver la información de los juegos registrados, incluyendo sus logros y porcentajes de debloqueo global.
- Ver la información de los usuarios registrados, incluyendo sus juegos y logros.

Una vez estás logueado, además de las funcionalidades anteriores, podrás acceder a las siguientes funcionalidades adicionales:

- Acceder a tu perfil de usuario, dónde podrás ver tu información personal, tus juegos y logros.
- Si accedes a un juego desde tu perfil de usuario o en el perfil de otro usuario registrado y te diriges a la sección de logros, podrás ver los logros que dicho usuario (tú mismo u otro usuario registrado) ha obtenido en dicho juego.