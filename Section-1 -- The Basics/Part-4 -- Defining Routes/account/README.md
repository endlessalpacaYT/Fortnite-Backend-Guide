# Account

1. Method: `POST`, Route: `/fortnite/api/game/v2/tryPlayOnPlatform/account/:accountId`
```javascript
res.setHeader("Content-Type", "text/plain");
res.status(200).send("true");
```

2. Method: ```GET```, Route: ```/account/api/public/account/:accountId/externalAuths```
```javascript
res.status(200).send([]);
```

3. Method: ```GET```, Route: ```/fortnite/api/game/v2/enabled_features```
```javascript
res.status(200).send([]);
```

4. Method: ```GET```, Route: ```/content-controls/:accountId```
```javascript
res.status(200).send([]);
```

5. Method: ```GET```, Route: ```/account/api/public/account```
```javascript
res.status(200).send({
    id: "fortnite",
    displayName: "fortnite",
    externalAuth: {}
});
```

6. Method: ```GET```, Route: ```/account/api/public/account/:accountId```
```javascript
res.status(200).send({
    id: "fortnite",
    displayName: "fortnite",
    name: "fortnite",
    email: "fortnite@fortnite.dev",
    failedLoginAttempts: 0,
    lastLogin: "Timestamp",
    numberOfDisplayNameChanges: 0,
    ageGroup: "UNKNOWN",
    headless: false,
    country: "US",
    lastName: "User",
    links: {},
    preferredLanguage: "en",
    canUpdateDisplayName: false,
    tfaEnabled: true,
    emailVerified: true,
    minorVerified: true,
    minorExpected: true,
    minorStatus: "UNKNOWN"
});
```

7. Method: ```POST```, Route: ```/api/v1/user/setting```
```javascript
res.status(200).send({
    status: "OK",
    code: 200
});
```

8. Method: ```GET```, Route: ```/socialban/api/public/v1/:accountId```
```javascript
res.status(200).send([]);
```

9. Method: ```GET```, Route: ```/presence/api/v1/_/:accountId/settings/subscriptions```
```javascript
res.status(200).send([]);
```

10. Method: ```GET```, Route: ```/fortnite/api/game/v2/privacy/account/:accountId```
```javascript
res.status(200).send([]);
```