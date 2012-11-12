## Engines

### GET
```shell
curl https://api.positionly.com/v1/engines/<google|yahoo|bing>.json
```

### Response
```json
[
    {
        "id": 1,
        "domain": "www.google.com.ar",
        "provider": "Google",
        "language_name": "español (Latinoamérica)"
        "created_at": "2011-09-17T00:40:17+02:00"
    },
    {
        "id": 3,
        "domain": "www.google.com.au",
        "provider": "Google",
        "language_name": "English"
        "created_at": "2011-09-17T00:40:17+02:00"
    },
    <...>
]
```
