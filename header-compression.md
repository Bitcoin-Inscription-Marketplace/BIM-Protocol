# Header and Compression

## Header

The Header is what is included in every single transaction containing BIM data. Any valid JSON can be used and does NOT need to have the whitespace, unlike below. Here is an example header:

```
{
    "previousTx": "",  // The previous transaction hash that interacts with the BIM inscription. Not necessary if this is a collection creation or new inscription
    "action": "", // The action that is being performed. Possible values: createbim, createcoll, send, sell, auction, offer, acceptoffer, offerpayment
    "data": {

    }, // The actual BIM data
    "signature": "" // The signature for verifing that the person performing the transaction has access to the private keys for the owner of the inscription or the person making the offer. Not required on createbim and createcoll
}
```

## Compression

Compression is done with the highly popular, LZMA2. This is because LZMA2 is known for incredibly high compression ratios, sacrificing speed for file size, which is very important when storing data in a blockchain. Compression is a required part of the BIM protocol and if compression is not performed then it is NOT BIM compliant. Please note that LZMA2 may increase file sizes on rare circumstances.