---
title: messages.deletePhoneCallHistory
description: messages.deletePhoneCallHistory parameters, return type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_deletePhoneCallHistory.html
---
# Method: messages.deletePhoneCallHistory
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|revoke|[Bool](../types/Bool.md) | Optional|


### Return type: [messages.AffectedFoundMessages](../types/messages.AffectedFoundMessages.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_AffectedFoundMessages = $MadelineProto->messages->deletePhoneCallHistory(['revoke' => Bool, ]);
```

Or, if you're into Lua:

```lua
messages_AffectedFoundMessages = messages.deletePhoneCallHistory({revoke=Bool, })
```
