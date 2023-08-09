# Get a User by Id

Get a specific user by their `userId`.

```
GET /v1/users/:userId
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter | Description                | Type      | Required |
| --------- | -------------------------- | --------- | -------- |
| `userId`  | Id of the user to retrieve | URL param | yes      |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}

```sh
curl "https://api.your_domain.com/v1/users/d6ed6474-784e-407e-a1ea-42a91d4c52b9" \
  -H "Authorization: ApiKey YOUR_KEY"
```

{% endtab %}
{% endtabs %}

### Response <a href="#response" id="response"></a>

```
{
  "userId": "d6ed6474-784e-407e-a1ea-42a91d4c52b9",
  "email": "user@example.org"
}
```
