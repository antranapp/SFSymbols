# SFSymbols
[![Build Status](https://travis-ci.org/Nirma/SFSymbol.svg?branch=master)](https://travis-ci.org/Nirma/SFSymbol)
![Swift 5.3](https://img.shields.io/badge/Swift-5.3-orange.svg)
[![Swift Package Manager compatible](https://img.shields.io/badge/Swift%20Package%20Manager-compatible-purple.svg)](https://github.com/apple/swift-package-manager)
[![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org)

All the SFSymbols at your fingertips.

## Usage 
`SFSymbol` are `static variables` that contain the identifier strings of all of apple's `SFSymbols` as well as which category they belong to and their availability.

You can iterate through all version compatible symbols by using the 'allSymbols' computed variables.

```swift
for symbol in SFSymbol.allSymbols {
	print(symbol.title)
}
```


If you want symbols only in a certain `Category` you can do so like this.

```swift
for symbol in  SFSymbol.Category.weather.symbols {
	print(symbol.title)
}
```


There are even common, human understandable, names for symbols. Feel free extend SFSymbols in your own project for more common names.

```swift
public extension SFSymbol{
    static let share   = squareAndArrowUp
    static let refresh = arrowClockwise
    static let copy    = docOnDoc
    static let writing = squareAndPencil
}

@available(iOS 14, macOS 14.0, tvOS 14.0, watchOS 7.0,  *)
public extension SFSymbol{
    static let edit    = rectangleAndPencilAndEllipsis
    static let filter  = lineHorizontal2DecreaseCircle
    static let sort    = arrowUpArrowDownCircle
}
```

There are extensions for `UIImage`, `Image`, `Button`, and `Label` that enable easy use of any `SFSymbol`.


### UIKit

```swift
UIImage(symbol: .playCircle)
```


### SwiftUI

```swift
Image(symbol: .playCircle)
```


```swift
VStack{
	Label("Sunset", symbol: .sunset)
	Label("Sunset", symbol: .sunset)
		    .foregroundColor(.red)
	Label("Sunset", symbol: .sunset, textColor: .orange)
        .foregroundColor(.yellow)
}
```


```swift
VStack{
	Button(symbol: .sunset){}
    .foregroundColor(.red)
	Button("Sunset", symbol: .sunset){}
     .foregroundColor(.yellow)
	Button("Sunset", symbol: .sunset, textColor : .orange){}
     .foregroundColor(.yellow)
}
```
                    
## About 
SFSymbols are a real treat from apple. Apple's official list of Symbols that are available to use free of charge when writing software on any of Apple's recent platforms. There is one downfall however, it is a pain in the neck to look up exact symbol names, take for example: 

`"square.and.line.vertical.and.square.fill"`

That is a long string to remember and digging through the catalog of SF Symbols to find in would be quite a waste of time.

Wouldn't it be easier if you could just use code completion?

![](https://media.giphy.com/media/jQ7lTLsv2poo2qLkUA/giphy.gif)

Thats what this super micro library aims to do.

## Installation 

### Swift Package Manager (Preferred)
Since Xcode integrated swift package manager natively into the IDE you can add SFSymbol simply by:

**`File`-> `Swift Packages` -> `Add Package Dependency...`**

when prompted to enter a package URL paste: 

`https://github.com/Rspoon3/SFSymbols` 


and click next & finish to automagically install SFSymbol through Xcode & SPM!

### Manual 
Don't want that additional third party dependency? Then just simply copy over the files into your project's appropriate folder!

## Acknowledgments ##

Thanks to [Nirma](https://github.com/Nirma) for the idea. This project was highly influence and based off of his [SFSymbol](https://github.com/Nirma/SFSymbol) package. I found that few things I would do differently and before I knew it, I had an offshoot of what he had already done that went in a different direction.

## Contributing to this project
**Contributions are highly welcome**

If there is something you wish to fix about the project, or wish to add any other kind of enhancements, propose to add to the project. Please feel free to send over a pull request 
or open an issue for this project. Check out [SFSymbolsCreator](https://github.com/Rspoon3/SFSymbolCreator) for easily updating this project files.

## License

SFSymbols is released under the MIT license. [See LICENSE](https://github.com/Rspoon3/SFSymbols/blob/main/LICENSE) for details.
