# Categories

## All Categories

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/categories
```

> successful JSON response

<!-- example response -->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": null,
    "data_count": 11
  },
  "pagination": {
    "total_pages": 1,
    "first_page": true,
    "last_page": true,
    "out_of_range": false,
    "previous_page": null,
    "current_page": 1,
    "next_page": null
  },
  "data": [
    {},
    {
      "id": 2,
      "name": "Sports",
      "created_at": "1979-04-13T04:20:00.778-04:00",
      "updated_at": "1979-04-13T04:20:00.778-04:00"
    },
    {}
  ]
}
```

This endpoint returns a paginated array of all categories.

### HTTP Request

`GET https://littlstar.com/api/v1/categories

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page      |         | specific page number of results
per_page  | 30      | number of results per page



## Single Category

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/categories/1
```

> successful JSON response

<!-- example response -->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": null,
    "data_count": null
  },
  "pagination": null,
  "data": {
    "id": 1,
    "name": "Sports",
    "created_at": "1979-04-13T04:20:00.778-04:00",
    "updated_at": "1979-04-13T04:20:00.778-04:00"
  }
}
```

This endpoint will return a JSON object containing specific details about the requested category.

### HTTP Request

`GET https://littlstar.com/api/v1/categories/:id`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | category's integer ID or slug

### Error Responses

Code | Message
---- | -------
404  | Couldn't find Category with 'id'=


## Single Category Videos

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/categories/1/videos
```

> successful JSON response

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": null,
    "data_count": 3
  },
  "pagination": {
    "total_pages": 1,
    "first_page": true,
    "last_page": true,
    "out_of_range": false,
    "previous_page": null,
    "current_page": 1,
    "next_page": null
  },
  "data": [
    {},
    {
      "id": 1,
      "slug": "b698da8a",
      "title": "Time Trials",
      "description": "",
      "sponsored": false,
      "featured": true,
      "score": 0,
      "created_at": "1979-04-13T04:20:00.778-04:00",
      "updated_at": "1979-04-13T04:20:00.778-04:00",
      "views": 0,
      "duration": 0,
      "versions": {
        "web": "",
        "mobile": "",
        "webm": ""
      },
      "posters": {
        "web": "",
        "mobile": "",
        "small": ""
      },
      "banners": {
        "large": "",
        "medium": "",
        "small": "",
        "thumbnail": ""
      },
      "user": {
        "id": "",
        "slug": "",
        "username": "",
        "avatar_url": ""
      },
      "stars": 0,
      "downvotes": 0,
      "stared": "true|false",
      "downvoted": "true|false"
    },
    {}
  ]
}
```

This endpoint will return all videos from the requested category.

### HTTP Request

`GET https://littlstar.com/api/v1/categories/:id/videos`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | category's integer ID or slug
page      |         | Specific page of results
per_page  | 30      | specific number of results per page

### Error Responses

Code | Message
---- | -------
404  | Couldn't find Category with 'id'=
