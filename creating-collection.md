# Creating Collection

Creating an Inscription does NOT require a previous transaction.

Here is what the header should look like when creating an inscription:

```
{
    "action": "createcoll",
    "timestamp": number,
    "data": {

    }
}
```

Here is what the data field should look like:

```
"data": {
    "traits": [

    ], // All the traits of the BIMs in the collection
    "bims": [

    ] // All of the BIM inscriptions in the collection
}
```

Here is what the traits field should look like:

```
"traits": [
    {
        "traitId": "", // What the trait ID is. This is what is used to allocate traits to BIM inscription.
        "traitDisplayName": "" // The display name of the trait
    }
]
```

Here is what the bims field should look like

```
"bims": [
    {
        "previousTx": "", // The previous transaction that the BIM is involved in
        "traits": [""] // A list of the traits. Must be the Id and not the display name.
    }
]
```