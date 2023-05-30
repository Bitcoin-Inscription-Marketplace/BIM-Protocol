# Pay for Auction

Here is what the header should look like when purchasing an inscription that is listed for sale:

```
{
    "rootTx": "",
    "action": "payauction",
    "timestamp": number,
    "data": {

    }
}
```

This is what the data field should look like:

```
"data": {
    "transferTo": "" // The address that the BIM inscription should be transferred to. This must be the same as the winner of the auction
}
```

There MUST be an output in the same transaction that transfers the listed amount to the wallet in the auction, both are in the auction bid listing. If it isn't the correct amount, then the BIM transaction is considered invalid.