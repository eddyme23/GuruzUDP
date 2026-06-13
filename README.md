UDP server installation for Hysteria-1, Http-Custom, SocksIP and ZiVPN Tunnel.
<br>

#### Installation
```
bash <(curl -sL https://raw.githubusercontent.com/eddyme23/GuruzUDP/master/udp.sh)
```
#### Check All Service Status
Run this command to confirm all services are green
```
systemctl status hysteria-server zivpn udp-custom udpgw
```
#### Validate NAT Rules
This ensures your traffic is actually being routed by checking your iptables.
You should see entries for both the 20000:50000 (Hysteria), SocksIP (1-65535) and 6000:19999 (ZiVPN)
```
iptables -t nat -L PREROUTING -v -n
```

           
----
Bash script by Eddme23 & Guruz GH
