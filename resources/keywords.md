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
curl -X POST -d @examples/keyword.json https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/keywords.json
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
curl -X DELETE 'https://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/keywords/<keyword id>.json
```

### Response
```json
{
    "status": "ok"
}
```

## Keyword Positions

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/engines/<engine id>/keywords/<keyword id>/positions.json
```

### Response
```json
{
    "id": 1,
    "group_id": null,
    "website_id": 1,
    "name": "example",
    "positions": {
        "2013-01-24": 66.4,
        "2013-01-25": 50,
        "2013-01-26": 72.6,
        "2013-01-27": 38.9,
        "2013-01-28": 54,
        "2013-01-29": 62.7,
        "2013-01-30": 48
    }
}
```
