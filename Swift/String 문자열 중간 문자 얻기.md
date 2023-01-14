```swift
extention String {
	func substring(from: Int, to: Int) -> String {
    guard from < count, to >= 0, to - from >= 0 else { return self }
    
   	let startIndex = index(self.startIndex, offsetBy: from)
		let endIndex = index(self.startIndex, offsetBy: to)
    
   	return String(self[startIndex ..< endIndex])
  }
}
```
