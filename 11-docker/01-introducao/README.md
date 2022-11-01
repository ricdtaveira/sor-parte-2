# Introdução #
>
O Docker é uma plataforma aberta para desenvolvimento, envio e execução de 
software. O Docker permite que você separe seus aplicativos de sua infraestrutura
de hardware permitindo uma entrega de software de forma rapida.
>

## A plataforma Docker ##
>
O Docker fornece a capacidade de empacotar e executar software em ambiente de
isolado chamado contêiner. O isolamento e a segurança permitem que você execute 
vários contêineres simultaneamente em um determinado host. 
>
>
Os contêineres são leves e contêm tudo o que é necessário para executar o 
software, daí, o aplicativo não precisa depender do que está instalado no host. 
>
>
Contêineres são instanciados na memória a partir de uma imagem. Imagens podem facilmente ser 
compartilhados enquanto trabalha e garantir que todos com quem você compartilha obtenham a mesma imagem 
gerada do mesmo contêiner que funciona da mesma maneira.
>
>
O Docker fornece ferramentas e uma plataforma para gerenciar o ciclo de vida de 
suas imagens e contêineres.
>
>
Desenvolva seu aplicativo e seus componentes de suporte usando contêineres.
>
>
O contêiner se torna a unidade para distribuir e testar seu aplicativo.
Quando estiver pronto, implante seu aplicativo em seu ambiente de produção, como 
um contêiner ou um serviço orquestrado. 
>
>
Isso funciona da mesma forma se seu ambiente de produção for um data center local, 
um provedor de nuvem ou um híbrido dos dois.
>

## A Arquitetura do Docker ##

>
O Docker usa uma arquitetura cliente-servidor. 
>
>
O cliente Docker conversa com o daemon do Docker , que faz o trabalho pesado de 
construir, executar e distribuir seus contêineres Docker. 
>
O cliente e o daemon do Docker podem ser executados no mesmo sistema ou você pode 
conectar um cliente do Docker a um daemon remoto do Docker. 
>
O cliente Docker e o daemon se comunicam usando uma API REST, em soquetes UNIX ou 
uma interface de rede. 
>
Outro cliente do Docker é o Docker Compose, que permite trabalhar com aplicativos que 
consistem em um conjunto de contêineres.
>
>
![Arquitetura do Docker.](/11-docker/99-figuras/arquitetura_docker.png "Arquitetura do Docker.")
>
>

>
>
O Docker Registry é um serviço na nuvem que funciona como um repositório de imagens Docker
que podem ser reutilizadas. 
>
O Serviço de Registry oficial é o [Docker Hub](https://hub.docker.com/_/registry).
>
>
As imagens contidas no Docker Hub são criadas por distribuições Linux e empresa desenvolvedoras de 
software livre.    
>
>
Desenvolvedores podem criar uma conta no Docker Hub e lá hospedarem imagens 
desenvolvidas para futura reutilização.
>
>
O meu repositório no Docker Hub é [ricdtaveira](https://hub.docker.com/search?q=ricdtaveira).
>