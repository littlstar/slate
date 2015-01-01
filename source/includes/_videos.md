# Videos

## All Videos

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/videos
```

<!-- example response -->
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

Returns a paginated array of all videos.

### HTTP Request

`GET https://littlstar.com/api/v1/videos`

<aside class="notice">
When authenticated with an X-Apikey header two additional properties, `stared` and `downvoted`, will be included in each of the video objects in the array indicating whether the currently authenticated user has stared or downvoted that video.
</aside>

<aside class="warning">
This endpoint currently returns a select subset of sponsored and featured videos.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page      |         | specific page number of results
per_page  | 30      | number of results per page


## Sponsored Videos

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/videos/sponsored
```

<!-- example response -->
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

Returns a paginated array of all sponsored videos.

### HTTP Request

`GET https://littlstar.com/api/v1/videos/sponsored`

<aside class="notice">
When authenticated with an X-Apikey header two additional properties, `stared` and `downvoted`, will be included in each of the video objects in the array indicating whether the currently authenticated user has stared or downvoted that video.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page      |         | specific page number of results
per_page  | 30      | number of results per page


## Featured Videos

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/videos/featured
```

<!-- example response -->
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

This endpoint returns a paginated array of all featured videos.

### HTTP Request

`GET https://littlstar.com/api/v1/videos/featured`

<aside class="notice">
When authenticated with an X-Apikey header two additional properties, `stared` and `downvoted`, will be included in each of the video objects in the array indicating whether the currently authenticated user has stared or downvoted that video.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page      |         | specific page number of results
per_page  | 30      | number of results per page


## Latest Videos

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/videos/latest
```

<!-- example response -->
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

Returns a paginated array of all latest videos.

### HTTP Request

`GET https://littlstar.com/api/v1/videos/latest`

<aside class="notice">
When authenticated with an X-Apikey header two additional properties, `stared` and `downvoted`, will be included in each of the video objects in the array indicating whether the currently authenticated user has stared or downvoted that video.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page      |         | specific page number of results
per_page  | 30      | number of results per page


## Single Video

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/videos/1
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
    "slug": "b698da8a",
    "title": "Time Trials",
    "description": "Ride along with a real Formula One driver and experience the thrill of speeding around the track first hand!",
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
  }
}
```

Returns the details for the requested video.

### HTTP Request

`GET https://littlstar.com/api/v1/videos/:id`

<aside class="notice">
A request for a video that is encoding, deleted, failed or currently hidden will result in a 403 error response with an appropriate error message. However, if the video is **hidden** and the current request has been authenticated by sending an X-Apikey header and the user requesting the video is the creator of the video, that video's details will be returned.
</aside>

<aside class="notice">
When authenticated with an X-Apikey header two additional properties, `stared` and `downvoted`, will be included in each of the video objects in the array indicating whether the currently authenticated user has stared or downvoted that video.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | video's integer ID or slug

### Error Responses

Code | Message
---- | -------
404  | Couldn't find Video with 'id'=
403  | Video is currently encoding
403  | Video has been deleted
403  | Video is not available
403  | Video is currently hidden


## Star

<!-- example request -->
```shell
curl -i -XPOST -H 'X-Apikey: [REQUIRED_APIKEY]' https://littstar.com/api/v1/videos/1/star
```

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": "Successfully starred video",
    "data_count": null
  },
  "pagination": null,
  "data": []
}
```

Star the requested video.

### HTTP Request

`POST https://littstar.com/api/v1/videos/1/star`

<aside class="warning">
An X-Apikey header containing a valid API key is required to access this endpoint.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | video's integer ID or slug

### Error Responses

Code | Message
---- | -------
401  | A valid apikey is required to access this endpoint
404  | Couldn't find Video with 'id'=


## Unstar

<!-- example request -->
```shell
curl -i -XDELETE -H 'X-Apikey: [REQUIRED_APIKEY]' https://littlstar.com/api/v1/videos/1/star
```

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": "Successfully unstarred video",
    "data_count": null
  },
  "pagination": null,
  "data": []
}
```

Unstar the requested video.

### HTTP Request

`DELETE https://littlstar.com/api/v1/videos/:id/star`

<aside class="warning">
An X-Apikey header containing a valid API key is required to access this endpoint.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | video's integer ID or slug

### Error Responses

Code | Message
---- | -------
401  | A valid apikey is required to access this endpoint
404  | Couldn't find Video with 'id'=


## Downvote

<!-- example request -->
```shell
curl -i -XPOST -H 'X-Apikey: [REQUIRED_APIKEY]' https://littstar.com/api/v1/videos/1/downvote
```

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": "Successfully downvoted video",
    "data_count": null
  },
  "pagination": null,
  "data": []
}
```

Downvote the requested video.

### HTTP Request

`POST https://littstar.com/api/v1/videos/1/downvote`

<aside class="warning">
An X-Apikey header containing a valid API key is required to access this endpoint.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | video's integer ID or slug

### Error Responses

Code | Message
---- | -------
401  | A valid apikey is required to access this endpoint
404  | Couldn't find Video with 'id'=


## Undownvote

<!-- example request -->
```shell
curl -i -XDELETE -H 'X-Apikey: [REQUIRED_APIKEY]' https://littlstar.com/api/v1/videos/1/downvote
```

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": "Successfully undownvoted video",
    "data_count": null
  },
  "pagination": null,
  "data": []
}
```

Undownvote the requested video.

### HTTP Request

`DELETE https://littlstar.com/api/v1/videos/:id/downvote`

<aside class="warning">
An X-Apikey header containing a valid API key is required to access this endpoint.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | video's integer ID or slug

### Error Responses

Code | Message
---- | -------
401  | A valid apikey is required to access this endpoint
404  | Couldn't find Video with 'id'=