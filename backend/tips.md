# Tips

## Comprobar ataques por ssh

sudo tail -f /var/log/auth.log

- Solucion: Instalar fail2ban
- cat /var/log/fail2ban
- sudo fail2ban-client status sshd

sudo tail -f /var/log/auth.log

- Solucion: Instalar fail2ban
- cat /var/log/fail2ban
- sudo fail2ban-client status sshd
