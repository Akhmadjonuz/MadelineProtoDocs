---
title: botInlineMediaResultDocument
description: botInlineMediaResultDocument attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: botInlineMediaResultDocument  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|id|[string](../types/string.md) | Yes|
|type|[string](../types/string.md) | Yes|
|document|[Document](../types/Document.md) | Optional|
|send\_message|[BotInlineMessage](../types/BotInlineMessage.md) | Yes|



### Type: [BotInlineResult](../types/BotInlineResult.md)


### Example:

```php
$botInlineMediaResultDocument = ['_' => 'botInlineMediaResultDocument', 'id' => 'string', 'type' => 'string', 'document' => Document, 'send_message' => BotInlineMessage];
```  


Or, if you're into Lua:

```lua
botInlineMediaResultDocument={_='botInlineMediaResultDocument', id='string', type='string', document=Document, send_message=BotInlineMessage}

```

