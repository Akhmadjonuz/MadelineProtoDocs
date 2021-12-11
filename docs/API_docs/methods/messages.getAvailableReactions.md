---
title: "messages.getAvailableReactions"
description: "messages.getAvailableReactions parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getAvailableReactions.html
---
# Method: messages.getAvailableReactions
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|hash|Array of [int](../types/int.md) | Optional|


### Return type: [messages.AvailableReactions](../types/messages.AvailableReactions.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_AvailableReactions = $MadelineProto->messages->getAvailableReactions(['hash' => [int, int], ]);
```

Or, if you're into Lua:

```lua
messages_AvailableReactions = messages.getAvailableReactions({hash={int}, })
```
