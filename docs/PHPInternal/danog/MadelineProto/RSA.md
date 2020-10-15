---
title: danog\MadelineProto\RSA: RSA class.
description: 

---
# `danog\MadelineProto\RSA`
[Back to index](../../index.md)

> Author: Daniil Gentili <daniil@daniil.it>  
  

RSA class.  




## Method list:
* `load(\danog\MadelineProto\TL\TL $TL, string $rsa_key): \Generator`
* `encrypt(string $data): string`

## Methods:
### `load(\danog\MadelineProto\TL\TL $TL, string $rsa_key): \Generator`

Load RSA key.


Parameters:
* `$TL`: `\danog\MadelineProto\TL\TL` TL serializer  
* `$rsa_key`: `string` RSA key  


Fully typed return value:
```
\Generator<int|mixed, array|mixed, mixed, self>
```
#### See also: 
* [`\danog\MadelineProto\TL\TL`: TL serialization.](./TL/TL.md)
* `\Generator`



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

### `encrypt(string $data): string`

Encrypt data.


Parameters:
* `$data`: `string` Data to encrypt  


---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)

---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)