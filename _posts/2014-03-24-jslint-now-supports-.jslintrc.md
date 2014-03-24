---
layout: post
title:  "JSLint now supports .jslintrc"
date:   2014-03-24
category: atom
---

I have just updated [jslint](https://atom.io/packages/jslint) too version [0.9.0](https://github.com/tcarlsen/atom-jslint/releases/tag/v0.9.0) and it now supports `.jslintrc` config files.

## What does that mean?

Before you had to add specific **jslint** configuration inside every single file in your project like this

```javascript
/*global $, atom*/
/*jslint indent: 2*/
```

But now you can add a `.jslintrc` file in your project root and the configuration will apply to every JavaScript file in that project.

```json
{
  "indent": 2,
  "predef": {
    "$": true,
    "atom": true
  }
}
```

For more on **jslint** configuration see the [official documentation](http://www.jslint.com/lint.html#options).
