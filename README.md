# DiscordWebhookAPI

[![](https://jitpack.io/v/xyz.mlserver/DiscordWebhookAPI.svg)](https://jitpack.io/#xyz.mlserver/DiscordWebhookAPI)
[![Twitter](https://badgen.net/twitter/follow/monster_2408?icon=twitter)](https://twitter.com/monster_2408)
[![Discord](https://discord.com/api/guilds/556844677115150366/widget.png)](https://discord.mlserver.xyz)

[Website](https://monster2408.com) | [Java Docs](https://docs.mlserver.jp/DiscordWebHookAPI/)


## Send Message for Discord WebHook

You can send message for Discord WebHook.
```java
DiscordWebHook message = new DiscordWebHook.Builder()
        .setContent("Hello, World!") // this is message content
        .setUsername("username") // this is username
        .setAvatarUrl("https://example.com/avatar.png") // this is avatar url
        .build();

// this is webhook url
String url = "https://discord.com/api/webhooks/123456789/abcdefg";

// send webhook
DiscordWebHookAPI.sendWebHook(url, message);
```

## Using with Maven

```xml
<repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
</repository>

<dependency>
    <groupId>xyz.mlserver</groupId>
    <artifactId>DiscordWebhookAPI</artifactId>
    <version>VERSION</version>
</dependency>
```

## Using with Gradle

```gradle
repositories {
    ...
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation 'xyz.mlserver:DiscordWebhookAPI:VERSION'
}
```

### Developer
#### JavaDoc Command
```shell
mvn javadoc:javadoc
```