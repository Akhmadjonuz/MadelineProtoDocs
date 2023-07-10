---
title: "danog\\MadelineProto\\EventHandler\\OutgoingMessage: Represents an outgoing message."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\EventHandler\OutgoingMessage`
[Back to index](../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Represents an outgoing message.  



## Properties
* `$id`: `int` Message ID
* `$message`: `string` Content of the message
* `$chatId`: `int` ID of the chat where the message was sent
* `$senderId`: `int` ID of the sender of the message (optional)
* `$date`: `int` 
* `$mentioned`: `bool` Whether we were mentioned in this message
* `$silent`: `bool` Whether this message was sent without any notification (silently)
* `$fromScheduled`: `bool` Whether this message is a sent scheduled message
* `$pinned`: `bool` Whether this message is a pinned message
* `$protected`: `bool` Whether this message is protected (and thus can't be forwarded or downloaded)
* `$viaBotId`: `int` If
* `$legacy`: `bool` Whether this message is incomplete because an update of MadelineProto is required.
* `$rawUpdate`: `array` 
---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)