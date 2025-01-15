Para obtener el client ID primero debemos registrarnos como desarrollador(https://www.instagram.com/developer/) y crear una aplicación(Manage Clients) 

Ejecutar en el navegador lo siguiente:

```sh
https://api.instagram.com/oauth/authorize/?client_id=CLIENT-ID&redirect_uri=REDIRECT-URI&response_type=code
```

Nos redigira a una dirección con el código, abrimo el terminal y ejecutamos el CURL:

```sh
curl -F 'client_id=CLIENT_ID' -F 'client_secret=CLIENT_SECRET' -F 'grant_type=authorization_code' -F 'redirect_uri=REDIRECT_URL' -F 'code=CODE' https://api.instagram.com/oauth/access_token
```

Luego nos devolvera el token:

```js
{
"access_token":"2967187836.6e63663.6cf57bc952de41d9aa27514f2a5c3f9d", 
"user": 
  {"website": "http://juanlopezdev.github.io",
  "id": "2967187836", 
  "full_name": "Juan Lopez",
  "username": "juanlopez.developer", 
  "profile_picture": "https://scontent.cdninstagram.com/t51.2885-19/s150x150/13151160_483068871883349_931594696_a.jpg", 
  "bio": "Web Developer \u0026 DotaLover :)"
  }
}
```

Ejecutar por ejemplo: https://api.instagram.com/v1/users/self/media/recent?access_token=2967187836.6e63663.6cf57bc952de41d9aa27514f2a5c3f9d

Documentación en 

https://www.instagram.com/developer/authentication/

https://www.instagram.com/developer/endpoints/users/#get_users_media_recent_self

OTRO METODO:

https://api.instagram.com/oauth/authorize/?client_id=CLIENT-ID&redirect_uri=REDIRECT-URI&response_type=code

Luego ejecutar:

https://instagram.com/oauth/authorize/?client_id=YOURCLIENTIDHERE&redirect_uri=HTTP://YOURREDIRECTURLHERE.COM&response_type=token

Documentacion: https://bobmckay.com/web/simple-tutorial-for-getting-an-instagram-clientid-and-access-token/
