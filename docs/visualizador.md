# Visualizador de Logs en Docker

Este proyecto incluye una herramienta visual basada en Docker que te permite explorar los archivos generados en la carpeta `logs/` de forma interactiva.

## 🚀 Ejecución

Para iniciar el visualizador, ejecuta el siguiente comando en tu terminal:

```bash
docker run -d -p 3000:3000 -e LOGS_DIR=/logs -v "/ruta/a/tu/carpeta/logs:/logs" maykolm/utec-logger:latest
```

📌 Reemplaza `"/ruta/a/tu/carpeta/logs"` con la ruta local donde se encuentren los archivos `.log`.

Por ejemplo:

```bash
docker run -d -p 3000:3000 -e LOGS_DIR=/logs -v "/home/ubuntu/logs:/logs" maykolm/utec-logger:latest
```

## 📁 ¿Qué hace?

* Escanea los archivos `.log` generados por `Logger`.
* Permite filtrarlos por **nombre**, **tipo** y **fecha**.
* Despliega el contenido en un panel accesible vía navegador web en [http://localhost:3000](http://localhost:3000).

## 🔒 Seguridad

Asegúrate de no exponer los logs sensibles si estás corriendo el contenedor en producción o ambientes accesibles por otros usuarios.