# Users

## Single User

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/users/1
```

> unauthenticated JSON response

<!-- example response-->
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
    "slug": "jsmith",
    "username": "jsmith",
    "first_name": "John",
    "last_name": "Smith",
    "bio": "",
    "avatar_url": "",
    "cred": 5,
    "created_at": "1979-04-13T04:20:00.778-04:00",
    "updated_at": "1979-04-13T04:20:00.778-04:00",
    "videos_count": 0,
    "full_name": "John Smith",
    "followers_count": 0,
    "following_count": 0,
    "following": "true|false"
  }
}
```

> authenticated JSON response

<!-- example response-->
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
    "email": "jsmith@example.com",
    "gender": "male",
    "age": 35,
    "apikey": "a1b2c3d4e5f6g7h8i9j",
    "id": 1,
    "slug": "jsmith",
    "username": "jsmith",
    "first_name": "John",
    "last_name": "Smith",
    "bio": "",
    "avatar_url": "",
    "cred": 5,
    "created_at": "1979-04-13T04:20:00.778-04:00",
    "updated_at": "1979-04-13T04:20:00.778-04:00",
    "videos_count": 0,
    "full_name": "John Smith",
    "followers_count": 0,
    "following_count": 0,
    "following": "true|false"
  }
}
```

This endpoint will return the publicly available details for the requested user.

### HTTP Request

`GET https://littlstar.com/api/v1/users/:id`

<aside class="notice">
If the X-Apikey authentication header is provided and the apikey matches the requested user's apikey then their full private profile will be returned.
</aside>

<aside class="notice">
When authenticated with an X-Apikey header an additional property named following will be included in the response indicating whether the currently authenticated user is following the requested user.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug

### Error Responses

Code | Message
---- | -------
404  | Couldn't find User with 'id'=


## Single User Videos

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/users/1/videos
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

This endpoint will return all videos created by the requested user.

### HTTP Request

`GET https://littlstar.com/api/v1/users/:id/videos`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug
page      |         | Specific page of results
per_page  | 30      | specific number of results per page

### Error Responses

Code | Message
---- | -------
404  | Couldn't find User with 'id'=


## Single User Feed

<!-- example request -->
```shell
curl -i -H 'X-Apikey: [OPTIONAL_APIKEY]' https://littlstar.com/api/v1/users/1/feed
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

This endpoint returns a paginated array of all videos from a user's public or private feed. A user's public feed comprises all videos created by that user as well as those stared by the user. A user's private feed includes everything from their public feed plus all videos created or stared by the users they follow.

### HTTP Request

`GET https://littlstar.com/api/v1/users/:id/feed`

<aside class="notice">
The requested user's public feed is returned by default, their private feed can be returned by providing their apikey in the X-Apikey header.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug
page      |         | Specific page of results
per_page  | 30      | specific number of results per page

### Error Responses

Code | Message
---- | -------
404  | Couldn't find User with 'id'=


## Followers

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/users/1/followers
```

> successful JSON response

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": null,
    "data_count": 30
  },
  "pagination": {
    "total_pages": 4,
    "first_page": true,
    "last_page": false,
    "out_of_range": false,
    "previous_page": null,
    "current_page": 1,
    "next_page": 2
  },
  "data": [
    {},
    {
      "id": 1,
      "slug": "jsmith",
      "username": "jsmith",
      "first_name": "John",
      "last_name": "Smith",
      "bio": "",
      "avatar_url": "",
      "cred": 5,
      "created_at": "1979-04-13T04:20:00.778-04:00",
      "updated_at": "1979-04-13T04:20:00.778-04:00",
      "videos_count": 0,
      "full_name": "John Smith",
      "followers_count": 0,
      "following_count": 0,
      "following": "true|false"
    },
    {}
  ]
}
```

This endpoint returns a paginated array of all users following the requested user.

### HTTP Request

`GET https://littlstar.com/api/v1/users/:id/followers`

<aside class="notice">
When authenticated with an X-Apikey header an additional property named following will be included in the response indicating whether the currently authenticated user is following the requested user.
</aside>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug
page      |         | Specific page of results
per_page  | 30      | specific number of results per page

### Error Responses

Code | Message
---- | -------
404  | Couldn't find User with 'id'=


## Following

<!-- example request -->
```shell
curl -i https://littlstar.com/api/v1/users/1/following
```

> successful JSON response

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": null,
    "data_count": 30
  },
  "pagination": {
    "total_pages": 4,
    "first_page": true,
    "last_page": false,
    "out_of_range": false,
    "previous_page": null,
    "current_page": 1,
    "next_page": 2
  },
  "data": [
    {},
    {
      "id": 1,
      "slug": "jsmith",
      "username": "jsmith",
      "first_name": "John",
      "last_name": "Smith",
      "bio": "",
      "avatar_url": "",
      "cred": 5,
      "created_at": "1979-04-13T04:20:00.778-04:00",
      "updated_at": "1979-04-13T04:20:00.778-04:00",
      "videos_count": 0,
      "full_name": "John Smith",
      "followers_count": 0,
      "following_count": 0,
      "following": "true|false"
    },
    {}
  ]
}
```

This endpoint returns a paginated array of all users followed by the requested user.

### HTTP Request

`GET https://littlstar.com/api/v1/users/:id/following`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug
page      |         | Specific page of results
per_page  | 30      | specific number of results per page

### Error Responses

Code | Message
---- | -------
404  | Couldn't find User with 'id'=


## Follow

<!-- example request -->
```shell
curl -i -XPOST -H 'X-Apikey: [REQUIRED_APIKEY]' https://littlstar.com/api/v1/users/1/follow
```

> successful JSON response

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": "Successfully started following user",
    "data_count": null
  },
  "pagination": null,
  "data": []
}
```

Start following the requested user.

### HTTP Request

`POST https://littlstar.com/api/v1/users/:id/follow`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug

### Error Responses

Code | Message
---- | -------
401  | A valid apikey is required to access this endpoint
404  | Couldn't find User with 'id'=


## Unfollow

<!-- example request -->
```shell
curl -i -XDELETE -H 'X-Apikey: [REQUIRED_APIKEY]' https://littlstar.com/api/v1/users/1/follow
```

> successful JSON response

<!-- example response-->
```json
{
  "meta": {
    "code": 200,
    "errors": null,
    "message": "Successfully stopped following user",
    "data_count": null
  },
  "pagination": null,
  "data": []
}
```

Stop following the requested user.

### HTTP Request

`DELETE https://littlstar.com/api/v1/users/:id/follow`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id        |         | user's integer ID or slug

### Error Responses

Code | Message
---- | -------
401  | A valid apikey is required to access this endpoint
404  | Couldn't find User with 'id'=
