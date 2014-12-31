---
title: API Documentation | Littldev

# Language tabs appear at the top of the right hand column.
# Selecting a language tab interactively switches code examples to that language
language_tabs:
  - shell: cURL
  #- ruby: Ruby
  #- python: Python
  #- PHP

toc_footers:
  - <a href='https://littlstar.com/register'>Join Littlstar to generate an API Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

# Each RESTful API endpoint is documented in its own includes template. The site layout will iterate over
# each of those files and output them in the order defined here.
includes:
  - example
  - errors

search: true
---

# Introduction

Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](http://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace `meowmeowmeow` with your personal API key.
</aside>

{% comment %}
  All individual RESTful endpoint documentation output below this point are defined in the includes/* directory.
{% endcomment %}

