# Configuración de AWS y CloudWatch

Para habilitar el envío de logs a **CloudWatch Logs** de AWS, necesitas definir algunas variables de entorno en tu sistema.

## Variables necesarias

```env
AWS_ACCESS_KEY_ID=TU_ACCESS_KEY
AWS_SECRET_ACCESS_KEY=TU_SECRET_KEY
AWS_SESSION_TOKEN=TU_SESSION_TOKEN (opcional, solo si usas sesión temporal)
AWS_REGION=us-east-1

CLOUD_WATCH_GROUP=NombreDelGrupoDeLogs
CLOUD_WATCH_STREAM=NombreDelStream
```

> ⚠️ Asegúrate de que las claves tengan los permisos necesarios para usar `logs:PutLogEvents`, `logs:CreateLogGroup`, `logs:CreateLogStream`, y `sts:GetCallerIdentity`.

## Cómo establecer variables en tu entorno

### En sistemas UNIX/macOS

Agrega esto a tu `.bashrc`, `.zshrc`, o ejecuta directamente:

```bash
export AWS_ACCESS_KEY_ID="..."
export AWS_SECRET_ACCESS_KEY="..."
export AWS_REGION="us-east-1"
export CLOUD_WATCH_GROUP="mi-grupo"
export CLOUD_WATCH_STREAM="mi-stream"
```

### En Windows (CMD)

```cmd
set AWS_ACCESS_KEY_ID=...
set AWS_SECRET_ACCESS_KEY=...
set AWS_REGION=us-east-1
set CLOUD_WATCH_GROUP=mi-grupo
set CLOUD_WATCH_STREAM=mi-stream
```

## Resultado

Una vez configurado correctamente, el logger enviará automáticamente los logs a CloudWatch además de imprimirlos por consola y almacenarlos localmente en la carpeta `logs/`.