# ssl
ssl stuff

CA AUTHENTICATION

  692  May/16 - 11:06:28 $ mkdir sslcert
  693  May/16 - 11:06:29 $ cd sslcert
  694  May/16 - 11:06:40 $ openssl req -out ca.pem -new -x509 
  696  May/16 - 11:06:47 $ openssl req -out ca.pem -new -x509 
 

  706  May/16 - 11:07:40 $ openssl genrsa -out server.key 1024 
  707  May/16 - 11:07:46 $ openssl req -key server.key -new -out server.req 
  710  May/16 - 11:08:35 $ vi file.srl
  711  May/16 - 11:08:49 $ openssl x509 -req -in server.req -CA  ca.pem  -CAkey  privkey.pem -CAserial file.srl -out server.pem 

  713  May/16 - 11:09:15 $ openssl genrsa -out client.key 1024 
  714  May/16 - 11:09:23 $ openssl req -key client.key -new -out client.req 
  715  May/16 - 11:09:40 $ openssl x509 -req -in client.req -CA ca.pem -CAkey privkey.pem -CAserial file.srl -out client.pem 


