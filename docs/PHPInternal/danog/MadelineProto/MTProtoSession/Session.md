---
title: danog\MadelineProto\MTProtoSession\Session: Manages MTProto session-specific data.
description: 

---
# `danog\MadelineProto\MTProtoSession\Session`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Manages MTProto session-specific data.  




## Method list:
* `resetSession(): void`
* `createSession(): void`
* `backupSession(): array`
* `ackOutgoingMessageId(string|int $message_id): bool`
* `gotResponseForOutgoingMessageId(string|int $message_id): bool`
* `ackIncomingMessageId(string|int $message_id): bool`
* `hasPendingCalls(): bool`
* `getPendingCalls(): array`
* `handleReject(array $request, \Throwable $data): void`
* `handleResponse(): void`
* `methodRecall(string $watcherId, array $args): void`
* `methodCallAsyncRead(string $method, array|\Generator $args, array $aargs): \Generator`
* `methodCallAsyncWrite(string $method, array|\Generator $args, array $aargs): \Generator`
* `objectCall(string $object, array $args, array $aargs): \Generator`
* `sendMsgsStateInfo(string|int $req_msg_id, array $msg_ids): \Generator`

## Methods:
### `resetSession(): void`

Reset MTProto session.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `createSession(): void`

Create MTProto session if needed.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `backupSession(): array`

Backup eventual unsent messages before session deletion.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `ackOutgoingMessageId(string|int $message_id): bool`

Acknowledge outgoing message ID.


Parameters:
* `$message_id`: `string|int` Message Id  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `gotResponseForOutgoingMessageId(string|int $message_id): bool`

We have gotten response for outgoing message ID.


Parameters:
* `$message_id`: `string|int` Message ID  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `ackIncomingMessageId(string|int $message_id): bool`

Acknowledge incoming message ID.


Parameters:
* `$message_id`: `string|int` Message ID  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasPendingCalls(): bool`

Check if there are some pending calls.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getPendingCalls(): array`

Get all pending calls (also clear pending state requests).


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `handleReject(array $request, \Throwable $data): void`

Reject request with exception.


Parameters:
* `$request`: `array` Request  
* `$data`: `\Throwable` Exception  


#### See also: 
* `\Throwable`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `handleResponse(): void`




---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `methodRecall(string $watcherId, array $args): void`

Recall method.


Parameters:
* `$watcherId`: `string` Watcher ID for defer  
* `$args`: `array` Args  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `methodCallAsyncRead(string $method, array|\Generator $args, array $aargs): \Generator`

Call method and wait asynchronously for response.
If the $aargs['noResponse'] is true, will not wait for a response.

Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `methodCallAsyncWrite(string $method, array|\Generator $args, array $aargs): \Generator`

Call method and make sure it is asynchronously sent (generator).


Parameters:
* `$method`: `string` Method name  
* `$args`: `array|\Generator` Arguments  
  Full type:
  ```
  array|\Generator<mixed, mixed, mixed, array>
  ```
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `objectCall(string $object, array $args, array $aargs): \Generator`

Send object and make sure it is asynchronously sent (generator).


Parameters:
* `$object`: `string` Object name  
* `$args`: `array` Arguments  
* `$aargs`: `array` Additional arguments  


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `sendMsgsStateInfo(string|int $req_msg_id, array $msg_ids): \Generator`

Send state info for message IDs.


Parameters:
* `$req_msg_id`: `string|int` Message ID of msgs_state_req that initiated this  
* `$msg_ids`: `array` Message IDs to send info about  


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)