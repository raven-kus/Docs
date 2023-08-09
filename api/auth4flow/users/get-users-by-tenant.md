# Get Users by Tenant

Get the users associated with a specific `tenant`.

```
GET /v1/tenants/:tenantId/users
```

### Parameters <a href="#parameters" id="parameters"></a>

| Parameter  | Description                                | Type      | Required |
| ---------- | ------------------------------------------ | --------- | -------- |
| `tenantId` | Id of the tenant from which to fetch users | URL param | yes      |

### Request <a href="#request" id="request"></a>

{% tabs %}
{% tab title="Curl" %}
```sh
curl "https://api.warrant.dev/v1/tenants/43f86srgs/users" \
    -H "Authorization: ApiKey YOUR_KEY"
```
{% endtab %}
{% endtabs %}

### Response

```
[
  {
    "userId": "a-user-id",
    "email": "user@example.org"
  },
  {
    "userId": "example2.com",
    "email": "hello@example2com"
  }
]
```
