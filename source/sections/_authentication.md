# Authentication

> To authenticate your request, include your API key in an X-Apikey header:

```shell
curl -H "X-Apikey: a1b2c3d4e5f6g7h8i9j" "endpoint"
```

> Make sure to replace `a1b2c3d4e5f6g7h8i9j` with your actual API key.

Most of the Littlstar API offers read-only access to available resources (videos, photos, users, etc). However, there are interactive endpoints that require a user to be authenticated before access can be granted.

Littlstar uses an API key based system to grant authenticated access to users of our API. Upon successful [registration](https://littlstar.com/register) a random API key is generated for every user and can be retrieved from the bottom of your [settings](https://littlstar.com/settings) page after [logging in](https://littlstar.com/login).
