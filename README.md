#### <a id="post_wallets_virtual"></a> Submit a virtual account ####

```
Method: POST 
URL: /wallets/iban/
```

The Virtual account management solution revolve around a self-service web-based delivery mechanism that offers customers real-time information access and account management within a virtual banking domain.

A customer is represented by a structure of accounts. Each of the customer's physical accounts in the bank's accounting system can be represented as a Master Account with its own unique iban. Each of these Master Accounts can have a set of ibans (virtual accounts) that must be in the same currency. 

Payments to and from the virtual account will be booked on the customer's physical account in the bank's accounting system. Information concerning the specific iban related to those payments will be provided in the account management system giving to the customer the possibility to earmark and easily allocate funds per business unit, per client, or incoming/outgoing transactions.

**Caution :** This service is only available for FX4BIZ users that have suscribed to the virtual account option program.

**Parameters:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| walletId | [ID](../conventions/formattingConventions.md#type_id) | Required | The code identifying on which physical account allocate funds linked to this virtual account. |

**Returns:**

| Field | Type | Description |
|-------|------|-------------|
| wallet | [Wallet Object](../objects/objects.md#wallet_object) | An object representing the wallet you just created. |

**Example:**
```js
POST /wallets/
{
    "walletId": "ND2da3"
}
```

<hr />


