# Uso del Logger

## Importación

Primero, importa el logger y los niveles disponibles:

```python
from utec_logger.logger import logger, Level
```

## Log Básico

```python
logger.info("Mensaje informativo")
logger.warning("Mensaje de advertencia")
logger.error("Mensaje de error")
logger.critical("Mensaje crítico")
```

## Log personalizado

También puedes usar la función general:

```python
logger.log("Este es un mensaje personalizado", level=Level.WARNING)
```

---

El logger mostrará mensajes con formato como este:

```
2025-05-02 15:45:33.123 | INFO | main.py:42 | Mensaje informativo
```

Y los almacenará en un archivo `.log` bajo la carpeta `/logs`, con nombre basado en la fecha y hora de ejecución.