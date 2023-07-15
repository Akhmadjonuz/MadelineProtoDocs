---
title: "danog\\MadelineProto\\EventHandler\\Media\\AbstractVideo: Represents a generic video."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\EventHandler\Media\AbstractVideo`
[Back to index](../../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

Represents a generic video.  



## Properties
* `$duration`: `int` Video duration in seconds
* `$supportsStreaming`: `bool` Whether the video supports streaming
* `$width`: `int` Video width
* `$height`: `int` Video height
* `$size`: `int` Media filesize
* `$fileName`: `string` Media file name
* `$fileExt`: `string` Media file extension
* `$creationDate`: `int` Media creation date
* `$mimeType`: `string` Media MIME type
* `$ttl`: `?int` Time-to-live of media
* `$thumbs`: `list<array>` Thumbnails
* `$videoThumbs`: `list<array>` Video thumbnails
* `$spoiler`: `bool` Whether the media should be hidden behind a spoiler
* `$botApiFileId`: `string` File ID in bot API format (always present even for users)
* `$botApiFileUniqueId`: `string` Unique file ID in bot API format (always present even for users)
* `$protected`: `bool` Whether this media is protected
---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)