# New Methods

## Inline Text Replacement
[Karl 👑🦆](https://forums.swift.org/t/additional-string-processing-apis/36255/3)

**Library:** Foundation

**Use:** If present, replaces all occurrences of the specified text within the current string. Compliments the existing [`replacingOccurrences(of:with:options:range:)`](https://developer.apple.com/documentation/swift/stringprotocol/3126775-replacingoccurrences).

**Example Method Signature:**
```
mutating func replaceOccurrences<Target, Replacement>(of target: Target, with replacement: Replacement, options: String.CompareOptions = [], range searchRange: Range<Self.Index>? = nil) where Target : StringProtocol, Replacement : StringProtocol
```

**Example Usage:**
```
str.replaceOccurrences(of: "Hello", with: "Guten Tag")
```

**Current Way to Achieve Example Result:**
```
str = str.replacingOccurrences(of: "Hello", with: "Guten Tag")
```

## Prefix/Suffix Removal
[davedelong](https://forums.swift.org/t/additional-string-processing-apis/36255/4)

**Library:** Standard Library

**Use:** If present, removes the specified prefix or suffix from a string.

**Example Method Signature:**
```
mutating func removePrefix(_ prefix: String)
func removingPrefix(_ prefix: String) -> String

mutating func removeSuffix(_ suffix: String)
func removingSuffix(_ suffix: String) -> String
```

**Example Usage:**
```
let prefixToRemove = "Title: "
str.removePrefix(prefixToRemove)
```

**Current Way to Achieve Example Result:**
```
let prefixToRemove = "Title: "
if str.hasPrefix(prefixToRemove) {
    str = String(str.dropFirst(prefixToRemove.count))
}
```
