---
title: "account.emailVerifiedLogin"
description: "account.emailVerifiedLogin attributes, type and example"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/account_emailVerifiedLogin.html
---
# Constructor: account.emailVerifiedLogin  
[Back to constructors index](/API_docs/constructors/index.html)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|email|[string](/API_docs/types/string.html) | Yes|
|sent\_code|[auth.SentCode](/API_docs/constructors/auth.SentCode.html) | Yes|



### Type: [account.EmailVerified](/API_docs/types/account.EmailVerified.html)


### Example:

```
$account_emailVerifiedLogin = ['_' => 'account.emailVerifiedLogin', 'email' => 'string', 'sent_code' => auth.SentCode];
```  