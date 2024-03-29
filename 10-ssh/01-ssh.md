# SSH #

>
O SSH é um serviço que permite o acesso remoto a uma máquina que possui um SSH Server executando.
>
>
O Processo que executa o SSH Server é chamado de sshd. Daemon de ssh server.
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

### Verificar se o pacote ssh server está instalado no Linux ###
>
```
$ sudo dpkg -l | less | grep ssh

```
>

### Iniciar um servidor SSH ### Iniciar
>
```
$ sudo systemctl start ssh.service
```
>
>
No WSL usar o comando `sudo service ssh start`
>

### Parar um servidor SSH ### 
>
```
$ sudo systemctl stop ssh.service
```
>

>
No WSL usar o comando `sudo service ssh stop`
>
### Reiniciar um servidor SSH ###
>
```
$ sudo systemctl restart ssh.service
```
>

>
No WSL usar o comando `sudo service ssh restart`
>

### Verificar o status do servidor SSH ###
>
```
$ sudo systemctl status ssh.service
```
>

>
No WSL usar o comando `sudo service ssh status`
>

### Habilitar e iniciar sshd para funcionar em boot time ###
>
```
$ sudo systemctl enable ssh.service
```
>

### Verificar se o sshd está habilitado para boot time ###
>
```
$ sudo systemctl is-enabled ssh.service
```
>



