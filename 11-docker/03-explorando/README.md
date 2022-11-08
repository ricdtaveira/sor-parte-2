# Explorando o Docker #

## Interatividade ##
>
O Docker permite uma interatividade com os containers por meio de comandos executados por
executados a partir do terminal.
>
### Verificar Containers ### 
>
É possível verificar a existência de containers com o comando abaixo.
> 
>
```
docker ps
```
>
![Contaniners em execução.](/11-docker/02-instalacao/99-imagens/tela_07.png "Containers em execução.")
>
>
A figura acima mostra a inexistência de containers em execução.
>

### Carga de uma Imagem no Modo Interativo ###
>
A seguir faremos a carga de uma imagem `ubuntu` e acessaremos 
o shell permitindo a execução de comandos no container.
>
>
```
$ docker run -i -t ubuntu /bin/bash
```
> 
>
![Interação com Containers.](/11-docker/02-instalacao/99-imagens/tela_08.png "Interação com Containers.")
>
>
O comando acima utilizou as opções: `-i` e `-t` em conjunto
com a `run` . O parâmetro `-i` diz ao Docker que queremos ter
interatividade com o container, e o `-t` que queremos nos linkar
ao terminal do container. 
>
Em seguida, informamos o nome da imagem usada, no caso `ubuntu`, e passamos o 
comando `/bin/bash` como argumento permitindo usar o shell do container.
>
>
A partir do prompt que é apresentado acima  com o usuário `root` podemos executar 
comandos do shell dentro do container.  
>

### Verificar dados do Container carregado ###
>
O comando demonstrado abaixo apresenta os dados do container. Os dados contidos
no arquivo `lsb-realease` possuem atributos da imagem do container.
>
> 
```
![Dados do Container.](/11-docker/03-explorando/99-figuras/tela_01.png "Dados do Container.")
```
>

### Listar Containers ### 
>
O Comado abaixo lista containers 

## Alteração de uma Imagem ##

>
O Modo interativo demonstrado anteriormente permite a instalação e configuração de aplicativos em um container 
criado a partir de uma imagem base.   
>
>
Seguiremos 
>

