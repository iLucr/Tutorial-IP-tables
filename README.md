# Tutorial-IP-tables
1. Introdução
2. Requisitos de construção 
3. Notas de instalação


Introdução
-----------
O Iptable precisa ser implementado no servidor Linux. IpTable é um programa escrito em C para configurar protocolos de IPv4
o seguinte toturial implemneta o Iptables em um servidor linux


Requisitos de construção
-------------
Para conseguir utilizar o Iptables é necessario utiliza rum servidor, no caso foi utilizado um servidor VT Ubuntu, na mquina virtual 


Notas de instalação e verificação
-------------
Ao instalar todos os requisitos citados você deve fazer o seguinte:
Abrir o terminal e seu linux e digitar o seguinte comando 
</br>
$apt-get install iptables
Para seguir para o proximo passo voce deve entrar no administrador do sistemas 
</br>

$sudo su
Ao fazer isso, o proximo passo é listar o iptables e saber se as tabelas foram aceitas, o que vem por padrão
</br>
-# iptables -L

O proximo passo é tentar adiconar um IP na tabela input
</br>
-# iptables -A INPUT -i 10 -j ACCEPT
O IP 10 não é aceito 


 para saber um IP aceitavel fazer o seguinte comando
 </br>
-# host facebook
o comando host mais o dominio

O proximo passo é adicionar o IP no bloco e adiconar as permissões do IP
-# iptables -A INPUT -s 157.240.216.35 -j DROP
DROP no caso nega as permissões do IP 
Para verificar se as permissões fprma concedidas vamos utilizar o seguinte comando
</br>
-# ping 157.240.216.35
se não pingar, funcionou. 

Após feito isso utilizar o proximo comando para salvar as alterações 
</br>
-# -s iptables-save

Após, listar o bloco.
</br>
-# iptables -L


