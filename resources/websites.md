## Websites

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites.json
```

### Response
```json
[
    {
        "id": 1,
        "account_id": 1,
        "name": "http://example.com",
        "title": "Example"
    },
    <...>
]
```

## Website

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>.json
```

### Response
```json
{
    "id": 1,
    "account_id": 1,
    "name": "http://example.com",
    "title": "Example",
    "engines": [
        {
            "id": 1,
            "website_id": 1,
            "engine_provider": "Google",
            "engine_name": "United States"
        },
        <...>
    ],
    "groups": [
        {
            "id": 1,
            "website_id": 1,
            "name": "Example"
        },
        <...>
    ],
    "keywords": [
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
}
```

## Create Website

### POST
```shell
curl -X POST -d @examples/website.json 'http://api.positionly.com/v1/accounts/<account id>/websites.json'
```

### Response
```json
{
    "status": "ok",
    "website": {
        "id": 1,
        "account_id": 1,
        "name": "http://example.com",
        "title": "Example",
        "engines": [
            {
                "id": 1,
                "website_id": 1,
                "engine_provider": "Google",
                "engine_name": "Polska"
            },
            <...>
        ]
    }
}
```

## Delete Website

### DELETE
```shell
curl -X DELETE 'http://api.positionly.dev/v1/accounts/<account id>/websites/<website id>.json
```

### Response
```json
{
    "status": "ok"
}
```
