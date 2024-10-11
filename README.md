# gd-version

*(this is the dumbest thing in the world)*

When doing requests to the gd servers, some requests require you to get the `game_version` and `binary_version` of gd:

```py
# example from https://wyliemaster.github.io/gddocs/#/endpoints/accounts/backupGJAccountNew

import requests

data = {
    "userName": "APIAccount",
    "password": "********", # This would be APIAccount's password
    "gameVersion": 22,
    "binaryVersion": 42,
    "saveData": "H4sIAAAAAAAAA8VaWXObSBD[...]",
    "secret": "Wmfv3899gc9"
}

req = requests.post("http://www.robtopgames.org/database/accounts/backupGJAccountNew.php", data=data)
print(req.text)
```

## how to use

It's the simplest thing ever. Here's an example using **Python**:

```py
import requests
req = requests.get("https://geming400.github.io/gd-version/")
print(req.json())
# returns:
# {"game_version": 22,
# "binary_version": 42}
```
