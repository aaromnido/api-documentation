---
title: "Authentication"
description: "How to authenticate and handle access tokens in the API-DOCUMENTATION API."
---

To interact with the API-DOCUMENTATION API, you need to authenticate using access tokens. This process ensures that only authorized users can access and manipulate the data.

## Obtaining an Access Token

To obtain an access token, you must send a POST request to the authentication endpoint with your credentials.

### Endpoint

```js "return true;" ins="https://api.example.com/api/auth/login" ins="tu_usuario" ins="tu_contraseña"
// Javascript code with syntax highlighting.
const url = 'https://api.example.com/api/auth/login';
const credentials = {
  username: 'tu_usuario',
  password: 'tu_contraseña'
};

fetch(url, {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify(credentials)
})
  .then(response => {
    if (!response.ok) {
      throw new Error('Error en la autenticación');
    }
    return response.json();
  })
  .then(data => {
    console.log('Token de acceso:', data.token);
    console.log('Expira en:', data.expires_in, 'segundos');
  })
  .catch(error => {
    console.error('Error:', error.message);
  });

```
<br>
Tras esto, ejecutar el siguiente comando para probar la API:

```bash
npm run dev
```