<hr>
Using feeds, you may listen for external events and notify your team using the available notification hooks.
<hr>

## Feed definition

Each `feed` is defined in the `feeds.js` file in the JSON format.

``` js
  {
    'name': 'feed name', //feed name
    'feed': 'http://url', //feed url
    'verify': true, //verify if field contains a ip/domain/address contained in any crawler range
    'field': 'title', //field to be processed
    'interval': 2 //pooling interval (mins)
  }
```

<hr>
## Feeds (`feeds.js`) file

`feeds.js` is where feeds are defined, this file must exists in `conf` folder.

``` js
  module.exports = [
  {
    'name': 'zone-h',
    'feed': 'http://www.zone-h.org/rss/defacements',
    'verify': true,
    'field': 'title',
    'interval': 2
  },
  {
    'name': 'phishtank',
    'feed': 'http://rss.phishtank.com/rss/asn/?asn=12345',
    'verify': false,
    'field': 'link',
    'interval': 2
  },
  {
    ...
  }
];
```

[meta:title]: <> (Feeds)