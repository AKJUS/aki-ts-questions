# Are External Scanners Commonly Used?

Let's start with what an external scanner is.

To quote the official docs:

> Many languages have some tokens whose structure is impossible or
> inconvenient to describe with a regular expression...

> Tree-sitter allows you to handle these kinds of tokens using
> external scanners. An external scanner is a set of C functions that
> you, the grammar author, can write by hand in order to add custom
> logic for recognizing certain tokens.

How common is this need?

## Discussion

As far as how common it is to have an external scanner, based on
searching locally fetched repositories, we found around 40% had
`src/scanner.c`.

If it's any consolation, if it turns out you need to implement an
external scanner, there are a fair number of examples to study :)

Note that a number of external scanners have been written using C++,
but [support was removed in
0.24.0](https://github.com/tree-sitter/tree-sitter/releases/tag/v0.24.0):

> Remove C++ support for external scanners ([#3602](https://github.com/tree-sitter/tree-sitter/pull/3602))

## References

* [External scanner official
  docs](https://tree-sitter.github.io/tree-sitter/creating-parsers/4-external-scanners.html)
* [comment@#53 (old tree-sitter-cli
  repository)](https://github.com/tree-sitter/tree-sitter-cli/issues/53#issuecomment-452462914) -
  early info about external scanners
* [External Scanner Building & Debugging](https://github.com/tree-sitter/tree-sitter/wiki/Tips-and-Tricks-for-a-grammar-author#external-scanner-building--debugging)
* [#219 Builtin support for white space sensitive
  languages](https://github.com/tree-sitter/tree-sitter/issues/219)
* [#281 Document external
  scanners](https://github.com/tree-sitter/tree-sitter/issues/281)
* [#1100 Runtime parsing
  variables](https://github.com/tree-sitter/tree-sitter/discussions/1100)
* [#1259 tree-sitter calls external scanner with all symbols marked
  valid](https://github.com/tree-sitter/tree-sitter/issues/1259)
* [#1627 External scanner in
  test](https://github.com/tree-sitter/tree-sitter/issues/1627)
* [comment@#2897](https://github.com/tree-sitter/tree-sitter/pull/2897#issuecomment-1928112073)

