# unblockGJUser20.php

Unblocks a user.

## Parameters

### Required Parameters

**accountID** - The unblocking person's account ID

**gjp2** - The unblocking person's [GJP2](/topics/encryption/gjp.md)

**targetAccountID** - The account ID of the person getting unblocked

**secret** - Wmfd2893gb7

### Optional Parameters

**gameVersion** - 22

**binaryVersion** - 42

**gdw** - 0

## Response

Always returns 1, regardless of if the target account exists or not.

## Example

<!-- tabs:start -->

### **Python**

```py
import requests

# With this code, DevExit is unblocking RobTop

data = {
        "accountID": 173831, # DevExit's account ID
        "gjp": "********", # This would be DevExit's password encoded with GJP encryption
        "targetAccountID": 71, # Robtop's account ID
        "secret": "Wmfd2893gb7"
}

req = requests.post("http://boomlings.com/database/unblockGJUser20.php", data=data)
print(req.text)

```

**Response**
```py
1
```

<!-- tabs:end -->
