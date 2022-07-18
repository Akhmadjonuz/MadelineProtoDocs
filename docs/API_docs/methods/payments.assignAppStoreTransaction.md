---
title: "payments.assignAppStoreTransaction"
description: "payments.assignAppStoreTransaction parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/payments_assignAppStoreTransaction.html
---
# Method: payments.assignAppStoreTransaction
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|restore|[Bool](/API_docs/types/Bool.html) | Optional|
|transaction\_id|[string](/API_docs/types/string.html) | Yes|
|receipt|[bytes](/API_docs/types/bytes.html) | Yes|


### Return type: [Updates](/API_docs/types/Updates.html)

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

// PHP 8+ syntax, use an array on PHP 7.
$Updates = $MadelineProto->payments->assignAppStoreTransaction(restore: Bool, transaction_id: 'string', receipt: 'bytes', );
```
