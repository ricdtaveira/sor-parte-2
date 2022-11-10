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
Arquivo Dockerfile inicial.
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
```
FROM ubuntu
MAINTAINER Daniel Romero <infoslack@gmail.com>
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

