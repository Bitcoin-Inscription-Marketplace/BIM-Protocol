# Header and Compression

## Header

The Header is what is included in every single transaction containing BIM data. Here is an example header:

```
{
    "previousTx": "",  // The previous transaction hash that interacts with the BIM inscription. Not necessary if this is a collection creation or new inscription
    "action": "", // The action that is being performed. Possible values: createbim, createcoll, send, sell, auction, offer, acceptoffer, offerpayment
    "data": {

    }, // The actual BIM data
    "signature": "" // The signature for verifing that the person performing the transaction has access to the private keys for the owner of the inscription or the person making the offer. Not required on createbim and createcoll
}
```