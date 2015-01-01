---
title: API Documentation | Littldev

# Language tabs appear at the top of the right hand column.
# Selecting a language tab interactively switches code examples to that language
language_tabs:
  - shell: cURL
  #- ruby: Ruby
  #- python: Python
  #- php: PHP

toc_footers:
  - <a href='https://littlstar.com/register'>Join Littlstar to generate an API Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>
  - '&copy; 2014 Little Star Media, Inc.'

# Each RESTful API endpoint is documented in its own includes template. The site layout will iterate over
# each of those files and output them in the order defined here.
includes:
  - login
  - users
  #- example
  #- errors

search: true
---

# Introduction

### Welcome to the official Littlstar V1 API documentation!

The following sections describe the features and functionality currently supported by our RESTful API. V1 of the Littlstar API is currently in an 'alpha' state, and as such all users should expect rapid changes and frequent breaks of backward compatibility.

If you come across any errors or bugs that you think we should know about, or if you'd just like to reach out and let us know how we're doing and what you'd like to see added and/or improved, please <a href="mailto:support@littlstar.com?subject=API%20Feedback">contact us directly</a>.

# Authentication

> To authenticate your request, include your API key in an X-Apikey header:

```shell
curl -H "X-Apikey: a1b2c3d4e5f6g7h8i9j" "endpoint"
```

> Make sure to replace `a1b2c3d4e5f6g7h8i9j` with your actual API key.

Most of the Littlstar API offers read-only access to available resources (videos, users, etc). However, there are interactive endpoints that require a user to be authenticated before access can be granted.

Littlstar uses an API key based system to grant authenticated access to users of our API. Upon successful [registration](https://littlstar.com/register) a random API key is generated for every user and can be retrieved from the bottom of your [settings](https://littlstar.com/settings) page after [logging in](https://littlstar.com/login).

<!-- All individual RESTful endpoint documentation output below this point are defined in the source/includes/_* directory. -->
