## Accounts

### GET
```shell
curl https://api.positionly.com/v1/accounts.json
```

### Response
```json
[
    {
        "id": 1,
        "name": "Example",
        "full_domain": "example.positionly.com",
        "created_at": "2012-09-17T00:40:18+02:00"
    },
    <...>
]
```

## Account

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>.json
```

### Response
```json
{
    "id": 1,
    "name": "Example",
    "full_domain": "example.positionly.com",
    "created_at": "2012-09-17T00:40:18+02:00",
    "websites": [
        {
            "id": 1,
            "account_id": 1,
            "name": "http://example.com",
            "title": "Example"
        },
        <...>
    ]
}
```
