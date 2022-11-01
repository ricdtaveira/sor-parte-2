# Instalação do Docker # 

>
A instalação será realizada em uma máquina virtual VirtualBox com a distribuição Lubuntu 20.04.
>
>
Seguiremos o tutorial [Como Instalar O Docker No Ubuntu 22.04 | 20.04](https://cloudcone.com/docs/article/how-to-install-docker-on-ubuntu-22-04-20-04/).
>

## Passos da Instalação ##

### Passo 1 - Atualizar o Sistema ### 
>
O primeiro passo é atualizar os repositórios locais das bibliotecas do Linux. 
>
>
Para isso, execute o comando:
>
>
```
$ sudo apt update
```
>
### Passo 2 - Instalar Dependencias ###
>
Algumas dependências são necessárias para que a instalação ocorra sem problemas. 
Portanto, execute o seguinte comando para instalá-las:
>
>
```
$ sudo apt install apt-transport-https curl gnupg-agent ca-certificates software-properties-common -y
```
>
### Passo 3 - Instale o Docker no Ubuntu ###
>
Com os requisitos instalados, a próxima etapa é instalar o Docker. 
>
>
Instalaremos o Docker Community Edition ( Docker CE ) que é de código aberto e gratuito para download e uso.
>
>
Para fazer isso, adicionaremos a chave GPGK.
>
>
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
>
Depois de adicionada chave gpg, adicione o repositório do Docker da seguinte maneira.
>
>
Nota: O Comando abaixo adiciona o repositório para o Ubuntu 20.04 Stable.
>
>
```
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```
>
>
Com a chave GPG e o repositório adicionados, execute o comando a seguir para instalar 
o Docker e os pacotes associados.
>
>
```
$ sudo apt install docker-ce docker-ce-cli containerd.io -y
```
>
>
O Comando acima instala o Docker e todos os pacotes, bibliotecas e dependências 
adicionais exigidos pelo Docker e pacotes associados.
>
>
Depois que o comando for executado com êxito, considere adicionar o usuário 
conectado no momento ao grupo docker. 
>
Isso permite que você execute o docker sem invocar o sudo.
>
>
```
$ sudo usermod -aG docker $USER
```
>
>
```
$ newgrp docker
```
>
>
Agora você pode executar comandos do Docker como um usuário 
comum sem nenhum impedimento.
>
### Passo 4 - Confirme se o Docker está instalado ###

### Passo 5 - Gerenciar o serviço Docker ###

### Passo 6 - Testar o Docker ###


