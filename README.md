[![pub package](https://img.shields.io/badge/pub-0.0.1-orange.svg)](https://pub.dartlang.org/packages/tree_view)
[![Build Status](https://travis-ci.org/ajilo297/flutter_tree_view.svg?branch=master)](https://travis-ci.org/ajilo297/flutter_tree_view)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Tree View

A Flutter package for a fully customisable tree view

#### Sample

<a href="https://imgur.com/d4n4p1b"><img src="https://i.imgur.com/d4n4p1b.gif" title="source: imgur.com" /></a>



### Installing

Add this to your `pubspec.yaml` file

```yaml
dependencies:
  tree_view_flutter: ^1.0.2
```

And run

```sh
flutter packages get
```

### Example

Let's assume we want to show a tree view with this structure:

```
Desktop
|-- documents
|   |-- Resume.docx
|   |-- Billing-Info.docx
|-- MeetingReport.xls
|-- MeetingReport.pdf
|-- Demo.zip
```

In this example

1. `Resume.docx` and `Billing-Info.docx` are **Child** widgets with
   `documents` as the **Parent**.
2. `documents`, `MeetingReport.xls`, `MeetingReport.xls` and `Demo.zip`
   are **Child** widgets with `Desktop` as a **Parent** widget.

The `TreeView` would look like this

```dart

var treeView = TreeView(
  parentList: [
    Parent(
      parent: Text('Desktop'),
      childList: ChildList(
        children: <Widget>[
          Parent(
            parent: Text('documents'),
            childList: ChildList(
              children: <Widget>[
                Text('Resume.docx'),
                Text('Billing-Info.docx'),
              ],
            ),
          ),
          Text('MeetingReport.xls'),
          Text('MeetingReport.pdf'),
          Text('Demo.zip'),
        ],
      ),
    ),
  ],
);
```

# 📃 License

    Copyright (c) 2024 Asad Khan

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

