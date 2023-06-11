---
title: "danog\\MadelineProto\\Tools: Some tools."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\Tools`
[Back to index](../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Some tools.  




## Constants
* `danog\MadelineProto\Tools::ALL_MIMES`: 


## Method list:
* [`testFibers(int $fiberCount): array{maxFibers: int, realMemoryMb: int, maps: ?int, maxMaps: ?int}`](#testfibersint-fibercount-arraymaxfibers-int-realmemorymb-int-maps-int-maxmaps-int)
* [`getMaps(): ?int`](#getmaps-int)
* [`getMaxMaps(): ?int`](#getmaxmaps-int)
* [`genVectorHash(array $ints): \string Vector hash`](#genvectorhasharray-ints-string-vector-hash)
* [`randomInt(int $modulus): int`](#randomintint-modulus-int)
* [`random(int $length): \string Random string`](#randomint-length-string-random-string)
* [`posmod(int $a, int $b): \int Modulo`](#posmodint-a-int-b-int-modulo)
* [`unpackSignedInt(string $value): int`](#unpacksignedintstring-value-int)
* [`unpackSignedLong(string $value): int`](#unpacksignedlongstring-value-int)
* [`unpackSignedLongString(string|int|array $value): string`](#unpacksignedlongstringstringintarray-value-string)
* [`packSignedInt(int $value): string`](#packsignedintint-value-string)
* [`packSignedLong(int $value): string`](#packsignedlongint-value-string)
* [`packUnsignedInt(int $value): string`](#packunsignedintint-value-string)
* [`packDouble(float $value): string`](#packdoublefloat-value-string)
* [`unpackDouble(string $value): float`](#unpackdoublestring-value-float)
* [`isArrayOrAlike(mixed $var): bool`](#isarrayoralikemixed-var-bool)
* [`arr(mixed $params): array`](#arrmixed-params-array)
* [`base64urlDecode(string $data): string`](#base64urldecodestring-data-string)
* [`base64urlEncode(string $data): string`](#base64urlencodestring-data-string)
* [`rleDecode(string $string): string`](#rledecodestring-string-string)
* [`rleEncode(string $string): string`](#rleencodestring-string-string)
* [`inflateStripped(string $stripped): \string JPG payload`](#inflatestrippedstring-stripped-string-jpg-payload)
* [`closeConnection(string $message): void`](#closeconnectionstring-message-void)
* [`end(array $what): mixed`](#endarray-what-mixed)
* [`isAltervista(): bool`](#isaltervista-bool)
* [`hasVar(object $obj, string $var): bool`](#hasvarobject-obj-string-var-bool)
* [`getVar(object $obj, string $var): mixed`](#getvarobject-obj-string-var-mixed)
* [`setVar(object $obj, string $var, mixed $val): void`](#setvarobject-obj-string-var-mixed-val-void)
* [`rethrow(\Throwable $e): void`](#rethrowthrowable-e-void)
* [`flock(string $file, int $operation, float $polling, ?\Amp\Cancellation $token, ?\Closure $failureCb): mixed`](#flockstring-file-int-operation-float-polling-ampcancellation-token-closure-failurecb-mixed)
* [`sleep(float $time): void`](#sleepfloat-time-void)
* [`readLine(string $prompt): string`](#readlinestring-prompt-string)
* [`echo(string $string): void`](#echostring-string-void)
* [`mbStrlen(string $text): int`](#mbstrlenstring-text-int)
* [`mbSubstr(string $text, int $offset, null|int $length): string`](#mbsubstrstring-text-int-offset-nullint-length-string)
* [`mbStrSplit(string $text, int $length): string[]`](#mbstrsplitstring-text-int-length-string)
* [`toCamelCase(string $input): string`](#tocamelcasestring-input-string)
* [`toSnakeCase(string $input): string`](#tosnakecasestring-input-string)
* [`markdownEscape(string $hwat): string`](#markdownescapestring-hwat-string)
* [`typeEscape(string $type): string`](#typeescapestring-type-string)
* [`methodEscape(string $method): string`](#methodescapestring-method-string)
* [`getMimeFromExtension(string $extension, string $default): string`](#getmimefromextensionstring-extension-string-default-string)
* [`getExtensionFromMime(string $mime): string`](#getextensionfrommimestring-mime-string)
* [`getExtensionFromLocation(mixed $location, string $default): string`](#getextensionfromlocationmixed-location-string-default-string)
* [`getMimeFromFile(string $file): string`](#getmimefromfilestring-file-string)
* [`getMimeFromBuffer(string $buffer): string`](#getmimefrombufferstring-buffer-string)

## Methods:
### `testFibers(int $fiberCount): array{maxFibers: int, realMemoryMb: int, maps: ?int, maxMaps: ?int}`

Test fibers.


Parameters:

* `$fiberCount`: `int`   



### `getMaps(): ?int`

Get current number of memory-mapped regions, UNIX only.



### `getMaxMaps(): ?int`

Get maximum number of memory-mapped regions, UNIX only.
Use testFibers to get the maximum number of fibers on any platform.


### `genVectorHash(array $ints): \string Vector hash`

Generate MTProto vector hash.


Parameters:

* `$ints`: `array` IDs  


Return value: Vector hash


### `randomInt(int $modulus): int`

Get random integer.


Parameters:

* `$modulus`: `int` Modulus  



### `random(int $length): \string Random string`

Get random string of specified length.


Parameters:

* `$length`: `int` Length  


Return value: Random string


### `posmod(int $a, int $b): \int Modulo`

Positive modulo
Works just like the % (modulus) operator, only returns always a postive number.


Parameters:

* `$a`: `int` A  
* `$b`: `int` B  


Return value: Modulo


### `unpackSignedInt(string $value): int`

Unpack base256 signed int.


Parameters:

* `$value`: `string` base256 int  



### `unpackSignedLong(string $value): int`

Unpack base256 signed long.


Parameters:

* `$value`: `string` base256 long  



### `unpackSignedLongString(string|int|array $value): string`

Unpack base256 signed long to string.


Parameters:

* `$value`: `string|int|array` base256 long  



### `packSignedInt(int $value): string`

Convert integer to base256 signed int.


Parameters:

* `$value`: `int` Value to convert  



### `packSignedLong(int $value): string`

Convert integer to base256 long.


Parameters:

* `$value`: `int` Value to convert  



### `packUnsignedInt(int $value): string`

Convert value to unsigned base256 int.


Parameters:

* `$value`: `int` Value  



### `packDouble(float $value): string`

Convert double to binary version.


Parameters:

* `$value`: `float` Value to convert  



### `unpackDouble(string $value): float`

Unpack binary double.


Parameters:

* `$value`: `string` Value to unpack  



### `isArrayOrAlike(mixed $var): bool`

Check if is array or similar (traversable && countable && arrayAccess).


Parameters:

* `$var`: `mixed` Value to check  



### `arr(mixed $params): array`

Create array.


Parameters:

* `$params`: `mixed` Params  



### `base64urlDecode(string $data): string`

base64URL decode.


Parameters:

* `$data`: `string` Data to decode  



### `base64urlEncode(string $data): string`

Base64URL encode.


Parameters:

* `$data`: `string` Data to encode  



### `rleDecode(string $string): string`

null-byte RLE decode.


Parameters:

* `$string`: `string` Data to decode  



### `rleEncode(string $string): string`

null-byte RLE encode.


Parameters:

* `$string`: `string` Data to encode  



### `inflateStripped(string $stripped): \string JPG payload`

Inflate stripped photosize to full JPG payload.


Parameters:

* `$stripped`: `string` Stripped photosize  


Return value: JPG payload


### `closeConnection(string $message): void`

Close connection with client, connected via web.


Parameters:

* `$message`: `string` Message  



### `end(array $what): mixed`

Get final element of array.


Parameters:

* `$what`: `array` Array  



### `isAltervista(): bool`

Whether this is altervista.



### `hasVar(object $obj, string $var): bool`

Checks private property exists in an object.


Parameters:

* `$obj`: `object` Object  
* `$var`: `string` Attribute name  



### `getVar(object $obj, string $var): mixed`

Accesses a private variable from an object.


Parameters:

* `$obj`: `object` Object  
* `$var`: `string` Attribute name  



### `setVar(object $obj, string $var, mixed $val): void`

Sets a private variable in an object.


Parameters:

* `$obj`: `object` Object  
* `$var`: `string` Attribute name  
* `$val`: `mixed` Attribute value  



### `rethrow(\Throwable $e): void`

Rethrow exception into event loop.


Parameters:

* `$e`: `\Throwable`   


#### See also: 
* `\Throwable`




### `flock(string $file, int $operation, float $polling, ?\Amp\Cancellation $token, ?\Closure $failureCb): mixed`

Asynchronously lock a file
Resolves with a callbable that MUST eventually be called in order to release the lock.


Parameters:

* `$file`: `string` File to lock  
* `$operation`: `int` Locking mode  
* `$polling`: `float` Polling interval  
* `$token`: `?\Amp\Cancellation` Cancellation token  
* `$failureCb`: `?\Closure` Failure callback, called only once if the first locking attempt fails.  


#### See also: 
* `\Amp\Cancellation`
* `\Closure`




### `sleep(float $time): void`

Asynchronously sleep.


Parameters:

* `$time`: `float` Number of seconds to sleep for  



### `readLine(string $prompt): string`

Asynchronously read line.


Parameters:

* `$prompt`: `string` Prompt  



### `echo(string $string): void`

Asynchronously write to stdout/browser.


Parameters:

* `$string`: `string` Message to echo  



### `mbStrlen(string $text): int`

Get Telegram UTF-8 length of string.


Parameters:

* `$text`: `string` Text  



### `mbSubstr(string $text, int $offset, null|int $length): string`

Telegram UTF-8 multibyte substring.


Parameters:

* `$text`: `string` Text to substring  
* `$offset`: `int` Offset  
* `$length`: `null|int` Length  



### `mbStrSplit(string $text, int $length): string[]`

Telegram UTF-8 multibyte split.


Parameters:

* `$text`: `string` Text  
* `$length`: `int` Length  



### `toCamelCase(string $input): string`

Convert to camelCase.


Parameters:

* `$input`: `string` String  



### `toSnakeCase(string $input): string`

Convert to snake_case.


Parameters:

* `$input`: `string` String  



### `markdownEscape(string $hwat): string`

Escape string for markdown.


Parameters:

* `$hwat`: `string` String to escape  



### `typeEscape(string $type): string`

Escape type name.


Parameters:

* `$type`: `string` String to escape  



### `methodEscape(string $method): string`

Escape method name.


Parameters:

* `$method`: `string` Method name  



### `getMimeFromExtension(string $extension, string $default): string`

Get mime type from file extension.


Parameters:

* `$extension`: `string` File extension  
* `$default`: `string` Default mime type  



### `getExtensionFromMime(string $mime): string`

Get extension from mime type.


Parameters:

* `$mime`: `string` MIME type  



### `getExtensionFromLocation(mixed $location, string $default): string`

Get extension from file location.


Parameters:

* `$location`: `mixed` File location  
* `$default`: `string` Default extension  



### `getMimeFromFile(string $file): string`

Get mime type of file.


Parameters:

* `$file`: `string` File  



### `getMimeFromBuffer(string $buffer): string`

Get mime type from buffer.


Parameters:

* `$buffer`: `string` Buffer  



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)
