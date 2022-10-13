# SSH #

>
O SSH é um serviço que permite o acesso remoto a uma máquina que possui um SSH Server executando.
>
>

>
## Instalação do SSH Server ##

> 
A sequencia de comandos abaixo autualiza os pacotes do Linux e em seguida instala o SSH Server.
>

```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install openssh-server
```
>

## Comandos para verificar o serviço SSH ##

### Iniciar um servidor SSH ### Iniciar
>
```
sudo systemctl start ssh.service
```
>

### Parar um servidor SSH ### 
>
```
sudo systemctl stop ssh.service
```
>
### Reiniciar um servidor SSH ###
>
```
sudo systemctl restart ssh.service
```
>
