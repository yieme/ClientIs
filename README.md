# ClientIs

Basic client OS detection with bot/crawler/spider support adapted from [gorangajic/isbot](https://github.com/gorangajic/isbot)

## Include

```js
<script src="https://rawgit.com/yieme/clientis/master/clientis.js"></script>
```

## ClientIs() usage

```js
ClientIs() // Bot, Windows, OSX, X11, Linux, iOS, Android or Unknown. Bot be returned if PhantomJS detected in this use case

ClientIs("Googlebot/2.1 (+http://www.google.com/bot.html)") // Bot

ClientIs("Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36") // Windows
```

## IsBot() usage

PhantomJS support is only good for the current client, not passed user agents.

```js
IsBot() // true if Bot detected including PhantomJS

IsBot("Googlebot/2.1 (+http://www.google.com/bot.html)") // true

IsBot("Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36") // false
```

## Global namespace collision

Fork this repo and change the last line of `isbot.js` to what you'd like:

```js
  ...
})(window, navigator, 'ClientIs', 'IsBot')
```

## License

MIT
