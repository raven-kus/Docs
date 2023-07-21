# Update a User

Update a user given their `userId`.

```
PUT /v1/users/:userId
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter | Description                                                   | Type      | Required |
| --------- | ------------------------------------------------------------- | --------- | -------- |
| `userId`  | The id of the user to update. Note that id cannot be changed. | URL param | yes      |
| `email`   | The email of the user.                                        | JSON body | no       |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v1/users/d6ed6474-784e-407e-a1ea-42a91d4c52b9" \
    -X PUT \
    -H "Authorization: ApiKey YOUR_KEY" \
    --data-raw \
    '{ "email": "updated@email.com" }'
```
{% endtab %}
{% endtabs %}

### Response <a href="#response" id="response"></a>

```
{
  "userId": "d6ed6474-784e-407e-a1ea-42a91d4c52b9",
  "email": "updated@email.com"
}
```
