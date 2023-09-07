---
title: "danog\\MadelineProto\\MTProtoTools\\DialogId: Represents the type of a bot API dialog ID."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\MTProtoTools\DialogId`
[Back to index](../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Represents the type of a bot API dialog ID.  




## Constants
* `danog\MadelineProto\MTProtoTools\DialogId::USER`: 

* `danog\MadelineProto\MTProtoTools\DialogId::CHAT`: 

* `danog\MadelineProto\MTProtoTools\DialogId::CHANNEL_OR_SUPERGROUP`: 

* `danog\MadelineProto\MTProtoTools\DialogId::SECRET_CHAT`: 

## Properties
* `$name`: `string` 

## Method list:
* [`getType(int $id): self`](#gettype)
* [`fromSecretChatId(int $id): \int Bot API secret chat ID`](#fromsecretchatid)
* [`toSecretChatId(int $id): \int MTProto secret chat ID`](#tosecretchatid)
* [`fromSupergroupOrChannel(int $id): int`](#fromsupergrouporchannel)
* [`toSupergroupOrChannel(int $id): int`](#tosupergrouporchannel)
* [`isSupergroupOrChannel(int $id): bool`](#issupergrouporchannel)
* [`isChat(int $id): bool`](#ischat)
* [`isUser(int $id): bool`](#isuser)
* [`isSecretChat(int $id): bool`](#issecretchat)
* [`cases(): array`](#cases)

## Methods:
### `getType(int $id): self`

Get the type of a dialog using just its bot API dialog ID.
For more detailed types, use API::getType, instead.

Parameters:

* `$id`: `int` Bot API ID.  



### `fromSecretChatId(int $id): \int Bot API secret chat ID`

Convert MTProto secret chat ID to bot API secret chat ID.


Parameters:

* `$id`: `int` MTProto secret chat ID  


Return value: Bot API secret chat ID


### `toSecretChatId(int $id): \int MTProto secret chat ID`

Convert bot API secret chat ID to MTProto secret chat ID.


Parameters:

* `$id`: `int` Bot API secret chat ID  


Return value: MTProto secret chat ID


### `fromSupergroupOrChannel(int $id): int`

Convert MTProto channel ID to bot API channel ID.


Parameters:

* `$id`: `int` MTProto channel ID  



### `toSupergroupOrChannel(int $id): int`

Convert bot API channel ID to MTProto channel ID.


Parameters:

* `$id`: `int` Bot API channel ID  



### `isSupergroupOrChannel(int $id): bool`

Checks whether the provided bot API ID is a supergroup or channel ID.


Parameters:

* `$id`: `int`   



### `isChat(int $id): bool`

Checks whether the provided bot API ID is a chat ID.


Parameters:

* `$id`: `int`   



### `isUser(int $id): bool`

Checks whether the provided bot API ID is a user ID.


Parameters:

* `$id`: `int`   



### `isSecretChat(int $id): bool`

Checks whether the provided bot API ID is a secret chat ID.


Parameters:

* `$id`: `int`   



### `cases(): array`





---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)