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
2. Faremos o mapeamento de um volume contido no host com um container contido no 
no container.
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
está sendo mapeado para o volume `/usr/share/nginx/html`.
>
>

>

### Exemplo de compartilhamento de volumes usando o Mysql ### 


