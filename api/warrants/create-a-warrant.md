# Create a Warrant

Create a new warrant that associates an object (`objectType` and `objectId`) to a `subject` via a `relation`.

```
POST /v1/warrants
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter    | Description                                                                                                                                                                                | Type      | Required |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | -------- |
| `objectType` | The type of object. Must be one of your system's existing object types.                                                                                                                    | JSON body | yes      |
| `objectId`   | The id of the specific object.                                                                                                                                                             | JSON body | yes      |
| `relation`   | The relation for this object to subject association. The relation must be valid as per the object type definition.                                                                         | JSON body | yes      |
| `subject`    | The subject for which this warrant applies. Subject can be a specific object (by id) or a set of objects matching the given objectType, objectId and relation.                             | JSON body | yes      |
| `policy`     | A boolean expression that must evaluate to `true` for this warrant to apply. The expression can reference variables that are provided in the `context` attribute of access check requests. | JSON body | no       |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v1/warrants" \
    -X POST \
    -H "Authorization: ApiKey YOUR_KEY" \
    --data-raw \
    '{
        "objectType": "report",
        "objectId": "23ft346",
        "relation": "editor",
        "subject": {
            "objectType": "user",
            "objectId": "15ads7823a9df7as433gk23dd"
        }
    }'
```
{% endtab %}
{% endtabs %}

```
{
  "objectType": "report",
  "objectId": "23ft346",
  "relation": "editor",
  "subject": {
    "objectType": "user",
    "objectId": "15ads7823a9df7as433gk23dd"
  }
}
```
