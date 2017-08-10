# ssl
ssl stuff

CA AUTHENTICATION

 $ mkdir sslcert
 
 $ cd sslcert
 
 $ openssl req -out ca.pem -new -x509 
 
 $ openssl req -out ca.pem -new -x509 



 $ openssl genrsa -out server.key 1024 
 
 $ openssl req -key server.key -new -out server.req 
 
 $ vi file.srl
 
 $ openssl x509 -req -in server.req -CA  ca.pem  -CAkey  privkey.pem -CAserial file.srl -out server.pem 

 
 $ openssl genrsa -out client.key 1024 
 
 $ openssl req -key client.key -new -out client.req 
 
 $ openssl x509 -req -in client.req -CA ca.pem -CAkey privkey.pem -CAserial file.srl -out client.pem 


