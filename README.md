<<<<<<< HEAD
# BeautyClick   
 
<h2>  Backend del proyecto BeautyCLIC en NodeJs</H2>  

<h3> Estructura de carpetas   </h3>

* `common/services/`
    * `mongoose.service.js`  
Aqui   se carga la configuracion de la base de datos desde el archivo `.env` que esta en la carpeta raiz 
`.env`
```php 
#PRIV KEY
PRIV_KEY = "-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEAyfmKEnrvSjcF5GjHH8GtuJ75DsLWn9e5O1UE+utY3o7ygpnX
UKPZ7eZz7+XAPl2IiQIXg3bi0Dd5yLX7YyRAL99YRYpw2Oj1o4SisEKqscMcv/wd
Fzu8eKEYRcFgnLk6eBILPW1h+J8xjtFWCqVShge43sXx4RoPVnWxGn3kxUc/WDlI
pITixT5ZxSeu22T+EfN/SUSI+FKgWs7AZ464bD0zKpRHMW9109MV4aDkSBB18kBB
e8c3BGayKwryjiraQrI0GnJsuhnJ/fLQvZWYj1osW9f7by6lOMsX+G9UznXqbjhs
3IPhplkwUQdgrq4NMYr8DHIVw8wW1BYUx9mPQwIDAQABAoIBAFLdVpCOb257dKdp
dYjJ5YRBdN1hgrzBvPVixFBODoABFe4PQA+NqfO5AQgDswPjTAkqGouNUzEqEYUP
ZLwgO1VoxMaDLhlQOreDy1uVfoLAEiOSRD0r/P9g2JyF4iVquVpZzNK+9dsTNTnr
GOn1Og5TTL3ZaIt6LaDDWI4N6LYm8mnhoT5yqryzBUMn2reSzhJGFKEYZsr+2mPi
Wb5CqQSPt0CpDvRkNvtSBlJWeS7tHlqtf7FmjmOUBfLI9SImqKWMLJ1fTMDqdb3v
NLRcQOOwhGvl78kItMSDtJxL1+YzJ8aMIDMIokPeIJpZ3ZMGziscViDA+oNzNLE3
FjSfCcECgYEA6RFgGrmexntjuvfuSC8+m2W+FVQQMjJSm2H497W0HW9jpD9JTOXu
X+3m+NfNN5xomdYsSXKGZe7EoAdaEL+vpEfi2PUo39hLb9YZ8bs9YJeyuPH/I/og
Y+EzpB7Uk3euT4gd+bpyC+dGkm23LEu7llcVERQdO3MWJV12iaw0JXcCgYEA3dj5
01pyjXrZ6oeiYWwdzQfgCkyFYfARLpwX/xKfDI+xwyqpWnFn14VoetXpMksq0XK4
ZIJz7WYLF3uF2RgF9kNtnLYfB0gbXt/SS6qqlQuFQBxJJ3F4mz8jIjK3bjhvkwmP
dJaZNfrI1//aTC4ygpChUluCrLmKEbdn8keyh5UCgYEAk3CVfnKcme1m6tl7WRji
H0Ze2HlEgazKC1gQOwwstE5KF5adlVMD2JXUfult/lco6ODPRWt40DUbGC1ucZgB
0ghT3nJA+FKJbmdgJEcSDfAJdOxKPoU2Rlkp5RJH4j5c/B0c8WVcTmFxiKJ1tUT3
l6ThQ9uYnoowoVSd73wLxQMCgYB9Sq6FnF534vsxxpqBtQL7qcfxaRgnoOLDVSsE
RusGuBzoIa71wnioMtM4FJmYavVqxwS21ypL2EbJY1zLqBKt65T7XawWe7Xhljz5
uRCQDqqZ85+pJB++ZiEcjlIkcMEq5MpdSTSMVO+bdgc+4RRrwu0pSz9492yv5spQ
/gcpJQKBgGJHXfqSh+NJMm+vX5fjbpNqYhFCB1Gz9g8zQ+g3Q+M7Uv3jpm1FA70e
OwTYcXOWgo6shq3wCj15TRg1U7djRLjRo9/L/RbIj3c7exdwpk/Y6nJYaahpVQQB
4Hb30WEbNXo0oF6sVX3GNcqM2+C1499N9A1U/p8MefG7y1OTEfi/
-----END RSA PRIVATE KEY-----"

PUB_KEY="-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAvjhjmdH6rryDJwtfduS9
giccEiDeNpNTUrGswp3ugW16CSk4P6qobXPKRM7gCwT/J+SdqA6RpKQUb6c08XDI
6sxsZgLajbFGxasU6qEbKDsCNXWXKMGRRTxjbnSG0GtYQFgrDR0TNHQSG0/r4oYZ
NA2hGqVfC5jrtuCrr/PPz117VN1MRrbx6rJaoNGpJDCxjZVSzlqW4lNpmY7kl8iR
eid6rNVbCTQULRXkudIrJN57NebzyazhfdfpdJVQ6Kx+9xmzaNsRptj6YIJ5yu8l
DmhEIMirr0YI1FuoMOFAKa5GgDgspJVLbBl5Z51XmzMytAwLZw4RB9sXw4NEz0sQ
4wIDAQAB
-----END PUBLIC KEY-----"

#MONGO CREDENTIALS
MONGO_CFG = "mongodb://beauty:mypwd@127.0.0.1:27017/beautyclic"

#server port
SERVER_PORT= 3000
```
Si no existe este archivo (a veces github no deja subirlo), rellenar el archivo example.env y cambiar el nombre a .env

Ir a mongosh y crear la base de datos:
```bash
mongosh
test>use beautyclic
beautyclic>db.createUser({user:"beauty",pwd:"mypwd",roles:[{role:"readWrite",db:"cifrado"}]})

```
Tambien hacer correr la base dadatos:
Esto es en Mac
`sudo ./mongod --port 27017 -dbpath /System/Volumes/Data/data/db`

En windows 
`mongod --port 27017 -dbpath c:\data\db` 

Las demas carpetas:
```bash 
/models
user.model.js 
userfile.model.js
crypto.model.js
cita.model.js
```
los tres primeros son para guardar la tabla de clientes y para cifra descifrar
En cita.model.js habra que incluir los esquemas de la base de datos y las funiones para realizar las consultas
```bash
/controllers
cita.controllers.js
user.controllers.js
contacto.controllers.js
```

TODO:  Contacto.controller es para gestionar los formularios 
TODO: cita.controllers.js , revisar las funciiones para que hagan las consultas adecuadas a cita.model.js
=======
# BeautyClick
>>>>>>> 37629d8 (Initial commit)
