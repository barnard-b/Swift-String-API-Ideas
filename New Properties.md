# New Properties

## isASCII
[Karl 👑🦆](https://forums.swift.org/t/additional-string-processing-apis/36255/3)

**Library:** Standard Library

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
```
let isASCIIResults = Set(str.compactMap({ $0.isASCII }))
let hasOnlyASCIICharacters = isASCIIResults.count == 1 && isASCIIResults.first == true
```

## Case Folded
[Dante-Broggi](https://forums.swift.org/t/additional-string-processing-apis/36255/5)

**Library:** Not Determined

**Use:** See [Case Folding: An Introduction](https://www.w3.org/International/wiki/Case_folding).

**Example Method Signature:**
```
public var casefolded: String { get }
```

**Example Usage:**
```
let normalized = str.casefolded
```

**Current Way to Achieve Example Result:**
Custom implementation or third party library based on http://www.unicode.org/Public/UNIDATA/CaseFolding.txt



