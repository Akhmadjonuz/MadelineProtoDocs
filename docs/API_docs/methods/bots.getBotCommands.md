---
title: bots.getBotCommands
description: bots.getBotCommands parameters, return type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/bots_getBotCommands.html
---
# Method: bots.getBotCommands
[Back to methods index](index.md)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|scope|[BotCommandScope](../types/BotCommandScope.md) | Yes|
|lang\_code|[string](../types/string.md) | Yes|


### Return type: [Vector\_of\_BotCommand](../types/BotCommand.md)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Vector_of_BotCommand = $MadelineProto->bots->getBotCommands(['scope' => BotCommandScope, 'lang_code' => 'string', ]);
```

Or, if you're into Lua:

```lua
Vector_of_BotCommand = bots.getBotCommands({scope=BotCommandScope, lang_code='string', })
```
