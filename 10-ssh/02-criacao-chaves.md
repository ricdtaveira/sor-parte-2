# Chaves Simétricas #
>
O protocolo SSH faz uso de criptografia usando chaves assimétricas (chave pública e chave privada). A chave privada 
é alocada na maquina cliente SSh e a chave pública criada é copiada para um diretório no servidor SSH.   
>

## Criação de Chaves (Publica e Privada)
>
Chaves Simétricas podem ser criadas no contexto do sistema operacional Windows usando o software `Puttygen` ou
no contexto do Linux usado o utilitario `ssh-keygen`.
>

## Copiar a Chave Pública para o SSH Server ##
>
Para fazer a cópia da Chave Pública para um servodor SSH é necessário ter um login e senha nesse servidor.
>
>
Usar o programa `ssh-copy-id` que vem incluído nos sistemas operacionais.
>