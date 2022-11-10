# Exemplo 2#

>
Copiar um arquivo para a area de configuração do Nginx. 
>
>
Um container é instanciado na memória a partir deuma imagemque o define.
>
>
## Docker File inicial ##
>
Arquivo `exemplo` que será copiado para a área do `Nginx`.
> 
>
```
server {
listen 8080 default_server;
server_name localhost;
root /usr/share/nginx/html;
index index.html index.htm;
}
```

>
Texto do arquivo Dockerfile que será usado na versão inicial da imagem 
inicial do exemplo-02.

>
 ```
FROM ubuntu
MAINTAINER Ricardo Taveira <ricdtaveira@gmail.com>
RUN apt-get update
RUN apt-get install -y nginx
ADD exemplo /etc/nginx/sites-enabled/default
EXPOSE 8080
 ```
>

### Docker File alterado ###
>
Arquivo Dockerfile com alterações implementado a feature para copiar 
o arquivo exemplo.   
>
>
```
FROM ubuntu
MAINTAINER Ricardo Taveira <ricdtaveira@gmail.com>
RUN apt-get update
RUN apt-get install -y nginx
ADD exemplo /etc/nginx/sites-enabled/default
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
ADD ./ /rails
WORKDIR /rails
EXPOSE 8080
CMD service nginx start

```

>

