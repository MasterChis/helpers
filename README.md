# helpers

## Configuración de la Conexión a la Base de Datos

Asegúrate de configurar correctamente la cadena de conexión en tu archivo `appsettings.json`:

```json
"ConnectionStrings": {
  "DB": "Server=YourServerName\\SQLEXPRESS; Database=YourDatabaseName; Integrated Security=true; Persist Security Info=False; TrustServerCertificate=True"
}
```

## Scaffolding de la base de datos (SQL Server)
```cmd
dotnet ef dbcontext scaffold "Server=MASTERCHIS\SQLEXPRESS;Database=Kikis_DB;Integrated Security=True;TrustServerCertificate=True" Microsoft.EntityFrameworkCore.SqlServer -o Data
```
