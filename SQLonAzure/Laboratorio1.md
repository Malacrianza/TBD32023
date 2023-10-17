### Guía Paso a Paso: Creación de una Base de Datos SQL en Azure

#### 1. Crear una Suscripción en Azure:

- Dirígete a [Azure Portal](https://portal.azure.com/).
- Haz clic en "Crear una cuenta gratuita".
- Sigue las instrucciones proporcionadas, como ingresar la información de pago, verificar tu identidad, etc. (No se te cobrará si estás en el período gratuito).
  
#### 2. Acceso al Portal de Azure:

- Una vez que hayas configurado tu cuenta, ingresa con tus credenciales en [Azure Portal](https://portal.azure.com/).

#### 3. Aprovisionamiento de un Servidor SQL:

1. En el menú izquierdo del portal de Azure, haz clic en "Crear un recurso".
2. En el cuadro de búsqueda, escribe "SQL Server" y selecciona "SQL Server (versión lógica)".
3. Haz clic en "Crear".
4. Llena los campos requeridos:
   - **Nombre del servidor**: Elige un nombre único.
   - **Suscripción**: Selecciona tu suscripción.
   - **Grupo de recursos**: Puedes crear uno nuevo o usar uno existente.
   - **Ubicación**: Elige la región geográfica donde quieres que esté ubicado tu servidor.
   - **Nombre de usuario del administrador**: Crea un nombre de usuario.
   - **Contraseña**: Crea y confirma una contraseña.
5. Haz clic en "Revisar + crear" y luego en "Crear" para provisionar el servidor.

#### 4. Creación de una Base de Datos SQL en Azure:

1. En el menú izquierdo, haz clic en "Crear un recurso".
2. Busca "Base de datos SQL" y selecciónalo.
3. Haz clic en "Crear".
4. Completa los campos requeridos:
   - **Nombre de la base de datos**: Ingresa el nombre deseado.
   - **Suscripción**: Selecciona tu suscripción.
   - **Grupo de recursos**: Usa el que elegiste/creaste anteriormente.
   - **Seleccionar fuente**: Elige "Ninguno" para una base de datos vacía o "Copia de seguridad" si tienes un respaldo.
   - **Servidor**: Selecciona el servidor que creaste anteriormente.
5. Haz clic en "Revisar + crear" y luego en "Crear".

#### 5. Importar Bases de Datos de Ejemplo OLTP y DWH:

Para este proceso, consideraremos que ya tienes archivos .bak (copias de seguridad) para OLTP y DWH.

1. Ve al servidor SQL que creaste.
2. Selecciona "Bases de datos" en el menú de la izquierda y haz clic en tu base de datos.
3. En el menú de la izquierda, busca la sección "Operaciones" y selecciona "Restaurar base de datos".
4. Elige "Desde una copia de seguridad" y sube tus archivos .bak de OLTP y DWH.
5. Sigue las instrucciones para restaurar la base de datos.

#### Notas:

- Las bases de datos de ejemplo, como AdventureWorks (OLTP) o AdventureWorksDW (DWH), podrían no estar disponibles directamente para Azure SQL Database. Es posible que necesites restaurarlos primero en un SQL Server local y luego usar herramientas como [Azure Data Migration Service](https://azure.microsoft.com/en-us/services/database-migration/) para migrar a Azure SQL Database.
  
- Asegúrate de configurar correctamente las reglas de firewall en tu servidor SQL en Azure para permitir conexiones desde tu IP o las IPs que necesites.

Espero que esta guía te sea útil para establecer tu base de datos SQL en Azure. ¡Buena suerte!
