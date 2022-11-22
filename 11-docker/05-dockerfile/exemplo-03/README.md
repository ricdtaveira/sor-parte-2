# Exemplo-3 #

>
Nesse exemplo mostraremos o uso de volumes compartilhados entre containers e um host.
>
## Introdução ##
>
Um volume pode ser um diretório localizado fora do sistema de arquivos de um container.
>
>
O Docker permite o mapeamento entre diretórios de um container e diretórios de um host.
>
>
É possivel manipular dados no container sem que tenham relação alguma com as 
informações da imagem.
>
>
Um volume pode ser compartilhado entre vários containers como ilustra a figura abaixo.
>

>
![Compartilhamento de Volumes.](/11-docker/99-figuras/tela_03.png "Volumes Compartilhados.")
>

## Gerenciando os dados dos volumes ##
>
Volumes são diretórios configurados dentro de um container que fornecem o recurso de 
compartilhamento e persistência de dados.
>

### Conceitos Fundamentais ### 
>
1. Volumes podem ser compartilhados ou reutiliados entre containers.
>
>
2. Toda alteração feita em um volume é de forma direta;
>
>
3. Volumes alterados não são incluídos quando atualizamos uma imagem. 
>

### Exemplo de compartilhamento de volumes usando o Nginx ### 
>
O exemplo a seguir usará o mapeamento de volumes entre um host e um container da seguinte
forma: 
1. Usaremos um container Nginx;
2. Faremos o mapeamento de um volume contido no host com um volume contido no container.
>
>
```
$ docker run -d -p 8080:8080 -v /tmp/nginx:/usr/share/nginx/html:ro nginx
```
>
>
As seguintes configurações estam caracterizadas como: 
>
>
1. A opção `-v` está definindo o mapeamento de volume onde, o volume `/tmp/nginx` 
localizado no host está sendo mapeado para o volume `/usr/share/nginx/html` localizado no container.
>
>
2. A opção `ro` define o volume como `read-only`.
>
>
3. A imagem a ser carregada é a `nginx`.
>
#### Teste de volume #### 
>
O teste consiste em fazer uma requisição http ao `nginx`.  
> 
>
Usar o comando abaixo:
```
$ curl -IL http://localhost:8080
```
>
> 
A requisição http irá falhar, pois não existe um arquivo `index.html`.
>
>
A correção dessa falha consiste em gravar um arquivo `index.html` no volume 
`/tmp/nginx/index.html` localizado no host. 
>
>
Usar o comando abaixo:
```
$ echo "It works!" > /tmp/nginx/index.html
$ curl http://localhost:8080
It works!
```
>

>
A resposta ao get do http `It works!`, evidencia a existencia de um arquivo index.html criado 
no volume /tmp/nginx/ localizado no host. Porém a requisição feita foi ao container no volume 
´/usr/share/nginx/html´ que correponde ao volume mapeado no host.
>
### Exemplo de compartilhamento de volumes usando o Mysql ### 
>
Usaremos nesse exemplo um container que executará um banco de dados Mysql. Nele, é possível 
controlar os dados que serão armazenados em disco, fazer backups e restaurações.
>
Usaremos o Dockerfile abaixo:
>
>
```
FROM ubuntu

MAINTAINER Ricardo Taveira <ricdaveira@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get install -y mysql/mysql-server:5.5

ADD my.cnf /etc/mysql/conf.d/my.cnf

RUN chmod 664 /etc/mysql/conf.d/my.cnf

ADD run /usr/local/bin/run

RUN chmod +x /usr/local/bin/run

VOLUME ["/var/lib/mysql"]

EXPOSE 3306
```


>
