---
title: "stories.getStoriesByID"
description: "stories.getStoriesByID parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stories_getStoriesByID.html
---
# Method: stories.getStoriesByID
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Optional|
|id|Array of [int](/API_docs/types/int.html) | Yes|


### Return type: [stories.Stories](/API_docs/types/stories.Stories.html)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$stories_Stories = $MadelineProto->stories->getStoriesByID(user_id: $InputUser, id: [$int, $int], );
```

