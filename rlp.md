# RLP Notation

This document defines the shared [RLP] primitive types and trailing limit comments used
across the devp2p specifications when RLP-encoded layouts are described inline.

## Primitive Types

- `P`: unsigned integer encoded as the shortest big-endian byte string.
- `B`: variable-length byte string.
- `B_N`: fixed-size byte string of `N` bytes.

Specifications may introduce local aliases such as `ReqID`, `ENR`, `Seq`, or `txₙ`, and
may narrow these shared primitives with protocol-specific limits.

## Trailing Limit Comments

- `// N!`: fixed-size field with exactly `N` content bytes.
- `// up to X bytes, up to Y items`: non-fixed list or structured field with at most `X`
  content bytes and `Y` contained items.
- `// up to X bytes`: non-fixed byte string or opaque value budgeted only by encoded
  size.

[RLP]: https://ethereum.org/en/developers/docs/data-structures-and-encoding/rlp