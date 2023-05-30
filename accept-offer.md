# Accepting Offer

Here is what the header should look like when accepting an offer:

```
{
    "rootTx": "",
    "action": "acceptoffer",
    "timestamp": number,
    "data": {

    },
    "signature": "SHA3-512 hash of signature of rootTx + action + timestamp + data"
}
```

This is what the data field should look like:

```
"data": {
    "txAccept": "" // The transaction that the offer was created in
}
```