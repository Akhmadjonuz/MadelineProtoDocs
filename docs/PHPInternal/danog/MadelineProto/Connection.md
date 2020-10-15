---
title: danog\MadelineProto\Connection: Connection class.
description: Manages connection to Telegram datacenters

---
# `danog\MadelineProto\Connection`
[Back to index](../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Connection class.  

Manages connection to Telegram datacenters


## Method list:
* `needReconnect(bool $needsReconnect): void`
* `shouldReconnect(): bool`
* `writing(bool $writing): void`
* `reading(bool $reading): void`
* `haveRead(): void`
* `getLastChunk(): float`
* `httpReceived(): void`
* `countHttpReceived(): int`
* `httpSent(): void`
* `countHttpSent(): int`
* `getID(): int`
* `getDatacenterID(): string`
* `getCtx(): \danog\MadelineProto\Stream\ConnectionContext`
* `isHttp(): bool`
* `isMedia(): bool`
* `isCDN(): bool`
* `connect(\danog\MadelineProto\Stream\ConnectionContext $ctx): \Generator`
* `sendMessage(array $message, bool $flush): \Generator`
* `flush(): void`
* `pingHttpWaiter(): void`
* `setExtra(\danog\MadelineProto\DataCenterConnection $extra, int $id): void`
* `getExtra(): \danog\MadelineProto\MTProto`
* `getShared(): \danog\MadelineProto\DataCenterConnection`
* `disconnect(bool $temporary): void`
* `reconnect(): \Generator`
* `getName(): string`
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
### `needReconnect(bool $needsReconnect): void`

Indicate if this socket needs to be reconnected.


Parameters:
* `$needsReconnect`: `bool` Whether the socket has to be reconnected  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `shouldReconnect(): bool`

Whether this sockets needs to be reconnected.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `writing(bool $writing): void`

Set writing boolean.


Parameters:
* `$writing`: `bool`   


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `reading(bool $reading): void`

Set reading boolean.


Parameters:
* `$reading`: `bool`   


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `haveRead(): void`

Tell the class that we have read a chunk of data from the socket.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getLastChunk(): float`

Get the receive date of the latest chunk of data from the socket.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `httpReceived(): void`

Indicate a received HTTP response.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `countHttpReceived(): int`

Count received HTTP responses.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `httpSent(): void`

Indicate a sent HTTP request.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `countHttpSent(): int`

Count sent HTTP requests.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getID(): int`

Get connection ID.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDatacenterID(): string`

Get datacenter concatenated with connection ID.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getCtx(): \danog\MadelineProto\Stream\ConnectionContext`

Get connection context.


#### See also: 
* [`\danog\MadelineProto\Stream\ConnectionContext`: Connection context class.](./Stream/ConnectionContext.md)



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isHttp(): bool`

Check if is an HTTP connection.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isMedia(): bool`

Check if is a media connection.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isCDN(): bool`

Check if is a CDN connection.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `connect(\danog\MadelineProto\Stream\ConnectionContext $ctx): \Generator`

Connects to a telegram DC using the specified protocol, proxy and connection parameters.


Parameters:
* `$ctx`: `\danog\MadelineProto\Stream\ConnectionContext` Connection context  


Fully typed return value:
```
\Generator<mixed, \danog\MadelineProto\Stream\StreamInterface, mixed, void>
```
#### See also: 
* [`\danog\MadelineProto\Stream\ConnectionContext`: Connection context class.](./Stream/ConnectionContext.md)
* [`\danog\MadelineProto\Stream\StreamInterface`: Generic stream interface.](./Stream/StreamInterface.md)
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `sendMessage(array $message, bool $flush): \Generator`

Send an MTProto message.
Structure of message array:
[
    // only in outgoing messages
    'body' => deserialized body, (optional if container)
    'serialized_body' => 'serialized body', (optional if container)
    'contentRelated' => bool,
    '_' => 'predicate',
    'promise' => deferred promise that gets resolved when a response to the message is received (optional),
    'send_promise' => deferred promise that gets resolved when the message is sent (optional),
    'file' => bool (optional),
    'type' => 'type' (optional),
    'queue' => queue ID (optional),
    'container' => [message ids] (optional),

    // only in incoming messages
    'content' => deserialized body,
    'seq_no' => number (optional),
    'from_container' => bool (optional),

    // can be present in both
    'response' => message id (optional),
    'msg_id' => message id (optional),
    'sent' => timestamp,
    'tries' => number
]

Parameters:
* `$message`: `array` The message to send  
* `$flush`: `bool` Whether to flush the message right away  


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `flush(): void`

Flush pending packets.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `pingHttpWaiter(): void`

Resume HttpWaiter.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setExtra(\danog\MadelineProto\DataCenterConnection $extra, int $id): void`

Connect main instance.


Parameters:
* `$extra`: `\danog\MadelineProto\DataCenterConnection` Shared instance  
* `$id`: `int` Connection ID  


#### See also: 
* [`\danog\MadelineProto\DataCenterConnection`: Datacenter connection.](./DataCenterConnection.md)



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getExtra(): \danog\MadelineProto\MTProto`

Get main instance.


#### See also: 
* [`\danog\MadelineProto\MTProto`: Manages all of the mtproto stuff.](./MTProto.md)



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getShared(): \danog\MadelineProto\DataCenterConnection`

Get shared connection instance.


#### See also: 
* [`\danog\MadelineProto\DataCenterConnection`: Datacenter connection.](./DataCenterConnection.md)



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `disconnect(bool $temporary): void`

Disconnect from DC.


Parameters:
* `$temporary`: `bool` Whether the disconnection is temporary, triggered by the reconnect method  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `reconnect(): \Generator`

Reconnect to DC.


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getName(): string`

Get name.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

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