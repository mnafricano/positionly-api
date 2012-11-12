## Keywords

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/keywords.json
```

### Response
```json
[
    {
        "id": 1,
        "group_id": null,
        "website_id": 1,
        "name": "example"
    },
    {
        "id": 2,
        "group_id": null,
        "website_id": 1,
        "name": "example test"
    },
    <...>
]
```

## Keyword

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/keywords/<keyword id>.json
```

### Response
```json
{
    "id": 1,
    "group_id": null,
    "website_id": 1,
    "name": "example",
    "website": {
        "id": 11,
        "account_id": 1,
        "name": "http://positionly.com",
        "title": "Example"
    },
    "group": null
}
```

## Create Keyword

### POST
```shell
curl -X POST -d @examples/keyword.json 'http://api.positionly.com/v1/accounts/<account id>/websites/<website id>/keywords.json'
```

### Response
```json
{
    "status": "ok",
    "keyword": {
        "id": 1,
        "group_id": null,
        "website_id": 1,
        "name": "example",
        "website": {
            "id": 11,
            "account_id": 1,
            "name": "http://example.com",
            "title": "Example"
        },
        "group": null
    }
}
```

## Delete Keyword

### DELETE
```shell
curl -X DELETE 'http://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/keywords/<keyword id>.json
```

### Response
```json
{
    "status": "ok"
}
```
