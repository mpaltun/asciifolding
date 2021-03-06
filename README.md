# asciifolding
[![Build Status](https://travis-ci.com/mpaltun/asciifolding.svg?branch=master)](https://travis-ci.com/mpaltun/asciifolding)

Rust port of Lucene's [Ascii folding filter](http://lucene.apache.org/core/8_0_0/analyzers-common/org/apache/lucene/analysis/miscellaneous/ASCIIFoldingFilter.html)  

From Lucene documentation:
> This class converts alphabetic, numeric, and symbolic Unicode characters which are not in the first 127 ASCII characters (the "Basic Latin" Unicode block) into their ASCII equivalents, if one exists.

## Example
```rust
use asciifolding::fold_to_ascii;


assert_eq!(fold_to_ascii("Fıstıkçı Şuayip"), "Fistikci Suayip");
```

## Reference
- https://github.com/apache/lucene-solr/blob/2ae4746365c1ee72a0047ced7610b2096e438979/lucene/analysis/common/src/java/org/apache/lucene/analysis/miscellaneous/ASCIIFoldingFilter.java
- https://github.com/kaedroho/rusticsearch
