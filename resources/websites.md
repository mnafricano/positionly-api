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
curl -X POST -d @examples/website.json https://api.positionly.com/v1/accounts/<account id>/websites.json
```

### Parameters

    * scheme
    * name
    * title

    * website_engines_attributes": [
        { "engine_id": 31 }
    ]
}


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
curl -X DELETE https://api.positionly.dev/v1/accounts/<account id>/websites/<website id>.json
```

### Response
```json
{
    "status": "ok"
}
```

## Website Positions

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/engines/<engine id>/positions.json
```

### Response
```json
{
    "id": 11,
    "account_id": 1,
    "name": "http://positionly.com",
    "title": "Example",
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
