---
title: "Plugins"
description: "MadelineProto offers a native plugin system, based on event handlers!"
nav_order: 13
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Plugins

MadelineProto offers a native plugin system, based on [event handlers](https://docs.madelineproto.xyz/docs/UPDATES.html)!

## Creating plugins

To create a plugin, simply create an [event handler](https://docs.madelineproto.xyz/docs/UPDATES.html) that extends the `PluginEventHandler` class, here's an example:

```php
<!-- cut_here examples/plugins/Danog/PingPlugin.php -->

```php
<?php declare(strict_types=1);

namespace MadelinePlugin\Danog;

use danog\MadelineProto\EventHandler\Attributes\Cron;
use danog\MadelineProto\EventHandler\Filter\FilterText;
use danog\MadelineProto\EventHandler\Message;
use danog\MadelineProto\EventHandler\SimpleFilter\Incoming;
use danog\MadelineProto\PluginEventHandler;

/**
 * Plugin event handler class.
 *
 * All properties returned by __sleep are automatically stored in the database.
 */
class PingPlugin extends PluginEventHandler
{
    private int $pingCount = 0;

    private string $pongText = 'pong';

    /**
     * You can set a custom pong text from the outside of the plugin:.
     *
     * ```
     * if (!file_exists('madeline.php')) {
     *     copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
     * }
     * include 'vendor/autoload.php';
     *
     * $a = new API('bot.madeline');
     * $plugin = $a->getPlugin(PingPlugin::class);
     *
     * $plugin->setPongText('UwU');
     * ```
     *
     * This will automatically connect to the running instance of the plugin and call the specified method.
     */
    public function setPongText(string $pong): void
    {
        $this->pongText = $pong;
    }

    /**
     * Returns a list of names for properties that will be automatically saved to the session database (MySQL/postgres/redis if configured, the session file otherwise).
     */
    public function __sleep(): array
    {
        return ['pingCount', 'pongText'];
    }
    /**
     * Initialization logic.
     */
    public function onStart(): void
    {
        $this->logger("The bot was started!");
        $this->logger($this->getFullInfo('MadelineProto'));

        $this->sendMessageToAdmins("The bot was started!");
    }

    /**
     * This cron function will be executed forever, every 60 seconds.
     */
    #[Cron(period: 60.0)]
    public function cron1(): void
    {
        $this->sendMessageToAdmins("The ping plugin is online, total pings so far: ".$this->pingCount);
    }

    #[FilterText('ping')]
    public function pingCommand(Incoming&Message $message): void
    {
        $message->reply($this->pongText);
        $this->pingCount++;
    }
}

```

<!-- cut_here_end examples/plugins/Danog/PingPlugin.php -->
```

## Installing plugins

## 

<a href="https://docs.madelineproto.xyz/docs/DATABASE.html">Next section</a>