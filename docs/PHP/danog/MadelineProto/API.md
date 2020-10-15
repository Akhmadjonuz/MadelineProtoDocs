---
title: danog\MadelineProto\API: Main API wrapper for MadelineProto.
description: 

---
# `danog\MadelineProto\API`
[Back to index](../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Main API wrapper for MadelineProto.  




## Constants
* `danog\MadelineProto\API::RELEASE`: Release version.

* `danog\MadelineProto\API::NOT_LOGGED_IN`: We're not logged in.

* `danog\MadelineProto\API::WAITING_CODE`: We're waiting for the login code.

* `danog\MadelineProto\API::WAITING_SIGNUP`: We're waiting for parameters to sign up.

* `danog\MadelineProto\API::WAITING_PASSWORD`: We're waiting for the 2FA password.

* `danog\MadelineProto\API::LOGGED_IN`: We're logged in.

* `danog\MadelineProto\API::SECRET_EMPTY`: Secret chat was not found.

* `danog\MadelineProto\API::SECRET_REQUESTED`: Secret chat was requested.

* `danog\MadelineProto\API::SECRET_READY`: Secret chat was found.


## Method list:
* `startAndLoop(string $eventHandler): void`
* `startAndLoopMulti(\danog\MadelineProto\API[] $instances, string[]|string $eventHandler): void`
* `startAndLoopAsync(string $eventHandler): \Generator`
* `MTProtoToBotAPI(array $data): \Amp\Promise<array>`
* `MTProtoToTd(mixed $params): \Amp\Promise`
* `MTProtoToTdcli(mixed $params): \Amp\Promise`
* `acceptCall(array $call): \Amp\Promise`
* `acceptSecretChat(array $params): \Amp\Promise`
* `acceptTos(): \Amp\Promise`
* `addUser(array $user): \Amp\Promise`
* `after(\Generator|\Promise $a, \Generator|\Promise $b): \Amp\Promise`
* `all((\Generator|\Promise)[] $promises): \Amp\Promise`
* `any((\Promise|\Generator)[] $promises): \Amp\Promise`
* `arr(mixed $params): array`
* `base64urlDecode(string $data): string`
* `base64urlEncode(string $data): string`
* `botAPIToMTProto(array $arguments): \Amp\Promise<array>`
* `botLogin(string $token): \Amp\Promise`
* `call(\Generator|\Promise|mixed $promise): \Amp\Promise`
* `callFork(\Generator|\Promise $promise, ?\Generator|\Promise $actual, string $file): \Amp\Promise|mixed`
* `callForkDefer(\Generator|\Promise $promise): void`
* `callStatus(int $id): mixed`
* `checkTos(): \Amp\Promise`
* `cleanup(): \Amp\Promise`
* `closeConnection(string $message): void`
* `complete2faLogin(string $password): \Amp\Promise`
* `completeCall(array $params): \Amp\Promise`
* `completePhoneLogin(string $code): \Amp\Promise`
* `completeSignup(string $first_name, string $last_name): \Amp\Promise`
* `confirmCall(array $params): \Amp\Promise`
* `connectToAllDcs(bool $reconnectAll): \Amp\Promise`
* `declineTos(): \Amp\Promise`
* `discardCall(array $call, array $reason, array $rating, bool $need_debug): \Amp\Promise`
* `discardSecretChat(int $chat): \Amp\Promise`
* `downloadToBrowser(array|string $messageMedia, callable $cb): \Amp\Promise`
* `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): \Amp\Promise`
* `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): \Amp\Promise`
* `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): \Amp\Promise Downloaded file path`
* `downloadToResponse(array|string $messageMedia, \ServerRequest $request, callable $cb): \Amp\Promise Returned response`
* `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface $stream, callable $cb, int $offset, int $end): \Amp\Promise`
* `echo(string $string): \Amp\Promise`
* `end(array $what): mixed`
* `exportAuthorization(): \Amp\Promise`
* `extractBotAPIFile(array $info): ?array`
* `fileGetContents(string $url): \Amp\Promise`
* `first((\Promise|\Generator)[] $promises): \Amp\Promise`
* `flock(string $file, int $operation, float $polling, ?\Promise $token, ?callable $failureCb): \Amp\Promise<?callable>`
* `fromSupergroup(int $id): float|int`
* `fullChatLastUpdated(mixed $id): \Amp\Promise<int>`
* `fullGetSelf(): \Amp\Promise<array|bool>`
* `genVectorHash(array $ints): \int Vector hash`
* `getAllMethods(): mixed`
* `getAuthorization(): mixed`
* `getCachedConfig(): mixed`
* `getCall(int $call): mixed`
* `getCdnConfig(string $datacenter): \Amp\Promise`
* `getConfig(array $config, array $options): \Amp\Promise`
* `getDNSClient(): mixed`
* `getDataCenterConnections(): mixed`
* `getDataCenterId(): int|string`
* `getDialogs(bool $force): \Amp\Promise`
* `getDownloadInfo(mixed $messageMedia): \Amp\Promise<array>`
* `getEventHandler(): mixed`
* `getExtensionFromLocation(mixed $location, string $default): string`
* `getExtensionFromMime(string $mime): string`
* `getFileInfo(mixed $constructor): \Amp\Promise<array>`
* `getFolderId(mixed $id): ?int`
* `getFullDialogs(bool $force): \Amp\Promise`
* `getFullInfo(mixed $id): \Amp\Promise FullInfo object`
* `getHTTPClient(): mixed`
* `getHint(): mixed`
* `getId(mixed $id): int`
* `getInfo(mixed $id, bool $recursive): \Amp\Promise Info object`
* `getLogger()`
* `getMethodNamespaces(): mixed`
* `getMethodsNamespaced(): mixed`
* `getMimeFromBuffer(string $buffer): string`
* `getMimeFromExtension(string $extension, string $default): string`
* `getMimeFromFile(string $file): string`
* `getPropicInfo(mixed $messageMedia): \Amp\Promise<array>`
* `getPsrLogger()`
* `getPwrChat(mixed $id): \Amp\Promise<array> Chat object`
* `getSecretChat(array|int $chat): mixed`
* `getSelf(): array|bool`
* `getSettings(): mixed`
* `getTL(): mixed`
* `getVar(object $obj, string $var): mixed`
* `getWebTemplate(): mixed`
* `hasAllAuth(): mixed`
* `hasEventHandler(): mixed`
* `hasReportPeers(): mixed`
* `hasSecretChat(array|int $chat): mixed`
* `hasVar(object $obj, string $var): bool`
* `importAuthorization(mixed $authorization): \Amp\Promise`
* `inflateStripped(string $stripped): \string JPG payload`
* `initSelfRestart(): mixed`
* `isAltervista(): bool`
* `isArrayOrAlike(mixed $var): bool`
* `isIpc(): mixed`
* `isSupergroup(int $id): bool`
* `logger(string $param, int $level, string $file): mixed`
* `logout(): \Amp\Promise`
* `loop(callable|null $callback): \Amp\Promise`
* `loopFork(): \Amp\Promise`
* `markdownEscape(string $hwat): string`
* `mbStrSplit(string $text, int $length): array`
* `mbStrlen(string $text): float|int`
* `mbSubstr(string $text, int $offset, ?int $length): string`
* `methodCall(string $method, array|\Generator $args, array $aargs): \Amp\Promise`
* `methodCallWrite(string $method, array|\Generator $args, array $aargs): \Amp\Promise`
* `methodEscape(string $method): string`
* `packDouble(float $value): string`
* `packSignedInt(int $value): string`
* `packSignedLong(int $value): string`
* `packUnsignedInt(int $value): string`
* `peerIsset(mixed $id): \Amp\Promise`
* `phoneLogin(string $number, int $sms_type): \Amp\Promise`
* `posmod(int $a, int $b): \int Modulo`
* `random(int $length): \string Random string`
* `randomInt(int $modulus): int`
* `readLine(string $prompt): \Amp\Promise<string>`
* `rekey(int $chat): \Amp\Promise`
* `report(string $message, string $parseMode): \Amp\Promise`
* `requestCall(mixed $user): \Amp\Promise`
* `requestSecretChat(mixed $user): \Amp\Promise`
* `resetUpdateState(): mixed`
* `resolveUsername(string $username): \Amp\Promise`
* `restart(): void`
* `rethrow(\Throwable $e, string $file): void`
* `rleDecode(string $string): string`
* `rleEncode(string $string): string`
* `secretChatStatus(int $chat): mixed`
* `serializeAll(): void`
* `setCallback(callable $callback): mixed`
* `setEventHandler(class-string<\danog\MadelineProto\EventHandler> $eventHandler): \Amp\Promise`
* `setNoop(): mixed`
* `setReportPeers(int|string $userOrId): \Amp\Promise`
* `setVar(object $obj, string $var, mixed $val): void`
* `setWebTemplate(string $template): mixed`
* `setWebhook(string $hook_url, string $pem_path): mixed`
* `setupLogger(): mixed`
* `sleep(int|float $time): \Amp\Promise`
* `some((\Promise|\Generator)[] $promises): \Amp\Promise`
* `start(): \Amp\Promise`
* `stop(): void`
* `tdToMTProto(array $params): \Amp\Promise<array>`
* `tdToTdcli(mixed $params): mixed`
* `tdcliToTd(array $params, array $key): mixed`
* `timeout(\Generator|\Promise $promise, int $timeout): \Amp\Promise`
* `timeoutWithDefault(\Promise|\Generator $promise, int $timeout, mixed $default): \Amp\Promise<\TReturn>|\Promise<\TReturnAlt>`
* `toCamelCase(string $input): string`
* `toSnakeCase(string $input): string`
* `toSupergroup(int $id): float|int`
* `typeEscape(string $type): string`
* `unpackDouble(string $value): float`
* `unpackFileId(string $fileId): mixed`
* `unpackSignedInt(string $value): int`
* `unpackSignedLong(string $value): int`
* `unpackSignedLongString(string $value): string`
* `unsetEventHandler(bool $disableUpdateHandling): mixed`
* `update2fa(array $params): \Amp\Promise`
* `updateSettings(\danog\MadelineProto\SettingsAbstract $settings): \Amp\Promise`
* `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): \Amp\Promise`
* `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): \Amp\Promise`
* `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): \Amp\Promise`
* `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): \Amp\Promise`
* `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): \Amp\Promise`
* `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): \Amp\Promise`
* `wait(\Generator|\Promise $promise, bool $ignoreSignal): mixed`
* `async(bool $async): void`
* `init(): void`
* `initAsynchronously(): \Generator`
* `inited(): bool`
* `forceInit(bool $inited): void`
* `getWebAPITemplate(): string`
* `setWebAPITemplate(): void`

## Methods:
### `startAndLoop(string $eventHandler): void`

Start MadelineProto and the event handler (enables async).
Also initializes error reporting, catching and reporting all errors surfacing from the event loop.

Parameters:
* `$eventHandler`: `string` Event handler class name  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `startAndLoopMulti(\danog\MadelineProto\API[] $instances, string[]|string $eventHandler): void`

Start multiple instances of MadelineProto and the event handlers (enables async).


Parameters:
* `$instances`: `\danog\MadelineProto\API[]` Instances of madeline  
* `$eventHandler`: `string[]|string` Event handler(s)  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `startAndLoopAsync(string $eventHandler): \Generator`

Start MadelineProto and the event handler (enables async).
Also initializes error reporting, catching and reporting all errors surfacing from the event loop.

Parameters:
* `$eventHandler`: `string` Event handler class name  


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `MTProtoToBotAPI(array $data): \Amp\Promise<array>`

Convert MTProto parameters to bot API parameters.


Parameters:
* `$data`: `array` Data  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `MTProtoToTd(mixed $params): \Amp\Promise`

MTProto to TD params.


Parameters:
* `$params`: `mixed` Params  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `MTProtoToTdcli(mixed $params): \Amp\Promise`

MTProto to TDCLI params.


Parameters:
* `$params`: `mixed` Params  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `acceptCall(array $call): \Amp\Promise`

Accept call.


Parameters:
* `$call`: `array` Call  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `acceptSecretChat(array $params): \Amp\Promise`

Accept secret chat.


Parameters:
* `$params`: `array` Secret chat ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `acceptTos(): \Amp\Promise`

Accept terms of service update.


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `addUser(array $user): \Amp\Promise`

Add user info.


Parameters:
* `$user`: `array` User info  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `after(\Generator|\Promise $a, \Generator|\Promise $b): \Amp\Promise`

Call promise $b after promise $a.


Parameters:
* `$a`: `\Generator|\Promise` Promise A  
* `$b`: `\Generator|\Promise` Promise B  


#### See also: 
* `\Generator`
* `\Promise`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `all((\Generator|\Promise)[] $promises): \Amp\Promise`

Returns a promise that succeeds when all promises succeed, and fails if any promise fails.
Returned promise succeeds with an array of values used to succeed each contained promise, with keys corresponding to the array of promises.

Parameters:
* `$promises`: `(\Generator|\Promise)[]` Promises  


#### See also: 
* `\Generator`
* `\Promise`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `any((\Promise|\Generator)[] $promises): \Amp\Promise`

Returns a promise that is resolved when all promises are resolved. The returned promise will not fail.


Parameters:
* `$promises`: `(\Promise|\Generator)[]` Promises  


#### See also: 
* `\Promise`
* `\Generator`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `arr(mixed $params): array`

Create array.


Parameters:
* `$params`: `mixed` Params  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `base64urlDecode(string $data): string`

base64URL decode.


Parameters:
* `$data`: `string` Data to decode  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `base64urlEncode(string $data): string`

Base64URL encode.


Parameters:
* `$data`: `string` Data to encode  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `botAPIToMTProto(array $arguments): \Amp\Promise<array>`

Convert bot API parameters to MTProto parameters.


Parameters:
* `$arguments`: `array` Arguments  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `botLogin(string $token): \Amp\Promise`

Login as bot.


Parameters:
* `$token`: `string` Bot token  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `call(\Generator|\Promise|mixed $promise): \Amp\Promise`

Convert generator, promise or any other value to a promise.


Parameters:
* `$promise`: `\Generator|\Promise|mixed`   
  Full type:
  ```
  \Generator<mixed, mixed, mixed, \TReturn>|\Promise<\TReturn>|\TReturn
  ```


Fully typed return value:
```
\Promise<\TReturn>
```
#### See also: 
* `\Generator`
* `\Promise`
* `\TReturn`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `callFork(\Generator|\Promise $promise, ?\Generator|\Promise $actual, string $file): \Amp\Promise|mixed`

Call promise in background.


Parameters:
* `$promise`: `\Generator|\Promise` Promise to resolve  
* `$actual`: `?\Generator|\Promise` Promise to resolve instead of $promise  
* `$file`: `string` File  


#### See also: 
* `\Generator`
* `\Promise`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `callForkDefer(\Generator|\Promise $promise): void`

Call promise in background, deferring execution.


Parameters:
* `$promise`: `\Generator|\Promise` Promise to resolve  


#### See also: 
* `\Generator`
* `\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `callStatus(int $id): mixed`

Get call status.


Parameters:
* `$id`: `int` Call ID  


Fully typed return value:
```
int|\Amp\Promise<int>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `checkTos(): \Amp\Promise`

Check for terms of service update.


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `cleanup(): \Amp\Promise`

Cleanup memory and session file.


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `closeConnection(string $message): void`

Close connection with client, connected via web.


Parameters:
* `$message`: `string` Message  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `complete2faLogin(string $password): \Amp\Promise`

Complete 2FA login.


Parameters:
* `$password`: `string` Password  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `completeCall(array $params): \Amp\Promise`

Complete call handshake.


Parameters:
* `$params`: `array` Params  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `completePhoneLogin(string $code): \Amp\Promise`

Complet user login using login code.


Parameters:
* `$code`: `string` Login code  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `completeSignup(string $first_name, string $last_name): \Amp\Promise`

Complete signup to Telegram.


Parameters:
* `$first_name`: `string` First name  
* `$last_name`: `string` Last name  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `confirmCall(array $params): \Amp\Promise`

Confirm call.


Parameters:
* `$params`: `array` Params  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `connectToAllDcs(bool $reconnectAll): \Amp\Promise`

Connects to all datacenters and if necessary creates authorization keys, binds them and writes client info.


Parameters:
* `$reconnectAll`: `bool` Whether to reconnect to all DCs  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `declineTos(): \Amp\Promise`

Decline terms of service update.
THIS WILL DELETE YOUR ACCOUNT!

#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `discardCall(array $call, array $reason, array $rating, bool $need_debug): \Amp\Promise`

Discard call.


Parameters:
* `$call`: `array` Call  
* `$reason`: `array`   
* `$rating`: `array` Rating  
* `$need_debug`: `bool` Need debug?  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `discardSecretChat(int $chat): \Amp\Promise`

Discard secret chat.


Parameters:
* `$chat`: `int` Secret chat ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `downloadToBrowser(array|string $messageMedia, callable $cb): \Amp\Promise`

Download file to browser.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:
* `$messageMedia`: `array|string` File to download  
* `$cb`: `callable` Status callback (can also use FileCallback)  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `downloadToCallable(mixed $messageMedia, callable|\danog\MadelineProto\FileCallbackInterface $callable, callable $cb, bool $seekable, int $offset, int $end, int $part_size): \Amp\Promise`

Download file to callable.
The callable must accept two parameters: string $payload, int $offset
The callable will be called (possibly out of order, depending on the value of $seekable).
The callable should return the number of written bytes.

Parameters:
* `$messageMedia`: `mixed` File to download  
* `$callable`: `callable|\danog\MadelineProto\FileCallbackInterface` Chunk callback  
* `$cb`: `callable` Status callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether the callable can be called out of order  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to stop downloading (inclusive)  
* `$part_size`: `int` Size of each chunk  


Fully typed return value:
```
\Amp\Promise<true>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `downloadToDir(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $dir, callable $cb): \Amp\Promise`

Download file to directory.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$dir`: `string|\danog\MadelineProto\FileCallbackInterface` Directory where to download the file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Fully typed return value:
```
\Amp\Promise<false|string>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `downloadToFile(mixed $messageMedia, string|\danog\MadelineProto\FileCallbackInterface $file, callable $cb): \Amp\Promise Downloaded file path`

Download file.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$file`: `string|\danog\MadelineProto\FileCallbackInterface` Downloaded file path  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Return value: Downloaded file path

Fully typed return value:
```
\Amp\Promise<false|string>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `downloadToResponse(array|string $messageMedia, \ServerRequest $request, callable $cb): \Amp\Promise Returned response`

Download file to amphp/http-server response.
Supports HEAD requests and content-ranges for parallel and resumed downloads.

Parameters:
* `$messageMedia`: `array|string` File to download  
* `$request`: `\ServerRequest` Request  
* `$cb`: `callable` Status callback (can also use FileCallback)  


Return value: Returned response

Fully typed return value:
```
\Amp\Promise<\Amp\Http\Server\Response>
```
#### See also: 
* `\ServerRequest`
* `\Amp\Http\Server\Response`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `downloadToStream(mixed $messageMedia, mixed|\danog\MadelineProto\FileCallbackInterface $stream, callable $cb, int $offset, int $end): \Amp\Promise`

Download file to stream.


Parameters:
* `$messageMedia`: `mixed` File to download  
* `$stream`: `mixed|\danog\MadelineProto\FileCallbackInterface` Stream where to download file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$offset`: `int` Offset where to start downloading  
* `$end`: `int` Offset where to end download  


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `echo(string $string): \Amp\Promise`

Asynchronously write to stdout/browser.


Parameters:
* `$string`: `string` Message to echo  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `end(array $what): mixed`

Get final element of array.


Parameters:
* `$what`: `array` Array  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `exportAuthorization(): \Amp\Promise`

Export authorization.


Fully typed return value:
```
\Amp\Promise<array{0: int|string, 1: string}>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `extractBotAPIFile(array $info): ?array`

Extract file info from bot API message.


Parameters:
* `$info`: `array` Bot API message object  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `fileGetContents(string $url): \Amp\Promise`

Get contents of remote file asynchronously.


Parameters:
* `$url`: `string` URL  


Fully typed return value:
```
\Amp\Promise<string>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `first((\Promise|\Generator)[] $promises): \Amp\Promise`

Returns a promise that succeeds when the first promise succeeds, and fails only if all promises fail.


Parameters:
* `$promises`: `(\Promise|\Generator)[]` Promises  


#### See also: 
* `\Promise`
* `\Generator`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `flock(string $file, int $operation, float $polling, ?\Promise $token, ?callable $failureCb): \Amp\Promise<?callable>`

Asynchronously lock a file
Resolves with a callbable that MUST eventually be called in order to release the lock.


Parameters:
* `$file`: `string` File to lock  
* `$operation`: `int` Locking mode  
* `$polling`: `float` Polling interval  
* `$token`: `?\Promise` Cancellation token  
* `$failureCb`: `?callable` Failure callback, called only once if the first locking attempt fails.  


#### See also: 
* `\Promise`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `fromSupergroup(int $id): float|int`

Convert bot API channel ID to MTProto channel ID.


Parameters:
* `$id`: `int` Bot API channel ID  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `fullChatLastUpdated(mixed $id): \Amp\Promise<int>`

When were full info for this chat last cached.


Parameters:
* `$id`: `mixed` Chat ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `fullGetSelf(): \Amp\Promise<array|bool>`

Get info about the logged-in user, not cached.


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `genVectorHash(array $ints): \int Vector hash`

Generate MTProto vector hash.


Parameters:
* `$ints`: `array` IDs  


Return value: Vector hash

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getAllMethods(): mixed`

Get full list of MTProto and API methods.


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getAuthorization(): mixed`

Get authorization info.


Fully typed return value:
```
int|\Amp\Promise<int>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getCachedConfig(): mixed`

Get cached server-side config.


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getCall(int $call): mixed`

Get call info.


Parameters:
* `$call`: `int` Call ID  


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getCdnConfig(string $datacenter): \Amp\Promise`

Store RSA keys for CDN datacenters.


Parameters:
* `$datacenter`: `string` DC ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getConfig(array $config, array $options): \Amp\Promise`

Get cached (or eventually re-fetch) server-side config.


Parameters:
* `$config`: `array` Current config  
* `$options`: `array` Options for method call  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDNSClient(): mixed`

Get async DNS client.


Fully typed return value:
```
\Amp\Dns\Resolver|\Amp\Promise<\Amp\Dns\Resolver>
```
#### See also: 
* `\Amp\Dns\Resolver`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDataCenterConnections(): mixed`

Get all datacenter connections.


Fully typed return value:
```
array<\danog\MadelineProto\DataCenterConnection>|\Amp\Promise<array<\danog\MadelineProto\DataCenterConnection>>
```
#### See also: 
* `\danog\MadelineProto\DataCenterConnection`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDataCenterId(): int|string`

Get main DC ID.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDialogs(bool $force): \Amp\Promise`

Get dialog peers.


Parameters:
* `$force`: `bool` Whether to refetch all dialogs ignoring cache  


Fully typed return value:
```
\Amp\Promise<list<mixed>>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDownloadInfo(mixed $messageMedia): \Amp\Promise<array>`

Get download info of file
Returns an array with the following structure:.
`$info['ext']` - The file extension
`$info['name']` - The file name, without the extension
`$info['mime']` - The file mime type
`$info['size']` - The file size

Parameters:
* `$messageMedia`: `mixed` File ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getEventHandler(): mixed`

Get event handler.


Fully typed return value:
```
\danog\MadelineProto\EventHandler|\Amp\Promise<\danog\MadelineProto\EventHandler>
```
#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](./EventHandler.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getExtensionFromLocation(mixed $location, string $default): string`

Get extension from file location.


Parameters:
* `$location`: `mixed` File location  
* `$default`: `string` Default extension  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getExtensionFromMime(string $mime): string`

Get extension from mime type.


Parameters:
* `$mime`: `string` MIME type  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getFileInfo(mixed $constructor): \Amp\Promise<array>`

Get info about file.


Parameters:
* `$constructor`: `mixed` File ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getFolderId(mixed $id): ?int`

Get folder ID from object.


Parameters:
* `$id`: `mixed` Object  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getFullDialogs(bool $force): \Amp\Promise`

Get full info of all dialogs.


Parameters:
* `$force`: `bool` Whether to refetch all dialogs ignoring cache  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getFullInfo(mixed $id): \Amp\Promise FullInfo object`

Get full info about peer, returns an FullInfo object.


Parameters:
* `$id`: `mixed` Peer  


Return value: FullInfo object

Fully typed return value:
```
\Amp\Promise<array>
```
#### See also: 
* [https://docs.madelineproto.xyz/FullInfo.html](https://docs.madelineproto.xyz/FullInfo.html)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getHTTPClient(): mixed`

Get async HTTP client.


Fully typed return value:
```
\Amp\Http\Client\HttpClient|\Amp\Promise<\Amp\Http\Client\HttpClient>
```
#### See also: 
* `\Amp\Http\Client\HttpClient`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getHint(): mixed`

Get current password hint.


Fully typed return value:
```
string|\Amp\Promise<string>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getId(mixed $id): int`

Get bot API ID from peer object.


Parameters:
* `$id`: `mixed` Peer  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getInfo(mixed $id, bool $recursive): \Amp\Promise Info object`

Get info about peer, returns an Info object.


Parameters:
* `$id`: `mixed` Peer  
* `$recursive`: `bool` Internal  


Return value: Info object

Fully typed return value:
```
\Generator<int|mixed, \Amp\Promise|\Amp\Promise<string>|array, mixed, array{InputPeer: array{_: string, user_id?: mixed, access_hash?: mixed, min?: mixed, chat_id?: mixed, channel_id?: mixed}, Peer: array{_: string, user_id?: mixed, chat_id?: mixed, channel_id?: mixed}, DialogPeer: array{_: string, peer: array{_: string, user_id?: mixed, chat_id?: mixed, channel_id?: mixed}}, NotifyPeer: array{_: string, peer: array{_: string, user_id?: mixed, chat_id?: mixed, channel_id?: mixed}}, InputDialogPeer: array{_: string, peer: array{_: string, user_id?: mixed, access_hash?: mixed, min?: mixed, chat_id?: mixed, channel_id?: mixed}}, InputNotifyPeer: array{_: string, peer: array{_: string, user_id?: mixed, access_hash?: mixed, min?: mixed, chat_id?: mixed, channel_id?: mixed}}, bot_api_id: int|string, user_id?: int, chat_id?: int, channel_id?: int, InputUser?: array{_: string, user_id?: int, access_hash?: mixed, min?: bool}, InputChannel?: array{_: string, channel_id: int, access_hash: mixed, min: bool}, type: string}>
```
#### See also: 
* [https://docs.madelineproto.xyz/Info.html](https://docs.madelineproto.xyz/Info.html)
* `\Amp\Promise`
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getLogger()`

Get logger.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMethodNamespaces(): mixed`

Get TL namespaces.


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMethodsNamespaced(): mixed`

Get namespaced methods (method => namespace).


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMimeFromBuffer(string $buffer): string`

Get mime type from buffer.


Parameters:
* `$buffer`: `string` Buffer  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMimeFromExtension(string $extension, string $default): string`

Get mime type from file extension.


Parameters:
* `$extension`: `string` File extension  
* `$default`: `string` Default mime type  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMimeFromFile(string $file): string`

Get mime type of file.


Parameters:
* `$file`: `string` File  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getPropicInfo(mixed $messageMedia): \Amp\Promise<array>`

Get download info of the propic of a user
Returns an array with the following structure:.
`$info['ext']` - The file extension
`$info['name']` - The file name, without the extension
`$info['mime']` - The file mime type
`$info['size']` - The file size

Parameters:
* `$messageMedia`: `mixed` File ID  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getPsrLogger()`

Get PSR logger.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getPwrChat(mixed $id): \Amp\Promise<array> Chat object`

Get full info about peer (including full list of channel members), returns a Chat object.


Parameters:
* `$id`: `mixed` Peer  


Return value: Chat object

#### See also: 
* [https://docs.madelineproto.xyz/Chat.html](https://docs.madelineproto.xyz/Chat.html)



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getSecretChat(array|int $chat): mixed`

Get secret chat.


Parameters:
* `$chat`: `array|int` Secret chat ID  


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getSelf(): array|bool`

Get info about the logged-in user, cached.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getSettings(): mixed`

Return current settings.


Fully typed return value:
```
\danog\MadelineProto\Settings|\Amp\Promise<\danog\MadelineProto\Settings>
```
#### See also: 
* [`\danog\MadelineProto\Settings`: Settings class used for configuring MadelineProto.](./Settings.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getTL(): mixed`

Get TL serializer.


Fully typed return value:
```
\danog\MadelineProto\TL\TL|\Amp\Promise<\danog\MadelineProto\TL\TL>
```
#### See also: 
* `\danog\MadelineProto\TL\TL`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getVar(object $obj, string $var): mixed`

Accesses a private variable from an object.


Parameters:
* `$obj`: `object` Object  
* `$var`: `string` Attribute name  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getWebTemplate(): mixed`

Get web template.


Fully typed return value:
```
string|\Amp\Promise<string>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasAllAuth(): mixed`

Checks whether all datacenters are authorized.


Fully typed return value:
```
bool|\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasEventHandler(): mixed`

Check if an event handler instance is present.


Fully typed return value:
```
bool|\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasReportPeers(): mixed`

Check if has report peers.


Fully typed return value:
```
bool|\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasSecretChat(array|int $chat): mixed`

Check whether secret chat exists.


Parameters:
* `$chat`: `array|int` Secret chat ID  


Fully typed return value:
```
bool|\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasVar(object $obj, string $var): bool`

Checks private property exists in an object.


Parameters:
* `$obj`: `object` Object  
* `$var`: `string` Attribute name  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `importAuthorization(mixed $authorization): \Amp\Promise`

Import authorization.


Parameters:
* `$authorization`: `mixed` Authorization info  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `inflateStripped(string $stripped): \string JPG payload`

Inflate stripped photosize to full JPG payload.


Parameters:
* `$stripped`: `string` Stripped photosize  


Return value: JPG payload

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `initSelfRestart(): mixed`

Initialize self-restart hack.


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isAltervista(): bool`

Whether this is altervista.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isArrayOrAlike(mixed $var): bool`

Check if is array or similar (traversable && countable && arrayAccess).


Parameters:
* `$var`: `mixed` Value to check  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isIpc(): mixed`

Whether we're an IPC client instance.


Fully typed return value:
```
bool|\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `isSupergroup(int $id): bool`

Check whether provided bot API ID is a channel.


Parameters:
* `$id`: `int` Bot API ID  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `logger(string $param, int $level, string $file): mixed`

Logger.


Parameters:
* `$param`: `string` Parameter  
* `$level`: `int` Logging level  
* `$file`: `string` File where the message originated  


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `logout(): \Amp\Promise`

Log out currently logged in user.


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `loop(callable|null $callback): \Amp\Promise`

Start MadelineProto's update handling loop, or run the provided async callable.


Parameters:
* `$callback`: `callable|null` Async callable to run  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `loopFork(): \Amp\Promise`

Start MadelineProto's update handling loop in background.


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `markdownEscape(string $hwat): string`

Escape string for markdown.


Parameters:
* `$hwat`: `string` String to escape  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `mbStrSplit(string $text, int $length): array`

Telegram UTF-8 multibyte split.


Parameters:
* `$text`: `string` Text  
* `$length`: `int` Length  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `mbStrlen(string $text): float|int`

Get Telegram UTF-8 length of string.


Parameters:
* `$text`: `string` Text  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `mbSubstr(string $text, int $offset, ?int $length): string`

Telegram UTF-8 multibyte substring.


Parameters:
* `$text`: `string` Text to substring  
* `$offset`: `int` Offset  
* `$length`: `?int` Length  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `methodCall(string $method, array|\Generator $args, array $aargs): \Amp\Promise`

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
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `methodCallWrite(string $method, array|\Generator $args, array $aargs): \Amp\Promise`

Call method and make sure it is asynchronously sent.


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
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `methodEscape(string $method): string`

Escape method name.


Parameters:
* `$method`: `string` Method name  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `packDouble(float $value): string`

Convert double to binary version.


Parameters:
* `$value`: `float` Value to convert  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `packSignedInt(int $value): string`

Convert integer to base256 signed int.


Parameters:
* `$value`: `int` Value to convert  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `packSignedLong(int $value): string`

Convert integer to base256 long.


Parameters:
* `$value`: `int` Value to convert  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `packUnsignedInt(int $value): string`

Convert value to unsigned base256 int.


Parameters:
* `$value`: `int` Value  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `peerIsset(mixed $id): \Amp\Promise`

Check if peer is present in internal peer database.


Parameters:
* `$id`: `mixed` Peer  


Fully typed return value:
```
\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `phoneLogin(string $number, int $sms_type): \Amp\Promise`

Login as user.


Parameters:
* `$number`: `string` Phone number  
* `$sms_type`: `int` SMS type  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `posmod(int $a, int $b): \int Modulo`

Positive modulo
Works just like the % (modulus) operator, only returns always a postive number.


Parameters:
* `$a`: `int` A  
* `$b`: `int` B  


Return value: Modulo

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `random(int $length): \string Random string`

Get random string of specified length.


Parameters:
* `$length`: `int` Length  


Return value: Random string

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `randomInt(int $modulus): int`

Get random integer.


Parameters:
* `$modulus`: `int` Modulus  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `readLine(string $prompt): \Amp\Promise<string>`

Asynchronously read line.


Parameters:
* `$prompt`: `string` Prompt  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `rekey(int $chat): \Amp\Promise`

Rekey secret chat.


Parameters:
* `$chat`: `int` Secret chat to rekey  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `report(string $message, string $parseMode): \Amp\Promise`

Report an error to the previously set peer.


Parameters:
* `$message`: `string` Error to report  
* `$parseMode`: `string` Parse mode  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `requestCall(mixed $user): \Amp\Promise`

Request VoIP call.


Parameters:
* `$user`: `mixed` User  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `requestSecretChat(mixed $user): \Amp\Promise`

Request secret chat.


Parameters:
* `$user`: `mixed` User to start secret chat with  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `resetUpdateState(): mixed`

Reset the update state and fetch all updates from the beginning.


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `resolveUsername(string $username): \Amp\Promise`

Resolve username (use getInfo instead).


Parameters:
* `$username`: `string` Username  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `restart(): void`

Restart update loop.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `rethrow(\Throwable $e, string $file): void`

Rethrow error catched in strand.


Parameters:
* `$e`: `\Throwable` Exception  
* `$file`: `string` File where the strand started  


#### See also: 
* `\Throwable`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `rleDecode(string $string): string`

null-byte RLE decode.


Parameters:
* `$string`: `string` Data to decode  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `rleEncode(string $string): string`

null-byte RLE encode.


Parameters:
* `$string`: `string` Data to encode  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `secretChatStatus(int $chat): mixed`

Get secret chat status.


Parameters:
* `$chat`: `int` Chat ID  


Fully typed return value:
```
int|\Amp\Promise<int>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `serializeAll(): void`

Serialize all instances.
CALLED ONLY ON SHUTDOWN.

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setCallback(callable $callback): mixed`

Set update handling callback.


Parameters:
* `$callback`: `callable` Callback  


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setEventHandler(class-string<\danog\MadelineProto\EventHandler> $eventHandler): \Amp\Promise`

Set event handler.


Parameters:
* `$eventHandler`: `class-string<\danog\MadelineProto\EventHandler>` Event handler  


#### See also: 
* [`\danog\MadelineProto\EventHandler`: Event handler.](./EventHandler.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setNoop(): mixed`

Set NOOP update handler, ignoring all updates.


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setReportPeers(int|string $userOrId): \Amp\Promise`

Set peer(s) where to send errors occurred in the event loop.


Parameters:
* `$userOrId`: `int|string` Username(s) or peer ID(s)  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setVar(object $obj, string $var, mixed $val): void`

Sets a private variable in an object.


Parameters:
* `$obj`: `object` Object  
* `$var`: `string` Attribute name  
* `$val`: `mixed` Attribute value  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setWebTemplate(string $template): mixed`

Set web template.


Parameters:
* `$template`: `string` Template  


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setWebhook(string $hook_url, string $pem_path): mixed`

Set webhook update handler.


Parameters:
* `$hook_url`: `string` Webhook URL  
* `$pem_path`: `string` PEM path for self-signed certificate  


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setupLogger(): mixed`

Setup logger.


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `sleep(int|float $time): \Amp\Promise`

Asynchronously sleep.


Parameters:
* `$time`: `int|float` Number of seconds to sleep for  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `some((\Promise|\Generator)[] $promises): \Amp\Promise`

Resolves with a two-item array delineating successful and failed Promise results.
The returned promise will only fail if the given number of required promises fail.

Parameters:
* `$promises`: `(\Promise|\Generator)[]` Promises  


#### See also: 
* `\Promise`
* `\Generator`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `start(): \Amp\Promise`

Log in to telegram (via CLI or web).


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `stop(): void`

Stop update loop.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `tdToMTProto(array $params): \Amp\Promise<array>`

Convert TD to MTProto parameters.


Parameters:
* `$params`: `array` Parameters  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `tdToTdcli(mixed $params): mixed`

Convert TD parameters to tdcli.


Parameters:
* `$params`: `mixed` Parameters  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `tdcliToTd(array $params, array $key): mixed`

Convert tdcli parameters to tdcli.


Parameters:
* `$params`: `array` Params  
* `$key`: `array` Key  


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `timeout(\Generator|\Promise $promise, int $timeout): \Amp\Promise`

Create an artificial timeout for any \Generator or Promise.


Parameters:
* `$promise`: `\Generator|\Promise`   
* `$timeout`: `int`   


#### See also: 
* `\Generator`
* `\Promise`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `timeoutWithDefault(\Promise|\Generator $promise, int $timeout, mixed $default): \Amp\Promise<\TReturn>|\Promise<\TReturnAlt>`

Creates an artificial timeout for any `Promise`.
If the promise is resolved before the timeout expires, the result is returned

If the timeout expires before the promise is resolved, a default value is returned

Parameters:
* `$promise`: `\Promise|\Generator` Promise to which the timeout is applied.  
  Full type:
  ```
  \Promise<\TReturn>|\TGenerator
  ```
* `$timeout`: `int` Timeout in milliseconds.  
* `$default`: `mixed`   
  Full type:
  ```
  \TReturnAlt
  ```


#### See also: 
* `\Promise`
* `\Generator`
* `\TReturn`
* `\TGenerator`
* `\TReturnAlt`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `toCamelCase(string $input): string`

Convert to camelCase.


Parameters:
* `$input`: `string` String  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `toSnakeCase(string $input): string`

Convert to snake_case.


Parameters:
* `$input`: `string` String  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `toSupergroup(int $id): float|int`

Convert MTProto channel ID to bot API channel ID.


Parameters:
* `$id`: `int` MTProto channel ID  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `typeEscape(string $type): string`

Escape type name.


Parameters:
* `$type`: `string` String to escape  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `unpackDouble(string $value): float`

Unpack binary double.


Parameters:
* `$value`: `string` Value to unpack  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `unpackFileId(string $fileId): mixed`

Unpack bot API file ID.


Parameters:
* `$fileId`: `string` Bot API file ID  


Fully typed return value:
```
array|\Amp\Promise<array>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `unpackSignedInt(string $value): int`

Unpack base256 signed int.


Parameters:
* `$value`: `string` base256 int  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `unpackSignedLong(string $value): int`

Unpack base256 signed long.


Parameters:
* `$value`: `string` base256 long  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `unpackSignedLongString(string $value): string`

Unpack base256 signed long to string.


Parameters:
* `$value`: `string` base256 long  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `unsetEventHandler(bool $disableUpdateHandling): mixed`

Unset event handler.


Parameters:
* `$disableUpdateHandling`: `bool` Whether to also disable internal update handling (will cause errors, otherwise will simply use the NOOP handler)  


Fully typed return value:
```
void|\Amp\Promise<void>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `update2fa(array $params): \Amp\Promise`

Update the 2FA password.
The params array can contain password, new_password, email and hint params.

Parameters:
* `$params`: `array` The params  


#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `updateSettings(\danog\MadelineProto\SettingsAbstract $settings): \Amp\Promise`

Parse, update and store settings.


Parameters:
* `$settings`: `\danog\MadelineProto\SettingsAbstract` Settings  


#### See also: 
* `\danog\MadelineProto\SettingsAbstract`
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `upload(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb, bool $encrypted): \Amp\Promise`

Upload file.


Parameters:
* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `uploadEncrypted(\danog\MadelineProto\FileCallbackInterface|string|array $file, string $fileName, callable $cb): \Amp\Promise`

Upload file to secret chat.


Parameters:
* `$file`: `\danog\MadelineProto\FileCallbackInterface|string|array` File, URL or Telegram file to upload  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `uploadFromCallable(mixed $callable, int $size, string $mime, string $fileName, callable $cb, bool $seekable, bool $encrypted): \Amp\Promise`

Upload file from callable.
The callable must accept two parameters: int $offset, int $size
The callable must return a string with the contest of the file at the specified offset and size.

Parameters:
* `$callable`: `mixed` Callable  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$seekable`: `bool` Whether chunks can be fetched out of order  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Amp\Promise<array{_: string, id: string, parts: int, name: string, mime_type: string, key_fingerprint?: mixed, key?: mixed, iv?: mixed, md5_checksum: string}>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `uploadFromStream(mixed $stream, int $size, string $mime, string $fileName, callable $cb, bool $encrypted): \Amp\Promise`

Upload file from stream.


Parameters:
* `$stream`: `mixed` PHP resource or AMPHP async stream  
* `$size`: `int` File size  
* `$mime`: `string` Mime type  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `uploadFromTgfile(mixed $media, callable $cb, bool $encrypted): \Amp\Promise`

Reupload telegram file.


Parameters:
* `$media`: `mixed` Telegram file  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `uploadFromUrl(string|\danog\MadelineProto\FileCallbackInterface $url, int $size, string $fileName, callable $cb, bool $encrypted): \Amp\Promise`

Upload file from URL.


Parameters:
* `$url`: `string|\danog\MadelineProto\FileCallbackInterface` URL of file  
* `$size`: `int` Size of file  
* `$fileName`: `string` File name  
* `$cb`: `callable` Callback (DEPRECATED, use FileCallbackInterface)  
* `$encrypted`: `bool` Whether to encrypt file for secret chats  


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* [`\danog\MadelineProto\FileCallbackInterface`: File callback interface.](./FileCallbackInterface.md)
* `\Amp\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `wait(\Generator|\Promise $promise, bool $ignoreSignal): mixed`

Synchronously wait for a promise|generator.


Parameters:
* `$promise`: `\Generator|\Promise` The promise to wait for  
* `$ignoreSignal`: `bool` Whether to ignore shutdown signals  


#### See also: 
* `\Generator`
* `\Promise`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `async(bool $async): void`

Enable or disable async.


Parameters:
* `$async`: `bool` Whether to enable or disable async  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `init(): void`

Blockingly init.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `initAsynchronously(): \Generator`

Asynchronously init.


#### See also: 
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `inited(): bool`

Check if we've already inited.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `forceInit(bool $inited): void`

Mark instance as (de)inited forcefully.


Parameters:
* `$inited`: `bool` Whether to mark the instance as inited or deinited  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getWebAPITemplate(): string`

Get web API login HTML template string.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setWebAPITemplate(): void`

Set web API login HTML template string.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)