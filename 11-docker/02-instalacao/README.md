# Instalação do Docker # 

>
A instalação será realizada em uma máquina virtual VirtualBox com a distribuição Lubuntu 20.04.
>
>
Seguiremos o tutorial [Como Instalar O Docker No Ubuntu 22.04 | 20.04](https://cloudcone.com/docs/article/how-to-install-docker-on-ubuntu-22-04-20-04/).
>
>
Chamar o terminal do Lubuntu e seguir com os passos a seguir digitando comandos shell.
>
>
![nicio da Instalaçãoclearning.](/11-docker/02-instalacao/99-imagens/tela_01.png "Inicio da Instalação.")
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
### Passo 2 - Instalar Dependências ###
>
Algumas dependências são necessárias para que a instalação ocorra sem problemas. 
>
>
Portanto, execute o comando abaixo para instalá-las:
>
>
```
$ sudo apt install apt-transport-https curl gnupg-agent ca-certificates software-properties-common -y
```
>
### Passo 3 - Instale o Docker no Ubuntu ###
>
Com as dependências instaladas, a próxima etapa é instalar o Docker. 
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
Depois de adicionada chave GPGK, adicione o repositório do Docker da seguinte maneira.
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
conectado no momento ao grupo Docker. 
>
Isso permite que você execute comandos Docker sem invocar o sudo.
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
>
Para verificar se o Docker está instalado, execute o comando:
>
```
$ docker version
```
> 
>
Na saída abaixo, você pode ver que instalamos o Docker 20.10, que é a versão mais recente 
do Docker no momento da publicação deste tutorial.
>
>
![Saída da Instalação.](/11-docker/02-instalacao/99-imagens/tela_02.png "Verificação da Instalação.")
>



### Passo 5 - Gerenciar o serviço Docker ###
>
Por padrão, o Docker inicia automaticamente na instalação. 
>
>
Para verificar isso, execute o comando:
>
>
```
$ sudo systemctl status docker
```
>
>
![Status de Execução do Docker.](/11-docker/02-instalacao/99-imagens/tela_03.png "Verificação da Execução.")
>
>
O status Active: active (running) indica que o Docker está carregado e executando.
>
>
Se, por algum motivo, o Docker não estiver em execução, basta executar o seguinte 
comando:
>
>
```
$ sudo systemctl start docker
```
>
>
Para permitir que o Docker seja iniciado automaticamente toda vez na inicialização do 
sistema, execute o comando:
>
>
```
$ sudo systemctl enable docker
```
>
>
Para reiniciar o Docker, execute:
>
>
```
$ sudo systemctl restart docker
```
>


### Passo 6 - Testar o Docker ###
>
Para testar o Docker, vamos carregar uma imagem 'hello-world' carregada no Docker Hub. 
>
A partir dessa imagem, será criado um container que exibe uma mensagem 'Hello world' 
no terminal junto com os passos do que acontecem após a execução do comando.
>
>
Executar o comando abaixo para testar a execução de um container.
>
>
```
docker run hello-world
```
>
>
![Hello World !.](/11-docker/02-instalacao/99-imagens/tela_04.png "Teste de Execução.")
>
>
Para confirmar a criação de imagens no sistema, execute o comando:
>
>
```
docker images
```
>
>
![Imagem Criada!.](/11-docker/02-instalacao/99-imagens/tela_05.png "Imagem Criada.")
>
>
Depois que o contêiner é criado, ele sai ou para automaticamente. 
>
Você ainda pode verificar os contêineres parados conforme mostrado.
>
>
O comando abaixo quando executado mostrou dois contêineres que 
foram carregados e finalizaram sua execução.
>
>
```
docker ps -a
```
>
>
![Contêineres Finalizados!.](/11-docker/02-instalacao/99-imagens/tela_06.png "Contêineres finalizados.")
>


