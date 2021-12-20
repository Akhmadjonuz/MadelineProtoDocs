---
title: messages.getFavedStickers
description: Get faved stickers
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getFavedStickers.html
---
# Method: messages.getFavedStickers
[Back to methods index](index.md)



Get faved stickers

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|hash|[long](../types/long.md) |  | Yes|


### Return type: [messages.FavedStickers](../types/messages.FavedStickers.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_FavedStickers = $MadelineProto->messages->getFavedStickers(['hash' => long, ]);
```

Or, if you're into Lua:

```lua
messages_FavedStickers = messages.getFavedStickers({hash=long, })
```
