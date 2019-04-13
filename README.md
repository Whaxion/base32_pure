# base32_pure
[![CircleCI](https://circleci.com/gh/Whaxion/base32_pure.svg?style=svg)](https://circleci.com/gh/Whaxion/base32_pure)

Encodes and decodes binary string or integer tokens to and from base32.

Based on [wrimle's base32_pure library](https://github.com/wrimle/base32_pure/)

## Description

It uses the Crockford alphabet defined at http://www.crockford.com/wrmg/base32.html -
which is probably not the most efficient, but it is tolerant to user mistakes.

* It's case insensitive
* I, l and 1 maps to the same value
* 0 and O maps to the same value
* U is excluded to reduce the likelyhood of accidental obscenity

## Installation

1. Add the dependency to your `shard.yml`:

   ```yaml
   dependencies:
     base32_pure:
       github: whaxion/base32_pure
   ```

2. Run `shards install`

## Usage

/!\ Doesn't work with integer and hypenation /!\

```crystal
require "base32_pure"

encoded = Base32::Crockford.encode("Some token")
Base32::Crockford.decode(encoded)
```

## Contributing

1. Fork it (<https://github.com/whaxion/base32_pure/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Contributors

- [Whaxion](https://github.com/whaxion) - creator and maintainer
