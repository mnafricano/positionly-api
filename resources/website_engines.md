## Website Engines

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/engines.json
```

### Response
```json
[
    {
        "id": 1,
        "website_id": 1,
        "engine_provider": "Google",
        "engine_name": "United States"
    },
    <...>
]
```

## Website Engine

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/engines/<engine id>.json
```

### Response
```json
{
    "id": 1,
    "website_id": 1,
    "engine_provider": "Google",
    "engine_name": "United States"
}
```

## Create Website Engine

### POST
```shell
curl -X POST -d @examples/engine.json https://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/engines.json
```

### Response
```json
{
    "status": "ok",
    "engine": {
        "id": 1,
        "website_id": 1,
        "engine_provider": "Google",
        "engine_name": "United States"
    }
}
```

## Delete Website Engine

### DELETE
```shell
curl -X DELETE https://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/engines/<engine id>.json
```

### Response
```json
{
    "status": "ok"
}
```
