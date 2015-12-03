title: '我在用的 Xcode 插件 '
date: 2015-12-03 23:35:47
tags: [Object-c,Xcode]
categories: Xcode
---

# 插件过期解决方案

1. 查看Xcode UUID     `   defaults read /Applications/Xcode.app/Contents/Info DVTPlugInCompatibilityUUID
`

2. 用Xcode打开插件项目，将UUID添加进xxx-info.plist的DVTPlugInCompatibilityUUIDs即可。 



# 注释插件
[VVDocumenter 下载](https://github.com/onevcat/VVDocumenter-Xcode)

Window->VVDocumenter 钩选Add Default User Information(objc only) 输入用户名或工号

# 自动格式化插件
[ClangFormat 下载](https://github.com/travisjeffery/ClangFormat-Xcode)

1. 安装ClangFormat
2. 将以下代码保存为 .clang-format 放入项目Xcode项目根目录下
3. Xcode->Edit->Clang Format->File (既选择自定义格式化配置文件)
4. Xcode->Edit->Clang Format->Enable Format on Save (保存后对当前文件进行格式化)

```
 BinPackParameters: true
 BinPackArguments: true
 ColumnLimit:     160
 ConstructorInitializerAllOnOneLineOrOnePerLine: false
 ...
 KeepEmptyLinesAtTheStartOfBlocks: true
 NamespaceIndentation: None
 ObjCBlockIndentWidth: 4
 ObjCSpaceAfterProperty: false
 ObjCSpaceBeforeProtocolList: true
 PenaltyBreakBeforeFirstCallParameter: 19
  ...
 Standard:        Cpp11
 IndentWidth:     4
 TabWidth:        8
 UseTab:          Never
```

# CocoaPods

[CocoaPods 下载](https://github.com/kattrali/cocoapods-xcode-plugin)


# 代码提示

[FuzzyAutocomplete 下载](https://github.com/FuzzyAutocomplete/FuzzyAutocompletePlugin)

配置：Editor->FuzzyAutocomplete

# 图片选择插件
[UIimage imageNamed:@""];提供图片预览，名称提示  [KSImageNamed 下载](https://github.com/ksuther/KSImageNamed-Xcode)

# TODO插件

[XToDo 下载](https://github.com/trawor/XToDo)

View->ToDo List 或快捷键 ^T 查看任务列表






















