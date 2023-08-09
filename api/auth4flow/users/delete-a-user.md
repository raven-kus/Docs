# Delete a User

Delete a user by `userId`.

```
DELETE /v1/users/:userId
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter | Description                         | Type      | Required |
| --------- | ----------------------------------- | --------- | -------- |
| `userId`  | The `userId` of the user to delete. | URL param | yes      |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}

```sh
curl "https://api.your_domain.com/v1/users/d6ed6474-784e-407e-a1ea-42a91d4c52b9" \
    -X DELETE \
    -H "Authorization: ApiKey YOUR_KEY" \
```

{% endtab %}
{% endtabs %}

### Response <a href="#response" id="response"></a>

```
200 OK
```
