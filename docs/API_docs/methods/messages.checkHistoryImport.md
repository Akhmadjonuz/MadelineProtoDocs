---
title: "messages.checkHistoryImport"
description: "messages.checkHistoryImport parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_checkHistoryImport.html
---
# Method: messages.checkHistoryImport
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|import\_head|[string](/API_docs/types/string.html) | Yes|


### Return type: [messages.HistoryImportParsed](/API_docs/types/messages.HistoryImportParsed.html)

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_HistoryImportParsed = $MadelineProto->messages->checkHistoryImport(['import_head' => 'string', ]);
```
