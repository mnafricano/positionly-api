## Notes

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/notes.json
```

### Response
```json
[
    {
        "id": 1,
        "owner_id": 1,
        "website_id": 1,
        "account_id": 1,
        "bodytext": "Note",
        "created_at": "2012-05-01T10:18:10+02:00"
    },
    {
        "id": 2,
        "owner_id": 1,
        "website_id": 1,
        "account_id": 1,
        "bodytext": "Another note",
        "created_at": "2012-05-01T10:18:21+02:00"
    },
    <...>
]
```

## Note

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/notes/<note id>.json
```

### Response
```json
{
    "id": 1,
    "owner_id": 1,
    "website_id": 1,
    "account_id": 1,
    "bodytext": "Note",
    "created_at": "2012-05-01T10:18:10+02:00",
    "website": {
        "account_id": 1,
        "id": 1,
        "name": "http://example.com",
        "title": "Example"
    },
    "keywords": [],
    "engines": []
}
```

## Create Note

### POST
```shell
curl -X POST -d @examples/group.json 'http://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/notes.json
```

### Response
```json
{
    "status": "ok",
    "note": {
        "id": 1,
        "owner_id": 1,
        "website_id": 1,
        "account_id": 1,
        "bodytext": "Note",
        "created_at": "2012-05-01T10:18:10+02:00",
        "website": {
            "account_id": 1,
            "id": 1,
            "name": "http://example.com",
            "title": "Example"
        },
        "keywords": [],
        "engines": []
    }
}
```

## Delete Note

### DELETE
```shell
curl -X DELETE 'http://api.positionly.dev/v1/accounts/<account id>/websites/<website id>/notes/<note id>.json
```

### Response
```json
{
    "status": "ok"
}
```
