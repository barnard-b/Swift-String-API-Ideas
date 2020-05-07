# New Properties

## isASCII
[Karl 👑🦆](https://forums.swift.org/t/additional-string-processing-apis/36255/3)

**Use:** Returns whether this string is capable of providing access to validly-encoded ASCII contents. Similar to the existing [`isContiguousUTF8`](https://developer.apple.com/documentation/swift/string/3201133-iscontiguousutf8).

**Example Method Signature:**
```
public var isASCII: Bool { get }
```

**Example Usage:**
```
let hasOnlyASCIICharacters = str.isASCII
```

**Current Way to Achieve Example Result:**
Not applicable.
