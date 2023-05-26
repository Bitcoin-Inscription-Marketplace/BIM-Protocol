# Purchasing Inscription that is listed for Sale

Here is what the header should look like when purchasing an inscription that is listed for sale:

```
{
    "previousTx": "",
    "action": "buy",
    "timestamp": number,
    "data": {

    }
}
```

This is what the data field should look like:

```
"data": {
    "transferTo": "" // The address that the BIM inscription should be transferred to
}
```

There MUST be an output in the same transaction that transfers the listed amount to the wallet in the listing, both are in the sale listing, which must be in the previousTx. If it isn't the correct amount, then the BIM transaction is considered invalid.