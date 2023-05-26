# Creating Inscription

Creating an Inscription does NOT require a previous transaction.

Here is what the header should look like when creating an inscription:

```
{
    "action": "createbim",
    "timestamp": number,
    "data": {

    }
}
```

Here is what the data field should look like:

```
"data": {
    "bimData": "base-64 encoded data", // The actual data of the BIM
    "sendTo": "address" // The address to send the BIM inscription to
}
```