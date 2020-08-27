# API 设计规范

## 目录

* [核心要点](#核心要点)
* [命名](#命名)
  * [传达更为清晰的用法](#传达更为清晰的用法)
  * [尝试更为流畅的表述](#尝试更为流畅的表述)
  * [使用更为精准的术语](#使用更为精准的术语)
* [设计惯例](#设计惯例)
  * [常规设计惯例](#常规设计惯例)
  * [参数名称](#参数名称)
  * [参数标签](#参数标签)
* [特殊场景说明](#特殊场景说明)

## 核心要点

* **在使用时表意清晰是设计 API 的第一要义。** 例如方法和属性的实体只会定义一次，但是会经常性地使用。设计 API 的本意就是要让这些使用场景变得简明扼要。何谓优秀的设计？仅仅通过声明就足以推断 API 的含义；经常在用例中对该设计进行考量，使之在上下文中表意清晰。

* **表意清晰比简单的描述显得更为重要。** 虽然 Swift 代码可以编写得简练精干，但用最少的字符数来减少代码量并不是 Swift 设计之初的本意。简略的 Swift 代码往往是强类型语言系统和语言的特性所带来的负面影响，它（指精简的代码）无形中减少了固有的代码模板。

* **为每一处的声明都添加注释文档。** 编写的注释文档有助于深入了解所写的代码内容，会对你的设计产生深远的影响，所以别忘了它。

  > 如果你无法通过简单的术语去描述你所设计 API 的功能性的话，**那你可能需要重新评估你设计的 API 了。**

  * **采用 Swift 专用的 [Markdown 版本](https://developer.apple.com/library/archive/documentation/Xcode/Reference/xcode_markup_formatting_ref/)**

  * **开头的概要**需要描述定义的实体。大多数情况下，浏览 API 的定义和概要即可完全地掌握它的用法。
  
  ```Swift
  /// Returns a "view" of `self` containing the same elements in
  /// reverse order.
  func reversed() -> ReverseCollection
  ```

> Source: [https://swift.org/documentation/api-design-guidelines/](https://swift.org/documentation/api-design-guidelines/)
