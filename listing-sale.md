# Listing Inscription for Sale

Here is what the header should look like when listing an inscription for sale:

```
{
    "rootTx": "",
    "action": "sell",
    "timestamp": number,
    "data": {

    },
    "signature": "SHA3-512 hash of signature of rootTx + action + timestamp + data"
}
```

This is what the data field should look like:

```
"data": {
    "price": number, // The price in satoshis
    "payTo": "" // The address that the payment must be given to
}
```