# Create an Object Type

Create a new object type.

```
POST /v1/object-types
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                          | Type      | Required |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | -------- |
| `type`      | A string identifier for this new object type. The `type` can only be composed of lower-case alphanumeric chars and/or '-' and '\_'.                                                                                                                                                                                                                                                                                                                  | JSON body | yes      |
| `relations` | The set of all supported relationships that objects of this type can have with other objects (established via warrants). By default, each provided relation can be explicitly assigned to objects via warrants. This default case is represented by the empty relation definition `{}`. You can also specify more complex relation inheritance rules. See [object types concepts](https://docs.warrant.dev/concepts/object-types/) for more details. | JSON body | yes      |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v1/object-types" \
    -X POST \
    -H "Authorization: ApiKey YOUR_KEY" \
    --data-raw \
    '{
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
    }'
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
