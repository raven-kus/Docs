# Create a User

```
POST /v1/users
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter | Description                                                                                                                                                                                                                                                                                                                                           | Type      | Required |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | -------- |
| `userId`  | User defined string identifier for this user. If not provided, Warrant will create an id for the user and return it. In this case, you should store the id in your system as you will need to provide it for any authorization requests for that user. Note that userIds in Warrant must be composed of alphanumeric chars and/or '-', '\_', and '@'. | JSON body | no       |
| `email`   | Email address for this user (optional). Designed to be used as a UI-friendly identifier.                                                                                                                                                                                                                                                              | JSON body | no       |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}

```sh
curl "https://api.your_domain.com/v1/users" \
  -X POST \
  -H "Authorization: ApiKey YOUR_KEY" \
  --data-raw \
  '{"userId":"d6ed6474-784e-407e-a1ea-42a91d4c52b9"}'Response
```

{% endtab %}
{% endtabs %}

```
{
  "userId": "d6ed6474-784e-407e-a1ea-42a91d4c52b9",
  "email": null
}
```
