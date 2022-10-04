# TP curl - comprendre les requêtes et les réponses HTTP

Pour les questions suivantes, vous devez utiliser l'url suivante : https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe

Pour tous les appels vous devez ajouter un header pour identifier votre appel parmis ceux des autres étudiants : x-student : massibdl

## Faire un appel curl : copier la commande exécutée et indiquer la requête et la réponse
curl --header "x-student:massibdl"  https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe -v

*   Trying 46.4.105.116:443...
*   Trying 2a01:4f8:141:1d3::2:443...
* Immediate connect fail for 2a01:4f8:141:1d3::2: Le réseau n'est pas accessible
* Connected to webhook.site (46.4.105.116) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
* successfully set certificate verify locations:
*  CAfile: /etc/ssl/certs/ca-certificates.crt
*  CApath: /etc/ssl/certs
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
* TLSv1.3 (IN), TLS handshake, Certificate (11):
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
* TLSv1.3 (IN), TLS handshake, Finished (20):
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.3 (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
* ALPN, server did not agree to a protocol
* Server certificate:
*  subject: CN=webhook.site
*  start date: Jul 31 23:09:19 2022 GMT
*  expire date: Oct 29 23:09:18 2022 GMT
*  subjectAltName: host "webhook.site" matched cert's "webhook.site"
*  issuer: C=US; O=Let's Encrypt; CN=R3
*  SSL certificate verify ok.
> GET /6f594809-a4b4-483e-841b-0c3b0a00edfe HTTP/1.1
> Host: webhook.site
> User-Agent: curl/7.74.0
> Accept: */*
> x-student:massibdl
> 
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* old SSL session ID is stale, removing
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Server: nginx
< Content-Type: text/plain; charset=UTF-8
< Transfer-Encoding: chunked
< Vary: Accept-Encoding
< X-Request-Id: 2fccb12f-d0b9-4c0a-bf2e-14ebadf54eb0
< X-Token-Id: 6f594809-a4b4-483e-841b-0c3b0a00edfe
< Cache-Control: no-cache, private
< Date: Tue, 04 Oct 2022 14:35:35 GMT
< 
* Connection #0 to host webhook.site left intact



## Quel est la version du protocole utilisé par le serveur ?
http/1.1


## Quels sont les headers que l'on envoie dans la requête ? Quels sont leur sens ?
> GET /6f594809-a4b4-483e-841b-0c3b0a00edfe HTTP/1.1 id de ressource et le protocol et sa version

> Host: webhook.site :nom domaine 

> User-Agent: curl/7.74.0

> Accept: */* indique quels sont les types de contenu, exprimés sous la forme de types MIME, que le client sera capable d'interpréter.

> x-student:massibdl identifiant du client 
> 

 
## Quelles informations pouvez-vous trouver à propos du certificat SSL ?
SL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384

## Quel est le code de la réponse ? Que signifie-t-il ?
200 OK


## Quels headers recevez vous dans la response ? Quels sont leur sens ?
< HTTP/1.1 200 OK

< Server: nginx

< Content-Type: text/plain; charset=UTF-8

< Transfer-Encoding: chunked

< Vary: Accept-Encoding

< X-Request-Id: 2fccb12f-d0b9-4c0a-bf2e-14ebadf54eb0

< X-Token-Id: 6f594809-a4b4-483e-841b-0c3b0a00edfe

< Cache-Control: no-cache, private

< Date: Tue, 04 Oct 2022 14:35:35 GMT

< 


## Faire un appel curl en envoyant du texte brut : copier la commande exécutée et indiquer la requête et la réponse
 curl "x-student:massibdl" -H "contenent-Type: text/plain" -X POST -d "hello"  https://webhook.site/6f594809-a4b4-483e-841b-0c3b0a00edfe -v

ote: Unnecessary use of -X or --request, POST is already inferred.
* Closing connection -1
curl: (3) URL using bad/illegal format or missing URL
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 46.4.105.116:443...
* Connected to webhook.site (46.4.105.116) port 443 (#0)
* ALPN, offering h2
* ALPN, offering http/1.1
* successfully set certificate verify locations:
*  CAfile: /etc/ssl/certs/ca-certificates.crt
*  CApath: /etc/ssl/certs
* TLSv1.3 (OUT), TLS handshake, Client hello (1):
* TLSv1.3 (IN), TLS handshake, Server hello (2):
* TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
* TLSv1.3 (IN), TLS handshake, Certificate (11):
* TLSv1.3 (IN), TLS handshake, CERT verify (15):
* TLSv1.3 (IN), TLS handshake, Finished (20):
* TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
* TLSv1.3 (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
* ALPN, server did not agree to a protocol
* Server certificate:
*  subject: CN=webhook.site
*  start date: Jul 31 23:09:19 2022 GMT
*  expire date: Oct 29 23:09:18 2022 GMT
*  subjectAltName: host "webhook.site" matched cert's "webhook.site"
*  issuer: C=US; O=Let's Encrypt; CN=R3
*  SSL certificate verify ok.
> POST /6f594809-a4b4-483e-841b-0c3b0a00edfe HTTP/1.1
> Host: webhook.site
> User-Agent: curl/7.74.0
> Accept: */*
> contenent-Type: text/plain
> Content-Length: 5
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 5 out of 5 bytes
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* old SSL session ID is stale, removing
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Server: nginx
< Content-Type: text/plain; charset=UTF-8
< Transfer-Encoding: chunked
< Vary: Accept-Encoding
< X-Request-Id: ac54cf60-f27e-4cf5-ac4e-404afef44f44
< X-Token-Id: 6f594809-a4b4-483e-841b-0c3b0a00edfe
< Cache-Control: no-cache, private
< Date: Tue, 04 Oct 2022 15:41:11 GMT
< 
* Connection #0 to host webhook.site left intact


## Faire un appel curl en envoyant du JSON (avec les bons headers) : copier la commande exécutée et indiquer la requête et la réponse


## Faire une appel curl en envoyant une basic authentication en utilisant 2 méthodes différentes : copier les commandes exécutées et indiquer la requête et la réponse à chaque fois 


## Exécuter la commande suivante avec la méthode GET puis indiquer la réponse : curl https://demo.api-platform.com/books/07dd4786-aaa7-4d08-a467-076b76f1d1b6 


## Exécuter la commande suivante avec la méthode PATCH  puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1


## Quel est le code HTTP reçu ? Quel est sa signification ?


## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/1


## Exécuter la commande suivante puis indiquer la réponse : curl https://demo.api-platform.com/top_books/9999


## Quel est le code HTTP ? Que signifie-t-il ?


## Exécuter la requête suivante et copier la réponse : curl https://google.fr


## Quel est le code HTTP reçu ? Pouvez-vous expliquer cette réponse ?


## Comment éviter cette réponse ? Trouvez 2 solutions différentes et détaillez les.
