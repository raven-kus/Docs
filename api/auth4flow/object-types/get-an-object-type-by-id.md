# Get an Object Type by Id

Get a specific object type by `type` id.

```
GET /v1/object-types/:type
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter | Description                                 | Type      | Required |
| --------- | ------------------------------------------- | --------- | -------- |
| `type`    | The type id of the object type to retrieve. | URL param | yes      |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}

```sh
curl "https://api.your_domain.com/v1/object-types/report" \
    -H "Authorization: ApiKey YOUR_KEY"
```

{% endtab %}
{% endtabs %}

### Response <a href="#response" id="response"></a>

```
{
  "type": "report",
  "relations": {
    "parent": {},
    "owner": {},
    "editor": {
      "inheritIf": "owner"
    },
    "viewer": {
      "inheritIf": "anyOf",
      "rules": [
        {
          "inheritIf": "editor"
        },
        {
          "inheritIf": "viewer",
          "ofType": "report",
          "withRelation": "parent"
        }
      ]
    }
  }
}
```
