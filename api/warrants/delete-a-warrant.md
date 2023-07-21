# Delete a Warrant

Delete a warrant, if it exists. The warrant to be deleted is specified by the combination of the `objectType`, `objectId`, `relation`, `subject`, and (optionally) `policy` provided in the delete request.

```
DELETE /v1/warrants
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter    | Description                                                                                                                                                                                                          | Type      | Required |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | -------- |
| `objectType` | The type of object. Must be one of your system's existing object types.                                                                                                                                              | JSON body | yes      |
| `objectId`   | The id of the specific object.                                                                                                                                                                                       | JSON body | yes      |
| `relation`   | The relation for this object to subject association. The relation must be valid as per the object type definition.                                                                                                   | JSON body | yes      |
| `subject`    | The specific subject (object, user etc.) to be associated with the object. A subject can either be a specific object (by id) or a group of objects defined by a set containing an objectType, objectId and relation. | JSON body | yes      |
| `policy`     | A boolean expression that must evaluate to `true` for this warrant to apply. The expression can reference variables that are provided in the `context` attribute of access check requests.                           | JSON body | no       |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v1/warrants" \
    -X DELETE \
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
    }'Response
```
{% endtab %}
{% endtabs %}

```
200 OK
```
