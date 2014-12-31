# Login

<!-- example request -->
```shell
curl -i -XPOST -H 'Content-Type: application/json' -d '{\"user\":{\"login\":\"\",\"password\":\"\"}}' https://littlstar.com/api/v1/login
```

> successful login JSON response:

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

Login to an existing user account.

### HTTP Request

`POST https://littlstar.com/api/v1/login`

### Query Parameters

Parameter      | Default | Description
---------      | ------- | -----------
user[login]    |         | user's email or username
user[password] |         | user's password

### Error Responses

Code | Message
---- | -------
400  | Missing required user parameter
401  | Invalid login or password
