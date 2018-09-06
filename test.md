# chat.removeChatUser

Removers users from a chatroom

## Parameters

| Parameter | Type | Description       | 
| --- | :---: | :--- |
| chatID |  `Int`  | Unique chat identification number |
| userIDs |  `Int array`  | Array of unique user identification numbers to be removed |

## Result
The method returns `result:object` containing chat ID object array of participants and sequence ID.

| Parameter | Type | Description |
| ---- | ---- | ---- |
| participants | `Object array` | Array of participant objects |
| chatID | `Int` | Unique chat identification number | 
| seqID | `Int` | Sequence identification number |


## Example

### JSON Request example
```JSON
{
    "method": "chat.removeChatUser",
    "version": 2,
    "id":"1b9fc394-2213-4a74-8f7e-b39d10ec3d73",
    "params": {
        "chatID": 1234,
        "userIDs": [ 
                     123, 
                     456, 
                     789
                  ]
    }
}
```

### JSON Result example
```JSON
{
    "method": "chat.removeChatUser",
    "version": 2,
    "id":"1b9fc394-2213-4a74-8f7e-b39d10ec3d73",
    "result": {
        "participants": ---```TBD```---,
        "chatID": 1234,
        "seqID": 1234 
    }
}
```


## Possible errors

* Chat room has not been found with this chat room **ID**
* User has not been found in this request
* User has not been found in database, please try again later
* This method is not allowed at this time
* Incorrect JSON structure, please review documentations
