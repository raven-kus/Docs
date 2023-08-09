# Update an Object Type

Update an object type.

```
PUT /v1/object-types/:type
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter   | Description                                                                                                                                   | Type      | Required |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------- | -------- |
| `type`      | The id of the object type to update.                                                                                                          | URL param | yes      |
| `relations` | The set of all relations for this object type. See [object types concepts](https://docs.warrant.dev/concepts/object-types/) for more details. | JSON body | yes      |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v1/object-types/report" \
    -X PUT \
    -H "Authorization: ApiKey YOUR_KEY" \
    --data-raw \
    '{
        "relations": {
            "editor": {},
            "owner": {},
            "parent": {},
            "viewer": {}
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
    "editor": {},
    "owner": {},
    "parent": {},
    "viewer": {}
  }
}
```
