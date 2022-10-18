# SCP # 

>
O SCP é um comando que é instalado junto com o SSH. Esse comando permite a cópia de arquivos entre máquinas.
>

## Exemplos ##

### Exemplo 01 ### 
```
$ scp teste.txt root@10.0.0.1:/tmp
```
>
Copia o arquivo local `teste.txt` para a maquina `10.0.0.1`, realizando logim como usuário `root`, e
e disponibilizando o citadoarquivo no diretório `/tmp`no destino.
>

### Exemplo 02 ### 
```
scp -p 45000 teste.txt taveira@srv.taosys.com.br:
```
>
Conecta-se à porta `45000` da maquina `srv.taosys.com.br` como `taveira`. Em seguida, transfere o arquivo 
`teste.txt` para a referida máquina. Como não foi citado um diretório de destino, seráusado o home diretório, 
ou seja `\home\taveira`.  
>

### Exemplo 03 ### 
```

```
>

>
