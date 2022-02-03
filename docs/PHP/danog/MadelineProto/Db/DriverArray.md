---
title: "danog\\MadelineProto\\Db\\DriverArray: Array caching trait."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\Db\DriverArray`
[Back to index](../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Array caching trait.  




## Method list:
* `initConnection()`
* `initStartup(): \Generator`
* `getTable(): string`
* `setTable(string $table): self`
* `getInstance(string $table, \danog\MadelineProto\Db\DbArray|array|null $previous, \danog\MadelineProto\Settings\Database\DatabaseAbstract $settings): \Amp\Promise`
* `getArrayCopy(): \Amp\Promise`
* `isset(string|int $key): \Amp\Promise`
* `unset(string|int $key): \Amp\Promise`
* `set(string|int $index, mixed $value): \Amp\Promise`
* `offsetGet(string|int $index): \Amp\Promise`
* `count(): \Amp\Promise<int>`
* `clear(): \Amp\Promise`
* `getIterator()`

## Methods:
### `initConnection()`

Initialize connection.



### `initStartup(): \Generator`

Initialize on startup.


#### See also: 
* `\Generator`




### `getTable(): string`

Get the value of table.



### `setTable(string $table): self`

Set the value of table.


Parameters:

* `$table`: `string`   



### `getInstance(string $table, \danog\MadelineProto\Db\DbArray|array|null $previous, \danog\MadelineProto\Settings\Database\DatabaseAbstract $settings): \Amp\Promise`




Parameters:

* `$table`: `string`   
* `$previous`: `\danog\MadelineProto\Db\DbArray|array|null`   
* `$settings`: `\danog\MadelineProto\Settings\Database\DatabaseAbstract`   


Fully typed return value:
```
\Amp\Promise<static>
```
#### See also: 
* [`\danog\MadelineProto\Db\DbArray`: DB array interface.](../../../danog/MadelineProto/Db/DbArray.html)
* [`\danog\MadelineProto\Settings\Database\DatabaseAbstract`: Base class for database backends.](../../../danog/MadelineProto/Settings/Database/DatabaseAbstract.html)
* `\Amp\Promise`




### `getArrayCopy(): \Amp\Promise`

Get Array copy.


Fully typed return value:
```
\Amp\Promise<array<string|int, \T>>
```
#### See also: 
* `\T`
* `\Amp\Promise`




### `isset(string|int $key): \Amp\Promise`

Check if element is set.


Parameters:

* `$key`: `string|int`   


Fully typed return value:
```
\Amp\Promise<bool>
```
#### See also: 
* `\Amp\Promise`




### `unset(string|int $key): \Amp\Promise`

Unset element.


Parameters:

* `$key`: `string|int`   


Fully typed return value:
```
\Amp\Promise<mixed>
```
#### See also: 
* `\Amp\Promise`




### `set(string|int $index, mixed $value): \Amp\Promise`

Set element.


Parameters:

* `$index`: `string|int`   
* `$value`: `mixed`   
  Full type:
  ```
  \T
  ```


#### See also: 
* `\T`
* `\Amp\Promise`




### `offsetGet(string|int $index): \Amp\Promise`

Get element.


Parameters:

* `$index`: `string|int`   


Fully typed return value:
```
\Amp\Promise<\T>
```
#### See also: 
* `\T`
* `\Amp\Promise`




### `count(): \Amp\Promise<int>`

Count number of elements.


#### See also: 
* `\Amp\Promise`




### `clear(): \Amp\Promise`

Clear all elements.


#### See also: 
* `\Amp\Promise`




### `getIterator()`

Get iterator.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)