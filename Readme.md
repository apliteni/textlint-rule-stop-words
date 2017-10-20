# textlint-rule-stop-words

[![textlint fixable rule](https://img.shields.io/badge/textlint-fixable-green.svg?style=social)](https://textlint.github.io/)
[![Build Status](https://travis-ci.org/sapegin/textlint-rule-stop-words.svg)](https://travis-ci.org/sapegin/textlint-rule-stop-words)
[![npm](https://img.shields.io/npm/v/textlint-rule-stop-words.svg)](https://www.npmjs.com/package/textlint-rule-stop-words)

[textlint](https://github.com/textlint/textlint) rule to find filler words, buzzwords and chiches — 1600+ words and phrases.

For example:

* and etc.
* the month of
* thick as a brick
* utilize

(You can disable some words or add your own.)

![](https://d3vv6lp55qjaqc.cloudfront.net/items/2P3W3w0d1N0K421H333m/textlint-rule-stop-words.png)

## Installation

```shell
npm install textlint-rule-stop-words
```

## Usage

```shell
textlint --fix --rule stop-words Readme.md
```

## Configuration

By default the rule will check against my personal [dictionary](./dict.txt). You can change it in your `.textlintrc`:

```js
{
  "rules": {
    "stop-words": {
      // Load default dictionary (see dict.txt in the repository)
      "defaultWords": true,
      // Syntax elements to skip. Overrides the default
      "skip": ["Blockquote"],
      // Extra words
      "words": [
        "etc.",
        "you can"
      ],
      // Excluded words
      "exclude": [
        "utilize",
        "period of time"
      ],
      // OR load terms from a file
      "words": "~/stop-words.txt"
    }
  }
}
```

Read more about [configuring textlint](https://github.com/textlint/textlint/blob/master/docs/configuring.md).

## Tips & tricks

Use [textlint-filter-rule-comments](https://github.com/textlint/textlint-filter-rule-comments) to disable stop-words check for particular paragraphs:

```markdown
<!-- textlint-disable stop-words -->

Oh my javascript!

<!-- textlint-enable -->
```

## Sources

* Grammar & Writing for Creators
* [297 Flabby Words and Phrases That Rob Your Writing of All Its Power](https://smartblogger.com/weak-writing/)
* [no-cliches](https://github.com/dunckr/no-cliches/)
* [fillers](https://github.com/wooorm/fillers/)
* [hedges](https://github.com/wooorm/hedges/)
* [weasels](https://github.com/wooorm/weasels/)
* [buzzwords](https://github.com/wooorm/buzzwords/)
* [retext-simplify](https://github.com/wooorm/retext-simplify/)

## Change log

The change log can be found on the [Releases page](https://github.com/sapegin/textlint-rule-stop-words/releases).

## Contributing

Everyone is welcome to contribute. Please take a moment to review the [contributing guidelines](Contributing.md).

## Authors and license

[Artem Sapegin](http://sapegin.me) and [contributors](https://github.com/sapegin/textlint-rule-stop-words/graphs/contributors).

MIT License, see the included [License.md](License.md) file.
