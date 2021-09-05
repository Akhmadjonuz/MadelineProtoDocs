---
title: messages.chatAdminsWithInvites
description: messages.chatAdminsWithInvites attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/messages_chatAdminsWithInvites.html
---
# Constructor: messages.chatAdminsWithInvites  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|admins|Array of [ChatAdminWithInvites](../types/ChatAdminWithInvites.md) | Yes|
|users|Array of [User](../types/User.md) | Yes|



### Type: [messages.ChatAdminsWithInvites](../types/messages.ChatAdminsWithInvites.md)


### Example:

```php
$messages_chatAdminsWithInvites = ['_' => 'messages.chatAdminsWithInvites', 'admins' => [ChatAdminWithInvites, ChatAdminWithInvites], 'users' => [User, User]];
```  


Or, if you're into Lua:

```lua
messages_chatAdminsWithInvites={_='messages.chatAdminsWithInvites', admins={ChatAdminWithInvites}, users={User}}

```

