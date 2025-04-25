# helpers

## Configuración de la Conexión a la Base de Datos

Asegúrate de configurar correctamente la cadena de conexión en tu archivo `appsettings.json`:

```json
"ConnectionStrings": {
  "DB": "Server=YourServerName\\SQLEXPRESS; Database=YourDatabaseName; Integrated Security=true; Persist Security Info=False; TrustServerCertificate=True"
}
