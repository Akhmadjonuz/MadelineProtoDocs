---
title: danog\MadelineProto\Settings\Connection: Connection settings.
description: 

---
# `danog\MadelineProto\Settings\Connection`
[Back to index](../../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Connection settings.  




## Method list:
* `getProtocol(): string`
* `setProtocol(class-string<\danog\MadelineProto\Stream\MTProtoBufferInterface> $protocol): self`
* `getIpv6(): bool`
* `setIpv6(bool $ipv6): self`
* `getSslSubdomains(): array`
* `setSslSubdomains(array $sslSubdomains): self`
* `getMinMediaSocketCount(): int`
* `setMinMediaSocketCount(int $minMediaSocketCount): self`
* `getMaxMediaSocketCount(): int`
* `setMaxMediaSocketCount(int $maxMediaSocketCount): self`
* `getRobinPeriod(): int`
* `setRobinPeriod(int $robinPeriod): self`
* `getDefaultDc(): int`
* `getDefaultDcParams(): array`
* `setDefaultDc(int $defaultDc): self`
* `getProxies(): array`
* `addProxy(class-string<\danog\MadelineProto\Stream\StreamInterface> $proxy, array $extra): self`
* `setProxy(array $proxies): self`
* `clearProxies(): self`
* `removeProxy(string $proxy, array $extra): self`
* `getObfuscated(): bool`
* `setObfuscated(bool $obfuscated): self`
* `getTestMode(): bool`
* `setTestMode(bool $testMode): self`
* `getTransport(): class-string<\danog\MadelineProto\Stream\RawStreamInterface>`
* `setTransport(class-string<\danog\MadelineProto\Stream\RawStreamInterface> $transport): self`
* `getRetry(): bool`
* `setRetry(bool $retry): self`
* `getTimeout(): int`
* `setTimeout(int $timeout): self`
* `getUseDoH(): bool`
* `setUseDoH(bool $useDoH): self`
* `getBindTo(): ?string`
* `setBindTo(?string $bindTo): self`
* `hasChanged(): bool`

## Methods:
### `getProtocol(): string`

Get protocol identifier.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setProtocol(class-string<\danog\MadelineProto\Stream\MTProtoBufferInterface> $protocol): self`

Set protocol identifier.


Parameters:
* `$protocol`: `class-string<\danog\MadelineProto\Stream\MTProtoBufferInterface>` Protocol identifier  


#### See also: 
* `\danog\MadelineProto\Stream\MTProtoBufferInterface`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getIpv6(): bool`

Get whether to use ipv6.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setIpv6(bool $ipv6): self`

Set whether to use ipv6.


Parameters:
* `$ipv6`: `bool` Whether to use ipv6  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getSslSubdomains(): array`

Get subdomains of web.telegram.org for https protocol.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setSslSubdomains(array $sslSubdomains): self`

Set subdomains of web.telegram.org for https protocol.


Parameters:
* `$sslSubdomains`: `array` Subdomains of web.telegram.org for https protocol.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMinMediaSocketCount(): int`

Get minimum media socket count.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setMinMediaSocketCount(int $minMediaSocketCount): self`

Set minimum media socket count.


Parameters:
* `$minMediaSocketCount`: `int` Minimum media socket count.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getMaxMediaSocketCount(): int`

Get maximum media socket count.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setMaxMediaSocketCount(int $maxMediaSocketCount): self`

Set maximum media socket count.


Parameters:
* `$maxMediaSocketCount`: `int` Maximum media socket count.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getRobinPeriod(): int`

Get robin period (seconds).


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setRobinPeriod(int $robinPeriod): self`

Set robin period (seconds).


Parameters:
* `$robinPeriod`: `int` Robin period (seconds).  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDefaultDc(): int`

Get default DC ID.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getDefaultDcParams(): array`

Get default DC params.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setDefaultDc(int $defaultDc): self`

Set default DC ID.


Parameters:
* `$defaultDc`: `int` Default DC ID.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getProxies(): array`

Get proxy identifiers.


Fully typed return value:
```
array<class-string<\danog\MadelineProto\Stream\StreamInterface>, array>
```
#### See also: 
* `\danog\MadelineProto\Stream\StreamInterface`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `addProxy(class-string<\danog\MadelineProto\Stream\StreamInterface> $proxy, array $extra): self`

Add proxy identifier to list.


Parameters:
* `$proxy`: `class-string<\danog\MadelineProto\Stream\StreamInterface>` Proxy identifier  
* `$extra`: `array` Extra  


#### See also: 
* `\danog\MadelineProto\Stream\StreamInterface`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setProxy(array $proxies): self`

Set proxies.


Parameters:
* `$proxies`: `array` Proxies  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `clearProxies(): self`

Clear proxies.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `removeProxy(string $proxy, array $extra): self`

Remove specific proxy pair.


Parameters:
* `$proxy`: `string`   
* `$extra`: `array`   


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getObfuscated(): bool`

Get whether to use the obfuscated protocol.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setObfuscated(bool $obfuscated): self`

Set whether to use the obfuscated protocol.


Parameters:
* `$obfuscated`: `bool` Whether to use the obfuscated protocol.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getTestMode(): bool`

Get whether we're in test mode.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setTestMode(bool $testMode): self`

Set whether we're in test mode.


Parameters:
* `$testMode`: `bool` Whether we're in test mode.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getTransport(): class-string<\danog\MadelineProto\Stream\RawStreamInterface>`

Get transport identifier.


#### See also: 
* `\danog\MadelineProto\Stream\RawStreamInterface`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setTransport(class-string<\danog\MadelineProto\Stream\RawStreamInterface> $transport): self`

Set transport identifier.


Parameters:
* `$transport`: `class-string<\danog\MadelineProto\Stream\RawStreamInterface>` Transport identifier.  


#### See also: 
* `\danog\MadelineProto\Stream\RawStreamInterface`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getRetry(): bool`

Get whether to retry connection.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setRetry(bool $retry): self`

Set whether to retry connection.


Parameters:
* `$retry`: `bool` Whether to retry connection.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getTimeout(): int`

Get connection timeout.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setTimeout(int $timeout): self`

Set connection timeout.


Parameters:
* `$timeout`: `int` Connection timeout.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getUseDoH(): bool`

Get whether to use DNS over HTTPS.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setUseDoH(bool $useDoH): self`

Set whether to use DNS over HTTPS.


Parameters:
* `$useDoH`: `bool` Whether to use DNS over HTTPS  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `getBindTo(): ?string`

Get bind on specific address and port.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `setBindTo(?string $bindTo): self`

Set bind on specific address and port.


Parameters:
* `$bindTo`: `?string` Bind on specific address and port.  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `hasChanged(): bool`

Get whether this setting was changed, also applies changes.


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)