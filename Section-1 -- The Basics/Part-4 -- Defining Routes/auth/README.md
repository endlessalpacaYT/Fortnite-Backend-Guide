# Auth

1. Method: ```POST```, Route: ```/account/api/oauth/token```
```javascript
res.status(200).send({
    access_token: "eg1~fortnite",
    expires_in: 28800,
    expires_at: "9999-12-02T01:12:01.100Z",
    token_type: "bearer",
    refresh_token: "eg1~fortnite",
    refresh_expires: 86400,
    refresh_expires_at: "9999-12-02T01:12:01.100Z",
    account_id: "fornite",
    client_id: "fornite",
    internal_client: true,
    client_service: "fortnite",
    displayName: "fornite",
    app: "fortnite",
    in_app_id: "fornite",
    device_id: "fornite"
});
```

2. Method: ```POST```, Route: ```/account/api/oauth/verify```
```javascript
res.status(200).send({
    access_token: "eg1~fortnite",
    expires_in: 28800,
    expires_at: "9999-12-02T01:12:01.100Z",
    token_type: "bearer",
    refresh_token: "eg1~fortnite",
    refresh_expires: 86400,
    refresh_expires_at: "9999-12-02T01:12:01.100Z",
    account_id: "fornite",
    client_id: "fornite",
    internal_client: true,
    client_service: "fortnite",
    displayName: "fornite",
    app: "fortnite",
    in_app_id: "fornite",
    device_id: "fornite"
});
```

3. Method: ```DELETE```, Route: ```/account/api/oauth/sessions/kill```
```javascript
res.status(200).send({
    status: "OK",
    code: 200
})
```

4. Method: ```DELETE```, Route: ```/account/api/oauth/sessions/kill/:token```
```javascript
res.status(200).send({
    status: "OK",
    code: 200
})
```