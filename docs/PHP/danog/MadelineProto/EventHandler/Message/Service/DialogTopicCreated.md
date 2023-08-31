---
title: "danog\\MadelineProto\\EventHandler\\Message\\Service\\DialogTopicCreated: A [forum topic](https://core.telegram.org/api/forum#forum-topics) was created."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\EventHandler\Message\Service\DialogTopicCreated`
[Back to index](../../../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

A [forum topic](https://core.telegram.org/api/forum#forum-topics) was created.  



## Properties
* `$title`: `string` Topic name.
* `$iconColor`: `int` If no custom emoji icon is specified, specifies the color of the fallback topic icon (RGB), one of 0x6FB9F0, 0xFFD67E, 0xCB86DB, 0x8EEE98, 0xFF93B2, or 0xFB6F5F.
* `$iconEmojiId`: `?int` ID of the [custom emoji](https://core.telegram.org/api/custom-emoji) used as topic icon.
* `$id`: `int` Message ID
* `$out`: `bool` Whether the message is outgoing
* `$chatId`: `int` ID of the chat where the message was sent
* `$senderId`: `int` ID of the sender of the message
* `$replyToMsgId`: `?int` ID of the message to which this message is replying
* `$date`: `int` When was the message sent
* `$topicId`: `?int` ID of the forum topic where the message was sent
* `$threadId`: `?int` ID of the message thread where the message was sent
* `$replyToScheduled`: `bool` Whether this is a reply to a scheduled message
* `$mentioned`: `bool` Whether we were mentioned in this message
* `$silent`: `bool` Whether this message was sent without any notification (silently)
* `$ttlPeriod`: `?int` Time-to-live of the message

## Method list:
* [`__construct(\danog\MadelineProto\MTProto $API, array $rawMessage, array $info, string $title, int $iconColor, ?int $iconEmojiId)`](#__construct-danog-madelineproto-mtproto-api-array-rawmessage-array-info-string-title-int-iconcolor-int-iconemojiid)
* [`isReply(): bool`](#isreply-bool)
* [`getReply(class-string<\T> $class = 'danog\\MadelineProto\\EventHandler\\AbstractMessage'): ?\T`](#getreply-class-string-t-class-danog-madelineproto-eventhandler-abstractmessage-t)
* [`delete(bool $revoke = true): void`](#delete-bool-revoke-true-void)
* [`reply(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, array|null $replyMarkup = NULL, int|null $sendAs = NULL, int|null $scheduleDate = NULL, bool $silent = false, bool $noForwards = false, bool $background = false, bool $clearDraft = false, bool $noWebpage = false, bool $updateStickersetsOrder = false): \danog\MadelineProto\EventHandler\Message`](#reply-string-message-danog-madelineproto-parsemode-parsemode-danog-madelineproto-parsemode-text-array-null-replymarkup-null-int-null-sendas-null-int-null-scheduledate-null-bool-silent-false-bool-noforwards-false-bool-background-false-bool-cleardraft-false-bool-nowebpage-false-bool-updatestickersetsorder-false-danog-madelineproto-eventhandler-message)
* [`block(bool $stories): bool`](#block-bool-stories-bool)
* [`unblock(bool $stories): bool`](#unblock-bool-stories-bool)

## Methods:
### `__construct(\danog\MadelineProto\MTProto $API, array $rawMessage, array $info, string $title, int $iconColor, ?int $iconEmojiId)`




Parameters:

* `$API`: `\danog\MadelineProto\MTProto`   
* `$rawMessage`: `array`   
* `$info`: `array`   
* `$title`: `string`   
* `$iconColor`: `int`   
* `$iconEmojiId`: `?int`   


#### See also: 
* `\danog\MadelineProto\MTProto`




### `isReply(): bool`

Check if the current message replies to another message.



### `getReply(class-string<\T> $class = 'danog\\MadelineProto\\EventHandler\\AbstractMessage'): ?\T`

Get replied-to message.
May return null if the replied-to message was deleted or if the message does not reply to any other message.

Parameters:

* `$class`: `class-string<\T>` Only return a reply if it is of the specified type, return null otherwise.  


#### See also: 
* `\T`




### `delete(bool $revoke = true): void`

Delete the message.


Parameters:

* `$revoke`: `bool` Whether to delete the message for all participants of the chat.  



### `reply(string $message, \danog\MadelineProto\ParseMode $parseMode = \danog\MadelineProto\ParseMode::TEXT, array|null $replyMarkup = NULL, int|null $sendAs = NULL, int|null $scheduleDate = NULL, bool $silent = false, bool $noForwards = false, bool $background = false, bool $clearDraft = false, bool $noWebpage = false, bool $updateStickersetsOrder = false): \danog\MadelineProto\EventHandler\Message`

Reply to the message.


Parameters:

* `$message`: `string` Message to send  
* `$parseMode`: `\danog\MadelineProto\ParseMode` Parse mode  
* `$replyMarkup`: `array|null` Keyboard information.  
* `$sendAs`: `int|null` Peer to send the message as.  
* `$scheduleDate`: `int|null` Schedule date.  
* `$silent`: `bool` Whether to send the message silently, without triggering notifications.  
* `$noForwards`: `bool`   
* `$background`: `bool` Send this message as background message  
* `$clearDraft`: `bool` Clears the draft field  
* `$noWebpage`: `bool` Set this flag to disable generation of the webpage preview  
* `$updateStickersetsOrder`: `bool` Whether to move used stickersets to top  


#### See also: 
* [`\danog\MadelineProto\ParseMode`: Indicates a parsing mode for text.](../../../../../danog/MadelineProto/ParseMode.html)
* [`\danog\MadelineProto\EventHandler\Message`: Represents an incoming or outgoing message.](../../../../../danog/MadelineProto/EventHandler/Message.html)




### `block(bool $stories): bool`

Adds the user to the blacklist.


Parameters:

* `$stories`: `bool`   



### `unblock(bool $stories): bool`

Deletes the user from the blacklist.


Parameters:

* `$stories`: `bool`   



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)