---
title: "danog\\MadelineProto\\RPCError\\FloodWaitError: Represents a FLOOD_WAIT_ RPC error returned by telegram."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\RPCError\FloodWaitError`
[Back to index](../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Represents a FLOOD_WAIT_ RPC error returned by telegram.  




## Method list:
* `getWaitTime()`
* `wait()`
* `getLocalization()`
* `setLocalization()`
* `updateTLTrace()`
* `getTLTrace()`
* `setTLTrace(string $tlTrace)`
* `prettifyTL(string $init, array $trace)`

## Methods:
### `getWaitTime()`

Returns the required waiting period in seconds before repeating the RPC call.



### `wait()`

Waits for the required waiting period.



### `getLocalization()`

Get localized error name.



### `setLocalization()`

Set localized error name.



### `updateTLTrace()`

Update TL trace.



### `getTLTrace()`

Get TL trace.



### `setTLTrace(string $tlTrace)`

Set TL trace.


Parameters:

* `$tlTrace`: `string` TL trace  



### `prettifyTL(string $init, array $trace)`

Generate async trace.


Parameters:

* `$init`: `string` Method name  
* `$trace`: `array` Async trace  



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)