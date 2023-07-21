# Get Object Types

Get list of all object types.

```
GET /v1/object-types
```

### Request <a href="#request" id="request"></a>



{% tabs %}
{% tab title="Curl" %}
```shell
curl "https://api.warrant.dev/v1/object-types" \
    -H "Authorization: ApiKey YOUR_KEY"
```
{% endtab %}
{% endtabs %}

### Response <a href="#response" id="response"></a>

```
[
  {
    "type": "role",
    "relations": {
      "parent": {},
      "owner": {},
      "editor": {
        "inheritIf": "owner"
      },
      "member": {
        "inheritIf": "member",
        "ofType": "role",
        "withRelation": "parent"
      },
      "viewer": {
        "inheritIf": "editor"
      }
    }
  },
  {
    "type": "tenant",
    "relations": {
      "member": {}
    }
  }
]
```

\
\
