# Get Users

Get a collection of users.

```
GET /v1/users
```

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}

```sh
curl "https://api.your_domain.com/v1/users" \
    -H "Authorization: ApiKey YOUR_KEY"
```

{% endtab %}
{% endtabs %}

### Response

```
[
  {
    "userId": "newUser2",
    "email": "email2@userid.com"
  },
  {
    "userId": "email@userid.com",
    "email": null
  },
  {
    "userId": "04a2f51d-f3ce-4fa7-8aa6-26cc802d236e",
    "email": null
  },
  {
    "userId": "user1",
    "email": null
  }
]
```
