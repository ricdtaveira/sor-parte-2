# Explorando o Docker #

## Interatividade ##
>
O Docker permite uma interatividade com os containers. 
>
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
Em seguida, informamos o nome da imagem usada, no caso ubuntu, e passamos o 
comando `/bin/bash` como argumento permitindo usar o shell do container.
>
>
A partir do prompt que apresenta com o usuário `root` podemos executar 
comandos do shell dentro do container.  
>





