# Check

Check for the presence of relation(s) between specific subjects and objects in your access model (object types & warrants). This is the primary runtime 'check' API designed for use within your applications.

For example, you may want to check if the user (subject) identified by userId `5djfs6` can `view` (relation) the report (object) with id `avk2837`. A warrant check for this condition will return `Authorized` if the relation is valid as per the access model or `Not Authorized` if it is not valid.

```
POST /v2/authorize
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter  | Description                                                                                                                                                                                                                                                       | Type      | Required |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | -------- |
| `op`       | The logical operator to use when `warrants` contains more than one warrant. Valid values are `allOf` and `anyOf`. `allOf` will return “Authorized” only if all warrants are found, and `anyOf` will return “Authorized” if at least one of the warrants is found. | JSON body | no       |
| `warrants` | Array of warrants that you want to check. Each warrant should be formatted as below in the `Warrant Parameters` table.                                                                                                                                            | JSON body | yes      |

### Warrant Parameters <a href="#warrant-parameters" id="warrant-parameters"></a>

| Parameter    | Description                                                                                                                        | Type      | Required |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------- | --------- | -------- |
| `objectType` | The type of object. Must be one of your system's existing object types.                                                            | JSON body | yes      |
| `objectId`   | The id of the specific object.                                                                                                     | JSON body | yes      |
| `relation`   | The relation to check for this object to subject association. The relation must be valid as per the object type definition.        | JSON body | yes      |
| `subject`    | The specific subject for which access will be checked. Can be a specific object by id or an objectType, objectId and relation set. | JSON body | yes      |
| `context`    | Contextual data to use for resolving the access check. This data will be used when evaluating warrant policies.                    | JSON body | no       |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v2/authorize" \
    -X POST \
    -H "Authorization: ApiKey YOUR_KEY" \
    --data-raw \
    '{
        "warrants": [
            {
                "objectType": "report",
                "objectId": "avk2837",
                "relation": "viewer",
                "subject": {
                    "objectType": "user",
                    "objectId": "5djfs6"
                }
            }
        ]
    }'
```
{% endtab %}
{% endtabs %}

```
200 OK

{
    "code": 200,
    "result": "Authorized"
}
```
