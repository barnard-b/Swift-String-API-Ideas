# Swift String API-Ideas
Ideas for new String APIs - Swift Programming Language

Discussion: https://forums.swift.org/t/additional-string-processing-apis/36255

---

# New Methods

## Prefix/Suffix Removal
[davedelong](https://forums.swift.org/t/additional-string-processing-apis/36255/4)

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
