# Keychain

## This requires an external file which i have uploaded. Creds to LawinserverV2 for the keychain.json

First Require the file:
```javascript
const keychain = require("./path/to/your/keychain.json");
```

then define the route:
```javascript
app.get('/fortnite/api/storefront/v2/keychain', (req, res) => {
    return res.status(200).send(keychain);
})
```