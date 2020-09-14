# Monitorear Linux desde la Web
En este espacio encontrarás el código del video ....

Para modificar el código, debes abrir en un editor de textos el archivo monitor_linux.sh.
La variable WEB_DIR deberá ser reemplazada con la ruta de tu directorio Web.

El archivo se ejecuta con el comando sudo ./monitor_linux.sh

## Configurar tarea con cron
Acceder como usuario root 

crontab -u root -e

Añadimos la tarea
*/5 * * * *  sudo /opt/monitorlinux.sh 2>&1 | logger -t monitortag

Se ejecutará cada 5 minutos e imprimirá los logs en syslog con la etiqueta monitortag.

Para dar seguimiento a los logs generados por la tarea, utilizamos el comando:

grep monitortag /var/log/syslog





