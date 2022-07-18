---
title: "danog\\MadelineProto\\VoIPServerConfig: Manages storage of VoIP server config."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\VoIPServerConfig`
[Back to index](../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages storage of VoIP server config.  




## Method list:
* `update(array $config): void`
* `get(): \array The settings`
* `updateDefault(array $configDefault): void`
* `getDefault(): \array The settings`
* `getFinal(): array`

## Methods:
### `update(array $config): void`

Update shared call settings.


Parameters:

* `$config`: `array` The settings  



### `get(): \array The settings`

Get shared call settings.


Return value: The settings


### `updateDefault(array $configDefault): void`

Update default shared call settings.


Parameters:

* `$configDefault`: `array` The settings  



### `getDefault(): \array The settings`

Get default shared call settings.


Return value: The settings


### `getFinal(): array`

Get final settings.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)