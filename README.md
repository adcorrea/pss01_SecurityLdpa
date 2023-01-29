# pss01_SecurityLdpa
Projeto funcional com autenticação usando LDPA do Spring Security

Requitos

JDK 11

ApacheDS Studio

Docker

Instruções de uso
Instalar o ApacheDS Studio no link https://directory.apache.org/studio/downloads.html.


Abrir o cmd e rodar o comando abaixo para baixar a imagem do ApacheDS Server e subir no docker (precisa do docker instalado)

docker run --name ldap -d -p 389:10389 openmicroscopy/apacheds

Link da imagem no dockerhub
https://hub.docker.com/r/openmicroscopy/apacheds


Abrir o ApacheDS Studio e colocar essas configurações

Hostname: Localhost
Port: 389

BindDN or User: uid=admin,ou=system
password: secret


Importar na instancia dc=openmicroscopy,dc=org o arquivo resources\users.ldif

# #Teste

Acessar a url http:\\localhost:8080\login

user: mnardone
password: nardone01

user: lnardone
password: nardone02

