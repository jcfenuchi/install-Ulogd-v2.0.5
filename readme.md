# Guia de instalação do Ulogd 

## Comandos:

### Requisitos para compilar o Ulogd
```
sudo apt update && sudo apt install -y libnfnetlink-dev libnetfilter-log-dev libnetfilter-queue-dev libnfnetlink-dev libnfnetlink0 libnetfilter-log1 libnetfilter-queue1
```
### Compilando o Ulogd
````
cd ./ulogd-2.0.5 
./configure 
#Suporte ao SQL use ./configure --with-mysql
make
sudo make install
```` 

### Veja se foi instalado
```
ulogd -d
ulogd --version
```` 

### Copie o Arquivo padrão para/usr/local/etc/ulogd.conf ou /etc/ulogd.conf
```
cp ./../ulogd.conf usr/local/etc/ulogd.conf
cp ./../ulogd.conf /etc/ulogd.conf
```
##### Obs: fica a sua escolha decidir onde ele vai ficar

## Copie as Libs para o local Certo
```
cp ./../ulogd /usr/lib64/
```
##### Obs: é o caminho do diretorios onde é colocado os plugins no arquivo ulogd.conf

#

### Para mais verifique!
### https://rlworkman.net/howtos/ulogd.html