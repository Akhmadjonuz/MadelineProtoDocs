---
title: inputNotifyPeer
description: Notifications generated by a certain user or group.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: inputNotifyPeer  
[Back to constructors index](index.md)



Notifications generated by a certain user or group.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | Optional|User or group|



### Type: [InputNotifyPeer](../types/InputNotifyPeer.md)


### Example:

```php
$inputNotifyPeer = ['_' => 'inputNotifyPeer', 'peer' => InputPeer];
```  


Or, if you're into Lua:

```lua
inputNotifyPeer={_='inputNotifyPeer', peer=InputPeer}

```

