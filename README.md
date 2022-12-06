# Tutorial-IP-tables
1. Introdução
2. Requisitos de construção 
3. Notas de instalação


Introdução
-----------
Notas de instalação e verificação
----------
Ao instalar todos os requisitos citados você deve fazer o seguinte:
Abrir o terminal e seu linux e digitar o seguinte comando 
$apt-get install iptables
Para seguir para o proximo passo voce deve entrar no administrador do sistemas 
$sudo su
Ao fazer isso, o proximo passo é listar o iptables
# iptables -L
# iptables -A INPUT -i 10 -j ACCEPT
# host facebook
# iptables -A INPUT -i 157.240.216.35 -j DROP
# ping 157.240.216.35
# -s iptables-save
# iptables -L
# iptables -A INPUT -s 157.240.216.35 -j DROP
# iptables -L --line-number
