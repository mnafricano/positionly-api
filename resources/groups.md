## Groups

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/groups.json
```

### Response
```json
[
    {
        "id": 1,
        "website_id": 1,
        "name": "Example"
    },
    {
        "id": 2,
        "website_id": 1,
        "name": "Other"
    },
    <...>
]
```

## Group

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/groups/<group id>.json
```

### Response
```json
{
    "id": 1,
    "website_id": 1,
    "name": "Example",
    "website": {
        "id": 11,
        "account_id": 1,
        "name": "http://example.com",
        "title": "Example"
    },
    "keywords": []
}
```

## Create Group

### POST
```shell
curl -X POST -d @examples/group.json https://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/groups.json
```

### Response
```json
{
    "status": "ok",
    "group": {
        "id": 1,
        "website_id": 1,
        "name": "Example",
        "website": {
            "id": 11,
            "account_id": 1,
            "name": "http://example.com",
            "title": "Example"
        },
        "keywords": []
    }
}
}
```

## Delete Group

### DELETE
```shell
curl -X DELETE https://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/groups/<group id>.json
```

### Response
```json
{
    "status": "ok"
}
```
