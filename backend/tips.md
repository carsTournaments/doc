# Tips

## Comprobar ataques por ssh

sudo tail -f /var/log/auth.log

* Solucion: Instalar fail2ban
* cat /var/log/fail2ban
* sudo fail2ban-client status sshd

Para obtener un **listado con el número de veces que ha sido bloqueada cada una de las IP** ejecutaremos el siguiente comando en la terminal:

> zgrep -h "Ban " /var/log/fail2ban.log\* | awk '{print $NF}' | sort | uniq -c

Si pretendemos obtener un **listado las IP que han sido bloqueadas durante el día** de hoy ejecutamos el siguiente comando:

> grep "Ban " /var/log/fail2ban.log | grep `date +%Y-%m-%d` | awk '{print $NF}' | sort | awk '{print $1,"("$1")"}' | logresolve | uniq -c | sort -n

En el caso que pretendamos obtener un **listado del número de bloqueos por día y por servicio** ejecutaremos el siguiente comando:

> zgrep -h "Ban " /var/log/fail2ban.log\* | awk '{print $5,$1}' | sort | uniq -c





**`sudo lsof -PiTCP -sTCP:LISTEN`**

Nos muestra las aplicaciones y los puertos que se estan usando
