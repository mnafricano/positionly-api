## Beta Notice

* Please note that this is a beta version of our API
* Methods, keys, and structure might change before the API hits a stable branch
* The current version of the API is **read-only**

## OAuth2

This information is provided to you by Positionly.

> Client id: 4b1b0c8888287b81d57bf5b5ec176521
> Client secret: 6b5504ccf4b33f6b5fd108916b8fe50f

## Authorization

### POST
```shell
curl -X POST -d 'grant_type=password&username=<your username>&password=<your password>&client_id=4b1b0c8888287b81d57bf5b5ec176521&client_secret=6b5504ccf4b33f6b5fd108916b8fe50f' 'https://auth.positionly.com/oauth2/token'
```

### Response
```json
{
    "access_token":"37e120ae8ae9752105079bb28f07cfff",
    "token_type":"bearer",
    "expires_in":3599,
    "refresh_token":"6b6f99496dde0faf947e8b964360d2e7"
}
```

## Refresh token

### POST
```shell
curl -X POST -d 'grant_type=refresh_token&refresh_token=<your refresh token>&client_id=4b1b0c8888287b81d57bf5b5ec176521&client_secret=6b5504ccf4b33f6b5fd108916b8fe50f' 'https://auth.positionly.com/oauth2/token'
```

### Response
```json
{
    "access_token":"1eb14d5bd9d51af6f398ca2cd9b0fbcf",
    "token_type":"bearer",
    "expires_in":3599,
    "refresh_token":"6b6f99496dde0faf947e8b964360d2e7"
}
```

# API

## Accounts

### GET
```shell
curl https://api.positionly.com/v1/accounts.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
[
    {
        "id": 1
        "name": "Example"
        "full_domain": "example.positionly.com"
        "created_at": "2012-09-17T00:40:18+02:00"
    }
]
```

## Account

### GET
```shell
curl https://api.positionly.com/v1/accounts/1.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
{
    "id": 1
    "name": "Example"
    "full_domain": "example.positionly.com"
    "created_at": "2012-09-17T00:40:18+02:00"
    "websites": [
        {
            "account_id": 1
            "id": 1
            "name": "http://example.com"
            "title": "Example"
        }
    ]
}
```

## Websites

### GET
```shell
curl https://api.positionly.com/v1/accounts/1/websites.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
[
    {
        "account_id": 1
        "id": 1
        "name": "http://example.com"
        "title": "Positionly"
    }
]
```

## Website

### GET
```shell
curl https://api.positionly.com/v1/accounts/1/websites/1.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
{
    "account_id": 1
    "id": 11
    "name": "http://example.com"
    "title": "Positionly"
    "website_engines": [
        {
            "id": 1
            "website_id": 1
            "engine_provider": "Google"
            "engine_name": "United States"
        }
    ],
    "groups": [
        {
            "id": 1
            "name": "Example"
            "website_id": 1
        }
    ],
    "keywords": [
        {
            "id": 1
            "group_id": null
            "name": "example"
            "website_id": 1
        },
        {
            "id": 2
            "group_id": null
            "name": "example test"
            "website_id": 1
        }
    ]
}
```

## Notes

### GET
```shell
curl https://api.positionly.com/v1/accounts/1/websites/1/notes.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
[
    {
        "account_id": 1
        "website_id": 1
        "owner_id": 1
        "id": 1
        "bodytext": "Note"
        "created_at": "2012-05-01T10:18:10+02:00"
    },
    {
        "account_id": 1
        "website_id": 1
        "owner_id": 1
        "id": 2
        "bodytext": "Another note"
        "created_at": "2012-05-01T10:18:21+02:00"
    }
]
```

## Note

### GET
```shell
curl https://api.positionly.com/v1/accounts/1/websites/1/notes/1.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
{
    "account_id": 1
    "website_id": 1
    "owner_id": 1
    "id": 1
    "bodytext": "Note"
    "created_at": "2012-05-01T10:18:10+02:00"
    "website": {
        "account_id": 1
        "id": 1
        "name": "http://example.com"
        "title": "Example"
    },
    "keywords": []
}
```

## Positions

### GET
```shell
curl https://api.positionly.com/v1/accounts/1/websites/1/engines/1/keywords/1/positions.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf&date_from=2012-08-01&date_to=2012-08-30
```

### Response
```json
{
    "website_id": 1
    "group_id": null
    "id": 1
    "name": "example"
    "positions": {
        "2012-08-04": 15
        "2012-08-01": 14
        "2012-08-02": 15
        "2012-08-03": 15
        "2012-08-05": 15
        "2012-08-06": 15
        "2012-08-07": 14
        "2012-08-08": 13
        "2012-08-09": 14
        "2012-08-10": 14
        "2012-08-11": 12
        "2012-08-12": 13
        "2012-08-13": 13
        "2012-08-14": 15
    }
}
```

## User

### GET
```shell
curl https://api.positionly.com/v1/user.json?access_token=1eb14d5bd9d51af6f398ca2cd9b0fbcf
```

### Response
```json
{
    "id": 3
    "name": "Adrian Dulić"
    "email": "adulic@gmail.com"
    "avatar": "/avatars/medium/missing.png"
}
```