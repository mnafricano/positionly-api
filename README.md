## Beta Notice

* Please note that this is a beta version of our API
* Methods, keys, and structure might change before the API hits a stable branch

## OAuth2

This information is provided to you by Positionly.

* **Client ID**: de3be2752e8ae27a11cd96a6b0999b0f
* **Client secret**: 8d87664221c09681c3d3bc283a50bf73

## Authorization

### POST
```shell
curl -X POST -d 'grant_type=password&username=<your_username>&password=<your_password>&client_id=de3be2752e8ae27a11cd96a6b0999b0f&client_secret=8d87664221c09681c3d3bc283a50bf73' 'https://auth.positionly.com/oauth2/token'
```

### Response
```json
{
    "access_token": "37e120ae8ae9752105079bb28f07cfff",
    "token_type": "bearer",
    "expires_in": 3599,
    "refresh_token": "6b6f99496dde0faf947e8b964360d2e7"
}
```

## Refresh token

### POST
```shell
curl -X POST -d 'grant_type=refresh_token&refresh_token=<your_refresh_token>&client_id=de3be2752e8ae27a11cd96a6b0999b0f&client_secret=8d87664221c09681c3d3bc283a50bf73' 'https://auth.positionly.com/oauth2/token'
```

### Response
```json
{
    "access_token": "1eb14d5bd9d51af6f398ca2cd9b0fbcf",
    "token_type": "bearer",
    "expires_in": 3599,
    "refresh_token": "6b6f99496dde0faf947e8b964360d2e7"
}
```

## Request examples

```shell
curl -H 'Authorization: <access token>' 'https://api.positionly.com/v1/...'
```

or

```shell
curl 'https://api.positionly.com/v1/...?access_token=<access token>'
```
