# Categories

## All Categories

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/categories
```

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

Returns a paginated array of all categories.

### HTTP Request

`GET https://littlstar.com/api/v1/categories`

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

Returns the details for the requested category.

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
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/categories/1/videos
```

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

Returns a paginated array of all videos in the requested category.

### HTTP Request

`GET https://littlstar.com/api/v1/categories/:id/videos`

<aside class="notice">
When authenticated with an X-Apikey header two additional properties, `stared` and `downvoted`, will be included in each of the video objects in the array indicating whether the currently authenticated user has stared or downvoted that video.
</aside>

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
