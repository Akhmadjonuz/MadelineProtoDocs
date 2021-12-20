---
title: channels.getSponsoredMessages
description: channels.getSponsoredMessages parameters, return type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_getSponsoredMessages.html
---
# Method: channels.getSponsoredMessages
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](../types/InputChannel.md) | Optional|


### Return type: [messages.SponsoredMessages](../types/messages.SponsoredMessages.md)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_SponsoredMessages = $MadelineProto->channels->getSponsoredMessages(['channel' => InputChannel, ]);
```

Or, if you're into Lua:

```lua
messages_SponsoredMessages = channels.getSponsoredMessages({channel=InputChannel, })
```
