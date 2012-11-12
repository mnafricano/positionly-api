## Positions

### GET
```shell
curl https://api.positionly.com/v1/accounts/<account id>/websites/<website id>/engines/<engine id>/keywords/<keyword id>/positions.json?date_from=2012-08-01&date_to=2012-08-30
```

### Response
```json
{
    "id": 1,
    "group_id": null,
    "website_id": 1,
    "name": "example",
    "positions": {
        "2012-08-04": 15,
        "2012-08-01": 14,
        "2012-08-02": 15,
        "2012-08-03": 15,
        "2012-08-05": 15,
        "2012-08-06": 15,
        "2012-08-07": 14,
        "2012-08-08": 13,
        "2012-08-09": 14,
        "2012-08-10": 14,
        "2012-08-11": 12,
        "2012-08-12": 13,
        "2012-08-13": 13,
        "2012-08-14": 15
    }
}
```
