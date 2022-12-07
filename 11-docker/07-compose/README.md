# Docker Compose #

>## Introdução ###
O Docker Compose é a ferramenta que permite a criação de vários containers que são configurados
para permitir a integração de serviços por meio de conexões de rede. 
>
>
Em cada container é configurado um serviço que se integra aos demais. Um conjunto de containers atuando
isoladamente se integram para compor uma solução.
>

### Aplicações ### 
>
Ambientes que envolvem desenvolvimento de aplicações e ambientes de operação 
envolvendo vários serviços isolados rodando em servidores dedicados são exemplos
de uso do Docker com Compose.
> 

### Implementação ###
>
O uso do Docker Compose pressupõe a configuração de um arquivo no qual são configurados
os container que irão compor a solução.
>
>

>
#### Uma aplicação Web que acessa um banco de dados ####
Em um container é instalado um servidor web Apache com PHP. Em um outro container é 
instalado um servidor de Banco de Dados com Mysql.
>
>
#### 
>