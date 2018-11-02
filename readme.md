# dictionary-cy-gb

Welsh (United Kingdom) spelling dictionary in UTF-8.

Useful with [hunspell][], [`nodehun`][nodehun], [`nspell`][nspell],
Open Office, LibreOffice, FireFox and Thunderbird, or [macOS][].

The dictionary itself is gratefully sourced from [elastic/hunspell](https://github.com/elastic/hunspell/tree/master/dicts/cy_GB), whose license is included here, and the source for generating the module is directly taken from [wooorm/dictionaries](https://github.com/wooorm/dictionaries).

## Installation

[npm][]:

```bash
npm install dictionary-cy-gb
```

## Usage

```js
var enGB = require('dictionary-cy-gb')

enGB(function (err, result) {
  console.log(err || result)
});
```

Yields:

```js
{ dic: <Buffer>,
  aff: <Buffer> }
```

Where `dic` is a buffer for the dictionary file at `index.dic` (in UTF-8), and
`aff` is a buffer for the affix file at `index.aff` (in UTF-8).

Or directly load the files, using something like:

```js
var path = require('path')
var base = require.resolve('dictionary-cy-gb')

fs.readFileSync(path.join(base, 'index.dic'), 'utf-8')
fs.readFileSync(path.join(base, 'index.aff'), 'utf-8')
```

## License

### Dictionary and affix file
GPL – © 2004, Canolfan Bedwyr, University Of Wales, Bangor. 

### Node module
MIT © [Titus Wormer][home].

[hunspell]: http://hunspell.github.io

[nodehun]: https://github.com/nathanjsweet/nodehun

[nspell]: https://github.com/wooorm/nspell

[macos]: https://github.com/wooorm/dictionaries#macos

[source]: http://wordlist.aspell.net/dicts/

[npm]: https://docs.npmjs.com/cli/install

[dictionaries]: https://github.com/wooorm/dictionaries

[home]: https://wooorm.com