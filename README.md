Parsec.fs
=========

Pure F# Parsec Implementation

## Features

* Written 100% in F#
* Self-contained single source file
* Compatible with [Fable](https://fable.io/) compiler
* API almost identical to [FParsec](https://www.quanttec.com/fparsec/)

## Compatibility with FParsec

* Parsec.fs does not support stream input, so it backtracks by default.
* Several combinators behave differently.
  * `regex` only accepts regex with `RegexOptions.ECMAScript`. This is to ensure compatibility between .NET and Fable.
  * `unicodeReturn / unicodeSpaces` are not supported.
  * Generic `numberLiteral(L)` is not implemented.
  * `pfloat` does not parse hex float numbers and numbers without fraction.
* Parsec.fs does not contain operator‐precedence parer implementation.

## License

See Parsec.fs.
