---
title: Login
description: A reference page in my new Starlight docs site.
---

### Request Parameters

| Parameter | Type   | Description                      |
| --------- | ------ | -------------------------------- |
| username  | string | Your username                    |
| password  | string | Your password                    |

### Request Example with `curl`

```bash
curl -X POST https://api.example.com/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "username": "tu_usuario",
    "password": "tu_contraseña"
}'
