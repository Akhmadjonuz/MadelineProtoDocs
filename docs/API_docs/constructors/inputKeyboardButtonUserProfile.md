---
title: inputKeyboardButtonUserProfile
description: inputKeyboardButtonUserProfile attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: inputKeyboardButtonUserProfile  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|text|[string](../types/string.md) | Yes|
|user\_id|[InputUser](../types/InputUser.md) | Optional|



### Type: [KeyboardButton](../types/KeyboardButton.md)


### Example:

```php
$inputKeyboardButtonUserProfile = ['_' => 'inputKeyboardButtonUserProfile', 'text' => 'string', 'user_id' => InputUser];
```  


Or, if you're into Lua:

```lua
inputKeyboardButtonUserProfile={_='inputKeyboardButtonUserProfile', text='string', user_id=InputUser}

```

