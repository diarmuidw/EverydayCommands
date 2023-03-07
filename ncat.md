# NCat examples

## Listener (Windows) 
Install using nmap
~~~
ncat -v -ulp 514
~~~

##Sender (Windows)
~~~
ncat.exe -uv <ip_address> 514
~~~
(specify port as ncat uses tcp by default)
~~~
ncat -v -u <ipaddress> 53 
~~~

## Ncat as a proxy or relay  (Linux)
from https://www.linuxtechi.com/nc-ncat-command-examples-linux-systems/ 
~~~
ncat -l 8080 | ncat 192.168.1.200 80
~~~
