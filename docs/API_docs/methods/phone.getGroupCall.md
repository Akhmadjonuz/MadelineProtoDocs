---
title: "phone.getGroupCall"
description: "phone.getGroupCall parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/phone_getGroupCall.html
---
# Method: phone.getGroupCall
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|call|[InputGroupCall](/API_docs/types/InputGroupCall.html) | Yes|
|limit|[int](/API_docs/types/int.html) | Yes|


### Return type: [phone.GroupCall](/API_docs/types/phone.GroupCall.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$phone_GroupCall = $MadelineProto->phone->getGroupCall(['call' => InputGroupCall, 'limit' => int, ]);
```
