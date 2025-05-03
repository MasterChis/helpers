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

## Generar token aleatorio (C#)
```cmd
public static string GenerateRandomString(int length) {
    
    string validChars = 
        "ABCDEFGHIJKLMNOPQRSTUVWXYZ" +
        "abcdefghijklmnopqrstuvwxyz" +
        "0123456789";

    Random random = new Random();
    StringBuilder password = new StringBuilder();

    for (int i = 0; i < length; i++) {
        int index = random.Next(validChars.Length);

        password.Append(validChars[index]);
    }

    return password.ToString();
}
```
