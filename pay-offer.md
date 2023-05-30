# Pay for Offer

Here is what the header should look like when purchasing an inscription that is listed for sale:

```
{
    "rootTx": "",
    "action": "offerpayment",
    "timestamp": number,
    "data": {

    }
}
```

This is what the data field should look like:

```
"data": {
    "txAccept": "" // The transaction that shows the acceptance of the offer
}
```

There MUST be an output in the same transaction that transfers the listed amount to the wallet in the auction, both are in the auction bid listing. If it isn't the correct amount, then the BIM transaction is considered invalid.