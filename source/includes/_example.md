<!--heading for the resource name-->
# RESOURCE

<!--heading for the resource 'index' endpoint-->
## Get All RESOURCE

<!--optional example code-->
```shell
curl -H "X-Apikey: a1b2c3d4e5f6g7h8i9j" "http://example.com/RESOURCE"
```

> Optional example code annotation...

<!--optional example response-->
```json
[
  {
    "id": 1,
    "created_at": date/time,
    "updated_at": date/time
  },
  {
    "id": 2,
    "created_at": date/time,
    "updated_at": date/time
  }
]
```

<!--optional explanation of endpoint functionality-->
This endpoint retrieves all RESOURCE.

### HTTP Request

`GET http://example.com/RESOURCE`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | | specific page number of results
per_page | 30 | number of results per page

<!--option success 'green' message-->
<aside class="success">
success message
</aside>

<!--option notice 'blue' message-->
<aside class="notice">
notice message
</aside>

<!--option warning 'red' message-->
<aside class="warning">
warning message
</aside>


<!--heading for the resource 'show' endpoint-->
## Get a Specific RESOURCE

<!--optional example code-->
```shell
curl -H "X-Apikey: a1b2c3d4e5f6g7h8i9j" "http://example.com/RESOURCE/1"
```

> Optional example code annotation...

<!--optional example response-->
```json
{
  "id": 1,
  "created_at": date/time,
  "updated_at": date/time
}
```

<!--optional explanation of endpoint functionality-->
This endpoint retrieves a specific RESOURCE.

### HTTP Request

`GET http://example.com/RESOURCE/:id`

<!--optional success 'green' message-->
<aside class="success">
success message
</aside>

<!--optional notice 'blue' message-->
<aside class="notice">
notice message
</aside>

<!--optional warning 'red' message-->
<aside class="warning">
warning message
</aside>

